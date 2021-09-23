# Prueba_API_0.1
 Probando creacion de API con postman de cliente y sin interfaz
 para ejecutar contar con postaman instalado o algun otro servicio de cliente. este programa cuenta con metodos POST GET PUT Y DELETE.
 Para inicializar el servidor a nivel local es necesario contar con python +3.x , se debe de abrir una terminal en la carpeta descargada y ejecutar los siguientes comandos

 env/Scripts/activation
 app.py

 se inicializara el servidor y para interactuar con el mismo abrimos la aplicacion postman en el cual creamos un nuevo http request. vamos a crear 5 ventanas para probar lo configurado.
 1-. 
    POST : http://127.0.0.1:5000/tasks 
    Headers: Content-Type
    Value : application/json
    Body (raw):   
                {
                "title" : "Second Task"
                }
presionar send y enviara titulo id fecha de creacion y confirmacion de si se encuentra completo el listado de tareas
 
 2-.
    GET : http://127.0.0.1:5000/tasks 
presionar send y mostrara todas las tareas

3-.
    PUT : http://127.0.0.1:5000/tasks?id=2  //Aqui seteamos los parametros con la url, en este caso el id
    Body (raw):
                {
                    "title"  : "Title 2 Updated"
                }
Send y modificara el titulo del ID 2

4-.
    DELETE : http://127.0.0.1:5000/tasks?id=2  //Aqui seteamos los parametros con la url, en este caso el id
Send y se borrara la tarea

5-.
    PUT : http://127.0.0.1:5000/tasks/completed?id=1&completed=1    // modificamos url ya que no podemos repetir requests con la misma url,definimos los parametros a modificar desde la url.
Send y se dara la tarea completa con su respectivo id
