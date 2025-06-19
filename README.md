# Proyecto 4: "Gestión de dependencias en IaC con patrones Facade, Adapter y Mediator"

**Alumno:** Alanya Campos, Luis Alberto

**Código:** 20210290J

**Correo:** luis.alanya.c@uni.pe

**Repositorio del Proyecto:** https://github.com/Jharvichu/PC3_Grupo8_Proyecto4

### Rol en el equipo

Para este proyecto, me encargué de la creación de algunas *issues* para cada *sprint*, como también de la elaboración de guías informativas para la buena elaboración de ramas y *commits*. Contribuí al desarrollo de algunos módulos (como `mediator` y `facade`). Implementé también los tres *hooks* que usamos durante el proyecto (`pre-commit`, `msg-commit` y `pre-push`) como también el *script* `setup.sh` que crea el entorno de trabajo.

### Instrucciones

```bash
$ git clone https://github.com/AlbeCamp21/mi_proyecto_individual.git
$ cd mi_proyecto_individual
# Entrando al entorno de trabajo
$ source setup.sh
# Probar hooks (pre-commit y pre-push)
$ ./.git/hooks/pre-commit
$ ./.git/hooks/pre-push 
# Probar módulo Facade
$ cd facade/
$ terraform init
$ terraform apply -auto-approve
# Probar módulo Mediator
$ cd mediator/
$ terraform init
$ terraform apply -auto-approve
```

> Se tuvieron que modificar algunas dependencias del módulo Facade hacía el módulo Adapter, debido a que dicho módulo lo elaboró otro miembro del grupo.



