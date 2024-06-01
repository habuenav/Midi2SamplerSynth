# Midi2Sampler
Midi2Sampler es una aplicación web que convierte archivos MIDI en instrucciones compatibles con Arduino y la librería samplerSynth (https://github.com/habuenav/samplerSynth) , permitiendo la reproducción de archivos MIDI en la placa ESP32 utilizando las características de la librería samplerSynth.
fue desarrollada usando la libreria Tone.js para javascript.

## Características
* <b>Conversión de archivos MIDI:</b> Convierte archivos MIDI en instrucciones Arduino.
* <b>Compatibilidad con samplerSynth:</b> Genera código compatible con la librería samplerSynth para ESP32.
* <b>Interfaz amigable:</b> Interfaz web intuitiva para cargar archivos MIDI y configurar las opciones de conversión.
* <b> Reproducción de MIDI:</b> Reproduce archivos MIDI directamente desde la aplicación web utilizando Tone.js.
  
## Uso
Requisitos
Navegador web moderno (Google Chrome, Mozilla Firefox, etc.)
Placa ESP32
Librería samplerSynth instalada en el entorno Arduino

## Instrucciones
* <b>Abre el archivo index.html en tu navegador.</b>
* <b>Arrastra y suelta el archivo MIDI en el área designada o usa el botón de carga.</b>
#### Configura las opciones:
* <b>Tipo de código: Selecciona si deseas generar un Sketch completo o solo una Función.</b>
* <b>Nombre de la función: Si seleccionas Función, proporciona un nombre para la función.</b>
* <b>Instrumento: Elige el instrumento que deseas usar para la reproducción.</b>
* <b>Volumen: Ajusta el volumen de la reproducción.</b>
* <b>Poly: Establece el número máximo de notas que pueden sonar simultáneamente.</b>
* <b>Por ultimo Carga tu archivo MIDI.</b>

## Reproduce el MIDI en tu ESP32
El código Arduino generado aparecerá en el área de resultados.
Copia el código y pégalo en tu entorno de desarrollo Arduino.
Sube el código a tu ESP32:
Conecta tu ESP32 a tu computadora, sube el código generado y si todos esta bien configurado y conectado este empezara a sonar.

## Reproduce el MIDI en la aplicacion Web
Usa la aplicación web para reproducir el archivo MIDI y verificar cómo sonará en tu ESP32.

## Interfaz 
<img src='https://postimg.cc/qt4FkL5S' title='Interfaz' />

#### Codigo de ejemplo
```
#include <samplerSynth.h>

void setup() {
  Serial.begin(115200);
  initSynth();
  setVolumen(3);
  setInstrumento(6);
}
byte nota=60;
void loop() {
notaOn(nota);
delay(500);
nota++;
if(nota==72){nota=60; delay(5000);}   
}
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

