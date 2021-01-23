# OTHERNET acceso libre a datos desde el espacio
En torno a un servicio de broadcast digital de datos desde satélites geostacionarios. Othernet provee a pequeños dispotivos locales o _hostpots_ de repositorios de datos metereológicos, noticias, Wikipedia, mesanjes y archivos que pueden ser compartidos en el segmento terrestre. 
Para Europa central tenemos el acceso a través del satélite Astra 3B, orientación 23.5E que opera en banda Ku.

## Una larga historia
Inspirado en el proyecto [RACHEL](https://worldpossible.org/) que permite montar una plataforma autónoma de contenidos y formación como punto de acceso wifi allí donde no hay internet. [Syed Karim](https://www.linkedin.com/in/syedkarim1/) graduado en informatica por la Universidad de Ilinois, replanteó a lo grande este concepto. ¿Y si los RACHEL se actualizan desde el espacio?. Así podrían desvincularse de las redes terrestres, y por ende, estar en cualquier parte del mundo donde al menos un panel solar pueda dar energia. 

<img src="./img/outernetgraphic-300x139.png" align="center" />

Y este concepto se materializó en 2015 en el proyecto Outernet con su dispositivo _Lantern_ que abogaba por la libre información, la educación y el acceso un nivel básico de noticias en cualquier parte del mundo idependientemente de su localización, recursos o infraestructuras. Una primera aportación de la organización MDIF (Media Development Investment Fund) permitió construir un prototipo de receptor y un acuerdo con los operadores de los satélites Galaxy 19 y Hot Bird.

<img src="./img/LanternBoardDesing.png" align="center" />

Y así fué como nació la campañana de _crowdfunding_ ["Latern: A Global Satellite Data Radio"](https://igg.me/at/outernet/x#/updates/all) en Indiegogo. Con un presupuesto de 390K$ alcanzando los 573K$. En la que participé apadriné un Lantern para ser donado a paises africanos. Por lo que me vi privado de tener un receptor hasta que me apunté a una segunda ronda en la que había la posibilidad de tener un dispositivo DIY basado en un receptor de DVB-S2 (Geniatech Mygica HDStar) y una _single board computer_ como una Raspbery Pi. Pero de nuevo me quedé con las ganas porque nunca me funcionó. El clásico problema de incompatibilidad de versiones y la falta de soporte frustó el intento. Pese a que la propia Raspberry Pi Fundation 

<img src="./img/FirstLantern.jpg" width="400" align="center" />

Por otra parte ya había pasado más de una año tras completarse la campaña y al proyecto se replantea el segmento espacial. Habían pasado del pensar en una constelación de micro-satélites propios en órbita baja (LEO) construidos por la escocesa Clyde Space. A contratar un transpondedor de un geostacionario. Finalmente llegaron a un acuerdo con ViaSat para el uso de un _beam_ que empezó con 20MB por día de _uplink_ desde el satélite SkyTerra-1 en banda L. Lo que garantizaba la recepción con antenas pequeñas. En 2018 el proyecto se renombra a Othernet y transita por una serie de diseños de receptor. 

En 2020 el proyecto se consolida como una empresa M2M en Chicago (Ilinois USA) con Syed Karim como CEO. Y define una solución más comercial y menos maker. Un receptor propio basado en arquitectura ARM y receptor de banda Ku con decodificación LoRa que da un ancho de banda de solo 20 Kbaudios pero suficiente para el tipo de contenidos que se manejan. Respecto a la cobertura. El servicio de banda Ku geostacionario; a América del Norte es proporcionado por el SES-2 en 87° Oeste y para Europa por el Astra 3B en 23.5 ° Este.

Y es aqui cuando me reengancho adquiriendo el Dreamcatcher, reciclando una antena parabólica offset de 120 cm y poniendo todos mis conocimientos técnicos en marcha para hacer mi _primer contacto_.


 
