---
title: "Cuál es la mejor alternativa para Cloud9 IDE"
date: 2019-05-11T10:48:18-05:00
draft: false
tags:
    - IDE
    - Desarrollo de Sofware
    - Programación
---

En la actualidad existe una gran variedad de herramientas de programación tanto para
diseño, desarrollo, pruebas, versionamiento, etc. El día de hoy vamos a hablar
sobre editores de código e IDEs, herramientas de desarrollo que nos permiten escribir
aplicaciones.

Podemos encontrar varios editores de código bastante populares como Visual Studio Code,
Sublime Text, Atom, Vim/Neovim, entre otros. Inclusive existen entornos integrados de
desarrollo que nos ofrecen mayores funcionalidades como autocompletado, debugging, etc.
Entre estos entornos integrados de desarrollo (IDE) podemos encontrar a IntelliJ IDEA,
Microsoft Visual Studio, Eclipse, NetBeans, entre otros.

Todas estas herramientas las usamos en nuestro entorno de trabajo local es decir en
nuestro computador. Pero en los últimos años se han desarrollando varias
iniciativas para que estos editores de código e IDEs migren a la "nube" uno de estos
IDEs en línea es Cloud9 (C9) que fue creado en 2010 y adquirido en 2016 por Amazon. C9
es uno de los mejores IDEs en línea, este IDE
nos permitía tener entornos de trabajo remotos que contaban con 2GB de almacenamiento y
hasta 1GB de memoria RAM bajo la capa gratuita, lo que era suficiente para realizar
desarrollo de aplicaciones pequeñas y medianas, además de brindarnos una IP pública
para visualizar nuestra aplicación.

![](https://paper-attachments.dropbox.com/s_A2575D6F4C8C61CBDE0D7E83B9A422C78DC9528D78D4A1DBAC773AA6A37157AF_1558030775343_cloud9.png)

Desde la adquisición de C9 por Amazon ya no existe
la capa gratuita y C9 pasó a ser un servicio integrado de Amazon Web Services (AWS) por
lo que debemos pagar por el uso del IDE ya que corre en una instancia de Amazon Elastic
Compute Cloud (Amazon EC2). Los servidores del servicio anterior de C9 dejarán de funcionar para el 30 de Junio del 2019 por lo que ya no podremos usar C9, a menos que usémos C9 dentro de AWS.

Pero a todo esto, porque nos importaría tener un IDE en línea si podemos contar
con mucha más RAM, procesamiento y espacio en nuestras máquinas locales, bueno
voy a mencionar algunas de las ventajas de un IDE en la nube frente a
un entorno de desarrollo local.

Ventajas:

* Puedes desarrollar desde cualquier lugar lo que para mi representa libertad de movimiento ya que muchas veces no llevas tu computadora contigo, con un IDE en línea puedes abrir tu proyecto desde cualquier computadora.
* Te brinda una IP pública estática por lo que puedes compartir tu trabajo con alguien más, por ejemplo si algún cliente te pide que realices una página web tu puedes desarrollarla en el IDE en línea y mostrarlo a tu cliente remotamente sin necesidad de comprar un dominio y configurarlo.
* Te brinda un entorno de trabajo remoto no se limita solo al IDE o al editor de código te brinda una instancia de Linux con lo que puedes instalar todo lo que necesites y si como yo usas Windows siempre es bueno poder tener una máquina con linux para desarrollar.

También existen algunas desventajas de un IDE en línea.

Desventajas:

* Necesitas una conexión a internet por lo que sino cuentas con una no podrás avanzar en tu proyecto.
* Capacidad limitada a diferencia de un entorno de desarrollo local donde básicamente puedes usar toda la capacidad de tu computador.

Y ahora que IDE en línea usar si C9 se pasa a AWS donde debemos pagar y
configurar manualmente la IP estática a diferencia del anterior servicio de C9 que nos proveía una IP estática por defecto.

Existen varias alternativas para C9, como Codeanywhere, Koding, Eclipse Che, entre otros.
Aunque son bastante buenos ninguno nos ofrece la facilidad de uso y las funcionalidades de C9.
Recientemente Microsoft anuncio Visual Studio Online, a pesar de ser una gran iniciativa este
editor de código, no es un entorno de trabajo completo
sino más bien se asemeja a la edición de código que implementa GitLab, aunque se espera que en
el futuro podamos contar con entornos de desarrollo completos.

Y hasta eso qué? Existe una gran alternativa llamada goormIDE desarrollada por la empresa
Coreana Goorm, este IDE es la perfecta alternativa para C9 ya que
nos ofrece todas sus ventajas: varios entornos de desarrollo, una capa gratuita, además nos
permite colaborar con otros desarrolladores en tiempo real y una IP pública estática para compartir
nuestros proyectos.

![](https://paper-attachments.dropbox.com/s_A2575D6F4C8C61CBDE0D7E83B9A422C78DC9528D78D4A1DBAC773AA6A37157AF_1558031446055_goormide.png)

Y como empiezo? Ingresa a la página de goormIDE y registrate una vez registrado
debes llenar un formulario mencionando para qué vas a usar los espacios de trabajo de goormIDE, cuando se apruebe tu solicitud que en promedio se demora 24h
puedes comenzar a crear ambientes de desarrollo, y disfrutar de todos los beneficios que
te ofrece un IDE en línea.
