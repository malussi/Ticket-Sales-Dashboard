# Ticket Sales Dashboard - Análisis Estático de Código

Proyecto desarrollado para la **Evaluación Sumativa III** de la asignatura *Calidad de Componentes de Software*.

## Descripción
Este repositorio contiene el código fuente del proyecto **Ticket Sales Dashboard** y la documentación técnica de su proceso de validación. El objetivo central ha sido aplicar técnicas de **análisis estático de código** utilizando **SonarQube** para garantizar estándares de calidad, seguridad y mantenibilidad en el ciclo de vida del desarrollo de software.

## Objetivos del Análisis
* **Identificación de Riesgos:** Detección de *Security Hotspots* y vulnerabilidades en el código fuente.
* **Evaluación de Mantenibilidad:** Reducción de deuda técnica y mejora en la legibilidad del código.
* **Validación:** Implementación de mejores prácticas de la industria según el modelo SQuaRE (ISO/IEC 25010).

## Ejecución Técnica
El análisis se realizó mediante un entorno aislado utilizando **Docker**, lo que permite una ejecución consistente, limpia y reproducible.

## Video de Presentación
Puedes ver la explicación técnica y la auditoría completa del proyecto aquí:
[Ver video de la Evaluación Sumativa III - Ticket Sales Dashboard](https://youtu.be/0mCYDlJxkvU?si=icwL7VLzJM2-LYyw)

**Comando de ejecución:**
```bash
docker run --rm --network=host \
  -e SONAR_HOST_URL="http://localhost:9000" \
  -e SONAR_TOKEN="TU_TOKEN_AQUI" \
  -v "${PWD}:/usr/src" \
  sonarsource/sonar-scanner-cli \
  "-Dsonar.projectBaseDir=/usr/src"
