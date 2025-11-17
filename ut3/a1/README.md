<center>

# INFORME INTELLIJ IDEA


</center>

---
***Nombres: Alejandro, Diego A, Eugenio, Juan P y Johan***
***Curso: 1º DAM***
---

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)

---

#### ***Introducción***. <a name="id1"></a>

En esta practica se va a presentar un informe sobre IntelliJ IDEA.

#### ***Objetivos***. <a name="id2"></a>

El objetivo de la practica es conocer un poco mas sobre este software de entornos de desarrollo, como descargarlo y utilizarlo.

#### ***Material empleado***. <a name="id3"></a>

Para la practica se han usado tanto las terminales de varios equipos para redactar el informe como maquinas virtuales para la descarga del software. La maquina que usamos tenia una SO Linux Ubuntu con 4 GB de Memoria RAM.

#### ***Desarrollo***. <a name="id4"></a>

Para empezar podemos comenzar hablando sobre el origen brevemente. IntelliJ fue creado por la empresa JetBrains. Nacio en principio solo para Java pero hoy en día el IDE soporta una gran variedad de lenguajes de programacion.

La instalacion del programa es bastante sencilla. Los pasos que vas a ver los realizamos como mencionamos anteriormente en una maquina virtual Linux Ubuntu.
- Lo que vamos a hacer primero es ir a la pagina del software para descargarnos los archivos del programa (Captura 1ª "Descargar_IntelliJ IDEA" en la carpeta img/).
- Posteriormente lo que vamos a hacer es entrar en la terminal y movernos a la carpeta donde hemos descargado los archivos. Ahi nos meteremos una vez mas dentro de la carpeta del archivo descargado. Dentro de esta encontraremos el archivo que tendremos que instalar desde la terminal (Captura 2ª "Instalacion_IntelliJ IDEA Terminal" en la carpeta img/).
- Por ultimo lo quer tendremos que hacer es salir a la localizacion donde hayamos instalado el programa y entrar en el para empezar a trabajar con el IDE (Captura 3ª "IntelliJ_Instalado" en la carpeta img/). 

Ahora para podemos hablar de las caracteristicas que tiene este software.
+ Compilador / Interprete:
- IntelliJ no tiene un compilador de por sí integrado en el software. Este usa otros compiladores ya existentes, principalmente el compilador estándar de Java llamado “javac”. Además, no sólo se puede utilizar este sino que IntelliJ te permite usar compiladores de más lenguajes como Kotlin, Scala, Groovy, etc.
- Una de las mayores fortalezas del compilador que usa IntelliJ IDEA es su compilación incremental. Esto significa que cada vez que se realice un cambio, en vez de recompilar todo el código desde cero, IntelliJ solo compila los archivos modificados.

+ Depurador / Debugger:
- Este está completamente integrado dentro de IntelliJ IDEA. Permite la ejecución de líneas concretas de código, con puntos de interrupción de distintos tipos:
	+ Condicionales:
		- Permiten que el código se detenga si se cumple una condición booleana.
	+ Dependientes:
		- Esto depende de un primer checkpoint. Si el primero no se completa el dependiente no llegará a activarse.
	+ De excepción:
		- Permiten detener la ejecución de un programa en el punto exacto donde se genere una excepción (error).

+ Control de versiones:
- El control de versiones o VCS de intelliJ IDEA soporta la integración nativa de sistemas populares como Git o Subversion.

+ Refactorización:
- Las Herramientas de refactorización dentro de IntelliJ IDEA permiten modificar la estructura del código de forma segura y eficiente.
Podemos renombrar elementos de forma segura. Extraer métodos para simplificar el código. Eliminar código muerto o no utilizado

+ Plugins:
- IntelliJ IDEA tiene una amplia variedad de plugins que podemos utilizar. Los para mencionar algunos los podemos dividir en algunas secciones principales como:
	+ De productividad:
		- Git Toolbox. Información adicional sobre Git.
		- SonarLint. Analiza la calidad del código.
	+ De desarrollo:
		- Cucumber for Java/Gherkin. Esenciales para los proyectos que usen metodologías de Desarrollo guiado por comportamiento. 
		- .env Files support. Permite reconocer correctamente los archivos .env dentro del IDE.
	+ De temas:
		- Atom material Icons. Reemplaza los iconos del software para hacerlos más coloridos, visibles y entendibles.


> ***IMPORTANTE:*** si estamos capturando una terminal no hace falta capturar todo el escrito.

---

#### ***Conclusiones***. <a name="id5"></a>

Con este informe que hemos desarrollado podemos sacar la conclusion de que el software de desarrollo IntelliJ IDEA funciona como una herramienta potente que al ser sacada fue una completa revolucion en la industria. Puede que hoy sea superada por otros programas como VSC pero podemos decir que sigue siendo uno de los mejores softwares para el desarrollo de entornos.
