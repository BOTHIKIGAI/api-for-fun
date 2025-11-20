# Configuración de pre commit

## ¿Que es?

Pre-commit es una herramienta diseñada para gestionar y mantener hooks de pre-commit en proyectos que utilizan Git. Estos hooks son scripts que se ejecutan automáticamente antes de realizar un commit, asegurando que el código cumpla con ciertos estándares o reglas predefinidas, como formateo, linting o corrección de errores comunes.

## Pasos para configurar

1. Asegurar la instalación de pre commit en nuestro entorno virtual

```terminal
uv add pre-commit
```

2. Si no existe, agregar el archivo de configuración `.pre-commit-config.ymal` en la **raiz del proyecto**
3. Investigar algun hook en la web para python y agregarlo al archivo de configuración

La actual configuración del proyecto es la siguiente

```ymal
default_install_hook_types:
  - pre-commit
  - commit-msg

repos:
  - repo: https://github.com/astral-sh/ruff-pre-commit
    rev: v0.14.4
    hooks:
      - id: ruff-check
      - id: ruff-format

  - repo: https://github.com/compilerla/conventional-pre-commit
    rev: v4.3.0
    hooks:
      - id: conventional-pre-commit
        stages: [commit-msg]
        args: []
```

## Hooks implementados

### RUFF

El hook de RUFF es un elemento que asegura que no tenga problemas de linting el archivo y lo formatea para que siga las reglas que hemos definido en el [archivo de configuración](../ruff.toml)

### Conventional pre commit

El hook de conventional pre commit asegura el nombramiento del commit siga las practicas adecuadas definidas por [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#specification). Si necesitas mas información sobre como realizar commits y las reglas puedes consulart el siguiente [enlace](https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13)
