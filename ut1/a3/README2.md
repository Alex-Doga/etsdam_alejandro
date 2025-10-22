
<center>

# TÍTULO DE LA PRÁCTICA


</center>

***Nombre: Alejandro Donate García***
***Curso: 1ªDAM*** 

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


#### ***Introducción***. <a name="id1"></a>

Trabajo de ETS por Alejandro Donate García para la práctica con repositorios. 

#### ***Objetivos***. <a name="id2"></a>

La práctica consitirá en ir utilizando una serie de comandos en git para modificar y agragar informacion a un repositorio de la asignatura. 

#### ***Material empleado***. <a name="id3"></a>

Para esta práctica se han utilizado tanto máquinas virtuales como el propio ordenador de clase/casa. Usamos GitHub y las terminales de ambas, la máquina virtual y el pc. 

#### ***Desarrollo***. <a name="id4"></a>

1. Lo primero que tenemos que hacer es irnos a GitHub y realiza una clonacion del repositorio que usaremos en la práctica. Tendremos que coger la clave ssh y usar el comando `git clone "ssh del repositorio"` para traernoslo al pc de manera remota. 
___
2. Seguidamente lo que nos pide la práctica es crear un README.md dentro del repositorio y posteriormente tendremos que realizar el primer `git commit -m` de la prácica. El mensaje que tenemos que poner dentro del commit es "Mensaje inicial". Por último en este paso tendremos que hacer un `git push origin main` para llevar los cambios desde nuestro repositorio remoto al original en GitHub.
___
3. Ahora volviendo a nuestro repositorio remoto, tenemos que añadir un fichero de texto así `touch private.txt`. Esto nos agregara un fichero de texto plano llamado "privado.txt". Despues tendremos que crear una carpeta con el mismo nombre pero en español, `mkdir privado`. Ahora lo que nos pide la práctica es que le pidamos a GitHub que no nos reconozca estos dos últimos archivos creados. Sería con el codigo `echo "private.txt" >> .gitignore` y `echo "/privado" >> .gitignore`. Hacemos un `git add .` y un `git commit -m "Añadido ficheros .gitignore"`.
___
4. Posteriormente lo que haremos será es crear un fichero de texto plano "1.txt" con `touch 1.txt`. Lo añadiremos y haremos commit. 
___
5. Creamos un tag `tag v0.1`. y luego haremos `git push --tag origin main` para enviar el tag al repositorio original en GitHub. 
___
6. Ahora crearemos una nueva rama para trabajar con un nuevo archivo. `git branch v0.2` y dentro con un `git switch v0.2` crearemos un archivo 2.txt con `touch 2.txt`. Lo añadimos y hacemos commit. Luego enviamos los cambios al repositorio original en GitHub. Seguidamente usaremos `git merge v0.2 -m "merge v0.2 sin conflictos"` para unir la rama v0.2 con la rama main. 
___
7. En la rama original modificaremos el archivo "1.txt" para añadirle la linea de texto "Hola" dentro. Hacemos add y commit. Luego hacemos `git swtich v0.2` y nos cambiamos a la rama v0.2 para hacer lo mismo en el archivo "1.txt" solo que añadiendo "Adios". Hacemos add y commit. 
___
8. Ahora volviendo a la rama main, haremos un merge con v0.2 pero nos dará error. Ahí usaremos `vim 1.txt` para arreglar el merge. Volvemos a hacer add y commit. 
___
9. Por último añadiremos un tag a la rama v0.2 con `git tag v0.2` y eliminaremos la rama con `git branch -d v0.2`. Haremos un commit final para guardar todos los cambios realizados en este último paso.

#### ***Conclusiones***. <a name="id5"></a>

Sacamos como conclusión el uso de los comando de git, que sirven para ir cogiendo soltura en el desarrollo y trabajo con repositorios remotos. 
