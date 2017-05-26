
# Que conduces  cuantas ganas :  Una medición de desigualdad para Colombia 

Descripción y Motivación
Datos publicados por el banco mundial sugieren que a 2014 Colombia es el país más desigual de América (ver tabla 1 ).  No solo es preocupante la distancia en equidad respecto a otros países , es preocupante la persistencia de la desigualdad en Colombia  y las consecuencias que trae  esto para un país  en desarrollo.   Siendo la desigualdad un  fenómeno de vital importancia para el futuro y desarrollo del país es importante idear diversas medidas de este fenómeno para el análisis y para el diseño de política. En este trabajo se plantea una medición de desigualdad para Colombia, basada en el trabajo de Kholodilin et al. ( 2012) los cuales crean una medición de desigualdad para Alemania. 

	Gini 2014 
Colombia	53.5
Paraguay	51.67
Brasil	51.48
Panamá	50.7
Honduras	50.64
Chile	50.45
Guatemala	48.66
Costa Rica	48.53
Bolivia	48.4
México	48.21
Dominicana Republica	47.07
Ecuador	45.38
Perú	44.14
Argentina	42.67
El Salvador	41.84
Uruguay	41.6
Fuente : Banco Mundial 

Algunas de las principales motivaciones del trabajo son : 
•	Los métodos de recolección de datos tradicionales ( ej .  encuestas de hogares )  son costosos 
•	Las encuestas de hogares tienen serios problemas de under reporting cuando se pregunta el ingreso. 
•	La periodicidad de estas medidas es  larga debido a la dificultad de recolectar los datos por diversos sitios del territorio colombiano 
•	No existe una medida de desigualdad para la clase media en Colombia 
•	Se pueden dar mejores indicadores de desigualdad a nivel de ciudad 
•	Los carros como bien durable y como señal de estatus social de su dueño son un buen proxy de riqueza , por lo cual tener información de venta de precios de carro en diferentes lugares de Colombia es una forma indirecta de medir el ingreso de los colombianos , y de esta forma construir indicadores de desigualdad. 

Métodos Usados : 
1.	Scrapping : 
-	Los precios de carros usados y nuevos para distintas ciudades se encuentran en la página de internet http://www.tucarro.com.co/ . 
-	Para moverse a través de la página se usó “ Selenium”  , y para  capturar los datos de cada carro se usó “ Beautifol Soup”  ,  muy resumidamente el  programa iniciaba desde el menú de todos los carros y automóviles de la página se metía uno por uno sacaba la información , y el acabar los carros de una página cambiaba a la siguiente.  El código está disponible en el repositorio 
-	Para cada carro se obtuvo : Precio, Kilometraje, Ciudad de venta, Color, Marca, Modelo, Año, Airbag,  Asientos, Frenos, Tracción, Sonido, Combustible, Cilindraje, y otros. 


2.	Almacenamiento de los datos :  

-	Los datos de cada página se guardaban en un diccionario , aproximadamente eran 48 carros por página  luego de almacenar los datos de cada carro en un diccionario , estos se pasaban a pandas y posteriormente  cada 10 páginas se creaba una copia de estos datos a Excel.  
3.	Procesamiento de los datos : 
-	Una vez obtenida la base de datos  todos los cálculos propios y limpieza de la base se hicieron en Stata  para obtener los coeficientes de Gini ,  y una vez obtenidos estos  los mapas se hicieron en QGIS. 





Resultados : 

![alt text](https://github.com/juanpbaquero/Trabajo-Final-/blob/master/mapaginnicarros.jpg)


 
Figura 1: Precio promedio de carros en Colombia 

En la Figura 1 observamos el precio promedio de carros por región .  Se observa mayores precios promedio en el departamento de Tolima y  en el departamento de Santander , se observa el menor precio promedio en  Boyacá y Caldas.  En la Figura 2 se muestra el análisis de desigualdad basado en los precios de los carros , se observa  mayor desigualdad en el departamento del Tolima Cundinamarca ( Bogotá D.C) ,  Antioquia Bolívar y Atlántico  y una menor desigualdad en Huila Valle del Cauca y Caldas.  
En la Figura 3 se observa el mapa del índice de Gini medido por encuestas de hogares por United Nations ,  se observa que tiene mayor cobertura a nivel del territorio nacional lo cual es una gran ventaja de los métodos tradicionales y un pitfall del método usado acá .  Respecto a la medición,  ambos mapas no son comparables dado que la medida contemplada acá es una medida de desigualdad de la clase media hacia arriba .  







 
Figura 2: Mapa índice de Gini  medido por precios de carros

 i 


Figura 3: Mapa índice de Gini capturado por medio de encuestas de hogares 



Bibliografía
 
Kholodilin, K. A., & Siliverstovs, B. (2012). Measuring regional inequality by internet car price advertisements: Evidence for Germany. Economics Letters, 116(3), 414-417.
