<center>

# UT4-A1 Digrama de clases para una plataforma de cursos online


</center>

***Nombre: Alejandro Donate García***

***Curso: 1º DAM*** 

### ÍNDICE

+ [Enunciado](#id1)
+ [Objetivos](#id2)
+ [Tabla de clases, relaciones y cardinalidades](#id3)



#### ***Enunciado***. <a name="id1"></a>

Una plataforma de formación online necesita un sistema que permita gestionar cursos, usuarios y el proceso de matriculación y evaluación. Realizar un diagrama de clases UML que permita modelar el sistema atendiendo a las siguientes premisas:

La plataforma gestiona usuarios registrados, de los cuales se almacenan un identificador, nombre y correo electrónico, y que pueden iniciar y cerrar sesión en el sistema. Existen dos tipos de usuarios: alumnos y profesores. Los alumnos, además de los datos comunes, disponen de un número de expediente y pueden matricularse en cursos ofrecidos por la plataforma, así como consultar las calificaciones obtenidas. Los profesores, identificados también como usuarios, cuentan con una especialidad y son los responsables de crear cursos y de evaluar a los alumnos en las distintas actividades.

Los cursos ofrecidos por la plataforma se identifican mediante un código, un título y una descripción, y pueden publicarse o cerrarse. Cada curso se estructura internamente en módulos formativos, que representan bloques temáticos ordenados dentro del curso. De cada módulo se almacena su nombre y el orden que ocupa dentro del curso, y permite acceder a los contenidos que lo forman. Un curso debe estar estructurado en módulos para poder impartirse.

Dentro de cada módulo se proponen actividades evaluables, de las que se registra un título y una fecha límite de entrega. Los alumnos pueden entregar una actividad dentro del plazo establecido. Las actividades son utilizadas para evaluar el progreso del alumnado, pero su definición no depende necesariamente de un único módulo concreto.

Como resultado de la evaluación de una actividad, se generan calificaciones, en las que se almacena la nota obtenida y un comentario asociado. Las calificaciones permiten determinar si una actividad ha sido superada o no. Un alumno puede obtener varias calificaciones a lo largo de su formación, y una misma actividad puede dar lugar a varias calificaciones correspondientes a distintos alumnos.

Un alumno puede estar matriculado simultáneamente en varios cursos y un mismo curso puede contar con varios alumnos matriculados. No es obligatorio que todos los alumnos estén matriculados en algún curso en un momento determinado, ni que un curso tenga alumnos mientras no esté publicado.

Los profesores utilizan las calificaciones exclusivamente en el momento de evaluar a los alumnos, sin que exista una relación permanente de almacenamiento entre profesores y calificaciones.

A partir de estas premisas, se deberá identificar correctamente las clases implicadas, sus atributos y métodos, así como deducir el tipo de relación existente entre ellas y las cardinalidades correspondientes, utilizando notación UML estándar.

#### ***Tabla de clases, relaciones y cardinalidades***. <a name="id2"></a>

En la siguiente tabla debes especificar cada clase, la relación existente entre clases, justificación de la relación, cardinalidad y justificación de la cardinalidad


|    Clase origen     |    Clase destino    |                      Tipo de relación                       |                                                             Argumento del tipo de relación                                                              | Cardinalidad |                                           Argumento de la cardinalidad                                           |
|:-------------------:|:-------------------:|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|:------------:|:----------------------------------------------------------------------------------------------------------------:|
|        User         |       Student       |         Recibe la conección de Herencia de Student.         |                                                 Conecta con Student al recibir su relación de Herencia.                                                 |    1 - n     |                                     User puede almacenar muchos estudiantes.                                     |
|        User         |       Teacher       |         Recibe la conección de Herencia de Teacher.         |                                                 Conecta con Teacher al recibir su relación de Herencia.                                                 |    1 - n     |                                     User pueder almacenar muchos profesores.                                     |
|       Student       |        User         |              Relación de Herencia hacia User.               |                                                 La clase Student hereda los atributos de la clase User.                                                  |    n - 1     |                                  Un estudiante solo pueder tener un id de User.                                  |
|       Student       |       Course        |            Relación de Agregación hacia Course.            |                                         La clase Student tiene componentes que forman parte de la clase Course.                                          | 1..n - 1..n  |                          1 o muchos estudiantes pueden pertenecer a 1 o muchos cursos.                           |
|       Teacher       |        User         |              Relación de Herencia hacia User.               |                                                 La clase Teacher hereda los atributos de la clase User.                                                  |    n - 1     |                                   Un profesor solo puede tener un id de User.                                    |
|       Teacher       |       Grades        |            Relación de Asociación hacia Grades.            |                                                    La clase Teacher usa los datos de la clase Grades.                                                    |   1 - 1..n   |                                   Un profesor puede manejar 1 o muchas notas.                                    |
|       Course        |       Student       |       Recibe la conección de Agregación de Student.        |                                              Conecta con Student por la relación anteriormente mencionada.                                              | 1..n - 1..n  |                    Al igual que antes, 1 o muchos cursos pueden tener 1 o muchos estudiantes.                    |
|       Course        |       Module        |         Recibe la conección de Composición Module.         |                                                     Conecta con Module de igual manera que Student.                                                      |    1 - n     |                                 1 curso puede estar formado por muchos modulos.                                  |
|       Module        |       Course        |           Relación de Composición hacia Course.            |                                             La clase Module no podria existir si la clase Course no existe.                                              |    n - 1     |                        muchos módulos solo pueden formar parte de 1 curso en especifico.                        |
|       Module        | Gradable Activities | Recibe la conección de Composición de Gradable Activities. |                                         Conecta con Gradable Activities de igual manera que de Course a Module.                                          |   1 - 0..n   |                     1 módulo puede tener dentro de el de 0 a muchas actividades evaluables.                     |
| Gradable Activities |       Module        |           Relación de Composición hacia Module.            |                                       La clase Gradable Activities no podria existir si la clase Module no existe.                                       |   0..n - 1   |               0 o muchas actividades evaluables pueden formar parte unicamente de un solo módulo.               |
| Gradable Activities |       Grades        |       Recibe la conección de Composición de Grades.        |                                           Conecta con Grades de igual manera que Module a Gradable Activities.                                           |    1 - n     | 1 actividad evaluable puede tener muchas notas pero dichas notas solo pueden pertenecer a 1 actividad evaluable. |
|       Grades        | Gradable Activities |      Relación de Composición de Gradable Activities.       |                                            La clase Grades no podria existir si la clase Gradable Activities.                                            |    n - 1     |   1 nota solo puede pertenecer a 1 actividad evaluable concreta pero dicha actividad puede tener muchas notas.   |
|       Grades        |       Teacher       |           Relación de Asociación hacia Teacher.            | La clase Grades permite a la clase Teacher usar sus datos. No requiriendo la existencia de la otra para funcionar ni agregando ningun detalle a la otra. |   1..n - 1   |                            1 o muchas notas pueden ser manejadas por 1 solo profesor.                            |
|       Grades        |       Student       |            Relación de Asociación con Student.             |                           Ambas categorias pueden existir independientemente pero se puede conectar la información de ambas.                            |    n - 1     |          1 estudiante puede tener muchas notas, pero las notas solo pueden pertenecer a 1 solo usuario.          |
|       Student       |       Grades        |             Relación de Asociación con Grades.             |                           Ambas categorias pueden existir independientemente pero se puede conectar la información de ambas.                            |    1 - n     |          1 estudiante puede tener muchas notas, pero las notas solo pueden pertenecer a 1 solo usuario.          |

> ***PISTA IMPORTANTE:*** El número de filas de la tabla se corresponde exactamente con el número de relaciones entre las clases.

#### ***Diagrama de clases***. <a name="id3"></a>

A continuación se muestra el diagrama de clases: 

<img src="/home/dam/Documentos/Entornos_de_desarrollo/etsdam_alejandro/ut4/a1/img/PlataformaFormativa.png">








> ***NOTA*** La imagen debe ser clara y estar correctamente insertada.
