# QA Automation with GitHub Actions

Repositorio de práctica enfocado en el uso de Git, GitHub y GitHub Actions
desde la perspectiva de un QA Engineer.

## 🎯 Objetivo
Simular un flujo real de calidad donde:
- QA valida reglas automáticamente
- Los Pull Requests se bloquean si QA falla
- Solo se integran cambios que cumplen estándares

## 🧪 Validaciones implementadas
- Verificación automática de existencia de README.md
- Ejecución de QA Check en:
  - Push a `main`
  - Pull Requests hacia `main`

## 🔁 Flujo de trabajo
1. Cambio en rama feature
2. Creación de Pull Request
3. Ejecución automática de QA
4. Bloqueo si QA falla
5. Merge solo con QA aprobado

## 🛠️ Herramientas usadas
- Git
- GitHub
- GitHub Actions
- YAML
- CI/CD básico

## 📁 Estructura
