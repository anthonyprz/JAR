
La particularidad de los ficheros .jar es que no necesitan ser descomprimidos para ser usados,
 es decir que el intérprete de Java es capaz de ejecutar los archivos comprimidos en un archivo jar directamente. 
Por ejemplo, si hemos recopilado todos los ficheros necesarios para ejecutar una aplicación en un fichero "aplic.jar",
 podemos lanzar la aplicación desde una terminal de texto mediante:
java -jar aplic.jar


Crear un directorio META-INF (¡las mayúsculas son importantes!) y dentro un fichero MANIFEST.MF. 
Este fichero indica, entre otras cosas, cual será la clase principal. A menudo el fichero MANIFEST.MF contiene una única línea:

    > Main-Class: Principal

indicando que Principal.class es la clase que contiene el método main.

Crear el fichero .jar mediante el comando

  >  jar cfm fich.jar META-INF/MANIFEST.MF *.class
    
El nombre fich.jar es el que nosotros queramos y corresponde al fichero .jar que se creará conteniendo todos los ficheros indicados 
(en este caso todos los ficheros .class). 

* Se puede comprobar que el contenido del fichero es el el adecuado escribiendo:

   > jar tf fich.jar 
    
que mostrará la lista de clases contenidas en el fichero. Este comando también puede ser útil para examinar el contenido 
de las librerías del sistema.

* Para lanzar el archivo basta con teclear ahora:


  >  java -jar fich.jar 
    
* Si alguna vez se quiere "desempaquetar" el contenido de un archivo jar se pueden usar las opciones "xf":


   > jar fich.jar 
    
Esto puede resultar particularmente útil si queremos echar un vistazo a algunos paquetes del sistema que vienen de esta forma. 

ventajas 

	 Los JARs son ejecutables
	 Los JARs contienen más que sólo código
	 Los JARs pueden ser referenciados implícitamente
	

 	Seguridad: se puede firmar digitalmente el contenido del fichero JAR
	Tiempo de descarga bajo: al descargarse todos los recursos necesarios de una aplicación
	Compresión: JAR comprime los ficheros
	Portabilidad: los ficheros JAR son un estándar del API
	Los ficheros JAR se empaquetan con el formato ZIP y Se utiliza el comando jar
	Empaquetado para extensiones, sellado y versionado
