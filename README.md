# Geolocalizacion
Azure geolocalizacion Mayra-Karlos

Azure Maps nos permite crear un mapa donde brinda una experiencia de búsqueda interactiva para los usuarios. Acontinuacion se explicaran los pasos básicos para su uso en algun proyecto:

1.Se debe de crea una cuenta en Azure Maps.

2.Obtener la clave de suscripción de Azure Maps para usarla en la aplicación web de demostración.

3.Se descarga y se abre la aplicación de mapas.


Este inicio usa el SDK web de Azure Maps; sin embargo, el servicio Azure Maps se puede usar con cualquier control de mapa, como estos controles de mapas populares de código abierto y tambien ciertos complementos.

#Requisitos previos

Si no se tiene una suscripción en Azure, se debe crea una cuenta gratuita antes de comenzar.

=Inicie sesión en el portal de Azure =


#Crear una cuenta de Azure Maps

Se crea una nueva cuenta de Azure Maps con los siguientes pasos:

	1.Seleccione Crear un recurso en la esquina superior izquierda de Azure Portal .

	2.Escriba Azure Maps en el cuadro Servicios de búsqueda y Marketplace .

	3.Seleccione Azure Maps en la lista desplegable que aparece y luego seleccione el botón Crear .

	4.En la página de recursos Crear una cuenta de Azure Maps , ingrese los siguientes valores y luego seleccione el botón Crear :

		A.La suscripción que desea utilizar para esta cuenta.
		B.El nombre del grupo de recursos para esta cuenta. Puede optar por Crear un grupo de recursos nuevo o 	Seleccionar un grupo de recursos existente .
		C.El nombre de su nueva cuenta de Azure Maps.
		D.El nivel de precios para esta cuenta. Seleccione Gen2 .
		E.Lea la Declaración de licencia y privacidad y luego seleccione la casilla de verificación para aceptar los 	términos.


#Obtenga la clave de suscripción para su cuenta

Una vez que la cuenta de Azure Maps se haya creado correctamente, recupere la clave de suscripción que le permite consultar las API de Maps.

	1.Abra su cuenta de Maps en el portal.

	2.En la sección de configuración, seleccione Autenticación .

	3.Copie la clave principal y guárdela localmente para usarla más adelante en este tutorial.


#Descarguar y actualizar la demostración de Azure Maps

1.Se copia el contenido del archivo: Interactive Search Quickstart.html .
2.Se guarda el contenido de este archivo localmente como AzureMapDemo.html . Ábrelo en un editor de texto.
3.Se agrega el valor de la clave principal que obtuvo en la sección anterior
  	A.Comente todo el código de la authOptionsfunción; este código se utiliza para la autenticación de Azure Active 
  	Directory.
	B.Descomente las dos últimas líneas de la authOptionsfunción; este código se utiliza para la autenticación de 	clave compartida, método que se utiliza en este 	inicio rápido.
	C.Reemplácela <Your Azure Maps Key>con el valor de la clave de suscripción de la sección anterior.

#Se debe abrir la aplicación de demostración

1.Se abre el archivo AzureMapDemo.html en el navegador de su elección.

2.Se puede notar el mapa de la ciudad de Los Ángeles. Acerque y aleja el zoom para ver cómo el mapa se representa automáticamente con más o menos información dependiendo del nivel de zoom.

3.Cambie el centro predeterminado del mapa. En el archivo AzureMapDemo.html , busque la variable denominada centro . Reemplace el valor del par de longitud y latitud para esta variable con los nuevos valores [-74.0060, 40.7128] . Guarde el archivo y actualice su navegador.

4.Pruebe la experiencia de búsqueda interactiva. En el cuadro de búsqueda en la esquina superior izquierda de la aplicación web de demostración, busque restaurantes .

5.Mueva el mouse sobre la lista de direcciones y ubicaciones que aparecen debajo del cuadro de búsqueda. Observe cómo el pin correspondiente en el mapa muestra información sobre esa ubicación. Para garantizar la privacidad de las empresas privadas, se muestran nombres y direcciones ficticios.

#Poner varias ubicaciones como predeterminado 

Las ubicaciones que se mostraran son las sientes:
		Universidad Tecnológica de Puebla.
		Catedral de la Cd. de Puebla.
		Fuerte de Loreto.
		Fuente de los Frailes.

1.Primero se declara la funcion addDefaultMarkers en donde se almacenan todas las ubicaciones y se manda a llamar la funcion marker:

 function addDefaultMarkers() {
    var locations = [
        { coordinates: [ -98.1516198071536, 19.05847425], name: "Location 1" },
        { coordinates: [  -98.1983963875387, 19.04281015], name: "Location 2" },
        { coordinates: [-98.1870100851584, 19.0577841], name: "Location 3" },
        { coordinates: [-98.2226237, 19.0537911], name: "Location 4" }
        // Add more locations as needed
    ];

    locations.forEach(function (location) {
        var marker = new atlas.Shape(new atlas.data.Point(location.coordinates));
        marker.addProperty('name', location.name);
        datasource.add([marker]);
    });
}


2.Despues se manda a llamar la funcion addDefaultMarkers dentro de la funcion GetMap: 

addDefaultMarkers();

3. Dentro de la variable map se pondra en el center las coordenadas de la Universidad Tecnologica de Puebla como punto de partida cundo el HTML se ejecute:

center: [-98.1516198071536, 19.05847425],

[![Evidencia-geolocalizacion.png](https://i.postimg.cc/ZY8nJBPs/Evidencia-geolocalizacion.png)](https://postimg.cc/14zsHzjD)



