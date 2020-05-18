---
title: "Sitios estáticos usar Gatsby o Nextjs"
date: 2020-05-17T21:37:17-05:00
draft: false
---

Al momento de desarrollar un sitio estático tenemos una [infinidad](https://www.staticgen.com/) de posibilidades.

Pero ¿Porqué desarrollar un sitio estático? Bueno un sitio estático tiene varios beneficios:

• Costo

• Mantenimiento

• Facilidad de configuración

**Costo:** Este blog se mantiene con $12 al año lo que es una cantidad interesante para mantener un sitio web 24/7. Y el costo del sitio viene de parte del nombre de dominio no del sitio en sí.

**Mantenimiento:** Lo único que necesitamos para tener actualizado el sitio y tenerlo corriendo es un repositorio de github en donde se almacene el código.

**Facilidad de configuración:** Gracias a herramientas como [Netlify](https://www.netlify.com/) el despliegue de un sitio estático no necesita tanta configuración.

Ahora bien una vez conocemos las ventajas de un sitio estático, ¿Cúando no sería recomendable usar un sitio estático? Pues bueno en estos casos:

• El contenenido cambia frecuentemente

• Necesitamos manejar una lógica compleja

**El contenenido cambia frecuentemente:** Cuando tenemos una web que cambia constantemente por su giro de negocio no es una buena idea usar un generador de sitios estáticos, ya que para que nuestro sitio se actualice debemos compilarlo con cada cambio y eso representaría un tiempo de carga considerable.

**Necesitamos manejar una lógica compleja:** Cuando nuestro sitio ya pasa a ser más bien una aplicación web y ya no solo presentamos información al usuario.

Ahora los mayores referentes para crear sitios estáticos con React son Gatsby y Nextjs cada uno tiene sus puntos fuertes, analizaremos cuál de estos es más recomendable usar.

En cuanto a Nextjs es un framework de React que destaca por su característica de server side rendering es decir que la página se genera desde el servidor lo que mejora considerablemente el SEO. Entre sus features Netxjs permite generar sitios estáticos pero este no es su fin principal a diferencia de Gatsby.

En cuanto al ecosistema Gatsby destaca como generador de sitios estáticos ya que tenemos mayores herramientas como [starters](https://www.gatsbyjs.org/starters/?v=2) y varios [pulgins](https://www.gatsbyjs.org/plugins/) que nos ayudan mientras desarrollamos, además muchas herramientas que trabajan con [JAMstack](https://jamstack.org/) tienen compatibiidad con Gatsby antes que con Nextjs.

Algo particular que encontre es que si deseamos colocar un sitio en un subdirectorio como `/blog`, en Gatsby podemos hacerlo con [pathPrefix](https://www.gatsbyjs.org/docs/path-prefix/), mientras que Nextjs esta feature no la encontre.

En mi opinión creo que si deseamos realizar una página estática la mejor elección es Gatsby mientras que si necesitamos un framework para manejar un sin número de páginas web en nuestra aplicación web la elección correcta sería Nextjs.

