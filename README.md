1. Introducción:

Este proyecto consiste en la fabricación y diseño de un pedal de efectos digital con Teensy 4.0 para guitarra eléctrica. En concreto de un efecto de Chorus en el cual la señal de la guitarra entrará en el pedal y se procesa para que una vez amplificada la señal se pueda escuchar la señal con el efecto.


2.¿Qué es?

El pedal tiene como objetivo conseguir la simulación de un efecto de Chorus digital, mediante programación de Teensy 4.0 con arduino.
La Teensy es una placa que procesa toda la información, y está especializada en proyectos de audio, ya que es más potente en estos casos que usar un arduino normal, como especificaciones generales hay que destacar la velocidad de procesamiento de 600Mhz, un tamaño muy compacto (el cual es perfecto para usarlo en pedales), posee una memoria la cual hace que sea muy útil para usarla en efectos de sonido a tiempo real (esto es debido a su velocidad de procesamiento y su baja latencia lo que hace que este dispositivo sea ideal para el tratamiento de instrumentos musicales), por último ofrece flexibilidad a la hora de conectar posibles controladores como potenciómetros, switch, leds o incluso pantallas que muestran el efecto que suene a tiempo real o para ver los parámetros y sus valores


3.Función (explicación general)

El pedal de chorus tiene como función principal enriquecer el sonido, es decir, aunque este solamente una guitarra sonando da la sensación de que hay varias sonando al mismo tiempo en vez de una (duplicando la señal recibida).

Su funcionamiento consiste en duplicar la señal de la guitarra para después modificar ligeramente una de ellas, modificando de una forma sutil el tono y el tempo con un leve retraso y una modulación en la frecuencia, además una vez se termine este proceso se mezclara con la señal original, se escuchará como una señal doble (2 guitarras a la vez).

Los potenciómetros que se necesitan son 4, los cuales consisten en el Profundidad, velocidad, mezcla y , a su vez también tiene un switch que es el encargado de activar y desactivar el efecto del pedal.


Algún ejemplo práctico se puede escuchar en algunas canciones como por ejemplo: messenger in a bottle (the police) buscando un sonido de guitarra envolvente.

4.Prototipo
Este prototipo inicialmente iba a ser analogico pero finalmente se realizo en formato digital gracias a Teensy 4.0, por lo tanto se tuvo que investigar sobre el chip, sobre cuál es su funcionamiento, para qué sirven los diferentes pines y entradas que posee, además a la hora de programarlo se podía desde arduino pero había que tener en cuenta de que la programación con arduino y teensy es diferente debido a la forma en la que se tienen que programar las cosas y las librerías necesarias para que sea funcional (descargar e instalar librerias especificas)
Los parámetros del Chorus están controlados por los diversos potenciometros y botones que se encuentran en la carcasa del pedal, entre ellos se encuentran los siguientes:

Depth (profundidad de chorus): controla la variación del retardo que se aplica a la señal de guitarra modulada (tiempo que se retarda del tempo original, es decir, la amplitud). (Controla la cantidad de la desafinación de la señal)

Rate/Speed (velocidad de modulación) controla la frecuencia del retardo, es decir, la velocidad a la que cambia el tempo del retardo de la señal duplicada. (Cambia la velocidad de la oscilación de la afinación/señal).

Mix (mezcla) es la mezcla como bien indica su nombre de la mezcla de la señal original y la señal procesada, esto nos indica la cantidad de efecto que se escucha en la señal de salida final (salida y entrada igual, o salida con la mezcla del efecto).

Shape LFO (cambia la forma de la onda) las formas de onda utilizadas son la senoidal (subida y bajada suave, natural y fluida), triangular (subida y bajada lineal, constante) y cuadrada (cambio brusco entre 2 valores)

Los potenciómetros están asignados a pines digitales pero en cambio el boton están asignados en los pines analógicos.

Activación de efecto, el otro boton/switch 3PDT funciona para la activación o desactivación del efecto del pedal, es decir, únicamente activará el chorus y dejará sonar la mezcla con el efecto o en el caso contrario dejará pasar la señal de la guitarra directamente al amplificador.

6.Materiales
Teensy 4.0 (X1)
Adaptador de Audición de Teensy (x1)
Potenciómetros de diversos valores 10K y 100K (controles de volumen, velocidad, profundidad y número de voces)
Fuente de alimentación compacta AC/DC de 230V a 5V (X1)
Perillas verdes, para poner en los potenciómetros (X4)
Conector Jack para PCB (X2)
Conector mini Jack (x1)
Interruptor pedal 3PDT (X1)
Resistencia 1K (X1)
Resistencia 200 (X1)
Led (X1)
Pines (x4)
Cables (protoboard, jack, mini-jack, aux)
Metacrilato (una plancha)
LPKF


7.Fallos
Problemas con la programación de teensy, reseteado varias veces de la teensy porque no funcionaba correctamente (habia dias que con el mismo código y mismo montaje funcionaba bien y otros días en los que no sin cambiar absolutamente nada), malas conexiones, teensy quemada, problemas con el botón 3pdt.
