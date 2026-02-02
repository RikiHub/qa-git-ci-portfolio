## QA Check – GitHub Actions

### Objetivo
Validar que el repositorio ejecute un workflow automático en cada push a `main`.

### Incidencia detectada
El workflow no se ejecutaba tras realizar push a la rama `main`.

### Análisis
Se detectó que el archivo `.github/workflows/qa-check.yml` no contenía
un trigger definido en la sección `on:`.

### Causa raíz
Faltaba el evento `push` apuntando a la rama `main`, por lo que GitHub
Actions no tenía condición para ejecutar el workflow.

### Solución aplicada
Se añadió el siguiente bloque al workflow:

```yaml
on:
  push:
    branches:
      - main
