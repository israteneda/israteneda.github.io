---
title: "Cuál es la mejor alternativa para Cloud9 IDE"
date: 2019-05-11T10:48:18-05:00
draft: true
tags:
    - IDE
    - Desarrollo de Sofware
    - Programación
---

En la actualidad existe una gran variedad de herramientas de programación tanto para
diseño, desarrollo, pruebas, versionamiento, etc. El día de hoy vamos a hablar
sobre editores de código, herramientas de desarrollo que nos permiten escribir
aplicaciones.

Podemos encontrar varios editores de código bastante populares como Visual Studio Code,
Sublime Text, Atom, Vim/Neovim, entre otros. Inclusive existen entornos integrados de
desarrollo que nos ofrecen mayores funcionalidades como autocompletado, debugging, etc.
Entre estos entornos integrados de desarrollo (IDE) podemos encontrar a IntelliJ IDEA,
Microsoft Visual Studio, EclIPse, NetBeans, entre otros.

Todas estas herramientas las usamos en nuestro entorno de trabajo local es decir en
nuestro computador. Pero en los últimos años se han venido desarrollando varias
iniciativas para que estos editores de código e IDEs se pasen a la "nube" una de estos
IDEs en línea es Cloud9 (C9) que fue creada en 2010 y adquirida en 2016 por Amazon. C9
es una de los mejores IDEs en línea, este IDE
nos permitia tener entornos de trabajo remoto que contaban con 2GB de almacenamiento y
hastal 1GB de memoria RAM bajo la capa gratuita, lo que era suficiente para realizar
desarrollo de aplicaciones pequeñas y medianas, además de brindarnos una IP pública
para visualizar nuestra aplicación. Desde la adquisición de C9 por Amazon ya no existe
la capa gratuita y C9 paso a ser un servicio integrado de Amazon Web Services (AWS) por
lo que debemos pagar por el uso del IDE ya que corre en una instancia de Amazon Elastic
Compute Cloud (Amazon EC2). Además los servidores de C9 antes que Amazon los adquiera
dejarán de proveer el servicio para el 30 de Junio por lo que ya no podremos usar C9,
a menos que usemos C9 dentro de AWS.

Pero a todo esto, porque nos importaría tener un IDE en línea si podemos contar
con mucha más RAM, procesamiento y espacio en nuestras máquinas locales, bueno
voy a mencionar algunas de las características de C9 que son ventajas frente a
un entorno de desarrollo local.

Ventajas:
- Puedes desarrollar desde cualquier lugar lo que para mi representa libertad de
movimiento ya que por A o B situación pueda que no tengas tu computadora contigo
y necesitas actualizar algún cambio a tu proyecto, con un IDE en línea puedes ir
a cualquier centro de alquiler de computadoras o en tu universidad o trabajo, abrir
tu proyecto y realizar los cambios necesarios.
- Te brinda una IP pública lo que se traduce en que puedes compartir tu trabajo con
alguien más, por ejemplo si algún cliente te pide que realices una página web tu puedes
desarrollarla en el IDE en línea y mostrarlo a tu cliente remotamente sin necesidad de
comprar un dominio y configurarlo.
- Te brinda un entorno de desarrollo completo C9 te brinda todo un entorno de trabajo
remoto no se limita solo al IDE o al editor de código te brinda una instancia de Linux
con lo que puedes instalar todo lo que necesites y si como yo usas Windows simpre es bueno
poder tener una máquina con linux para desarrollar.

Como todo en la vida no todo es perfecto, algunas desventajas de un IDE en línea.

Desventajas:
- Necesitas una conexión a internet por lo que sin no cuentas con una no podrás
avanzar en tu proyecto.
- Capacidad limitada a diferencia de un entorno de desarrollo local donde básicamente
puedes usar toda la capacidad de tu computador.

Y ahora que IDE en línea usar si C9 se pasa a AWS donde además que debemos pagar, debemos
configurar manualmente la IP pública y a diferencia del servicio de C9 que nos proveeía una IP estática
AWS C9 nos provee una IP dinámica a menos que paguemos por una IP pública estática.

Existen varias alternativas para C9, como lo son Codeanywhere, Koding, Eclipse Che, entre otros.
Aunque son bastante buenos ninguno nos ofrece la facilidad de uso y las funcionalidades de C9.
Recientemente Microsoft anuncio Visual Studio Online, a pesar de ser una gran iniciativa este
editor de código nos permitirá editar código pero todavía no es un entorno de trabajo completo
sino más bien se asemeja a la edición de código que implementa GitLab, aunque se espera que en
el futuro podamos contar con entornos de desarrollo completos.

Y hasta eso qué? Existe una gran alternativa llamada goormIDE desarrollada por la empresa
Koreana Goorm, este IDE se asemeja mucho a C9 y es la perfecta alternativa para C9 ya que
nos ofrece todas sus ventajas: varios entornos de desarrollo, una capa gratuita, además nos
permite colaborar con otros desarrolladores en tiempo real, una IP pública para compartir
nuestros proyectos.

Y como empiezo? Ingresa a la página de goormIDE y registraté una vez que te registres
debes mecionar para que vas a usar tu cuenta de goormIDE, una vez se apruebe tu solicitud
puedes comenzar a crear ambientes de desarrollo, y disfutar de todos los beneficios que
te ofrece un IDE en línea.
goormIDE nos ofrece 1GB de RAM y 10GB de almacenamiento.
