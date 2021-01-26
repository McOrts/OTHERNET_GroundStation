# OTHERNET acceso libre a datos desde el espacio
En pocas palabras, [OTHERNET](https://othernet.is/) es un servicio en torno a una emisión broadcast digital de datos desde satélites geoestacionarios. 
<img src="./img/outernet-what-is.png" width=400 align="right" />

Dicho de otra forma OTHERNET (Originalmente OUTERNET) provee a pequeños dispositivos locales o _hostpots_ de repositorios de datos metereológicos, noticias, Wikipedia, mensajes y archivos que pueden ser compartidos en el segmento terrestre. 

## Una larga historia
Inspirado en el proyecto [RACHEL](https://worldpossible.org/) que permite montar una plataforma autónoma de contenidos y formación como punto de acceso wifi allí donde no hay internet. [Syed Karim](https://www.linkedin.com/in/syedkarim1/) graduado en informática por la Universidad de Ilinois, replanteó a lo grande este concepto. ¿Y si los RACHEL se actualizan desde el espacio? Así podrían desvincularse de las redes terrestres, y por ende, estar en cualquier parte del mundo donde al menos un panel solar pueda darle energía.

<img src="./img/outernetgraphic-300x139.png" width=550 lign="left" />

Y este concepto se materializó en **2015 en el proyecto Outernet** desarrollando un dispositivo llamado _Lantern_ que abogaba por el acceso a la libre información, la educación y noticias en cualquier parte del mundo independientemente de su localización, recursos o infraestructuras. Una primera aportación de la organización MDIF (Media Development Investment Fund) permitió construir un prototipo de receptor y un acuerdo con los operadores de los satélites Galaxy 19 y Hot Bird para la conectividad con estos dispositivos.

<img src="./img/LanternBoardDesing.png" align="center" />

Y es aquí cuando Syed Karim decide crear la campaña de _crowdfunding_ ["Latern: A Global Satellite Data Radio"](https://igg.me/at/outernet/x#/updates/all) en Indiegogo para conseguir los fondos y dar a conocer el producto. Con un presupuesto de 390K$ que acabó alcanzando los 573K$ ya tenía garantizada la viabilidad del proyecto. Fuí uno de los primeros participantes en esta primera ronda pero mi aportación se destinó a apadrinar un receptor (Lantern) para ser donado a un colegio en países africanos. 

<img src="./img/FirstLantern.jpg" width=600 align="center" />

Privado entonces de tener un receptor, me apunté a una segunda ronda en la que había la posibilidad de tener un dispositivo DIY basado en un receptor de DVB-S2 (Geniatech Mygica HDStar) y una _single board computer_ como la Raspberry Pi. Pero de nuevo me quedé con las ganas porque nunca me funcionó. El clásico problema de incompatibilidad de versiones y la falta de soporte, frustró el intento.
<img src="./img/RPI_Outernet.jpg" align="right" />

Por otra parte ya **había pasado más de una año** tras completarse la campaña en Indiegogo y el proyecto **se replantea el segmento espacial**. Que había pasado, de proyectar una constelación de micro-satélites propios en órbita baja (LEO) construidos por la empresa escocesa Clyde Space. A contratar un transpondedor de un satélite geoestacionario. Finalmente llegaron a un acuerdo con ViaSat para el uso de un _beam_ que empezó con 20MB por día de _uplink_ desde el satélite SkyTerra-1 en la banda L. Lo que garantizaba la recepción con antenas pequeñas. 
</br>

**En 2018 el proyecto se renombra a Othernet** y transita por una serie de cambios de diseño de receptor y acuerdos con otros proveedores de satélites. Hasta que en 2020 el proyecto se consolida como una empresa M2M en Chicago (Ilinois USA) con Syed Karim a la cabeza como CEO. Y define una solución más comercial y menos _maker_. Un modem-punto de acceso propio basado en arquitectura ARM con receptor de banda Ku y decodificación LoRa. Lo que da un ancho de banda de solo 20K baudios pero suficiente para el tipo de contenidos que se manejan y teniendo en cuenta que el receptor tiene su propio sistema de archivos que es el que el usuario consume. Respecto a la cobertura global actual. Esta alcanza dos continentes gracias a estos geoestacionarios:

- América del Norte que es proporcionado por el SES-2 en 87° Oeste
- Europa por el Astra 3B en 23.5° Este.

Y es **a finales de 2020 cuando me reengancho** al proyecto adquiriendo el receptor Dreamcatcher, reciclando una antena parabólica offset de 120 cm, poniendo todos mis conocimientos técnicos en marcha, y aprendiendo otros muchos con el objetivo de hacer mi _primer contacto_.

## Cobertura
Viviendo en Europa me toca apuntar al Astra 3B. Para asegurarnos de la cobertura geográfica necesito saber el satélite y la banda que escucho: Ku. Con estos datos acudiremos a una aplicación que calcule el PIRE para nuestra localización como [SatBeams](https://www.satbeams.com/footprints). 

<img src="./img/Astra3B_footprint.png" align="center" />

El PIRE es la Potencia Isotrópica Radiada Equivalente. Simplificando mucho, este dato nos indica la potencia con la que llega la señal. Por tanto, cuanto más bajo sea este dato, más débil es la potencia de la señal en esa zona y como consecuencia, mayor diámetro de parabólica necesitaremos. En mi localización la recomendación es de una parábola de 60cm para el haz “Europe Wide”. Como yo estoy utilizando justo el doble, la recepción no debería ser un problema.

<img src="./img/4L_antena.png" width=300 align="right" />

## La antena
Aunque como hemos visto, captar la señal Othernet no me requiere un elemento receptor muy grande. He elegido una parábola grande porque tengo interés en reutilizar la instalación para conexiones con otros satélites como el Es'hail 2 / QO-100 que necesitan más ganancia.
Y por esta razón acepté de buen gusto la donación de una maltratada antena offset de 120cm que pude transportar gracias a mi ´clásico´.

### Restauración y montaje
<img src="./img/despiece_antena.jpg" align="center" />

Tocó despiezar, desoxidar, enderezar y pintar. Y como suele pasar, algo se rompió por el camino. Precisamente una de las piezas más criticas: el tornillo de ajuste de elevación. Así que pusimos en marcha una iniciativa maker local y gracias a mi amigo Toni Lupianez, tengo uno como nuevo.
|Problema-solución|Implementación|
|---|---|
|<img src="./img/problema_tornillo_ajuste_elevacion.jpg" width=200/>|<img src="./img/nuevo_tornillo_ajuste_elevacion.jpg" width=200/>|

Una vez completado el kit de antena parabólica. El montaje no representa muchas dificultades y se puede completar en seis sencillos pasos.
</br>
1. Una vez colocado el tope con dos tuercas laterales. Se ha podido fijar la abrazadera principal sobre el mástil con 4 tornillos de métrica 10 orientada longitudinalmente a la base a fin de proporcionar la máxima estabilidad.
<img src="./img/montaje_antena_paso1.jpg" width=200 align="center" />

2. Este modelo tiene tres pasadores que fijan la base de la parábola que atraviesan una estilo que sirve de indicador de elevación sobre un limbo graduado.
<img src="./img/montaje_antena_paso2.jpg" width=200 align="center" />

3. Seguidamente se fijan los pasadores en el otro extremo utilizando una platina que soportará el mecanismo de ajuste de elevación.
<img src="./img/montaje_antena_paso3.jpg" width=200 align="center" />

4. Antes de colocar la parábola es necesario tener el LNB y el soporte fijado ya que facilitará su posterior montaje.
<img src="./img/montaje_antena_paso4.png" align="center" />

5. Se fija la parábola con 6 tornillos de métrica 8.
<img src="./img/montaje_antena_paso5.png" align="center" />

6. Y finalmente se hace el ajuste del punto focal donde deberá estar el LNB. Podemos ahorrarnos los cálculos utilizando esta página web: https://www.satsig.net/pointing/finding-dish-offset-angle.htm
<img src="./img/calculo_foco_antena.png" align="center" />

### Orientación
<img src="./img/orientacion_antena.png" width= 400 align="right" />

Para orientar una antena parabólica hacia un satélite geoestacionario. Se necesitan 3 valores expresados en grados de ángulo:

- **Azimut**: ángulo horizontal respecto al Norte verdadero o geográfico en cuya vertical está el satélite posicionado.
- **Elevación**: ángulo vertical de la posición del satélite respecto a la línea del horizonte.
- **Polarización**: ángulo horario de captación de la señal respecto a la vertical. 

Hay muchas aplicaciones y páginas web para calcular estos parámetros de ajuste. Recomiendo [satlex](https://www.satlex.it/es/azel_calc.html) muy útil para casos como este en el que no conocemos el ángulo de _offset_ de la parábola. 

En todo caso se pueden hacer los cálculos con dos fórmulas sencillas que nos serán útiles para orientar la antena:
<img src="./img/parametros_elevacion_offset.png" width=300 align="right" />

- **Angulo de _offset_ (O)** 
- - Offset = secante ( diámetro menor / diámetro mayor )
- - sec(120/130) = 22,62°
- **Angulo de respecto a la horizontal (H)**
- - H = 90 - ( E - O ) donde E es el ángulo de elevación: 39,48 en mi caso
- - 90-(39,48-22,62) = 73,14°

Utilizando la aplicación móvil [Satellite Finder](https://apps.apple.com/us/app/satellite-finder-pro/id1075788157#?platform=iphone). Confirmamos los datos obtenidos anteriormente y nos permite hacer los ajustes utilizando directamente el compás y el inclinómetro de nuestro móvil que junto con la cámara, nos despejará la duda de obstáculos entre el satélite y nuestra ubicación.
 
|Ajuste elevación|Ajuste azimut|
|---|---|
|<img src="./img/satellite_finder_check_elevacion.png" width=200/>|<img src="./img/satellite_finder_check_azimut.png" width=200/>|

## Hardware
La [web oficial](https://othernet.is/products/dreamcatcher-v3-05) sigue ofreciendo el _Dreamcatcher v3.05 Data Radio Kit_ aunque informa que se va a deprecar por lo que su **precio está rebajado a $49**. Advierto que es una compra en USA por lo que al precio final habrá que sumarle gastos de envio de unos $30 y unas impredecibles tasas de aduana que deberían ser poco más que el 21% de IVA aplicable.

|Dreamcatcher v3.0|LNB|
|---|---|
|<img src="./img/Dreamcatcher-v3_05.png" width=600/>|<img src="./img/Dreamcatcher_LNB.png" width=200/>|
|Procesador a 1 GHz ARM|LNB 13V/18V bias tee|
|256 MB RAM|Entrada: 10,7-12,75GHz|
|Adaptador WiFi USB|L.O.:9,75/10.6GHz|
|Dos adaptadores microSD slots uno para contenidos|Ruido: 0,3dB (Typ.)|
|LEDs para recepción de paquetes, heartbeat, y alimentación|Ganancia: 60dB(Typ)|
|TCXO 2.5 PPM high precision||
|Botón para resetear wifi en modo AP||
|Tamaño 12 x 11.7 cm ||

### Resultado
Finalmente ya tengo todo dispuesto y la antena con una orientación aproximada. El Dreamcatcher queda situado en la parte trasera de la base protegido por una caja estanca.
</br>

<img src="./img/montaje_antena.jpg" align="center" />

<img src="./img/tuner.png" width=400 align="right" />

## Software
Si queremos que el dispositivo Dreamcatcher reciba mensajes de Othernet tendremos que cargar en una tarjeta micro-SSD la imagen del Skylark, que no es más que un Linux Debian adaptado a ARM con una aplicación adapta de RACHEL. 

La última versión la podemos descargar de: https://archive.othernet.is/Dreamcatcher3%20Skylark/ Yo he utilizado la v5.8 de 04-Mar-2020 que está disponible en este repositorio junto con la [guía de usuario](https://github.com/McOrts/OTHERNET_GroundStation/blob/main/docs/DreamcatcherV3.05.pdf) donde se explican más detalladamente algunos pasos de la instalación y configuración.
</br>
Resumiendo, el dispositivo crea un punto de acceso wifi sin credenciales, en un principio, desde el que accederemos a una aplicación web en la URL 10.0.0.1. Una vez dentro, las opciones propias para una instalación en Europa están dentro de la configuración de **Tuner** en la pestaña de Satellite.
</br>
<img src="./img/checklist.png" width=500 align="right" />

Finalmente si toda la instalación ha sido correcta. Desde el icono de **Log Viewer** en la pestaña de diagnósticos tendremos un checklist todo a OK tal cual así:

<img src="./img/status.png" width=300 align="right" />

## Primer contacto
Llegado a este punto con todos los inconvenientes resueltos. Deberíamos empezaremos a recibir paquetes. Si la antena no está todo bien ajustada, puede que nos encontraremos paquetes inconvenientes. Hay un mínimo de PER (Packet Error Rate) para que el proceso linux que interpreta los paquetes de datos pueda transformarlo en ficheros válidos. Esto lo veremos en 'System messages' dentro del icono de 'Log Viewer'.

En cuanto un solo paquete sea recibido. En la ventana de configuración **Tuner** pestaña de 'Status' encontraremos unos indicadores de la calidad de esta recepción. Los criterios más generales para interpretarlos son cuatro:

- La **relación Señal/Ruido** (SNR) debe entrar en el rango de -14 dB a +10 dB en el mejor de los casos.
- El valor de **Lock** a 'yes'
- El **RSSI** indicador de potencia de señal (Received Signal Strength Indicator) fluctuará entre los valores de -60 y -100 dBm.
- Cuando tengamos perfectamente ajustada la recepción, deberíamos tener un 100% de paquetes válidos y alcanzar un **ancho de banda** de 10.000 baudios (bps).

## Acceso a mi instalación
Fiel al propio espíritu del proyecto he querido dar acceso libre a mi instalación. Y para que se pueda ver de primera mano qué tipo de mensajes se reciben, la aplicación de previsión metereológica o navegar por wikipedia. He abierto un acceso web público donde podrás entrar con la siguiente credencial:

- Usuario: gest
- Password: gest
- URL: http://domohome.ddns.jazztel.es:48150
<img src="./img/apliacion_skylark.png" align="center" />

Solo necesitas un navegador y podrás acceder a OTHERNET desde tu dispositivo consultando la información en tiempo real que tenga actualizada en ese momento mi Dreamcatcher.

### En el mapa de _Ground Stations_
Tendremos todo preparado tras unas últimas tareas administrativas como la conexión a la red local, el cambio de password de administración y NAT de puertos para el acceso fuera de nuestra red.

El backoffice del sistema ofrece un mapa on-line de las estaciones activas en el mundo. Parece que somos 3 en España aunque el número varía a consecuencia de desconexiones de mantenimiento:
https://status.othernet.is/

# Agradecimientos
- Toni Lupianez [@tonilupi](https://twitter.com/tonilupi)
- IES?
