# Contribuciones de Luis Alanya

## Sprint 1

- 2025-06-08: Creé la estructura inicial del proyecto (carpetas y archivos vacíos), además del `.gitignore`.  
  
  Commit:
  -	`feat(structure): (Issue #1) crear estructura inicial de carpetas y archivos vacíos`

  Pull request grupal: [#8](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/8)

- 2025-06-09: Se crea la carpeta `hooks/` con los hooks que vamos a usar (`pre-commit`, `commit-msg` y `pre-push`). También se crea un scrip `setup.sh` para la generación del entorno de trabajo  
  
  Commit:
  -	`feat(git-hooks): (Issue #2) añadir pre-commit, commit-msg y pre-push en hooks/` (`5d6e444`)
  -	`feat(sh): (Issue #2) crear archivo setup.sh para generar entorno de trabajo` (`77133d1`)
  -	`docs(readme): (Issue #2) actualizar README con guía de setup.sh y explicación de hooks` (`47fd530`)

  Pull request grupal: [#9](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/9)

- 2025-06-10: Se modifica el hooks `pre-commit` como también el `setup.sh` para evitar salir del entorno virtual en caso de error (`exit 1`).
  
  Commit:
  -	`feat(hooks): (Issue #2) modificar hook pre-commit para que valide la rama de trabajo` (`ea901d7`)
  -	`fix(sh): (Issue #2) modificar setup.sh para evitar que se cierre el entorno al activarse` (`9ab79cf`)
  -	`docs(readme): (Issue #2) actualizar README para describir la nueva función del hook pre-commit` (`81bf0f3`)

  Pull request grupal: [#9](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/9)

- 2025-06-10: Se integran linters y scripts de validación, actualizando configuración y documentación del proyecto.

  Commits:
  - `ci(config): (Issue #4) agregar configuraciones de flake8, tflint y requirements para linting` (`6eca34f`)
  - `chore(sh): (Issue #4) añadir cabecera hashbang en scripts para cumplir lint` (`20376e9`)
  - `chore(sh): (Issue #4) añadir comentario shellcheck para evitar warning al activar el entorno en setup.sh` (`d1817eb`)
  - `feat(hooks): (Issue #4) agregar linters flake8, shellcheck, tflint, etc en pre-commit y pre-push` (`5e888b8`)
  - `feat(sh): (Issue #4) agregar scripts lint_all y validate_adapter para lint y validación` (`b46ff2d`)
  - `feat(config): (Issue #4) Agregar pytest-cov a requirements.txt` (`c9a339d`)
  - `docs(readme): (Issue #4) agregar documentación de los scripts creados y actualizar información de pre-commit y pre-push` (`f3948df`)
  - `fix(config): (Issue #4) Modificar .tflint.hcl para que esté con sintaxis moderna` (`b17b91e`)
  - `feat(tf): (Issue #4) Modificar adapter/main.tf para que esté correctamente formateado` (`f3126d3`)
  - `fix(hooks): (Issue #4) Modificar hooks para el correcto funcionamiento de la configuración .tflint.hcl` (`d4616c0`)

  Pull request grupal: [#12](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/12)

## Sprint 2

- 2025-06-13: Se implementa la fachada funcional y su orquestación, junto con documentación y ajustes de linting y cobertura.

  Commits:
  - `feat(sh): (Issue #18) crear scripts para facade: crear carpeta, archivo y lanzar servicio` (`5fa0305`)
  - `feat(py): (Issue #18) crear servicio dummy en python para módulo facade` (`8e7fe9c`)
  - `feat(tf): (Issue #18) crear orquestación y variables en terraform para módulo facade` (`64f7884`)
  - `docs(readme): (Issue #18) agregar documentación sobre los archivos sh, tf y py de facade` (`3d8347d`)
  - `fix(py): (Issue #18) arreglar archivos python para pasar prueba de flake8` (`05382b2`)
  - `feat(config): (Issue #18) agregar archivo de configuración coverage para omitir prueba en service_dummy.py` (`ac028ec`)
  - `fix(files): (Issue #18) añadir pequeños cambios a variables.tf y run_all.sh para pasar pruebas linting` (`e905c45`)

  Pull request grupal: [#28](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/)

- 2025-06-14: Se implementa integración de recursos, scripts y documentación para el módulo mediator.

  Commits:
  - `feat(tf): (Issue #26) agregar recursos nulos en main.tf de mediator para ejecución de scripts` (`5f62922`)
  - `feat(sh): (Issue #26) agregar scripts bash para la lectura y copia de archivo .txt generado por cliente_a` (`61c224a`)
  - `docs(readme): (Issue #26) agregar documentación sobre cambios agregados en los arhivos .tf y .sh en el módulo mediator` (`5c3834f`)
  - `docs(readme): (Issue #26) agregar explicación de ejecución para el módulo mediator` (`4e3a30f`)

  Pull request grupal: [#30](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/30)

## Sprint 3

- 2025-06-18: Se implementa integración de health check y automatización de despliegue para el módulo facade.

  Commits:
  - `feat(sh): (Issue #37) crear script health_check.sh para validar el servicio dummy` (`ae2b415`)
  - `feat(tf): (Issue #37) condicionar el despliegue a adapter_status y agregar variable` (`23076c7`)
  - `feat(sh): (Issue #37) automatizar apply de facade con variables generadas por adapter` (`dbcedc1`)
  - `docs(readme): (Issue #37) documentar integración adapter-facade con modificación de run_all.sh` (`5c5d721`)

  Pull request grupal: [#44](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/44)

- 2025-06-19: Se implementa validación, logging y mejoras en la integración de scripts y outputs para el módulo mediator.

  Commits:
  - `feat(sh): (Issue #39) agregar validaciones y guardar message_a.txt en facade/facade_dir` (`85d06c5`)
  - `feat(sh): (Issue #39) añadir funcionalidad de copiar message_b.txt generado por mediator` (`59c7424`)
  - `feat(tf): (Issue #39) agregar output de ruta de archivos generados para el uso de mediator` (`a36bcf7`)
  - `feat(tf): (Issue #39) usar outputs de facade y secuenciar recursos` (`81deaed`)
  - `feat(sh): (Issue #39) leer message_a.txt desde facade_dir y extraer solamente el mensaje` (`6180b7e`)
  - `feat(sh): (Issue #39) reenviar solo mensaje plano a message_b.txt dentro de mediator` (`1fbe723`)
  - `docs(readme): (Issue #39) agregar documentación de los cambios realizados en el issue` (`e033363`)

  Pull request grupal: [#47](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/47)
