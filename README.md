# Midi2SamplerSynth
Midi2SamplerSynth es una aplicación web que convierte archivos MIDI en instrucciones compatibles con Arduino y la librería samplerSynth (https://github.com/habuenav/samplerSynth) , permitiendo la reproducción de archivos MIDI en la placa ESP32 utilizando las características de la librería samplerSynth.
fue desarrollada usando la libreria Tone.js para javascript.

## Características
* <b>Conversión de archivos MIDI:</b> Convierte archivos MIDI en instrucciones Arduino.
* <b>Compatibilidad con samplerSynth:</b> Genera código compatible con la librería samplerSynth para ESP32.
* <b>Interfaz amigable:</b> Interfaz web intuitiva para cargar archivos MIDI y configurar las opciones de conversión.
* <b> Reproducción de MIDI:</b> Reproduce archivos MIDI directamente desde la aplicación web utilizando Tone.js.
  
## Requisitos
* Navegador web moderno (Google Chrome, Mozilla Firefox, etc.)
* Placa ESP32
* Librería samplerSynth instalada en el entorno Arduino

## Instrucciones
* Abre el archivo index.html en tu navegador.
* Arrastra y suelta el archivo MIDI en el área designada o usa el botón de carga.
#### Configura las opciones:
* <b>Tipo de código:</b> Selecciona si deseas generar un Sketch completo o solo una Función.
* <b>Nombre de la función:</b> Si seleccionas Función, proporciona un nombre para la función.
* <b>Instrumento:</b> Elige el instrumento que deseas usar para la reproducción.
* <b>Volumen:</b> Ajusta el volumen de la reproducción.</b>
* <b>Poly:</b> Establece el número máximo de notas que pueden sonar simultáneamente.
* <b>Por ultimo Carga tu archivo MIDI.</b>

## Reproduce el MIDI en tu ESP32
El código Arduino generado aparecerá en el área de resultados.
Copia el código y pégalo en tu entorno de desarrollo Arduino.
Sube el código a tu ESP32:
Conecta tu ESP32 a tu computadora, sube el código generado y si todos esta bien configurado y conectado este empezara a sonar.

## Reproduce el MIDI en la aplicacion Web
Usa la aplicación web para reproducir el archivo MIDI y verificar cómo sonará en tu ESP32.

## Interfaz
<details>
<summary> <b>Ver imagen</b> </summary>
<a href='https://postimg.cc/qt4FkL5S' target='_blank'><img src='https://i.postimg.cc/7L2rntMH/midi2sampler.png' border='0' width="50%" alt='Interfaz'/></a>
</details>

## Ejemplo Codigo generado

```
#include <samplerSynth.h>
void Riff() {
notaOn(67, 91, 166);
delay(333);notaOn(67, 93, 83);
delay(166);notaOn(62, 86, 166);
delay(333);notaOn(62, 98, 83);
delay(166);notaOn(67, 110, 166);
delay(333);notaOn(67, 98, 83);
delay(166);notaOn(62, 91, 166);
delay(333);notaOn(62, 94, 83);
delay(166);notaOn(63, 100, 166);
delay(333);notaOn(63, 95, 83);
delay(166);notaOn(63, 94, 166);
delay(166);notaOn(65, 108, 166);
delay(166);notaOn(63, 91, 166);
delay(166);notaOn(62, 90, 499);
}
void setup() {
Serial.begin(115200);
initSynth();
setVolumen(40);
setMaxNotas(8);
setInstrumento(0);
delay(1000);
Riff();
}
void loop() {}
```
## Acerca de
Este proyecto fue desarrollado por Holman Buenaventura en 2024. La idea surgió de la querer ampliar la utilidad de la libreria samplerSynth y lo que se buscaba era reproducir archivos MIDI en la placa ESP32
gracias a la librería samplerSynth, proporcionando una forma fácil y accesible de convertir y generar el código necesario para tal fin.

## Contribuciones
¡Las contribuciones son bienvenidas! Si tienes sugerencias, encuentra un error o deseas agregar una nueva característica, por favor abre un issue o envía un pull request.

## Donaciones
Si te gusto este proyecto o simplemente te sientes generoso, considera invitarme una cerveza. ¡Salud! :beers:<br/>
<a href="https://www.paypal.com/donate/?business=T8UBSMVJ2QT9Y&no_recurring=0&item_name=%C2%A1Gracias+por+tu+apoyo%21%0ATu+donaci%C3%B3n+es+de+gran+ayuda+y+es+un+incentivo+para+seguir+mejorando.&currency_code=USD"><img src="https://www.paypalobjects.com/digitalassets/c/website/marketing/latam/mx/accept-payments-online/icons/img_btn-donate2x.png" height="80"></a><br/>
¡Tu apoyo es invaluable!

