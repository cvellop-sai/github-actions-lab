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
