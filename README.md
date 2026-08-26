![Logo Institucional](https://github.com/JonatanBogadoUNLZ/PPS-Jonatan-Bogado/blob/9952aac097aca83a1aadfc26679fc7ec57369d82/LOGO%20AZUL%20HORIZONTAL%20-%20fondo%20transparente.png)

# UNLZ — Facultad de Ingeniería (Plantilla de Proyecto)
## Ingeniería Mecatrónica — README + estructura estándar

Este repositorio es una **PLANTILLA**.  
Los estudiantes deben **usar este repo como base** (fork o “Use this template”) y **reemplazar los textos entre corchetes** `[ ... ]` con la información real de su proyecto.

---

## 📛 Naming del repositorio (OBLIGATORIO)

El nombre del repositorio debe seguir este esquema:

**`ANIO_CUATRIMESTRE_TIPO_PROYECTO_APELLIDOS`**

Donde:
- **ANIO**: año de cursada (ej. `2026`)
- **CUATRIMESTRE**: `1C` o `2C`
- **TIPO**: `PPS` o `PF` (Proyecto Final)
- **PROYECTO**: nombre corto *sin espacios* (recomendado: `kebab-case` o `CamelCase`)
- **APELLIDOS**: apellidos de integrantes separados por `_` (sin tildes, sin ñ)

✅ Ejemplos:
- `2026_1C_PPS_ComederoSmart_Salto_Vazquez`
- `2026_2C_PF_MecaChess_Duarte_Diaz`
- `2025_2C_PPS_Escaner3D_DalleRivePrieto_Labreniuk`

> Nota: GitHub **no permite** usar “/” en el nombre del repositorio.  
> Por eso se usa **TIPO = PPS o PF** como campo separado.

---

## 🧩 Cómo usar esta plantilla (estudiantes)

0) **Crear el repo con el nombre correcto (OBLIGATORIO)**  
   Esquema: `ANIO_CUATRIMESTRE_TIPO_PROYECTO_APELLIDOS`

1) Crear tu repositorio desde esta plantilla:
   - Opción A (recomendada): **Use this template** → Create a new repository  
   - Opción B: **Fork**

2) Editar este archivo `README.md` completando todos los campos `[ ... ]`.

3) Subir archivos a las carpetas correspondientes:
   - Código en `CODIGO/`
   - Planos y esquemas en `PLANOS/`
   - Fotos / videos en `MULTIMEDIA/`
   - Datasheets en `DATASHEET/`
   - Informes en `INFORMES/`

---

## ✅ Checklist de entrega
- [X] Naming correcto del repo: `ANIO_CUATRIMESTRE_TIPO_PROYECTO_APELLIDOS`
- [ ] Título, autores, materia, **tipo (PPS/PF)**, año y cuatrimestre completos
- [ ] Brief completo (one-liner + pitch + problema + solución + alcance + estado)
- [ ] Instrucciones de uso reproducibles (otro puede correrlo)
- [ ] Lista de componentes con cantidades y modelos
- [ ] Esquemáticos/planos adjuntos en `PLANOS/`
- [ ] Fotos / video demostración en `MULTIMEDIA/`
- [ ] Informe PDF en `INFORMES/` (si aplica)

---

# Sistema de control wearable mediante señales EMG para rehabilitación motriz

**Tipo:** PF  
**Año:** 2026 — **Cuatrimestre:** 2C  

**Carrera:** Ingeniería Mecatrónica  
**Materia / Curso:** Proyecto en ingeniería mecatrónica  
**Docente / Cátedra:** Ezequiel, Blanca · Cristian, Lukaszewicz · Juan Ignacio, Szombach 
**Autor/es:** LOMAZZI, Bianca — [Legajo] · CHIMENTE, Matias — [Legajo]

---

## Introducción / Objetivo

**Contexto (2–4 líneas):**  
El proyecto se enfoca en personas que presentan limitaciones en la movilidad de las extremidades superiores. Busca introducir una solución tecnológica y accesible en los entornos de rehabilitación física para asistir tanto a pacientes como a profesionales de la salud.

**Problema a resolver:**  
La necesidad de potenciar y asistir los procesos de rehabilitación física convencionales mediante herramientas interactivas que aumenten la motivación y adherencia al tratamiento.

**Objetivo general:**  
Desarrollar un sistema integrado que combine hardware wearable, procesamiento de señales biomédicas y software interactivo para asistir la rehabilitación motriz.

**Objetivos específicos (opcional):**
- Capturar e interpretar impulsos eléctricos generados por la contracción muscular utilizando sensores EMG integrados en una manga auxética.
- Traducir las intenciones de movimiento en comandos inalámbricos para controlar un vehículo robótico.
- Proveer una plataforma web interactiva y lúdica ("Robrain Kids") que estimule al paciente y permita registrar indicadores de desempeño para el seguimiento médico.

---

## Índice
- [Brief](#brief)
- [Descripción técnica](#descripción-técnica)
- [Arquitectura del sistema](#arquitectura-del-sistema)
- [Instrucciones de uso](#instrucciones-de-uso)
- [Tecnologías utilizadas](#tecnologías-utilizadas)
- [Listado de componentes](#listado-de-componentes)
- [Esquemáticos / Planos](#esquemáticos--planos)
- [Fotos / Videos](#fotos--videos)
- [Estructura del repositorio](#estructura-del-repositorio)
- [Autor](#autor)
- [Licencia](#licencia)

---

## Brief

**One-liner (1 frase):**  
Sistema wearable basado en señales EMG que permite a pacientes en rehabilitación controlar un vehículo robótico y juegos interactivos para potenciar su recuperación física.

**Elevator pitch (30 segundos):**  
Este proyecto **Sistema de control wearable EMG** (tipo **PF**, **2026 2C**) resuelve **la falta de motivación y seguimiento en las terapias motrices** mediante **una manga con sensores electromiográficos conectada a un vehículo robótico y un entorno virtual gamificado.**.  
Está orientado a **personas y niños con limitaciones de movilidad en extremidades superiores** y permite **realizar un seguimiento objetivo de la evolución terapéutica.**  
Se implementa con **microcontroladores ESP32, sensores MyoWare e impresión 3D** y se valida mediante **el control efectivo del actuador y la interacción con la aplicación web.**.

### Problema
- **Contexto:** Entornos clínicos u hogareños de rehabilitación física, especialmente aquellos que tratan a niños y niñas.
- **Dolor principal:** [qué falla / qué es lento / qué es costoso / qué es riesgoso]
- **Impacto:** [tiempo, costo, errores, seguridad, calidad]

### Solución propuesta
- **Qué hace (features):**
  - Captura señales electromiográficas (EMG) adaptándose a la anatomía del brazo mediante una estructura auxética.
  - Controla de forma inalámbrica un vehículo robótico con mecanismo de prevención de colisiones.
  - Ofrece actividades lúdicas (ej. "Estallido de Globos", "Estrella de Rock") en la aplicación web "Robrain Kids".
- **Cómo lo hace (alto nivel):** Sensor EMG MyoWare → Unidad de control ESP32 → Transmisión inalámbrica → Vehículo robótico / Interfaz Web.
- **Valor diferencial:** Su portabilidad extrema por el diseño desmontable, el bajo consumo energético, la adaptabilidad de la manga impresa en 3D y su enfoque gamificado.

### Alcance
**Incluye:**
- [X] Desarrollo de manga auxética ajustable pasiva con electrodos.
- [X] Unidad de control central desmontable con Super Mini ESP32 y batería LiPo.
- [X] Vehículo robótico con sensor de proximidad y carrocerías 3D.
- [X] Aplicación web "Robrain Kids" para interacción y registro de progreso.

**No incluye (por ahora):**
- [A]
- [B]

### Estado del proyecto
- **Madurez:** Prototipo
- **Qué funciona hoy:** [lista corta]
- **Próximos pasos:** [lista corta]

### Demo rápida
- **Video / GIF:** [link o ruta en MULTIMEDIA]
- **Instrucciones express (2 minutos):**
  1) [Paso 1]
  2) [Paso 2]
  3) [Paso 3]

---

## Descripción técnica
El sistema se compone de una unidad wearable equipada con un sensor MyoWare que capta los impulsos de contracción muscular. Esta señal ingresa a una unidad central comandada por un ESP32 C3 Super Mini, alimentado por una batería LiPo de 3.7V (600mAh). Las señales procesadas son enviadas inalámbricamente para comandar tanto las acciones de un vehículo robótico (equipado con parada de emergencia por proximidad) como los eventos dentro del software web "Robrain Kids". El hardware se integra a la piel del usuario a través de una manga con geometría auxética impresa en 3D.

---

## Arquitectura del sistema

**Entradas (sensores / señales):**
- Sensor Electromiográfico (MyoWare)
- Sensor de proximidad (para detección de obstáculos)

**Procesamiento / Control:**
- Microcontrolador ESP32 C3 Super Mini
- Plataforma web para el registro de indicadores de desempeño

**Salidas (actuadores / señales):**
- Sistema de actuación del vehículo robótico (motores)

**Interfaz (si aplica):**
- Aplicación web "Robrain Kids" (dashboard interactivo de rehabilitación)

> (Opcional) Insertar diagrama:
![Diagrama de bloques](PLANOS/diagrama_bloques.png)

---

## Instrucciones de uso

### Requisitos previos
- [Software / IDE]
- [Drivers / librerías]
- [Hardware mínimo]

### Instalación / Puesta en marcha
1) [Clonar / descargar]
2) [Instalar dependencias]
3) [Cargar firmware / ejecutar]
4) [Validar funcionamiento]

### Uso
- **Modo normal:** [cómo se usa]
- **Calibración (si aplica):** [pasos]
- **Notas:** [cuidados, recomendaciones]

### Troubleshooting (opcional)
- **Problema:** [X] → **Solución:** [Y]
- **Problema:** [X] → **Solución:** [Y]

---

## Tecnologías utilizadas
- **Robótica / Control:** ESP32 C3 Super Mini, ESP32
- **Electrónica:** Sensor MyoWare, Batería LiPo 3.7V 600mAh, Sensores de proximidad.
- **Programación:** C, Python.
- **Plataformas / Tools:** [ROS / OpenCV / etc.]
- **IA (si aplica):** [modelo / técnica]

---

## Listado de componentes

| Componente | Cantidad | Modelo / Especificación | Función |
|---|---:|---|---|
| Sensor EMG | [2] | [Modelo] | [Función] |
| Microcontrolador | [2] | ESP 32 C3 Super Mini | [Función] |
| Microcontrolador | [1] | ESP 32 | [Función] |
| Bateria | [2] | LiPo 3.7 V 600 mAh | [Función] |
| Soporte wearable | [2] | Manga auxética 3D | [Función] |

---

## Esquemáticos / Planos
- [Plano/Esquemático 1] → `PLANOS/[archivo]`
- [Plano/Esquemático 2] → `PLANOS/[archivo]`

---

## Fotos / Videos
- Foto 1 → `MULTIMEDIA/[archivo]`
- Foto 2 → `MULTIMEDIA/[archivo]`
- Video demo → `MULTIMEDIA/[archivo]` o [link]

---

## Estructura del repositorio
- `CODIGO/` — Código fuente del proyecto.
- `MULTIMEDIA/` — Imágenes y videos.
- `PLANOS/` — Esquemáticos y diagramas.
- `DATASHEET/` — Hojas de datos y especificaciones.
- `INFORMES/` — Informes, Gantt, manuales, PDFs.

---

## Autor
**[LOMAZZI, Bianca]** — [Legajo]  
**[CHIMENTE, Matias]** — [Legajo]  
Contacto (opcional): [biancalujan58@gmail.com / [LinkedIn](https://www.linkedin.com/in/biancalomazzi/)]
Contacto (opcional): [matias.chimente@gmail.com / [LinkedIn](https://www.linkedin.com/in/matias-chimente/)]

---

## Licencia
[Definir según la cátedra: MIT / uso académico / etc.]

---

## About (descripción corta del repositorio)

El presente proyecto consiste en el diseño y desarrollo de un sistema integrado orientado a la rehabilitación motriz de personas con limitaciones en la movilidad de las extremidades superiores.

**PF — SISTEMA DE CONTROL EMG DE REHABILITACION MOTRIZ — FI-UNLZ — 2026 2C — Lomazzi, Chimente**
