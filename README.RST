# Geolocalizacion
Azure geolocalizacion Mayra-Karlos

Este inicio rápido demuestra cómo usar Azure Maps para crear un mapa que brinde a los usuarios una experiencia de búsqueda interactiva. Lo guía a través de estos pasos básicos:

1.Cree su propia cuenta de Azure Maps.

2.Obtenga su clave de suscripción de Azure Maps para usarla en la aplicación web de demostración.

3.Descargue y abra la aplicación de mapas de demostración.


Este inicio rápido usa el SDK web de Azure Maps; sin embargo, el servicio Azure Maps se puede usar con cualquier control de mapa, como estos controles de mapas populares de código abierto para los que el equipo de Azure Maps ha creado complementos.

#Requisitos previos

Si no tiene una suscripción a Azure, cree una cuenta gratuita antes de comenzar.

Inicie sesión en el portal de Azure .


#Crear una cuenta de Azure Maps

Cree una nueva cuenta de Azure Maps con los siguientes pasos:

1.Seleccione Crear un recurso en la esquina superior izquierda de Azure Portal .

2.Escriba Azure Maps en el cuadro Servicios de búsqueda y Marketplace .

3.Seleccione Azure Maps en la lista desplegable que aparece y luego seleccione el botón Crear .

4.En la página de recursos Crear una cuenta de Azure Maps , ingrese los siguientes valores y luego seleccione el botón Crear :

	A.La suscripción que desea utilizar para esta cuenta.
	B.El nombre del grupo de recursos para esta cuenta. Puede optar por Crear un grupo de recursos nuevo o 		Seleccionar un grupo de recursos existente .
	C.El nombre de su nueva cuenta de Azure Maps.
	D.El nivel de precios para esta cuenta. Seleccione Gen2 .
	E.Lea la Declaración de licencia y privacidad y luego seleccione la casilla de verificación para aceptar los 	términos.


#Obtenga la clave de suscripción para su cuenta

Una vez que su cuenta de Azure Maps se haya creado correctamente, recupere la clave de suscripción que le permite consultar las API de Maps.

1.Abra su cuenta de Maps en el portal.

2.En la sección de configuración, seleccione Autenticación .

3.Copie la clave principal y guárdela localmente para usarla más adelante en este tutorial.


#Descargue y actualice la demostración de Azure Maps

1.Copie el contenido del archivo: Interactive Search Quickstart.html .
2.Guarde el contenido de este archivo localmente como AzureMapDemo.html . Ábrelo en un editor de texto.
3.Agregue el valor de la clave principal que obtuvo en la sección anterior
  	A.Comente todo el código de la authOptionsfunción; este código se utiliza para la autenticación de Azure Active 
  	Directory.
	B.Descomente las dos últimas líneas de la authOptionsfunción; este código se utiliza para la autenticación de 	clave compartida, método que se utiliza en este inicio rápido.
	C.Reemplácela <Your Azure Maps Key>con el valor de la clave de suscripción de la sección anterior.

#Abra la aplicación de demostración

1.Abra el archivo AzureMapDemo.html en el navegador de su elección.

2.Observe el mapa que se muestra de la ciudad de Los Ángeles. Acerca y aleja el zoom para ver cómo el mapa se representa automáticamente con más o menos información dependiendo del nivel de zoom.

3.Cambia el centro predeterminado del mapa. En el archivo AzureMapDemo.html , busque la variable denominada centro . Reemplace el valor del par de longitud y latitud para esta variable con los nuevos valores [-74.0060, 40.7128] . Guarde el archivo y actualice su navegador.

4.Pruebe la experiencia de búsqueda interactiva. En el cuadro de búsqueda en la esquina superior izquierda de la aplicación web de demostración, busque restaurantes .

5.Mueva el mouse sobre la lista de direcciones y ubicaciones que aparecen debajo del cuadro de búsqueda. Observe cómo el pin correspondiente en el mapa muestra información sobre esa ubicación. Para garantizar la privacidad de las empresas privadas, se muestran nombres y direcciones ficticios.

