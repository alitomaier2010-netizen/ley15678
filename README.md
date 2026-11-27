# Conciencia digital, algoritmos y marco legal — Ley 15.678

**Actividad 10 — El uso de celulares en el aula** · Laboratorio de Programación (LPR) · 5.º 3.ª A-B · E.E.S.T. N.º 1 «Eduardo Ader» — Vicente López

Rama `ley15678` de la Actividad 10: un **filtro de decisiones** en Python que simula cómo un docente o un sistema escolar evalúa si un estudiante puede usar el dispositivo en un momento dado, según la Ley 15.678 de la Provincia de Buenos Aires.

| Caso | Contexto | Rama del algoritmo | Resultado |
|------|----------|--------------------|-----------|
| A | Autorización docente explícita con fin pedagógico | `if` | ✅ Acceso permitido (solo para estudiar) |
| B | Emergencia familiar validada por preceptoría | `elif` | 🔁 Canalización institucional |
| C | Sin autorización ni emergencia | `else` | ⛔ Restricción Ley 15.678 — celular en la mochila |

- Estudiante: **Alexis Maier**
- Integrantes del grupo: Alexis Maier (trabajo individual)
- Docente: Mansilla Muñoz York Elías
- Fecha de entrega: 25 de noviembre de 2026

## Datos institucionales

- **Institución:** E.E.S.T. N.º 1 «Eduardo Ader» — Vicente López
- **Curso:** 5.º 3.ª A-B
- **Materia:** Laboratorio de Programación (LPR)
- **Profesor:** Prof. York
- **Actividad:** 10 — Ley 15.678: conciencia digital y marco legal

## Presentación de la Actividad

Simulador en Python de los escenarios de uso de celulares en el aula según la Ley 15.678, con evaluación de authorize docente, emergencia familiar y uso personal.

## Integrantes y roles

| Integrante | Rol / tarea asignada | Aporte individual |
|---|---|---|
| Alexis Maier | Marco normativo, función de evaluación de casos, pruebas e informe | [ley15678](https://github.com/alitomaier2010-netizen/ley15678) |

## Requisitos e instalación

1. **Git** instalado para clonar el repositorio.
2. **Editor de código** (VS Code con extensiones de C/C++, o Visual Studio Community).
3. **Compilador g++** (MinGW-w64 / MSYS2) agregado al `PATH` del sistema.
4. Clonar y situarse en el directorio:

```bash
git clone https://github.com/alitomaier2010-netizen/ley15678.git
cd ley15678
```

## Estructura

```
ley15678/
├── .gitignore                                exclusión de caché de Python (*.pyc, __pycache__)
├── LICENSE                                   licencia MIT escolar
├── README.md                                 portada de la actividad y explicación técnica
├── docs/
│   └── InformeEEST1_LPR2026_ACT10_Ley_Maier_v1.0.0.pdf
│                                             informe APA v7 con diagrama, código, ejecución y reflexión
├── src/
│   └── ley_celulares.py                      filtro de decisiones if / elif / else
└── capturas/
    ├── diagrama_flujo.png                    diagrama de flujo (opción A, versión digital de la hoja de carpeta)
    └── ejecucion_consola.png                 captura de la ejecución de los tres casos
```

## Marco normativo

La Ley 15.678 (Provincia de Buenos Aires) prohíbe el uso de teléfonos celulares y dispositivos digitales por parte de los estudiantes de niveles primario y secundario durante la jornada escolar. La **regla general** es no usar pantallas en clase; la **excepción pedagógica** exige requerimiento y autorización explícita del docente con fines estrictamente pedagógicos. Llevar el celular en la mochila por seguridad en el trayecto no está prohibido: lo que la ley regula es su **uso** dentro del aula. Las emergencias familiares se canalizan institucionalmente mediante preceptoría y/o dirección.

## Explicación técnica

El script `src/ley_celulares.py` modela el contexto con dos variables booleanas: `autorizacion_docente` y `emergencia_familiar`. La función `evaluar_uso()` aplica la estructura condicional:

1. `if autorizacion_docente == True` → **acceso permitido** únicamente con fin pedagógico;
2. `elif emergencia_familiar == True` → **canalización institucional** a través de preceptoría/dirección;
3. `else` → **restricción** de la Ley 15.678: el celular permanece guardado en la mochila.

El orden importa: la autorización docente se evalúa primero porque es la única excepción que habilita el uso del dispositivo; la emergencia no habilita el uso libre, sino una vía de comunicación institucional. El programa ejecuta los tres casos de prueba para que cada rama quede verificada.

## Diagrama de flujo

El diagrama de la opción A se realizó a mano en la carpeta de la materia y se digitalizó en `capturas/diagrama_flujo.png` para incluirlo en el informe. Comienza en **INICIO**, consulta «¿Autorización docente?»; si es *sí* llega a **ACCESO PERMITIDO** (verde), si es *no* consulta «¿Emergencia validada?»; según corresponda termina en **CANALIZACIÓN INSTITUCIONAL** (amarillo) o **RESTRICCIÓN LEY 15.678** (rojo). Todas las ramas convergen en **FIN**.

## Ejecutar (PowerShell, desde la raíz del repositorio)

```
py src/ley_celulares.py
```

No requiere librerías externas: usa solo Python estándar (funciones, booleanos, `if/elif/else` y `f-strings`).

## Referencias del trabajo

- GitHub: https://github.com/alitomaier2010-netizen/ley15678
- GitLab: https://gitlab.com/Alitopro/ley15678

El informe APA v7 (`docs/InformeEEST1_LPR2026_ACT10_Ley_Maier_v1.0.0.pdf`) incluye ambas referencias en su sección final, junto con la norma y la documentación de Python.

**Espejo automático:** https://gitlab.com/Alitopro/ley15678
