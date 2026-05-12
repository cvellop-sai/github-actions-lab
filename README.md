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

Habría que modificar el código para que pase los tests, o eliminar los tests que fallan.
