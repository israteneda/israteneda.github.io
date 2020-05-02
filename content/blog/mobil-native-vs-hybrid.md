---
title: "Desarrollo móvil nativo vs híbrido"
date: 2020-03-01T15:26:09-05:00
draft: false
tags: 
    - Desarrollo móvil
---
En esta entrada analizaremos si es más conveniente desarrollar aplicaciones nativas (Android/iOS nativo) o aplicaciones híbridas (Ionic, Xamarin, Flutter). Este es un tema que se ha venido discutiendo desde hace mucho tiempo y cada forma de desarrollo presenta sus ventajas y desventajas.

![](https://paper-attachments.dropbox.com/s_7BD25BBB88BF21C277059519E71656972986037181B9D57C6AD31D25B17B6A16_1583094834741_app_hibrida_vs_app_nativa.jpg)

Hoy en día es crucial contar con una aplicación móvil, incluso hay negocios que se basa en una, como es el caso de Uber, Spotify, WhatsApp e Instagram. En el 2017 el 57% del tráfico de internet provenía de búsquedas de dispositivos móviles según [BrightEdge](https://www.brightedge.com/sites/default/files/BrightEdge-Mobile-Research-Paper-2017.pdf), es decir, las búsquedas en móvil representan la mitad de las búsquedas globales. Además, la gente usa su smartphone entre 3 y 5 horas al día, por este motivo es imprescindible contar con una aplicación móvil de calidad y que genere engagement en nuestros usuarios.

Según sea el caso debemos utilizar la tecnología que mejor se adapte a nuestro problema, como en toda disciplina no existe una solución única, así que, veamos cuando es conveniente usar desarrollo nativo y cuando desarrollo híbrido.

## Desarrollo Nativo

Es una buena idea el desarrollo nativo cuando:

• La aplicación que desarrollemos se acerca cada vez más al hardware, por ejemplo un dispositivo de punto de venta que tiene módulos de impresión de tickets, scanner QR, lector de tarjetas, etc.

• Una aplicación empresarial, hay aplicaciones que tiene un propósito único y necesitan ser administradas por la empresa, la mayoría de frameworks híbridos no ofrecen la completa administración del dispositivo con funcionalidades como modo kiosko, control de bloqueo del teléfono, instalación forzada de aplicaciones, etc. Esto lo tendremos que hacer con una aplicación nativa y en el caso de Android con una API para la gestión del dispositivo como [Android Managment API](https://developers.google.com/android/management).

• Cuando el performance, la seguridad y la calidad de la aplicación es importante, al tener una aplicación nativa tenemos el control completo del performance de la aplicación y en el caso de Android con 10 años en el mercado y con el ecosistema actual con el que cuenta, la seguridad y madurez ha mejorado mucho, lo que nos brinda un producto final de calidad.

## Desarrollo Híbrido

El desarrollo híbrido es conveniente en los siguientes casos:

• La mayor parte de la lógica del negocio se encuentra en el servidor, por lo que la información que se muestra al usuario va a ser consumida desde una API, en este caso el principal fin del aplicativo es mostrar información por lo que no abría conflicto con librerías nativas.

• Existe una aplicación web completa que maneja todo el negocio y queremos lanzar una aplicación móvil con el mismo equipo de trabajo y la misma tecnología, por ejemplo si contamos con una aplicación web realiza con React podemos utilizar React Native para implementar una aplicación móvil, si utilizamos Angular para el desarrollo podemos utilizar Ionic y en el caso que no trabajemos con estos framework podemos realizar una [PWA](https://web.dev/progressive-web-apps/).

• El presupuesto para una aplicación Android y iOS es limitado, cuando se trata por ejemplo de una startup que no puede costear dos equipos trabajando en Android e iOS, el desarrollo híbrido llega al rescate la mayoría de frameworks híbridos generan aplicativos para las dos plataformas iOS y Android con un solo código base, probablemente esta es la característica más atractiva para el uso de frameworks híbridos.

Estos son los principales casos de uso para una aplicación móvil y de acuerdo al problema con el que nos encontremos deberemos elegir entre nativo o híbrido. Recordemos que ninguna tecnología es mejor que otra, cada una tiene su caso de uso y debemos encontrar la que mejor se ajuste a nuestra situación.

Me gustaría hacer una mención especial al framework lanzado por Google, Flutter ya que, la mayoría de framework híbridos lo que hacen es transformar el código escrito en diferentes lenguajes a componentes de cada plataforma nativa, [Flutter](https://flutter.dev/) redibuja toda la UI haciendo que sea muy cercano al performance nativo, esta tecnología promete mucho ya que además Google proclama que será realmente multiplataforma permitiendo crear código para web, móvil y desktop con un solo código base, pero aún está en veremos ya que la plataforma aún está en una etapa temprana y cuenta con bastantes [isuues](https://github.com/flutter/flutter/issues) en github.