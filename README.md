# github-actions-lab

## 1. Workflow CI para el proyecto de frontend
### Archivo de workflow
1. Evento disparador del workflow al hacer PR y requisito de modificaciones en carpeta hangman-front.

![Evento y control sobre hangman-front](capturas/ci-01.png)

2. Job Build para compilar el proyecto en el entorno seleccionado ubuntu con node versión 20.

![Job Build](capturas/ci-02.png)

3. Ejecución de tests comprobar el correcto funcionamiento.

![Job Build](capturas/ci-03.png)

### Modificación
Se ha modificado el archivo hangman-front/src/index.html. Se cambia el título de la página web.

![Modificación index.html](capturas/ci-04.png)

## Ejecución de PR
Al hacer push del archivo index.html y ejecutar el pull request, el build finaliza correctamente y falla en los test.

![Ejecución de PR](capturas/ci-05.png)

Habría que modificar el código para que pase los tests, en este caso modificando el 1 por 2 en el argumento de .toHaveLength.

Una vez modificado ya pasa los tests.

![Ejecución de PR resuelto](capturas/ci-06.png)

![Ejecución de PR detalle](capturas/ci-07.png)


## 2. Workflow CD para el proyecto de frontend
### Archivo de workflow

1. Evento disparador del workflow: manual (workflow_dispatch).

![CD disparador](capturas/cd-01.png)

2. Tareas para el envío: checkout del proyecto, docker login y build and push.

![CD jobs](capturas/cd-02.png)

### Configuración de DOCKER_USER y DOCKER_SECRET

1. Variable DOCKER_USER

![Variable DOCKER_USER](capturas/cd-03.png)

2. Secret DOCKER_SECRET

![Secret DOCKER_SECRET](capturas/cd-04.png)


### Ejecución

1. Workflow

![workflow](capturas/cd-05.png)

![workflow detalle](capturas/cd-06.png)

2. Publicación en DockerHub

![imagen en DockerHub](capturas/cd-07.png)






   
