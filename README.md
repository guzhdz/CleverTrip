# CleverTrip (SISTEMA DE INFORMACION TURISTICA INTELIGENTE)

## Autores:
- [Inti Martinez Flores](https://github.com/inti2001) (intimtzflo@gmail.com)
- [Saul Alfonso Torres Munguia](https://github.com/NaClamandra) ()
- [Gustavo Hernández Cano](https://github.com/guzhdz) (guzhdz28@gmail.com)

## Antecedentes
Un gran número de personas al momento de realizar un viaje buscan realizar actividades recreativas, visitar exhibiciones y sitios de interés, comer en buenos restaurantes, o simplemente pasar un rato de entretenimiento, incluso al encontrarse en puntos diferentes de su propia ciudad, sin embargo no conocen sus alrededores, que tipos de lugares les gustaría visitar o simplemente requieren crear un plan para los días que estarán de viaje. Se propone el desarrollo de un sistema de búsqueda de información turística inteligente, utilizando técnicas de recomendación con inteligencia artificial y sistemas de búsqueda y planificación de viajes, con el objetivo principal de servir como un guía turístico a los usuarios brindando sugerencias de los mejores sitios (restaurantes, hoteles, lugares de interés, etc.) basados en sus gustos y preferencias y en función de su ubicación actual, y, por medio de la herramienta de creación de planes de viaje,  el usuario pueda organizar mejor sus actividades y posibles sitios de interés.
Palabras claves – Proyecto modular, Inteligencia artificial, Plan de viaje, API, Google Places, Google Maps, Firebase, Filtro colaborativo, TypeScript, JSON, Angular, NoSQL, MVC, Scrum, Microservicio.

## Info proyecto:
Link despliegue: https://clevertrip-59cb1.web.app/
Versión actual del código: CleverTrip 1.0
Licencia legal código: MIT Licence

## INTRODUCCIÓN
Desde siempre las personas han tenido la necesidad de buscar entretenimiento y actividades durante sus viajes o mientras disfrutan de su tiempo libre y aún más cuando no se encuentran en lugares no familiares o poco conocidos para ellos.
La mayoría de los casos,  las personas se ven limitadas a visitar únicamente lugares que ya conocen o  basarse exclusivamente en recomendaciones de sus amigos y familiares. En otras circunstancias, se encuentran sin ninguna referencia, lo que restringe considerablemente la posibilidad que tienen de descubrir nuevas ubicaciones que podrían resultar de su agrado y que, quizás, se hallan a pocos pasos de distancia, permaneciendo sin ser descubiertas hasta el momento.
	Después de identificar anteriormente las limitantes que puede tener el público, surgió el interés de brindar a las personas una manera sencilla y cómoda de buscar y encontrar nuevos lugares de interés que de otra forma pudieran no haber sido descubiertos, además de brindar la herramienta de plan de viaje para que los usuarios puedan aprovechar el tiempo de su viaje al máximo al ya tener una planeación previa del mismo.
	Entre los beneficios que se pueden listar de implementar una nueva forma para descubrir locaciones se encuentran y una herramienta para organizar los viajes futuros:
Recomendaciones basadas en los gustos del usuario.
Búsqueda en los alrededores de la ubicación actual del usuario y en cualquier lugar del planeta.
Filtros adaptables a las necesidades de cada persona, para realizar búsquedas más precisas.
Amplia gama de resultados de búsqueda, incrementando la posibilidad de descubrir nuevas locaciones de interés para el usuario.
Dar libertad al usuario para crear y planear de manera agradable los próximos viajes a realizar.
Asistir constantemente al usuario durante su viaje.
Además, se ha identificado la necesidad de las personas de optimizar al máximo su tiempo durante cualquier viaje. En respuesta a ello, se ha introducido una metodología para planificar los lugares a visitar, presentándose en un formato de itinerario que facilita la organización y ejecución de las actividades deseadas, además de una forma de establecer una ruta a seguir durante el viaje.
II. TRABAJOS RELACIONADOS
Antes de comenzar el desarrollo, y durante el mismo se consultó de manera constante aplicaciones o webs similares al proyecto que se llevaba a cabo. En dicha investigación se encontraron diversos proyectos que servían como solución al problema que se planteó previamente, tanto enfocadas en dar un servicio de información, búsqueda y recomendación de posibles destinos de viaje. 
A continuación se describen las aplicaciones que se encontraron:
TripAdvisor
TripAdvisor[1] es una plataforma web y una aplicación móvil que proporciona información sobre hoteles, restaurantes, atracciones y actividades turísticas en todo el mundo. También cuenta con una función de recomendaciones personalizadas basadas en tus preferencias y comportamiento de navegación. TripAdvisor fue fundada en febrero de 2000 por Stephen Kaufer y Langley Steinert en Needham, Massachusetts, Estados Unidos. Ofrece servicios gratuitos, pero también genera ingresos a través de publicidad y reservas en línea.
Sin embargo, esta llega a tener ciertos problemas:
La búsqueda aunque funciona correctamente, esta es algo limitada con pocos filtros de primera mano (solo categorías generales), enfocándose más en la recomendación constante. Para poder encontrar filtros más específicos se debe dar muchos pasos.
Los resultados de búsqueda son sesgados siempre beneficiando los lugares más costosos, lujosos y populares, provocando que lugares más pequeños no sean visibles o incluso inexistentes.
La privacidad es poca ya que cualquier persona puede acceder a la cuenta de otra para ver su actividad.
TripAdvisor, como cualquier plataforma, tiene intereses comerciales y puede priorizar ciertos establecimientos o anuncios pagados, lo que podría afectar la imparcialidad de las recomendaciones.
TripHobo
TripHobo[2] es una plataforma de planificación de viajes que ofrece itinerarios personalizados, sugerencias de actividades y atracciones turísticas en todo el mundo. Los usuarios pueden crear itinerarios detallados, incluyendo transporte, alojamiento y actividades, y también pueden compartirlos con otros viajeros. Necesitas crear una cuenta para poder utilizar esta plataforma.
Esta plataforma cuenta con una clara limitante y es que se enfoca demasiado en la planificación de viajes dando muchas herramientas para este pero dejando un poco de lado la búsqueda de los posibles  lugares a visitar, además que presenta una interfaz nada agradable que puede abrumar a varios usuarios. Por último la búsqueda y sus resultados cuenta con los mismos problemas que TripAdvisor al ser sesgada y dar un incompleto panorama de las opciones.
Yelp
Yelp[3] es una plataforma en línea que fue fundada en 2004, esta plataforma es una guía virtual exhaustiva que ofrece reseñas, calificaciones y comentarios sobre una amplia variedad de establecimientos, desde restaurantes y cafeterías hasta servicios profesionales, tiendas y más. La esencia de Yelp radica en proporcionar a los usuarios una valiosa fuente de información comunitaria, donde pueden compartir sus experiencias personales con otros usuarios en forma de reseñas detalladas.
Esta plataforma está bien establecida como sistema de búsqueda de lugares y actividades, así como destinos y hoteles, con distintas herramientas y filtros a su disposición creando un ambiente apto de búsqueda. Sin embargo solo se enfoca en eso en la búsqueda, ya que no proporciona ninguna herramienta para organizar o planificar algún viaje, solo enfocándose en recomendar y buscar lugares populares, siendo más una red social, al permitir tanta interacción entre los usuarios.
A lo largo de la aplicación no se encontraron más herramientas, aplicaciones o plataformas similares a nuestra solución. Solo se encontraban herramientas enfocadas en la búsqueda y registro de hoteles o viajes en aerolíneas así como también enfocados en agencias de viajes y tours prefabricados.
Algunos ejemplos:
Booking.com
Expedia
Google Maps (Mas un motor de búsqueda)
Viator
III. DESCRIPCIÓN DEL DESARROLLO DEL PROYECTO MODULAR
Durante la realización de este proyecto se utilizó la metodología ágil[4] scrum[5], con la cual se toman las tareas a realizar y se dividen en tareas más simples y de fácil realización.
Se comenzó con una redacción del plan de proyecto determinando las ideas principales y las funciones que tendría el proyecto así como también que partes del mismo cumplirían para cada módulo solicitado en el proyecto modular. A continuación se realizó una lista de requerimientos funcionales y no funcionales divididos en los módulos principales del proyecto y así establecer los objetivos del sistema. Después se realizó una investigación y selección de las distintas tecnologías a utilizar para la programación del proyecto, además de la selección de apis o servicios para cumplir con todos los requerimientos.
Finalmente antes de comenzar a realizar el proyecto se usó la herramienta de Diagrama de Gantt[6] para la división de tareas y tiempos a lo largo del desarrollo.
Para la comunicación efectiva entre los miembros del equipo se utilizó WhatsApp para cuestiones informales, ya que esta plataforma es de las más rápidas de la actualidad, mediante esta, se programaron reuniones del equipo y se trataron temas cuya resolución se podía resolver vía mensajes de texto.
Para la comunicación formal con la asesora del proyecto se utilizó la plataforma Google Meet para reuniones donde se mostraron avances y se resolvieron dudas sobre los mismos.
Se creó un repositorio[7] en la plataforma GitHub, con la cual se puede hacer un control sobre los cambios realizados al proyecto y en la que los integrantes del equipo pueden subir los avances que realizan y comparar los cambios.
Para la codificación del proyecto fue utilizado el framework de AngularJS[8] junto con su biblioteca de componentes Angular Material[9], mediante estas tecnologías fue posible la codificación del modelo de la página, su funcionalidad y conexión con base de datos.
La aplicación utiliza servicios de Google Places[10] y Google Maps Plattform[11] por medio de APIs a modo de microservicios para obtener información de geolocalización, rutas e información de los lugares.
Por medio del uso de los servicios Lambda y Api Gateway se establece el modelo de microservicios donde con simples peticiones desde la app principal se pueden realizar consultas a una base de datos NoSQL de Firebase[12] donde se almacena la información con la que la aplicación puede ejecutar las operaciones necesarias para generar las recomendaciones a los usuarios con la inteligencia artificial. Además de también hacerse las operaciones necesarias con la API de Google Maps.

La aplicación se divide en tres módulos principales, siendo el inicio de sesión y registro de cuenta (Gestión de cuentas de usuarios), recomendación y búsqueda de locaciones, gestión de cuenta y planes de viaje (Dashboard).
Cada uno de los módulos utiliza alguno de los microservicios[13] de la aplicación:
Gestión de cuentas de usuario (Microservicio de Base de datos)
Recomendación y búsqueda (Microservicio de Base de datos y de Google Api[14])
Dashboard (Microservicio de Base de datos y Google Api)

Ya realizadas las investigaciones y seleccionadas las tecnologías se realizaron un mapa de pantallas para establecer las vistas que tendremos y posteriormente se comenzó del diseño de las mismas.

Fig. 1 Camino de pantallas


Fig. 2 Diseño preliminar de vistas

Al tener ya establecidos los diseños de la estructura y vistas del sistema se comenzó con la programación del mismo, al principio se tuvo un problema de compatibilidad entre la versión de Angular  una dependencia pero se resolvió haciendo un downgrade de versión.

Se realizó el esqueleto de la aplicación como también la conexión con la base de datos, posteriormente se decidió el trabajo entre los tres integrantes donde uno se encargaría de la funcionalidad de la base de datos como de la aplicación en sí, otro se encargaría del diseño visual, interactividad y de hacer responsiva la aplicación y finalmente el último integrante se encargaría de la implementación del algoritmo de recomendación.

Mientras cada uno realizó sus respectivas tareas, hubo un apoyo mutuo entre los integrantes mientras se trabajaba. En cierto punto se contempló que el enfoque a un sistema de recomendación en base a contenido no iba a ser posible por lo que se optó por un enfoque a un sistema de recomendación de usuario a usuario (filtrado colaborativo).

Lo primero en terminarse fue el motor de búsqueda al cual se le realizaron pruebas constantes y arreglo de bugs, sin embargo el equipo no contempló que el uso de imágenes durante las pruebas les costaría mucho dinero por parte de la API de Google (el que proporcionaba la imagen), por lo que se optó desactivar las imágenes durante el desarrollo.

Cuando el integrante que se encargó del diseño había terminado en su mayoría el diseño de la aplicación se le pidió encargarse de la programación y estructuración de los microservicios en AWS.

Después se decidió continuar con el módulo de Dashboard, el cual fue el que más tiempo tomó debido a sus distintas funcionalidades. El equipo se encontró con distintos retos en cuanto a la funcionalidad de la base de datos y el mantener actualizada la aplicación, pero se terminó arreglando.

Terminado los dos módulos más importantes se continuó con el de recomendación (IA) además de realización de pruebas constantes y búsqueda de bugs, atento en el último módulo terminado, como en el resto de la app.

Finalmente antes de la primera revisión se trató de llegar a un prototipo estable de la aplicación para así presentar los avances ante el comité de evaluación, los cuales dieron algunas observaciones.

Observaciones:
Tendría que trabajar sobre el plan de viaje. 
Replantear la parte de sugerencias de viajes.
Justificar los beneficios que tiene su aplicación contrastando con lo que ya ofrece Google. 
Reconstruir el plan de viaje conforme a las necesidades de los viajeros. 
Realizar modificaciones basándose en situaciones reales de viajeros y sus necesidades.

En base a las observaciones obtenidas de la primera revisión se decidió implementar nuevas funcionalidades al sistema, enfocando los esfuerzos en el módulo de plan de viaje.

Fueron implementadas mejoras visuales tanto en la página principal como en la sección del dashboard, dando estilos más llamativos y agradables incitando al usuario a utilizar esta funcionalidad.

Se formuló una nueva funcionalidad “Tour de viaje” a partir de las observaciones referentes a diferenciar más nuestro sistema a la oferta de google. Esta nueva funcionalidad toma todas las visitas del plan de viajes de un usuario y genera una ruta que pasa por cada uno de los destinos del plan, además de agregar las opciones para seleccionar el medio de transporte a usar para cada ruta del tour. Existe la opción “Mi Tour” el cual acomoda el orden de las rutas en base al itinerario de visitas que el usuario definió, por otro lado existe la opción “Tour Recomendado” que acomoda el orden en base a la cercanía de los lugares, esto para que se tenga un circuito de visitas más eficiente. 

Bienvenida
Al ingresar a la plataforma el usuario se encontrará con una página de bienvenida donde explicará a grandes rasgos la funcionalidad de la aplicación y permitirá al mismo iniciar sesión o registrarse.
La aplicación demanda el registro de cuenta de usuario para su utilización, por lo tanto según si el usuario desea registrarse o iniciar sesión, este deberá clicar en  el respectivo botón.


Fig. 3 Bienvenida

Inicio de sesión
En la página de inicio de sesión se le permitirá al usuario iniciar con un correo y contraseña o en su defecto con una cuenta de Google, se escogió este método extra de inicio de sesión debido a las facilidades, ventajas y rapidez que aporta el uso de las tecnologías Google en el sistema para el inicio de sesión. También se le presenta la posibilidad de recuperar la contraseña o ir a la página de registro.


Fig. 4 Inicio de sesión

Registro
Dentro de la página de registro se presenta un formulario donde pide los datos para registrar al usuario, entre ellos:  correo, contraseña y nombre de usuario; cumpliendo con los requisitos necesarios, el usuario será capaz de registrarse. También se le presenta la posibilidad de navegar a la paginas en inicio de sesión en caso de ya poseer una cuenta.
Nota: Es necesario el validar el correo con el que se registre el usuario, en caso de haberse registrado de manera convencional (No mediante Google) de lo contrario no le permitirá acceder al sistema al usuario.

Fig. 5 Registro de cuenta

Página principal
Iniciada la sesión al usuario se le presenta la página principal donde aparecerán recomendaciones de locaciones en base a calificaciones que da el usuario dividido en categorías. También se presenta una barra de búsqueda desde donde el usuario podrá ingresar palabras clave para realizar una búsqueda general de localidades en base a lo anteriormente escrito o si desea ir directamente a la creación de planes de viaje. Además de un menú lateral y botones de categoría que permite navegar a las distintas funcionalidades de la aplicación.


Fig. 6 Página principal


Fig. 7  Recomendaciones

Fig. 8 Menú lateral

Búsqueda general
En la página de búsqueda general se presentan los resultados de la búsqueda realizada mediante la barra de búsqueda con una serie de filtros y un menú de categorías. El menú permite acceder a los resultados de búsqueda en base a cierto filtro de categoría y cada una de ellas tiene sus propios filtros de subcategorías, además de tener la capacidad de ordenar los resultados (Orden Alfabético Ascendente, Orden Alfabético Descendente y Orden según la calificación “rating” de los resultados). Dentro de la página se presenta de nuevo la barra de búsqueda para realizar una nueva y al seleccionar en una locación se presenta un diálogo mostrando la información relacionada a la misma.




Fig. 9 Búsqueda general

Diálogo de información de locación
Dentro del diálogo de la información sobre la locación, se presenta a detalle todos los datos que se tienen de dicha locación al igual que sus reseñas, el usuario es capaz de agregar el lugar su lista de favoritos, lista de interés, un plan de viaje ya creado o calificarla con una serie de botones en la parte inferior. Se presenta además un botón que envía al usuario a la página de ruta de viaje.


Fig. 10 Diálogo de información de locación

Ruta de viaje
Dentro de la página de ruta de viaje se presenta al usuario un mapa con una ruta a seguir desde su ubicación hasta el destino (locación anterior) en distintos modos de transporte (automóvil, caminando, bicicleta, transporte público), estos modos pueden ser seleccionados por una serie de botones, actualizando la ruta, tiempos estimados y distancias a recorrer cada vez que se selecciona un medio de transporte distinto.


Fig. 11 Ruta de viaje

Búsqueda categórica
Dentro de la pagina de busqueda categórica (accesible mediante alguno de los botones de la página principal que tiene una categoría), se presentan los resultados de una búsqueda realizada en base a una categoría de todas las locaciones cercanas a la ubicación actual del usuario, es una forma de realizar una búsqueda rápida de lo necesario en ese momento y de sitios de fácil acceso para el usuario. En esta página el usuario podrá filtrar en base a subcategorías como también ordenar los resultados en base a popularidad u orden alfabético (Ascendente o Descendente). Al igual que en la búsqueda general si una locación es seleccionada se presentará el diálogo de la información relacionada a la misma.


Fig. 12 Búsqueda general

Dashboard
Dentro de la página de Dashboard se presenta la información general de la cuenta del usuario en la plataforma, dando la posibilidad de configurarla en cualquier momento. Además se muestran tres secciones importantes: favoritos, planes de viaje e historial. Estas secciones pueden ser seleccionadas mediante un pequeño menú al inicio de la sección y también mediante el menú lateral.
La sección de favoritos presenta una lista de las locaciones que el usuario hubiera guardado como favoritos, siendo capaz de seleccionar alguna y que se muestre el diálogo se su información relacionada. La sección historial es similar solo que en este caso muestra las locaciones que el usuario ha visto a lo largo de la navegación de la plataforma.
Dentro de la sección de planes de viaje se presentan dos listas, una mostrando los viajes que el usuario ha creado y la segunda mostrando la lista de interés del usuario, siendo locaciones que le interesa visitar y agregar en alguno de sus planes de viaje. De la lista de viajes, se permite eliminarlos o ver sus detalles, estos serán desplegados en la parte inferior de las listas, mostrando la información general del viaje, pudiendo modificar los horarios y el nombre, así como agregar locaciones de la lista de interés al propio viaje y dándole un horario específico, además de brindar la posibilidad de generar un tour, donde lo enviará a la página de Tour de viaje
De la lista de interés se permite eliminar alguna locación de la lista, agregarla a uno de los viajes actuales o ver los detalles (abriendo el diálogo de su información relacionada).

Fig. 13 Dashboard (Planes de viaje)



Fig. 14 Dashboard (Detalles del Plan de viaje)

Tour de viaje
Una vez que el usuario hace click en el botón de generar tour desde la sección de detalles del plan de viaje, se abre la página del Tour de viaje. 

En esta página se puede observar el circuito que generan las rutas que pasan por cada visita del plan de viaje del usuario teniendo dos opciones para la generación de este circuito:

Mi Tour: Se calculan las rutas tomando en cuenta el itinerario establecido por el usuario para decidir qué lugar se tiene que visitar antes que otro.
Tour Recomendado: Se calculan las rutas en base a la cercanía de los lugares a visitar, haciendo que de esta manera se reduzca el tiempo de transporte aprovechando a visitar los lugares que se encuentran más cerca de su posición.

Por último se tiene la opción de generar cada una de las rutas en el medio de transporte que el usuario desee, ya sea caminando, en bicicleta, en automóvil o en transporte público.


Fig. 15 Tour de viaje

Hay que tomar en cuenta que todas las secciones de la plataforma son accesibles mediante botones o el menú desplegable (al igual que la opción de cerrar sesión), y siempre y cuando el usuario inicie sesión podrá utilizar las herramientas dadas por la plataforma.

Login y registro con FirebaseAuth
Se utilizó el componente de AngularJS para controlar el inicio de sesión y el registro de nuevos usuarios en el sistema, además de la utilización de un servicio (InicioService) para controlar las acciones de estos. Entre los métodos utilizados se encuentran:
createUserWithEmailAndPassword
signInWithEmailAndPassword
signInWithPopUp
Para la recuperación y verificación del email proporcionado por el usuario se utilizaron los métodos de sendEmailVerification y sendPasswordResetEmail.
Api Google Places:
La API de Google Places permite acceder a la información de lugares geográficos y comerciales, proporciona detalles específicos como dirección y horario de apertura y permite obtener lugares a partir de una ubicación dada. Entre los métodos implementados durante el desarrollo del sistema se encuentran:
getPlaceDetails
textSearch
nearBySearch
Api Google Routes[15]:
La API de Google Routes brinda la información  relacionada con la ruta de viaje recomendada entre punto A y punto B, además de que proporciona una manera de conocer el tiempo estimado de llegada al destino. El método implementado durante el desarrollo del sistema se denomina DistanceMatrix.
Api Geocoding[16]:
La API Geocoding permite acceder a los datos de Latitud (LAT) y Longitud(LNG) de una dirección formateada proporcionada. Entre los métodos implementados durante el desarrollo del sistema se encuentran:
getCurrentPosition
Objeto google.maps.Geocoder
El control de las API de Google es monitoreado a través de un proyecto de Google Cloud[17] en donde se observan a detalle las consultas generadas a los servicios que brinda Google.
Almacenamiento en la Base de Datos
La forma de almacenar la información en la base de datos de Firebase se realiza por medio de colecciones[18] y documentos[19], para el desarrollo del proyecto fue posible identificar las siguientes colecciones de datos:
Colección “usuarios”: En esta colección se almacenan los documentos referentes a cada usuario registrado del sistema con los siguientes campos:
nombre: nombre del usuario
correo: correo del usuario
calificadosId: identificador del documento de la lista de lugares calificados asociada con el usuario
favoritosId:identificador del documento de la lista de lugares favoritos asociada con el usuario
historialId:identificador del documento de la lista historial asociada con el usuario
interesesId:identificador del documento de la lista de lugares de interés asociada con el usuario
planesViajeId:identificador del documento de la lista de planes de viaje asociada con el usuario
Colección “listaUsuarios”: En esta colección se almacenan los id de todos los usuarios registrados en el sistema en un campo  “IDs”  de tipo Array.
Colecciones “listasFavoritos, listasIntereses y listasHistorial”: En estas colecciones se almacenan los documentos para las listas de lugares favoritos e historial respectivamente. Se almacenan con los siguientes campos:
FavoritosList/InteresesList/HistorialList: Campo de tipo matriz que almacena los registros de tipo mapa de cada lugar con los siguientes campos:
id: identificador del lugar
imgUrl: url de la imagen del lugar
nombre: nombre del lugar
rating: calificación del lugar entre 0 y 5
tipo: tipo de establecimiento
userId: Identificador del usuario asociado
Colección “listasCalificados”: En esta colección se almacenan los documentos para las listas de lugares calificados asociadas a cada usuario registrado en el sistema con los siguientes campos:
CalificadosList: Campo de tipo matriz que almacena los registros de tipo mapa de cada lugar calificado por el usuario con los siguientes campos:
id: identificador del lugar
imgUrl: url de la imagen del lugar
nombre: nombre del lugar
rating: calificación del lugar entre 0 y 5
ratingUsuario: calificación dada por el usuario entre 0 y 3
tipo: tipo de establecimiento
userId: Identificador del usuario asociado
Colección “listasPlanesViaje”: En esta colección se almacenan los documentos para las listas de planes de viaje asociadas a cada usuario registrado en el sistema con los siguientes campos:
PlanesViajeList: Campo de tipo matriz que almacena los registros de tipo mapa de cada plan de viaje creado por el usuario con los siguientes campos:
fechaFin: fecha de finalización del plan de viaje en formato Datetime
fechaInicio: fecha de inicio del plan de viaje en formato Datetime
idListaVisitas: Identificador de la lista de visitas asociada al plan de viaje
nombre: nombre del plan de viaje
userId: Identificador del usuario asociado
Colección “listasVisitas”: En esta colección se almacenan los documentos para las listas de visitas asociadas a los planes de viaje con los siguientes campos:
VisitasList: Campo de tipo matriz que almacena los registros de tipo mapa de cada plan de viaje creado por el usuario con los siguientes campos:
id: identificador del lugar
nombre: nombre del lugar
fechaVisita: fecha en que se tiene planeado visitar el lugar en formato Datetime
userId: Identificador del usuario asociado
Para las operaciones de lectura y escritura en la base de datos se utilizaron diferentes métodos para manipular los documentos dentro de las colecciones como los siguientes: 
Escritura: addDoc, deleteDoc, setDoc, updateDoc
Lectura: getDoc, getDocs
Manipulación de matrices: arrayUnion, arrayRemove

Módulo I Justificación de Arquitectura y Programación de Sistemas
La base fundamental del proyecto está basada en la programación web principalmente se utilizará TypeScript[20], HTML y CSS[21] junto con frameworks tales como Angular para crear una aplicación web con elementos modernos que se ajustan a las necesidades del proyecto por su flexibilidad y que además resultan atractivas para el usuario final.
El manejo de componentes en AngularJS permite tener un control por separado de los diferentes elementos que conforman la aplicación, facilita la reutilización de código y agiliza las tareas que se realizan dentro del sistema debido a su separación de responsabilidades SoC[22].
El sistema gestor de base de datos utilizado es Firebase este proporciona una base de datos NoSQL, en tiempo real, back-end y organizada en forma de árbol JSON.
Se seleccionó el patrón de arquitectura MVC (Modelo-Vista-Controlador)[23] puesto que al separar las distintas responsabilidades y mantener distintas capas que se encarguen de tareas concretas se asegura un mayor nivel de calidad de software, facilidad de desarrollo y mantenimiento, además al ser un patrón mayormente enfocado en soluciones web ofrece una mayor ventaja para poder manipular y mostrar datos al usuario de manera más eficiente. Con el uso de CSS, JavaScript y TypeScript integrados mediante el framework Angular podemos diseñar y programar la aplicación que resulta en una interfaz de usuario moderna, atractiva, flexible y amigable con el usuario final.
Debido a la estructura que proporciona el sistema gestor de base de datos en la que se manejan Colecciones y Documentos para almacenar la información, nuestra estructuración e intercambió de datos es por medio de archivos de formato JSON y de objetos con el formato de nuestros Documentos.
Modulo II Justificación de Sistemas Inteligentes
Inteligencia artificial aplicada mediante algoritmos de recomendación. Para ofrecer sugerencias personalizadas a los usuarios. Estos algoritmos pueden analizar los intereses, preferencias y comportamientos de los usuarios, así como los datos históricos, para recomendar destinos, actividades, restaurantes u otros servicios turísticos que se ajusten a sus gustos.
Se planteó en un primer momento utilizar un algoritmo de recomendación basado en contenido, no obstante, se replanteó esto puesto que dicho algoritmo requiere que la aplicación guarde de alguna manera la información de cada sitio, lo cual era inviable, al utilizar la API de Google Places para poder consultar la información; por lo tanto se optó por un algoritmo cuyas características le permitieran funcionar con colecciones de datos más pequeñas que se pueden almacenar fácilmente por la aplicación.
Sistema utilizado: El sistema de recomendaciones de filtrado colaborativo[24], se basa en el comportamiento y las preferencias de un grupo de usuarios para hacer recomendaciones a un usuario en particular. Opera mediante la recopilación de preferencias o gustos de un mismo consumidor comparados con los datos suministrados por personas con patrones similares. Este algoritmo consta de dos pasos principales, primero se calcula un rango de similitud entre el usuario objetivo y otros usuarios mediante el algoritmo de distancia euclidiana[25], y como segundo paso se clasifican los usuarios más parecidos a el usuario objetivo para así poder recomendar elementos guardados o calificados por los usuarios más parecidos.
Función dentro de la aplicación: El usuario tiene una lista de sitios a los que le ha dado cierta puntuación entre 1 (no me gusta), 2 (me gusta) y 3 (me encanta).
Al calcular la distancia euclidiana entre usuarios, obtenemos un porcentaje de similitud, este representa que tanto un usuario se parece, en cuanto a gustos a otro, con esto podemos recomendar a nuestro usuario objetivo los sitios que otros usuarios parecidos han calificado. Por lo que el algoritmo es capaz de identificar patrones de similitud entre usuarios.




Fig. 16 Ejemplo de recomendación
Módulo III Justificación de Sistemas Distribuidos

Con el uso del framework de AngularJS se trabajó con componentes y servicios de una manera modular en donde cada parte del sistema funciona por separado, de esta forma permite tener una mejor gestión del código.
La modularidad de los archivos incrementa el rendimiento del sistema al implementar el Lazy loading lo que significa que los módulos del sistema solo son cargados cuando estos son necesarios. Facilita la tarea de escalar el sistema a medida en que este crece en tamaño y complejidad, y todo esto sin afectar lo ya existente.
Además de la propia modularidad que ofrece angularJS se implementó un diseño basado en microservicios.
Una arquitectura de microservicios divide una aplicación en una serie de servicios implementables de forma independiente que se comunican a través de API. Este enfoque permite implementar y escalar cada servicio individual de forma independiente, así como la entrega rápida y frecuente de aplicaciones grandes y complejas. A diferencia de una aplicación monolítica, una arquitectura de microservicios permite a los equipos implementar nuevas funciones y hacer cambios más rápido, sin tener que volver a escribir una gran parte del código existente.
Así el proyecto es dividido en módulos donde mediante los microservicios cada módulo se encarga de una tarea específica como: 
Gestión de Base de datos
Obtención de datos de las API de Google

Fig. 17 Arquitectura modular propuesta

La arquitectura presentada divide la carga de trabajo en 2 microservicios principales, uno el cual se comunicará con la base de datos de Firestore[27] y otro que hará la comunicación con la API de Google places y demás servicios de Google, ambos microservicios residen en la nube de Amazon Web Services desde la cual accede el servidor y este transmite la información al cliente.
Estos microservicios residen en una nube de Amazon Web Service (AWS)[26], mediante servicios llamados Lambda y Api Gateway. La aplicación por sí sola no se encarga de realizar las operaciones necesarias de lectura, escritura o procesamiento y cálculo de datos, ya sea de la base de datos o lo referente a la API de Google, si no que el sistema se programó de manera que la app solo se encargue de la interacción con el usuario y renderización de vistas y cuando sea necesario hacer alguna operación de las antes mencionadas se haga una petición al servicio de API Gateway de AWS, este lo que hace es administrar todas esas operaciones y en base a qué petición fue hecha mandar llamar una función lambda que se encargará de realizar la tarea solicitada, Todas las funciones lambdas fueron programadas por los integrantes del equipo. Al terminar la función lambda envía una respuesta a la aplicación.
IV. RESULTADOS OBTENIDOS DEL PROYECTO
Se logró una división coherente de módulos principales dentro de la aplicación, logrando una mejor organización de tiempos y prioridades dentro del mismo y así poder cumplir con el objetivo principal de crear una aplicación funcional y con herramientas útiles para el usuario. Al inicio fue complicado establecer todas las funciones que se agregarían y determinar el alcance, pero con guía del asesor y organización previa se llegó a una división satisfactoria. 

Se logró la posibilidad de que el usuario tenga un biblioteca de sus lugares favoritos y viajes que desearía hacer, dando la posibilidad de organizarlos e incluso establecer horarios, incentivando la actividad de viajar a distintos lugares sabiendo que lugares cercanos le son útiles dependiendo de sus necesidades, además de generar planes de viaje y así planear sus siguientes aventuras.
Se consiguió implementar un algoritmo de inteligencia artificial, mediante el cual, el usuario obtiene recomendaciones personalizadas que se adaptan a sus gustos y preferencias, así el usuario puede acceder a nuevas opciones sin necesidad de buscar manualmente.
Se logró una conexión total y rápida con la API de Google dentro de un proyecto en Google Cloud, con esta conexión la aplicación fue capaz de aprovechar todos los servicios prestados por esta API y así solicitar todo tipo de información al alcance de un click, además de que se logró una conexión con una base de datos propia de la aplicación, donde se guardan los datos de las cuentas de usuario y registros de las propias cuentas que ayudarán a determinar las recomendaciones que se le presentan al usuario.

Se logró una aplicación con un sistema de búsqueda rápido y eficaz, capaz de proporcionar una serie de resultados amplia, sin ningún tipo de sesgo y siempre enfocándose en una búsqueda alrededor de la ubicación del usuario, teniendo el usuario la posibilidad de en cualquier momento buscar algún lugar cercano con un gran abanico de filtros. 

Se consiguió implementar un algoritmo de inteligencia artificial, mediante el cual, el usuario obtiene recomendaciones personalizadas que se adaptan a sus gustos y preferencias, así el usuario puede acceder a nuevas opciones sin necesidad de buscar manualmente.

Además se logró la posibilidad de que el usuario tenga un biblioteca de sus lugares favoritos y viajes que desearía hacer, dando la posibilidad de organizarlos e incluso establecer horarios, incentivando la actividad de viajar a distintos lugares sabiendo que lugares cercanos le son útiles para sus necesidades.
V. CONCLUSIONES Y TRABAJO A FUTURO
Se logró satisfactoriamente cumplir con los requerimientos propuestos al inicio del proyecto, creando una aplicación funcional, sencilla pero con herramientas útiles para el usuario, escalable y mejorable. Desde un inicio se planteó la aplicación como una herramienta multiplataforma, por lo que se logró un diseño responsivo siendo posible utilizar la aplicación tanto en computadora como móvil. El diseño y funcionalidad se tomó inspiración en aplicaciones similares como Tripadvisor, pero buscando un estilo propio y más sencillo.

En conclusión se logró una aplicación robusta y agradable al usuario, implementando un sistema de búsqueda rápido y eficaz, capaz de proporcionar una serie de resultados amplia, sin ningún tipo de sesgo y siempre enfocándose en una búsqueda alrededor de la ubicación del usuario, teniendo el usuario la posibilidad de en cualquier momento buscar algún lugar cercano con un gran abanico de filtros.

Como sugerencias a futuro surgieron distintas propuestas que se pueden implementar en la aplicación para mejorar la experiencia de usuario:

Inclusión de un sistema de opiniones y calificación de locaciones, donde los usuarios puedan compartir sus experiencias a otros usuarios y estos se guarden en la base de datos.

Inclusión de un sistema de recomendación de plan de viaje en base a gustos y preferencias de los usuarios, donde se arme un plan de viaje por sí solo mediante inteligencia artificial, así incentivar la actividad de viajar a otro lugar.

Añadir una mejor personalización de la cuenta, configuración de las imágenes del banner del perfil y foto de perfil, como también la adición de un modo oscuro de la aplicación.

Implementar un sistema que permita compartir en redes sociales las locaciones favoritas o planes de viaje realizados por el usuario.

Añadir conexión con distintas aplicaciones de transporte (Uber, Rappi, etc) y aplicaciones de hospedaje (Trivago).

Añadir un sistema de alertas y notificaciones para mantener al tanto al usuario del itinerario de su plan de viaje. y de esta manera mejorar su experiencia a lo largo de su travesía.

RECONOCIMIENTOS
Se agradece el apoyo y asesoría por parte la maestra Thelma Isabel Morales Ramirez por su ayuda incondicional antes, durante y después del desarrollo del proyecto modular. Debido a su guía y apoyo se logró un proyecto sólido, funcional y aterrizado en la cantidad de tiempo en que fue desarrollado. Se le agradecen sus correcciones, consejos y sobre todo conocimientos, ya que sin su apoyo el proyecto no sería posible.

Es importante destacar la tutoría y apoyo por parte del compañero de la universidad Jesus Angel Cota Lopez, quien ayudo y asesoro  a lo largo del desarrollo del proyecto, guiando en el proceso de la realización del mismo, para que este pudiera cumplir con los lineamientos de proyecto modular, además de un apoyo constante con información sobre el proceso de registro. Sin sus conocimientos y experiencia el proyecto no se hubiera registrado a tiempo y no sería un proyecto sólido y concreto.



REFERENCIAS
Tripadvisor, “Tripadvisor: más de mil millones de opiniones y aportes sobre hoteles, atracciones, restaurantes y más,” Tripadvisor. https://www.tripadvisor.com.mx/
TripHobo, “Vacation planner for your holidays: TripHobo,” TripHobo. https://www.triphobo.com/
Yelp, “Yelp,” Yelp. https://www.yelp.com.mx/guadalajara
 A. Cockburn, "Agile Software Development: The Cooperative Game," Addison-Wesley, 2006
M. Cohn, "Succeeding with Agile: Software Development Using
Scrum," Addison-Wesley, 2010.
J. A. Smith and D. S. Sutherland, "Successful Project Management," SAGE Publications, 2015.
 “Acerca de los repositorios - GitHub Enterprise Cloud Docs,” GitHub Docs.https://docs.github.com/es/enterprise-cloud@latest/repositories/creating-and-managing-repositories/about-repositories 
 “AngularJS — Superheroic JavaScript MVW Framework.” https://angularjs.org/ 
 A. C. Team, “Angular material,” Angular Material. https://material.angular.io/
 “Descripción general,” Google for Developers. https://developers.google.com/maps/documentation/places/web-service/overview?hl=es-419 
 Google Maps Platform, “Google Maps Platform - Soluciones de ubicación y de mapas,” Google Maps Platform. https://mapsplatform.google.com/intl/es-419/ 
 Firebase, “Firebase,” Firebase. https://firebase.google.com/?hl=es
 “¿Qué son los microservicios? | AWS,” Amazon Web Services, Inc. https://aws.amazon.com/es/microservices/#:~:text=Los%20microservicios%20son%20un%20enfoque,servicios%20son%20equipos%20peque%C3%B1os%20independientes.
  “¿Qué es una API y cómo funciona?” https://www.redhat.com/es/topics/api/what-are-application-programming-interfaces
“Documentación de Google Maps Platform,” Google for Developers. https://developers.google.com/maps/documentation/routes?hl=es-419
 “Descripción general de la API de Geocoding,” Google for Developers. https://developers.google.com/maps/documentation/geocoding/overview?hl=es-419
 “Servicios de cloud computing | Google Cloud,” Google Cloud. https://cloud.google.com/?hl=es
  “Modelo de datos de Cloud Firestore  |  Firebase,” Firebase. https://firebase.google.com/docs/firestore/data-model?hl=es-419
 “Modelo de datos de Cloud Firestore  |  Firebase,” Firebase. https://firebase.google.com/docs/firestore/data-model?hl=es-419
 “JavaScript with syntax for types.” https://www.typescriptlang.org/
 “CSS | MDN,” MDN Web Docs, Mar. 13, 2023. https://developer.mozilla.org/es/docs/Web/CSS
MENS, Tom; WERMELINGER, Michel. Separation of concerns for software evolution. Journal of software maintenance and evolution: research and practice, 2002, vol. 14, no 5, p. 311-315.
GONZÁLEZ, Yanette Díaz; ROMERO, Yenisleidy Fernández. Patrón Modelo-Vista-Controlador. Telemática, 2012, vol. 11, no 1, p. 47-57. 
S. Oni, «Introduction to recommendation System in Javascript», Medium, 7 de mayo de 2018. [En línea]. Disponible en: https://becominghuman.ai/introduction-to-recommendation-system-in-javascript-74209c7ff2f7 
GraphEverywhere, E. (2019, 29 octubre). Algoritmo de distancia euclidiana. GraphEverywhere. https://www.grapheverywhere.com/algoritmo-de-distancia-euclidiana/
MATHEW, Sajee; VARIA, J. Overview of amazon web services. Amazon Whitepapers, 2014, vol. 105, p. 1-22.
KESAVAN, Ram, et al. Firestore: The nosql serverless database for the application developer. En 2023 IEEE 39th International Conference on Data Engineering (ICDE). IEEE, 2023. p. 3376-3388.
