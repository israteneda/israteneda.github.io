---
title: "Color Picker en Android (Kotlin/Java)"
date: 2020-03-14T14:58:17-05:00
draft: false
tags: 
    - Desarrollo móvil
    - Android
---

![](https://media.giphy.com/media/SRqUihSSQEpQrArjFL/giphy.gif)

Hola a todos, en esta entrada vamos a crear un Color Picker en Android usando la librería [ColorSheet](https://github.com/msasikanth/ColorSheet) creada por [Sasikanth](https://github.com/msasikanth).

Comenzamos creando el proyecto, en este caso le pondré el nombre de **Color Picker**

![](https://i.imgur.com/jLK8XQU.png)

Hay que tener en cuenta que para utilizar esta librería la versión mínima del sdk debe ser la versión 21.

```groovy
defaultConfig {
    applicationId "com.example.colorpicker"
    minSdkVersion 21
    targetSdkVersion 29
    versionCode 1
    versionName "1.0"
    
    ...
}
```

Tanto para Java como para Kotlin debemos agregar las dependencias de ColorSheet y Material Design en `build.gradle (Module:app).`

```groovy
dependencies {
    ...

    // ColorSheet
    implementation "dev.sasikanth:colorsheet:1.0.1"

    // Material Design
    implementation 'com.google.android.material:material:1.1.0'
}
```

Una vez hemos añadido las dependencias y sincronizado el proyecto debemos cambiar el tema por defecto de la aplicación por un tema de Material Design:

De AppCompat:

```xml
<!-- Base application theme. -->
    <style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">
        <!-- Customize your theme here. -->
        ...
    </style>
```

A MaterialComponents:

```xml
<!-- Base application theme. -->
    <style name="AppTheme" parent="Theme.MaterialComponents.Light.NoActionBar">
        <!-- Customize your theme here. -->
        ...
    </style>
```

Ahora crearemos los siguientes elementos en `activity_main.xml`:

• `ConstraintLayout` con el id `layout_container`
• `Button` con el id `btn_color_picker`

![](https://i.imgur.com/5AEJX54.png)

Añadimos un array de colores en `colors.xml` dentro de la carpeta `values` del proyecto.

```xml
<array name="colors">
    <item>#F44336</item>
    <item>#E91E63</item>
    <item>#3F51B5</item>
    <item>#1E88E5</item>
    <item>#F4511E</item>
    <item>#546E7A</item>
    <item>#43A047</item>
</array>
```

Si deseamos cambiar el texto que se despliega en el Color Picker, podemos añadir el siguiente código a `strings.xml` en la carpeta `values` del proyecto.

```xml
<resources>
    <string name="app_name">Color Picker</string>

    <!-- ColorSheet -->
    <string name="pick_a_color">Selecciona un color</string>
</resources>
```

Una vez tenemos listo nuestras dependecias, la vista y los colores, vamos con el código.

## Java

Para Java añadiremos una dependecia más, ya que la libraría esta escrita en Kotlin necesitamos una interfaz llamada `Function1` para que el código pueda correr con Java, recordemos que Java y Kotlin son interoperables.

```groovy
dependencies {
    ...

    // ColorSheet
    implementation "dev.sasikanth:colorsheet:1.0.1"

    // Material Design
    implementation 'com.google.android.material:material:1.1.0'

    // Kotlin
    def kotlin_version = '1.3.61'
    implementation "org.jetbrains.kotlin:kotlin-stdlib-jdk7:$kotlin_version"
}
```

Ahora si vamos con el código de `MainActivity.java`:

```java
public class MainActivity extends AppCompatActivity {

    ConstraintLayout container;
    Button colorPicker;
    private Integer selectedColor = ColorSheet.NO_COLOR;
    private Boolean noColorOption = false;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        container = findViewById(R.id.layout_container);
        colorPicker = findViewById(R.id.btn_color_picker);
        final ColorSheet colorSheet = new ColorSheet();
        final int[] colors = getResources().getIntArray(R.array.colors);

        final Function1 listener = (new Function1() {
            public Object invoke(Object var1) {
                this.invoke(((Number)var1).intValue());
                return Unit.INSTANCE;
            }

            public final void invoke(int color) {
                container.setBackgroundColor(color);
                Toast.makeText(MainActivity.this, "Color: " + color, Toast.LENGTH_SHORT).show();
            }
        });

        colorPicker.setOnClickListener(new View.OnClickListener() {
            public void onClick(View v) {
                colorSheet.cornerRadius(8);
                colorSheet.colorPicker(colors, selectedColor, noColorOption, listener).show(getSupportFragmentManager());
            }
        });
    }
}
```

## Kotlin

`MainActivity.kt`

```java
class MainActivity : AppCompatActivity() {

    companion object {
        private const val COLOR_SELECTED = "selectedColor"
        private const val NO_COLOR_OPTION = "noColorOption"
    }

    private var selectedColor: Int = ColorSheet.NO_COLOR
    private var noColorOption = false

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val container:ConstraintLayout = findViewById(R.id.layout_container)
        val colorPicker: Button = findViewById(R.id.btn_color_picker)
        val colors = resources.getIntArray(R.array.colors)

        selectedColor = savedInstanceState?.getInt(COLOR_SELECTED) ?: colors.first()

        noColorOption = savedInstanceState?.getBoolean(NO_COLOR_OPTION) ?: false

        colorPicker.setOnClickListener {
            ColorSheet().cornerRadius(8)
                    .colorPicker(
                            colors = colors,
                            noColorOption = noColorOption,
                            selectedColor = selectedColor,
                            listener = { color ->
                                selectedColor = color
                                container.setBackgroundColor(color)
                                Toast.makeText(this, selectedColor.toString(), Toast.LENGTH_SHORT).show()
                            })
                    .show(supportFragmentManager)
        }
    }
}
```

Para el tutorial se utilizaron las siguientes herramientas:

```
Android Studio 3.6.1
Gradle 5.6.4
```