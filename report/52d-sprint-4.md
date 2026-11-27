### 5.2.4. Sprint 4

En esta sección se registra el Sprint 4, el Sprint de cierre de la versión (Release Review). Como las 31 User Stories del Product Backlog se implementaron en los Sprints 1 a 3, el Sprint 4 se organiza con ocho Technical Stories (TS01 a TS08) que cubren la calidad, la validación con usuarios, los videos, el despliegue final y el informe. Las evidencias de esta sección corresponden al avance al 2026-11-26.

#### 5.2.4.1. Sprint Planning 4

| Sprint # | Sprint 4 |
| :--- | :--- |
| **Sprint Planning Background** | |
| Date | 2026-11-26 (por confirmar) |
| Time | Por confirmar por el equipo |
| Location | Por confirmar por el equipo |
| Prepared By | Por confirmar por el equipo |
| Attendees (to planning meeting) | Por confirmar por el equipo |
| Sprint 3 Review Summary | En el Sprint 3 se implementaron los Web Services con 74 operaciones REST documentadas con OpenAPI, se integró la Web Application v1.2.0 con ellos y se etiquetaron el release v1.0.0 y el hotfix v1.0.1 (2026-11-14). Quedan por confirmar las historias US26, US28 y US29 (To-Review), y los productos desplegados no responden en sus URLs. |
| Sprint 3 Retrospective Summary | Pendiente: el equipo debe registrar las opiniones de la retrospectiva. |
| **Sprint Goal & User Stories** | |
| Sprint 4 Goal | **Nuestro enfoque está en** entregar la versión final de Trazza: los tres productos desplegados y verificados, con pruebas automatizadas, validados con usuarios de ambos segmentos y documentados. **Creemos que esto entrega** confianza para adoptar la plataforma **a** los transportistas y comerciantes MYPE de Lima Metropolitana, y un producto mantenible al equipo y al docente. **Esto se confirmará cuando** (1) el Landing Page, la Web Application y los Web Services estén desplegados en su versión final, con releases etiquetados en SemVer y sus URLs verificadas; (2) `./mvnw test` de los Web Services y `npm test` de la Web Application pasen al 100 %, con al menos 90 pruebas unitarias en la Web Application (antes de este Sprint había 17); (3) se registren entre 3 y 5 entrevistas de validación por segmento (de 6 a 10 en total) y la evaluación heurística de Nielsen con la severidad de cada hallazgo; (4) los videos About-the-Product y About-the-Team estén publicados; y (5) las **8 historias técnicas (44 SP)** estén cerradas y el informe tenga sus seis capítulos completos. |
| Sprint 4 Velocity | 44 Story Points |
| Sum of Story Points | 44 Story Points (TS01: 8, TS02: 8, TS03: 5, TS04: 5, TS05: 5, TS06: 5, TS07: 5, TS08: 3) |

#### 5.2.4.2. Aspect Leaders and Collaborators

Los aspectos del Sprint 4 corresponden a las Technical Stories. La asignación se propuso en el Sprint Planning 4 y debe ser confirmada por el equipo.

| Team Member (Last Name, First Name) | GitHub Username | Pruebas de los Web Services (L/C) | Pruebas de la Web Application (L/C) | Entrevistas y evaluación heurística (L/C) | Videos (L/C) | Despliegue final (L/C) | Informe final (L/C) |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| Checalla Apaza, Emanuel Renato | Emanuelca135 | C | C | C | C | C | C |
| Lozano Quispe, Fabricio Jofred | FabricioZz15 | C | C | L | C | C | C |
| Peñaranda Caldas, Gabriel Augusto | gapc2124 | L | C | C | C | L | C |
| Pezo Castilla, Maria Jose | MariaJosePezo | C | L | C | C | C | L |
| Vite Celis, Rodrigo Matias | rodriznnn | C | C | C | L | C | C |

#### 5.2.4.3. Sprint Backlog 4

El Sprint Backlog 4 contiene las ocho Technical Stories, definidas en la sección 3.3, y sus tareas. Al 2026-11-26, 20 tareas: 1 en **Done**, 1 en **In-Process**, 0 en **To-Review** y 18 en **To-do**.

| Id | Technical Story | Story Points |
| :--- | :--- | :---: |
| TS01 | Pruebas unitarias de los Web Services | 8 |
| TS02 | Pruebas de integración y aceptación de los Web Services | 8 |
| TS03 | Pruebas unitarias de la Web Application | 5 |
| TS04 | Entrevistas de validación | 5 |
| TS05 | Evaluación heurística y mejoras | 5 |
| TS06 | Videos About-the-Product y About-the-Team | 5 |
| TS07 | Despliegue final y release | 5 |
| TS08 | Informe final | 3 |

**URL público del Board:** [https://trazza.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog](https://trazza.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog)

| Sprint # | Sprint 4 | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **User Story** | | **Work-Item / Task** | | | | | |
| **Id** | **Title** | **Id** | **Title** | **Description** | **Estimation (Hours)** | **Assigned To** | **Status (To-do / In-Process / To-Review / Done)** |
| TS01 | Pruebas unitarias de los Web Services | T01 | Pruebas unitarias de IAM, shared y Matchmaking | Escribir pruebas del dominio y de los servicios de aplicación de IAM, shared y Matchmaking. | 8 | Peñaranda Caldas, Gabriel Augusto | To-do |
| TS01 | Pruebas unitarias de los Web Services | T02 | Pruebas unitarias de Execution | Escribir pruebas de los servicios de viaje, seguimiento GPS e incidencias. | 6 | Pezo Castilla, Maria Jose | To-do |
| TS01 | Pruebas unitarias de los Web Services | T03 | Pruebas unitarias de Billing | Escribir pruebas de planes, suscripciones, liquidaciones y compensaciones. | 6 | Lozano Quispe, Fabricio Jofred | To-do |
| TS01 | Pruebas unitarias de los Web Services | T04 | Pruebas unitarias de Reputation | Escribir pruebas de calificaciones y puntos de lealtad. | 6 | Vite Celis, Rodrigo Matias | To-do |
| TS02 | Pruebas de integración y aceptación de los Web Services | T05 | Pruebas de integración de los controladores REST | Probar los controladores contra una base de datos de prueba. | 8 | Checalla Apaza, Emanuel Renato | To-do |
| TS02 | Pruebas de integración y aceptación de los Web Services | T06 | Escenarios de aceptación en Gherkin | Redactar y automatizar los escenarios de aceptación de las historias principales. | 6 | Checalla Apaza, Emanuel Renato | To-do |
| TS03 | Pruebas unitarias de la Web Application | T07 | Pruebas unitarias de la Web Application: Execution | Agregar pruebas de las entidades, el store, el API, las rutas y las vistas de Execution, y su documentación. | 8 | Pezo Castilla, Maria Jose | Done |
| TS03 | Pruebas unitarias de la Web Application | T08 | Pruebas unitarias de la Web Application: otros contextos | Agregar pruebas de IAM, Matchmaking, Billing y Reputation. | 8 | Peñaranda Caldas, Gabriel Augusto | To-do |
| TS04 | Entrevistas de validación | T09 | Guion y agenda de las entrevistas | Preparar las tareas, las preguntas y la agenda con 3 a 5 participantes por segmento. | 4 | Lozano Quispe, Fabricio Jofred | To-do |
| TS04 | Entrevistas de validación | T10 | Realizar y grabar las entrevistas | Entrevistar a los participantes sobre el Landing Page y la aplicación y grabar cada sesión. | 8 | Lozano Quispe, Fabricio Jofred | To-do |
| TS04 | Entrevistas de validación | T11 | Registro y resumen de las entrevistas | Completar la sección 5.3.2 con los datos, los videos y el resumen de cada entrevista. | 4 | Checalla Apaza, Emanuel Renato | To-do |
| TS05 | Evaluación heurística y mejoras | T12 | Evaluación heurística | Aplicar las heurísticas con el formato del Anexo D y registrar los hallazgos con su severidad. | 6 | Lozano Quispe, Fabricio Jofred | To-do |
| TS05 | Evaluación heurística y mejoras | T13 | Corrección de los hallazgos | Corregir los hallazgos de severidad 3 y 4 en el Landing Page y la Web Application. | 6 | Peñaranda Caldas, Gabriel Augusto | To-do |
| TS06 | Videos About-the-Product y About-the-Team | T14 | Video About-the-Product | Producir y publicar el video en Microsoft Stream y YouTube, e incrustarlo en el Landing Page. | 8 | Vite Celis, Rodrigo Matias | To-do |
| TS06 | Videos About-the-Product y About-the-Team | T15 | Video About-the-Team | Producir y publicar el video del equipo en Microsoft Stream y YouTube. | 8 | Vite Celis, Rodrigo Matias | To-do |
| TS07 | Despliegue final y release | T16 | Despliegue de los Web Services | Desplegar los Web Services con su base de datos MySQL y registrar la URL de la documentación. | 8 | Peñaranda Caldas, Gabriel Augusto | To-do |
| TS07 | Despliegue final y release | T17 | Republicación del Landing Page y la Web Application | Volver a publicar el Landing Page y la Web Application y verificar sus URLs. | 4 | Peñaranda Caldas, Gabriel Augusto | To-do |
| TS07 | Despliegue final y release | T18 | Releases y etiquetas | Crear los releases finales con Semantic Versioning y actualizar los CHANGELOG. | 3 | Peñaranda Caldas, Gabriel Augusto | To-do |
| TS08 | Informe final | T19 | Reescritura del capítulo 5 | Reestructurar el capítulo 5 con los cuatro Sprints, la validación y el video. | 8 | Pezo Castilla, Maria Jose | In-Process |
| TS08 | Informe final | T20 | Revisión final del informe | Revisar los seis capítulos, el registro de versiones, los analíticos de colaboración y los anexos. | 6 | Pezo Castilla, Maria Jose | To-do |

#### 5.2.4.4. Development Evidence for Sprint Review

Las tablas muestran los commits sin merge entre el 2026-11-16 y el 2026-11-26. Los commits de la reestructuración del capítulo 5 que se hagan después de este archivo se reflejarán en el release siguiente del informe.

**trazza-webapp**

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | 1d7471d | test(execution): add trip status value object spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | 98bd03a | test(execution): add deviation alert entity spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | 982b7ec | test(execution): add incident entity spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | ee1898b | test(execution): add report incident command spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | bf58429 | test(execution): extend trip entity spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | 8c2cf29 | test(shared): add collections spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | efef248 | test(shared): add feedback service spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | 356c7ae | test(execution): add execution api spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | f74484e | test(execution): add execution store spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | 5f46949 | test(execution): add execution routes spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | 5c5d435 | test(execution): add trip list spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | ec5e155 | test(execution): add iot device list spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | a21e1f2 | test(execution): add incident panel spec | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | a3f5eeb | docs(execution): add bounded context documentation | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | 1e7ac96 | docs(execution): add tracking sequence diagram | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | a6910d1 | docs(adrs): add adr 014 trip tracking polling | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/service-execution-monitoring | c8db102 | docs(changelog): add unreleased execution tests and docs | - | 2026-11-26 |

**trazza-report**

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/5-product-implementation-validation-deployment | 42291c2 | docs(chapter 5): update software configuration management | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/5-product-implementation-validation-deployment | 6818287 | docs(chapter 5): restructure landing page services and applications implementation | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/5-product-implementation-validation-deployment | fa95ca5 | docs(chapter 5): add sprint 1 | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/5-product-implementation-validation-deployment | bd15b1d | docs(chapter 5): add sprint 2 | - | 2026-11-26 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/5-product-implementation-validation-deployment | 44125cb | docs(chapter 5): add sprint 3 | - | 2026-11-26 |

**trazza-website**

Sin commits al 2026-11-26.

**trazza-webservice**

Sin commits al 2026-11-26.

#### 5.2.4.5. Execution Evidence for Sprint Review

Al 2026-11-26 se agregaron pruebas unitarias a la Web Application y documentación del bounded context Service Execution & Monitoring (`docs/execution-bounded-context.md`, `docs/execution-sequence.puml` y el ADR-014 en `docs/adrs.md`). `npm test` ejecuta **94 pruebas en 18 archivos** y todas pasan.

| Archivo de prueba | Pruebas |
| :--- | :---: |
| src/app/app.spec.ts | 1 |
| src/app/billing/domain/model/plan.entity.spec.ts | 2 |
| src/app/execution/application/execution.store.spec.ts | 10 |
| src/app/execution/domain/commands/report-incident.command.spec.ts | 4 |
| src/app/execution/domain/model/deviation-alert.entity.spec.ts | 3 |
| src/app/execution/domain/model/incident.entity.spec.ts | 4 |
| src/app/execution/domain/model/trip-status.value-object.spec.ts | 3 |
| src/app/execution/domain/model/trip.entity.spec.ts | 9 |
| src/app/execution/infrastructure/execution-api.spec.ts | 12 |
| src/app/execution/presentation/components/incident-panel/incident-panel.spec.ts | 5 |
| src/app/execution/presentation/execution.routes.spec.ts | 5 |
| src/app/execution/presentation/views/iot-device-list/iot-device-list.spec.ts | 4 |
| src/app/execution/presentation/views/trip-list/trip-list.spec.ts | 6 |
| src/app/iam/domain/model/value-objects.spec.ts | 3 |
| src/app/reputation/domain/model/reputation.spec.ts | 2 |
| src/app/shared/application/collections.spec.ts | 7 |
| src/app/shared/domain/model/money.value-object.spec.ts | 4 |
| src/app/shared/presentation/services/feedback.service.spec.ts | 10 |

| Evidencia | Archivo esperado | Estado |
| :--- | :--- | :--- |
| Resultado de `npm test` de la Web Application | chapter5/sprint4-webapp-tests.png | Pendiente |
| Resultado de `./mvnw test` de los Web Services | chapter5/sprint4-webservice-tests.png | Pendiente |

**Video de navegación del Sprint 4:** Pendiente.

#### 5.2.4.6. Services Documentation Evidence for Sprint Review

En el Sprint 4 el contrato de los Web Services no cambia: sigue documentado con las 74 operaciones descritas en la sección 5.2.3.6. La Technical Story TS02 agregará pruebas de integración de los controladores y escenarios de aceptación, cuyos resultados se registrarán aquí. La URL de la documentación desplegada se registrará cuando se confirme el despliegue (TS07).

#### 5.2.4.7. Software Deployment Evidence for Sprint Review

La Technical Story TS07 reúne el despliegue final de los tres productos. Al 2026-11-26 los dominios de AWS Amplify del Landing Page y de la Web Application no resuelven en DNS, por lo que ambos se deben volver a publicar, y la plataforma y la URL de los Web Services están por confirmar.

| Software Component | Deployment Platform | Repository / Branch | Version | URL publicada | Estado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Landing Page | AWS Amplify | trazza-website / main | Pendiente | Pendiente | Pendiente (TS07) |
| Frontend Web Application | AWS Amplify | trazza-webapp / main | Pendiente | Pendiente | Pendiente (TS07) |
| Web Services (RESTful API) | Por confirmar | trazza-webservice / main | Pendiente | Pendiente | Pendiente (TS07) |

#### 5.2.4.8. Team Collaboration Insights during Sprint

La siguiente tabla cuenta los commits sin merge entre el 2026-11-16 y el 2026-11-26. Se actualizará al cierre del Sprint.

| Integrante | GitHub Username | trazza-report | trazza-website | trazza-webapp | trazza-webservice | Total |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| Checalla Apaza, Emanuel Renato | Emanuelca135 | 0 | 0 | 0 | 0 | 0 |
| Lozano Quispe, Fabricio Jofred | FabricioZz15 | 0 | 0 | 0 | 0 | 0 |
| Peñaranda Caldas, Gabriel Augusto | gapc2124 | 0 | 0 | 0 | 0 | 0 |
| Pezo Castilla, Maria Jose | MariaJosePezo | 5 | 0 | 17 | 0 | 22 |
| Vite Celis, Rodrigo Matias | rodriznnn | 0 | 0 | 0 | 0 | 0 |
| **Total** |  | **5** | **0** | **17** | **0** | **22** |

<div align="center">
  <img src="../assets/images/chapter5/sprint4-insights-webservice-contributors.png" alt="GitHub Insights, contribuidores de trazza-webservice durante el Sprint 4" width="800">
  <br><br>
  <img src="../assets/images/chapter5/sprint4-insights-webapp-contributors.png" alt="GitHub Insights, contribuidores de trazza-webapp durante el Sprint 4" width="800">
  <br><br>
  <img src="../assets/images/chapter5/sprint4-insights-webapp-network.png" alt="GitHub Insights, grafo de ramas de trazza-webapp durante el Sprint 4" width="800">
  <br><br>
  <img src="../assets/images/chapter5/sprint4-insights-website-contributors.png" alt="GitHub Insights, contribuidores de trazza-website durante el Sprint 4" width="800">
  <br><br>
  <img src="../assets/images/chapter5/sprint4-insights-report-contributors.png" alt="GitHub Insights, contribuidores de trazza-report durante el Sprint 4" width="800">
</div>
