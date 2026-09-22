# 🩺 MediCita

**Capstone — Equipo Medicita**

**Desafío:** Automatización del reagendamiento de citas médicas en los CESFAM de Providencia
**Contraparte:** Dirección de Salud de Providencia / CESFAM Dr. Alfonso Leng
**Estado actual:** En desarrollo — etapa de investigación

## Idea central

> Providencia ya cuenta con canales digitales y telefónicos para **solicitar** horas médicas (Telesalud, agendamiento telefónico); nuestro desafío es mejorar lo que ocurre **cuando esas horas ya asignadas necesitan modificarse**, facilitando el reagendamiento tanto para pacientes como para funcionarios.

## Equipo

| Integrante | Carrera o especialidad | Rol inicial | Usuario de GitHub |
|---|---|---|---|
| Isidora Franco | Ingeniería Civil Industrial | Investigación del proceso actual de agendamiento | — |
| Benjamín Huechuqueo | Ingeniería Civil en Computación e Informática | Investigación de necesidades y dificultades de usuarios | — |
| Martín Strauch | Ingeniería Civil Industrial | Análisis y propuesta de funcionalidades de MediCita | — |
| Leonardo Torres | Ingeniería Civil Electrónica | Organizar la información recopilada y apoyar en la definición de la propuesta y estructura inicial del prototipo | — |
| Martín Fariña | Ingeniería Civil en Computación e Informática | Gestión y documentación del repositorio GitHub / bitácora | `martinfarina-ux` |

## Valores del equipo

- **Responsabilidad**
- **Respeto**
- **Comprensión**
- **Compromiso**
- **Comunicación**

## Normas de funcionamiento

1. Cumplir con las tareas y plazos.
2. Mantener una comunicación respetuosa.
3. Avisar ante cualquier inconveniente.
4. Participar y colaborar entre los 5.
5. Resolver diferencias mediante el diálogo.

## Disponibilidad del equipo

| Integrante | Disponibilidad |
|---|---|
| Isidora Franco | Lunes / Martes / Miércoles |
| Benjamín Huechuqueo | Martes / Miércoles / Jueves |
| Leonardo Torres | Lunes / Miércoles / Viernes |
| Martín Strauch | Martes / Miércoles / Jueves |
| Martín Fariña | ⚠️ *pendiente* |

**Acuerdo:** nos adaptamos a los horarios de cada integrante, manteniendo el compromiso y la participación de los 5.

## Contexto

Los CESFAM son la puerta de entrada a la atención primaria de salud. En Providencia existen tres: **Dr. Hernán Alessandri**, **El Aguilucho** y **Dr. Alfonso Leng**, además de CECOSF y otros servicios de la red comunal.

La demanda es alta: durante 2025 la Dirección de Salud de Providencia registró **506.774 prestaciones y atenciones**, un **11,7% más que en 2024**.

## ¿Cómo se agendan hoy las citas?

Providencia cuenta con dos canales principales:

- **Agendamiento telefónico** — desde marzo de 2026, vía el número **800 077 098**, de lunes a viernes desde las 07:00 hrs, para horas médicas, dentales y ginecológicas (CESFAM y CECOSF).
- **Telesalud** — plataforma online donde el usuario solicita atención desde computador, celular o tablet; el equipo del CESFAM revisa la solicitud y luego informa la hora asignada.

Según el MINSAL, **agendamiento** es la asignación de una cita según la oferta disponible, mientras que **gestión de agenda** incluye organizar, mantener y asignar horas.

## ¿Dónde aparece nuestro problema?

El proyecto **no busca resolver el agendamiento inicial**, sino lo que ocurre **después** de que una hora ya fue asignada:

```
Hora asignada
   ↓
Se produce un cambio o cancelación
   ↓
El paciente necesita ser informado
   ↓
Se debe buscar una nueva alternativa
   ↓
Se modifica la agenda
   ↓
Se confirma la nueva hora
```

El MINSAL incluye dentro de la gestión de agenda las acciones destinadas a mantener y gestionar las horas de atención, buscando asegurar el acceso y **disminuir las inasistencias**.

> **Aún no tenemos un dato oficial** de Providencia sobre cuánto tiempo ocupa este proceso o cuántas horas se pierden por reagendamientos mal gestionados. Debe validarse directamente con funcionarios del CESFAM (ver sección de preguntas pendientes).

## Problemática

> **¿Cómo mejorar el proceso de reagendamiento de horas médicas para reducir tareas administrativas y facilitar la coordinación entre el CESFAM y los pacientes?**

## Involucrados

| Actor | Rol en el problema |
|---|---|
| 👤 Pacientes | Reciben la atención y necesitan ser informados cuando su hora cambia. |
| 👩‍💼 Funcionarios administrativos | Gestionan agendas, coordinación y comunicación con usuarios. |
| 👨‍⚕️ Profesionales de salud | Su disponibilidad forma parte de la agenda que debe gestionarse. |
| 🏥 CESFAM | Coordina recursos, profesionales, pacientes y disponibilidad de horas. |
| 🏛️ Municipalidad / Dirección de Salud | Administra y coordina la red comunal de salud. |

## Desafíos a enfrentar

- 📲 Mejorar la comunicación con los pacientes.
- 📅 Facilitar la búsqueda de nuevas horas.
- ⏱️ Reducir tareas repetitivas para funcionarios.
- 🔄 Evitar que los cambios de agenda generen pérdida de cupos.
- 📊 Mantener un registro del proceso.
- 👩‍💼 Mantener intervención humana cuando el caso lo requiera.

## Propuesta: MediCita

Herramienta de reagendamiento automatizado o semi-automatizado:

```
CESFAM modifica una hora
   ↓
📲 MediCita identifica al paciente afectado
   ↓
📩 Envía una notificación
   ↓
📅 Ofrece alternativas disponibles
   ↓
👤 Paciente selecciona una opción
   ↓
✅ Se registra el cambio
   ↓
🚨 Si existe un problema → interviene un funcionario
```

La idea **no es reemplazar a los funcionarios**, sino automatizar las tareas repetitivas y dejar los casos que requieren criterio humano al personal.

## Beneficios esperados

**Para los pacientes**
- Mayor facilidad para reagendar.
- Información más oportuna.
- Menos gestiones repetitivas.

**Para los funcionarios**
- Menor carga administrativa.
- Menos tareas manuales.
- Mejor organización de las agendas.

**Para el CESFAM**
- Mejor gestión de las horas.
- Mayor trazabilidad.
- Mejor aprovechamiento de los cupos disponibles.

## Impactos esperados

| Ámbito | Impacto |
|---|---|
| Operativo | Menor tiempo destinado a tareas repetitivas de reagendamiento. |
| Atención | Mejor comunicación y experiencia para los pacientes. |
| Funcionarios | Mayor disponibilidad de tiempo para otras tareas de gestión. |
| Sistema | Una gestión de agendas más eficiente y ordenada. |

## Lo que todavía necesitamos investigar

Preguntas a validar directamente con el CESFAM (próximo paso de investigación):

- ¿Cuántas horas se reagendan aproximadamente?
- ¿Por qué motivos se reagendan?
- ¿Quién realiza actualmente el proceso?
- ¿Cómo contactan al paciente?
- ¿Cuántos intentos de contacto realizan?
- ¿Cuánto demora aproximadamente un reagendamiento?
- ¿Qué ocurre si el paciente no responde?
- ¿Cómo se registra actualmente el cambio?
- ¿Qué pasa con el cupo que queda disponible?
- ¿Cuál es la principal dificultad que identifican los funcionarios?

## Objetivo del proyecto

**General:** automatizar el proceso de reagendamiento de citas médicas en los CESFAM de Providencia, reduciendo la carga administrativa y facilitando la gestión de horas para funcionarios y pacientes.

**Corto plazo (1 de septiembre de 2026):** completar la investigación inicial del proceso de reagendamiento y definir una propuesta de solución para MediCita, estableciendo las bases para el desarrollo del prototipo.

**Largo plazo:** desarrollar y presentar un prototipo funcional de MediCita que permita automatizar el reagendamiento de citas médicas en los CESFAM de Providencia.

## Compromisos individuales SMART

| Integrante | Compromiso al 1 de septiembre de 2026 |
|---|---|
| Isidora Franco | Recopilar y organizar información sobre el proceso actual de agendamiento y reagendamiento en los CESFAM de Providencia. |
| Benjamín Huechuqueo | Investigar las principales necesidades y dificultades de los usuarios relacionadas con el agendamiento y reagendamiento de horas. |
| Martín Strauch | Analizar y proponer las principales funcionalidades que debería tener MediCita. |
| Leonardo Torres | Organizar la información recopilada y apoyar en la definición de la propuesta y estructura inicial del prototipo. |
| Martín Fariña | Subir, estructurar y mantener actualizado el repositorio de GitHub del proyecto (bitácora y documentación). |

## 📓 Bitácora

Todo el avance clase a clase se documenta en [`bitacora/`](./bitacora/README.md), con una entrada por sesión siguiendo una [plantilla común](./bitacora/PLANTILLA.md).

| Sesión | Fecha | Foco |
|---|---|---|
| [Sesión 1](./bitacora/Sesion-01.md) | ⚠️ por confirmar | Contrato de equipo, investigación inicial y definición del problema |
