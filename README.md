## Objetivo
explorar las diferentes formas en que podemos utilizar event-filters y activity types  para especificar mejor cuándo se ejecutan los workflows de GitHub Actions.


## Tareas


1. Crear un archivo llamado `05-efilters.yaml` en la carpeta `.github/workflows` en la raíz del repositorio.. Los datos del workflow deben ser los siguientes:
    - nombre: 05 - Event Filters.
    - desencadentes:
      - push, usar filtros de eventos para restringir las ejecuciones de este workflow para que se activen **solo** mediante cambios en la rama `features`.
    - Trabajos:
        - `echo`, que tiene un solo step, que simplemente imprime el siguiente mensaje en la pantalla: `'Running whenever branch is features'`.
2. Confirmar los cambios sobre la rama principal (main) y subir (push) el código. Inspeccionar el resultado de la ejecución del workflow. :stuck_out_tongue:
3. Edite el archivo README.md (con cualquier texto) en la raíz del repositorio con los cambios que considere oportunos y confirme los cambios en una nueva rama `features`.
4. Confirmar los cambios y subir (push) el código. Inspeccionar el resultado de la ejecución del workflow.
5. Acceder a la rama principal de nuevo, y Crear un archivo llamado `06-atypes.yaml` en la carpeta `.github/workflows` en la raíz del repositorio.. Los datos del workflow deben ser los siguientes:
    - nombre: 06 - Activity Types.    
    - desencadentes: 
      - pull_request, únicamente con los activity types `opened` y `synchronize` para restringir el arranque del flujo solo para abrir y sincronizar PR's. Además, añadir un filtro para que solo aplique cuando la rama base sea `develop`
    - Trabajos:
        - `echo`, que tiene un solo step, que simplemente imprime el siguiente mensaje en la pantalla: `'Running whenever a PR is opened or synchronized AND base branch is develop'`.
6. Confirmar los cambios y subir (push) el código en la rama main. Inspeccionar el resultado de la ejecución del workflow.
7. Crear una rama `develop` a partir de main en el portal UI,  sincronizar el repositoiro en local,y crear una rama `feat-1-act-Types` a partir de develop.
8. Edite el archivo README.md en la raíz del repositorio con los cambios que considere oportunos y confirme los cambios en una la rama creada anteriormente
9. Confirmar los cambios y subir (push) el código. 
10. Crear un PR para fusionar la rama `feat-1-act-Types` en `develop`. Inspeccionar el resultado de la ejecución del workflow.
11. Edite de nuevo el archivo README.md en la rama `feat-1-act-Types`, confirme los cambios y suba (push) el código.  Inspeccionar el resultado de la ejecución del workflow.
