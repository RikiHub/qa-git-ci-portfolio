# 🧪 Evidencia QA – Resolución de Conflictos en Pull Request

## 📌 Contexto
Esto simula un escenario real de trabajo en un equipo de desarrollo donde
dos ramas modifican el mismo archivo y la misma sección, provocando un conflicto
durante el proceso de Pull Request.

El objetivo fue:
- Identificar el conflicto
- Analizar su causa
- Resolverlo correctamente
- Validar que no exista pérdida de funcionalidad

---

## 🧠 Escenario Simulado

- Rama base: `main`
- Rama 1: `feature/login`
- Rama 2: `feature/ui`
- Archivo afectado: `README.md`
- Sección afectada: `Login`

Ambas ramas realizaron cambios sobre la misma línea del archivo, generando un conflicto
al intentar hacer merge hacia `main`.

---

## 🚨 Detección del Conflicto

Durante la creación del Pull Request desde `feature/ui` hacia `main`,
GitHub detectó un conflicto automático indicando que el merge no podía realizarse
sin intervención manual.

Mensaje típico:
> This branch has conflicts that must be resolved

---

## 🔍 Análisis QA del Conflicto

El archivo presentaba los marcadores estándar de Git:

```text
<<<<<<< HEAD
Cambio relacionado con validación visual en frontend
=======
Cambio relacionado con validación backend de credenciales
>>>>>>> main
