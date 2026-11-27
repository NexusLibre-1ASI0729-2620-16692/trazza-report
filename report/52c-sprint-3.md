### 5.2.3. Sprint 3

En esta sección se registra el avance en producto y en trabajo colaborativo del Sprint 3, cuyo alcance fue la primera versión de los Web Services de Trazza con Spring Boot y su integración con la Frontend Web Application.

#### 5.2.3.1. Sprint Planning 3

En el Sprint 3 se implementaron los Web Services RESTful con persistencia en MySQL, validaciones y reglas de negocio en el servidor, y se reemplazó el Fake API de la Web Application por la integración con ese API. La planificación consideró 14 User Stories, entre ellas las cinco historias técnicas del RESTful API, con 88 Story Points.

| Sprint # | Sprint 3 |
| :--- | :--- |
| **Sprint Planning Background** | |
| Date | 2026-10-30 (fecha del primer commit del backend; por confirmar) |
| Time | Por confirmar por el equipo |
| Location | Por confirmar por el equipo |
| Prepared By | Por confirmar por el equipo |
| Attendees (to planning meeting) | Por confirmar por el equipo |
| Sprint 2 Review Summary | En el Sprint 2 se publicó el Landing Page v1.0.0 y la primera versión de la Web Application (v1.0.0 del 2026-10-06 en el CHANGELOG y etiqueta v1.1.0 del 2026-10-08), con los cinco bounded contexts navegables sobre un Fake API. |
| Sprint 2 Retrospective Summary | Pendiente: el equipo debe registrar las opiniones de la retrospectiva. |
| **Sprint Goal & User Stories** | |
| Sprint 3 Goal | **Nuestro enfoque está en** reemplazar el Fake API por los Web Services RESTful de Trazza (Spring Boot y MySQL) con los cinco bounded contexts, autenticación con tokens JWT y documentación OpenAPI, e integrarlos con la Web Application. **Creemos que esto entrega** a transportistas y comerciantes MYPE datos persistentes y reglas de negocio confiables (emparejamiento, seguimiento GPS con alerta de desvío mayor a 2 km, liquidación y calificaciones), y al equipo un contrato REST documentado para seguir construyendo. **Esto se confirmará cuando** los **74 endpoints** de los 16 controladores estén documentados y probables en Swagger UI, las **14 historias (88 SP)**, incluidas las 5 técnicas, pasen sus criterios de aceptación, la Web Application v1.2.0 consuma el API en el 100 % de sus flujos sin usar json-server, y el release v1.0.0 de los Web Services (con su hotfix v1.0.1) esté etiquetado en GitHub. |
| Sprint 3 Velocity | 88 Story Points |
| Sum of Story Points | 88 Story Points (US06: 5, US07: 5, US14: 5, US18: 5, US22: 5, US15: 8, US16: 5, US17: 5, US26: 8, US27: 5, US28: 8, US29: 8, US30: 8, US31: 8) |

**Resultado del Sprint.** Al cierre del Sprint los Web Services exponen 74 operaciones REST en 61 rutas y 16 controladores, documentadas con OpenAPI, y la Web Application v1.2.0 los consume. Los Web Services tienen 5 archivos de prueba y el release v1.0.0 y el hotfix v1.0.1 están etiquetados (2026-11-14).

#### 5.2.3.2. Aspect Leaders and Collaborators

En el Sprint 3 cada integrante lideró los servicios del bounded context en el que concentró sus commits y colaboró en los demás. Los aspectos de IAM, Matchmaking, configuración e integración los lideró el mismo integrante porque concentra esos commits en el historial.

| Team Member (Last Name, First Name) | GitHub Username | Shared Kernel y configuración (L/C) | IAM & Profiles (L/C) | Matchmaking & Routing (L/C) | Service Execution & Monitoring (L/C) | Payment & Billing (L/C) | Loyalty & Reputation (L/C) | Integración con la Web Application (L/C) |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Checalla Apaza, Emanuel Renato | Emanuelca135 | C | C | C | C | C | C | C |
| Lozano Quispe, Fabricio Jofred | FabricioZz15 | C | C | C | C | L | C | C |
| Peñaranda Caldas, Gabriel Augusto | gapc2124 | L | L | L | C | C | C | L |
| Pezo Castilla, Maria Jose | MariaJosePezo | C | C | C | L | C | C | C |
| Vite Celis, Rodrigo Matias | rodriznnn | C | C | C | C | C | L | C |

#### 5.2.3.3. Sprint Backlog 3

El Sprint Backlog 3 contiene las cinco historias técnicas del RESTful API, las historias funcionales que dependen del API y las tareas transversales de configuración, seguridad, documentación e integración. Al cierre del Sprint, 25 tareas: 22 en **Done**, 0 en **In-Process**, 3 en **To-Review** y 0 en **To-do**. Las historias US26, US28 y US29 están en **To-Review** porque su implementación existe en el código pero el equipo aún debe confirmar que cumplen sus criterios de aceptación.

**URL público del Board:** [https://trazza.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog](https://trazza.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog)

| Sprint # | Sprint 3 | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **User Story** | | **Work-Item / Task** | | | | | |
| **Id** | **Title** | **Id** | **Title** | **Description** | **Estimation (Hours)** | **Assigned To** | **Status (To-do / In-Process / To-Review / Done)** |
| US06 | Autenticación de Usuarios vía API (RESTful API) | T01 | Authentication REST API | Implementar el registro e inicio de sesión, la emisión de tokens de acceso y de refresco y la autorización por rol. | 8 | Peñaranda Caldas, Gabriel Augusto | Done |
| US07 | Registro de Usuarios vía API (RESTful API) | T02 | Registro de usuarios con contraseña cifrada | Implementar el registro de usuarios, sus perfiles y el cifrado de las contraseñas antes de almacenarlas. | 6 | Peñaranda Caldas, Gabriel Augusto | Done |
| US14 | Consulta de Rutas Disponibles vía API (RESTful API) | T03 | Consulta de rutas disponibles | Implementar el API de rutas de retorno y solicitudes de envío con filtros por origen y destino. | 6 | Peñaranda Caldas, Gabriel Augusto | Done |
| US18 | Registro de Ubicación GPS vía API (RESTful API) | T04 | Registro de ubicación GPS | Implementar el registro de puntos de seguimiento del viaje desde el teléfono o un dispositivo IoT. | 6 | Pezo Castilla, Maria Jose | Done |
| US22 | Registro de Calificaciones vía API (RESTful API) | T05 | Registro de calificaciones y promedio | Implementar el API de calificaciones y el recálculo del promedio del perfil calificado. | 6 | Vite Celis, Rodrigo Matias | Done |
| US15 | Visualización de Ubicación en Vivo | T06 | Seguimiento en vivo del viaje | Exponer los puntos de seguimiento del viaje y consumirlos en el mapa de la Web Application. | 6 | Pezo Castilla, Maria Jose | Done |
| US16 | Confirmación de Recojo de Mercadería | T07 | Confirmación de recojo | Implementar la acción de recojo y su registro en el historial de estados del viaje. | 4 | Pezo Castilla, Maria Jose | Done |
| US17 | Confirmación de Entrega | T08 | Confirmación de entrega | Implementar la acción de entrega y la apertura de la liquidación del flete. | 4 | Pezo Castilla, Maria Jose | Done |
| US30 | Alerta de Desvío en Ruta | T09 | Alerta de desvío en ruta | Generar una alerta cuando un punto de seguimiento se aleja más de 2 km de la ruta, y permitir reconocerla. | 6 | Pezo Castilla, Maria Jose | Done |
| US26 | Validación de Identidad (KYC) | T10 | Validación de identidad por DNI | Validar el DNI del transportista durante el registro y proteger sus datos personales. | 8 | Checalla Apaza, Emanuel Renato | To-Review |
| US27 | Cancelación Temprana de Solicitud | T11 | Cancelación antes del recojo | Implementar la cancelación del viaje antes del recojo con su motivo. | 5 | Peñaranda Caldas, Gabriel Augusto | Done |
| US28 | Gestión de Compensación (Lucro Cesante) | T12 | Compensación por lucro cesante | Implementar la compensación al transportista cuando el comerciante cancela con el viaje ya en curso. | 6 | Lozano Quispe, Fabricio Jofred | To-Review |
| US29 | Mensajería Integrada (Chat) | T13 | Mensajería integrada en las propuestas | Implementar el chat entre el comerciante y el transportista emparejado. | 8 | Peñaranda Caldas, Gabriel Augusto | To-Review |
| US31 | Confirmación de Recepción y Pago | T14 | Liquidación de flete y confirmación de recepción | Implementar la liquidación del flete y la confirmación de recepción del comerciante. | 8 | Lozano Quispe, Fabricio Jofred | Done |
| — | Constraint | T15 | Proyecto base, DDD y configuración | Crear el proyecto Spring Boot con la estructura por bounded context (`domain`, `application`, `infrastructure`, `interfaces`) y el shared kernel. | 8 | Peñaranda Caldas, Gabriel Augusto | Done |
| — | Constraint | T16 | Persistencia en MySQL | Configurar el datasource y JPA, y los repositorios de cada bounded context. | 6 | Peñaranda Caldas, Gabriel Augusto | Done |
| — | Constraint | T17 | Seguridad y datos personales | Configurar la firma de tokens, CORS y el cifrado y el hash de los datos personales. | 8 | Peñaranda Caldas, Gabriel Augusto | Done |
| — | Constraint | T18 | Mensajes de error en inglés y español | Agregar los mensajes de cada código de error en `messages.properties` y `messages_es.properties`. | 4 | Peñaranda Caldas, Gabriel Augusto | Done |
| — | Constraint | T19 | Documentación OpenAPI | Agregar springdoc-openapi y documentar los controladores con Swagger UI. | 4 | Peñaranda Caldas, Gabriel Augusto | Done |
| — | Constraint | T20 | Planes y suscripciones | Implementar los endpoints de planes y de suscripciones. | 6 | Lozano Quispe, Fabricio Jofred | Done |
| — | Constraint | T21 | Dispositivos IoT | Implementar el préstamo y la consulta de dispositivos IoT del transportista. | 4 | Pezo Castilla, Maria Jose | Done |
| — | Constraint | T22 | Puntos de lealtad | Implementar los endpoints de lealtad y el uso de puntos al confirmar un viaje. | 4 | Vite Celis, Rodrigo Matias | Done |
| — | Constraint | T23 | Integración de IAM y Matchmaking en la Web Application | Reemplazar el Fake API por el cliente HTTP de los Web Services en IAM y Matchmaking. | 8 | Peñaranda Caldas, Gabriel Augusto | Done |
| — | Constraint | T24 | Integración de Execution, Billing y Reputation | Reemplazar el Fake API en los contextos restantes y agregar mapas, sondeo y mensajes de error traducidos. | 8 | Peñaranda Caldas, Gabriel Augusto | Done |
| — | Constraint | T25 | Release v1.0.0 y hotfix v1.0.1 | Etiquetar el release de los Web Services y publicar el hotfix v1.0.1. | 4 | Peñaranda Caldas, Gabriel Augusto | Done |

#### 5.2.3.4. Development Evidence for Sprint Review

En el Sprint 3 se implementaron los Web Services con una arquitectura DDD por bounded context y se integró la Web Application con ellos. Las tablas muestran los commits sin merge entre el 2026-10-30 y el 2026-11-15: 287 de `trazza-webservice`, 74 de `trazza-webapp` y 3 de `trazza-report`. `trazza-website` no tuvo commits en este Sprint.

**trazza-webservice**

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | HEAD | e41076f | first commit | - | 2026-10-30 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | fa5efe5 | build: add project dependencies | - | 2026-10-30 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 04a12cd | chore: add base class | - | 2026-10-30 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 6586e41 | chore: add test base class | - | 2026-10-30 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | e3e0dfc | feat(shared): add CommandErrorKind | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | d4b45cd | feat(shared): add CommandError | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 74702ef | feat(shared): add Result | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | e2ed559 | feat(shared): add EnumText | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | b07cb2f | feat(shared): add GeoLocation | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 71e750b | feat(shared): add Money | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 1f18884 | feat(shared): add PhoneNumber | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | eedd9e3 | feat(shared): add PublicIds | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 5416c7d | feat(shared): add AuditableEntity | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 4714727 | feat(shared): add RowLocks | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | b67423b | feat(shared): add GeoLocationConverter | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | e819f06 | feat(shared): add PublicIdConverter | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 796fd8f | feat(shared): add Transactions | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 8cab0ed | build: add springdoc openapi dependency | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | f5e7d5b | feat(shared): add OpenApiConfiguration | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 8fd0c03 | feat(execution): add TripStatus value object | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 4932d8a | feat(execution): add IncidentType value object | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 77ad4bc | feat(execution): add IncidentStatus value object | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 1915926 | feat(execution): add TrackingSource value object | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 0b60c3d | feat(execution): add IotDeviceStatus value object | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | cd3ae49 | feat(execution): add TripStatusChange entity | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 3898770 | feat(execution): add IncidentEvidence entity | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 46c4868 | feat(execution): add Trip aggregate | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 6d42155 | feat(execution): add TrackingPoint aggregate | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | d282629 | feat(execution): add DeviationAlert aggregate | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | dde91ea | feat(execution): add Incident aggregate | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 6112bbf | feat(execution): add IotDevice aggregate | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 4d74e83 | feat(execution): add AssignDriverCommand command | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | b9353d8 | feat(execution): add PickUpTripCommand command | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | c04e681 | feat(execution): add DeliverTripCommand command | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 0ccaab0 | feat(execution): add ConfirmTripCommand command | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | c3221b1 | feat(execution): add CancelTripCommand command | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 0aa5a45 | feat(execution): add RecordTrackingPointCommand command | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | e1d6007 | feat(execution): add AcknowledgeDeviationAlertCommand command | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 2009546 | feat(execution): add ReportIncidentCommand command | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | c8db176 | feat(execution): add AddIncidentEvidenceCommand command | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 6657fd6 | feat(execution): add ResolveIncidentCommand command | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 1c1f8b2 | feat(execution): add TripView read model | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 5ac7db5 | feat(execution): add IotDeviceView read model | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | b51ce09 | feat(execution): add TrackingResult read model | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | af197ec | feat(execution): add TripCommandService domain service | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 37a7c7f | feat(execution): add TrackingCommandService domain service | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 358cb9a | feat(execution): add IncidentCommandService domain service | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | e85f8f1 | feat(execution): add ExecutionQueryService domain service | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | e40715b | feat(execution): add TripRepository repository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | f89a914 | feat(execution): add TrackingPointRepository repository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 78664cf | feat(execution): add DeviationAlertRepository repository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 6558c8e | feat(execution): add IncidentRepository repository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | a7fcd0c | feat(execution): add IotDeviceRepository repository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | bf9f139 | feat(execution): add TripSnapshot ACL snapshot | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | d9e9180 | feat(execution): add ExecutionContextFacade ACL facade | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 4121457 | feat(execution): add TripAccess application record | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 7b2ff25 | feat(execution): add TripAccessService application service | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | e8f4443 | feat(execution): add TripCommandServiceImpl command service | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 8bafae1 | feat(execution): add TrackingCommandServiceImpl command service | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | e13df23 | feat(execution): add IncidentCommandServiceImpl command service | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 1f9739c | feat(execution): add ExecutionQueryServiceImpl query service | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | d1ea340 | chore: configure messages and cors in application.yaml | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 59fec45 | feat(shared): add WebConfiguration | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | f245849 | feat(execution): add ExecutionContextFacadeImpl ACL facade implementation | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | f205d63 | feat(shared): add ProblemDetailsAssembler | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 145d57c | feat(execution): add TripPlaceResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | e1468d3 | feat(execution): add TripPartyResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 9e9e675 | feat(execution): add TripVehicleResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 15329a8 | feat(execution): add TripResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | fcf32a2 | feat(shared): add GlobalExceptionHandler | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 903e229 | feat(execution): add TripStatusChangeResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | c20bf74 | feat(execution): add AssignDriverResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 1d06f6a | feat(execution): add CancelTripResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | c2a2777 | feat(execution): add RecordTrackingPointResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 61287a5 | feat(execution): add TrackingPointResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | 7da9460 | feat(shared): add RestResults | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 5e5cdb6 | feat(execution): add DeviationAlertResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | efa83c5 | feat(i18n): add messages.properties | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 20cc249 | feat(execution): add TrackingResultResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 000e276 | feat(execution): add ReportIncidentResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 0fd8ae3 | feat(execution): add AddIncidentEvidenceResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | afe7c57 | feat(i18n): add messages_es.properties | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 4a1fb6b | feat(execution): add ResolveIncidentResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | d1fc035 | feat(execution): add IncidentEvidenceResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | e8b1bac | feat(execution): add IncidentResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | c5bc65a | test(shared): add GeoLocationTest | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 9338bff | feat(execution): add IotDeviceResource resource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 99e7236 | feat(execution): add ExecutionResourceAssembler assembler | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/shared | c532e3a | test(shared): add PublicIdConverterTest | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 244dac9 | feat(execution): add TripsController controller | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 62ae460 | feat(execution): add IotDevicesController controller | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/service-execution-monitoring | 762095e | test(execution): add TripTest | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 2be1c40 | feat(reputation): add LoyaltyReason value object | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | f8b47a3 | feat(reputation): add Rating aggregate | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | ff98d90 | feat(reputation): add LoyaltyPointEntry aggregate | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 75bf70b | feat(reputation): add RateTripCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | f5c8618 | feat(reputation): add RedeemPointsCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 4852109 | feat(reputation): add RatingView read model | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | bd71d23 | feat(reputation): add ReputationSummary read model | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 0f533a8 | feat(matchmaking): add MatchProposalStatus | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 82d3574 | feat(reputation): add LoyaltyAccount read model | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | a417c0b | feat(matchmaking): add ReturnRouteStatus | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | db67e83 | feat(matchmaking): add ShipmentRequestStatus | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 57668a1 | feat(matchmaking): add AcceptMatchProposalCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | c805904 | feat(matchmaking): add CancelMatchProposalCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | d4fa6a1 | feat(matchmaking): add CancelReturnRouteCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | c2ec7c8 | feat(matchmaking): add CancelShipmentRequestCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 82dc044 | feat(matchmaking): add CreateMatchProposalCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | d847636 | feat(matchmaking): add PlaceData | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 93b7c60 | feat(reputation): add ReputationCommandService | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 9368b19 | feat(matchmaking): add CreateReturnRouteCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 75cc290 | feat(matchmaking): add CreateShipmentRequestCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 8b39394 | feat(reputation): add ReputationQueryService | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 26049cb | feat(matchmaking): add RejectMatchProposalCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 797159b | feat(matchmaking): add SendMessageCommand | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 160c8c2 | feat(matchmaking): add MatchProposal | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 1a587ab | feat(reputation): add RatingRepository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 35afe50 | feat(matchmaking): add Message | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 3f71901 | feat(matchmaking): add ReturnRoute | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 3fc8e00 | feat(matchmaking): add ShipmentRequest | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 494da03 | feat(matchmaking): add ReturnRouteView | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 53fb26e | feat(matchmaking): add ShipmentRequestView | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | fdadfc0 | feat(matchmaking): add MessageView | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 60716ba | feat(reputation): add LoyaltyPointEntryRepository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 420071d | feat(matchmaking): add MatchProposalView | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 7c76cba | feat(matchmaking): add MatchProposalCommandService | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 9cd408f | feat(matchmaking): add ReturnRouteCommandService | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | cce6992 | feat(matchmaking): add ShipmentRequestCommandService | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | f4a2d91 | feat(matchmaking): add MatchmakingQueryService | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | b47a26f | feat(reputation): add RatingViewBuilder | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 91a53ba | feat(matchmaking): add MatchProposalRepository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | c34d72e | feat(matchmaking): add MessageRepository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | c5b01ef | feat(reputation): add ReputationCommandServiceImpl | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | f74d875 | feat(matchmaking): add ReturnRouteRepository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 8d32b9a | feat(matchmaking): add ShipmentRequestRepository | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | ad4b34c | feat(matchmaking): add TripContextSnapshot | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | a1d238d | feat(matchmaking): add MatchmakingContextFacade | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 5abf3ad | feat(matchmaking): add Places | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 3237736 | feat(reputation): add ReputationQueryServiceImpl | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | c7e31ae | feat(matchmaking): add MatchingRules | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 805d0d4 | feat(reputation): add ReputationContextFacade | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | b66bcc6 | feat(matchmaking): add MatchmakingContextFacadeImpl | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 16f9b80 | feat(reputation): add ReputationContextFacadeImpl | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | e77b4dc | feat(matchmaking): add CancelWithReasonResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | c6c8f6b | feat(reputation): add RateTripResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | e4fec7e | feat(reputation): add RedeemPointsResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | fdbc75f | feat(matchmaking): add CreateMatchProposalResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | d84cba5 | feat(matchmaking): add MessageResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 7e10c6d | feat(matchmaking): add PartyResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 98af764 | feat(matchmaking): add PlaceResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 5299467 | feat(matchmaking): add RouteVehicleResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | e63abb0 | feat(matchmaking): add SendMessageResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 70e0d08 | feat(matchmaking): add CreateReturnRouteResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 62e3c00 | feat(matchmaking): add CreateShipmentRequestResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 68fd123 | feat(matchmaking): add ReturnRouteResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 4ba3f48 | feat(matchmaking): add ShipmentRequestResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 08c7230 | feat(matchmaking): add MatchProposalResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | da0a7fa | feat(matchmaking): add MatchmakingResourceAssembler | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 8eaeade | feat(reputation): add RatingResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 1b58017 | feat(reputation): add ReputationSummaryResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 448e49c | feat(reputation): add LoyaltyEntryResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 86f47a3 | feat(reputation): add LoyaltyAccountResource | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | b8abad7 | feat(reputation): add ReputationResourceAssembler | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 014a9b0 | feat(reputation): add RatingsController | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/loyalty-reputation | 1e7cdef | feat(reputation): add LoyaltyController | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 836d57b | feat(billing): add BillingPeriod value object | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 70830b1 | feat(billing): add PricingUnit value object | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | ab3c06e | feat(billing): add MonitoringType value object | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 0a19f10 | feat(billing): add SubscriptionStatus value object | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 58239e0 | feat(billing): add PaymentStatus value object | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 9ee52a1 | feat(billing): add SettlementStatus value object | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 5a31a94 | feat(billing): add CompensationStatus value object | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 5ff7af4 | feat(billing): add CompensationAction value object | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | ac5c4b8 | feat(billing): add SubscriptionVehicle entity | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 286238e | feat(billing): add Plan aggregate | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 927abb8 | feat(billing): add SubscriptionPayment aggregate | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 9a93a9b | feat(billing): add Subscription aggregate | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 5013978 | feat(billing): add FreightSettlement aggregate | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 68855aa | feat(billing): add CancellationCompensation aggregate | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | c091189 | feat(matchmaking): add MatchmakingViewBuilder | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 9931231 | feat(matchmaking): add MatchProposalCommandServiceImpl | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 3055304 | feat(matchmaking): add ReturnRouteCommandServiceImpl | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | b4fb26b | feat(matchmaking): add ShipmentRequestCommandServiceImpl | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | cfb2ac0 | feat(matchmaking): add MatchmakingQueryServiceImpl | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 8ac44e4 | feat(matchmaking): add MatchProposalsController | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 9095a38 | feat(matchmaking): add ReturnRoutesController | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/matchmaking-routing | 2ef1355 | feat(matchmaking): add ShipmentRequestsController | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | c39676e | feat(billing): add SubscribeCommand | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 019c7c8 | feat(billing): add RenewSubscriptionCommand | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 327b349 | feat(billing): add CancelSubscriptionCommand | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 3b9e101 | feat(billing): add MarkFreightPaidCommand | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 07764be | feat(billing): add ConfirmFreightReceivedCommand | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | de930bb | feat(billing): add UpdateCompensationCommand | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 31abfad | feat(billing): add SubscribedVehicle read model | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | b433478 | feat(billing): add SubscriptionView read model | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 1823ddd | feat(billing): add FreightSettlementView read model | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | a71a824 | feat(billing): add CompensationView read model | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 05ce21c | feat(billing): add SubscriptionCommandService | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | f1bb8de | feat(billing): add SettlementCommandService | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | be0699f | feat(billing): add BillingQueryService | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 14c6c74 | feat(billing): add PlanRepository | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 59c4a30 | feat(billing): add SubscriptionRepository | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | acd0c03 | feat(billing): add SubscriptionPaymentRepository | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | e9b06db | feat(billing): add FreightSettlementRepository | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | c2e07c4 | feat(billing): add CancellationCompensationRepository | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | c7210bd | feat(billing): add BillingContextFacade | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 16b152d | feat(billing): add SubscriptionViewBuilder | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | cbd6810 | feat(billing): add SubscriptionCommandServiceImpl | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 3fb6190 | feat(billing): add SettlementCommandServiceImpl | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 7a40f3f | feat(billing): add BillingQueryServiceImpl | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 1444bc6 | feat(billing): add BillingContextFacadeImpl | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | aaf7704 | feat(billing): add PlanResource | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 36cbe0c | feat(billing): add SubscribedVehicleResource | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 89aade6 | feat(billing): add SubscriptionPaymentResource | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | cafe240 | feat(billing): add SubscriptionResource | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | b7c316f | feat(billing): add BillingTripResource | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | a910692 | feat(billing): add FreightSettlementResource | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 9de3bc3 | feat(billing): add MarkFreightPaidResource | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 9804729 | feat(billing): add CancellationCompensationResource | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 78f6b9a | feat(billing): add BillingResourceAssembler | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 54f3c6d | feat(billing): add PlansController | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | e6e8320 | feat(billing): add SubscriptionsController | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | bc0ef82 | feat(billing): add FreightSettlementsController | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 7e0a616 | feat(iam): implement Fleet and User services in Java | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 683c11c | feat(billing): add CancellationCompensationsController | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | bb8229a | test(billing): add BillingDomainTest | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | 0f3eeca | feat(billing): add SubscribeResource | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 994a414 | feat(iam): implement Fleet and User services in Java | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/payment-billing | d798503 | refactor(billing): rename package to trazzawebservice | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 4b6ed84 | git commit -m "feat(iam): port domain aggregates from C# to Java" -m "- Add Driver and Vehicle aggregates for fleet management. - Add SavedAddress record. - Add IdentityVerification aggregate for KYC process. - Add PersonIdentity aggregate with encrypted fields. - Add CarrierProfile and MerchantProfile aggregates. - Add RefreshToken aggregate for session management. - Add User and UserRole aggregates as account root. - Adapt C# types to Java idioms (Long, BigDecimal, LocalDateTime, UUID, byte[]). - Implement encapsulation with private fields and public getters." | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 893065e | feat(iam): implement domain model and commands for identity and fleet management | - Add Value Objects for DNI, RUC, Email and License Plate validation. - Add Enums and role constants for users, drivers and KYC statuses. - Implement immutable command records for sign up, authentication and fleet operations. - Add domain aggregates for users, profiles, vehicles, drivers and identity verification. | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 33ecb2e | feat(iam): add domain service interfaces and DTOs | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 5372235 | feat(iam): implement bcrypt hashing service | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 8507881 | feat(iam): implement JPA repositories for IAM module | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 4209277 | feat(iam): implement request authorization middleware and pipeline | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 041fc87 | feat(iam): implement personal data protection and simulated RENIEC provider | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 138b398 | feat(iam): implement personal data protection and simulated RENIEC provider | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | c8417c1 | feat(iam): implement anti-corruption layer facade | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | b6dd2b4 | feat(iam): add REST controllers for authentication and fleet management | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 4b56d85 | feat(iam): add REST controllers for authentication and fleet management | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-profiles | 4f11e8b | feat(iam): add REST controllers for authentication and fleet management | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 3a92ba3 | build: add jwt and security crypto dependencies | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 18ca49c | feat(iam): add value objects | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 795dfaa | feat(iam): add value objects | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 622c538 | feat(iam): add value objects | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 7298a0d | feat(iam): add aggregates | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 6f6ad7b | feat(iam): add aggregates | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 2540641 | feat(iam): add aggregates | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | fae013d | feat(iam): add aggregates | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 9a1e009 | feat(iam): add commands | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | c78cf3d | feat(iam): add commands | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 3d22691 | feat(iam): add commands | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | d346112 | feat(iam): add commands | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | f49c7d2 | feat(iam): add commands | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | e7bd4cd | feat(iam): add commands | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 507db09 | feat(iam): add commands | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 16577d3 | feat(iam): add domain services | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | c6c7e10 | feat(iam): add domain services | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | e692c5a | feat(iam): add repositories | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | ee79124 | feat(iam): add repositories | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | b1b5d16 | feat(iam): add repositories | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 9e97eda | feat(iam): add hashing and token services | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | cb53d02 | feat(iam): add outbound services | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 270ba1f | feat(iam): add outbound services | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 1e8d70d | feat(iam): add security services | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | d8ecc64 | feat(iam): add application services | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 77a3aee | feat(iam): add acl facade | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 0f1ac1f | feat(iam): add acl facade | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | a0c6a5b | feat(iam): add application services | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | e663f2c | feat(iam): add authorization | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 01079b1 | feat(iam): add authorization | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 4533944 | feat(iam): add authorization | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 3f0fd75 | feat(iam): add rest resources | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 9699c2c | feat(iam): add rest resources | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 59ed475 | feat(iam): add rest resources | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | daeed88 | feat(iam): add rest resources | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 666c924 | feat(iam): add rest resources | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | cb2c9c0 | feat(iam): add rest resources | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 14b21c6 | feat(iam): add rest resources | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | ebfc9b4 | feat(iam): add rest resources | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | c2ecad6 | feat(iam): add rest controllers | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 4914dcb | feat(iam): add rest controllers | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 4703d7b | feat(iam): configure token and personal data settings | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | feature/iam-core | 77cb53b | feat(config): add datasource and jpa settings | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | HEAD | 39bd2bf | chore(release): 1.0.0 | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | hotfix/1.0.1 | 1b3832b | fix(iam): use jackson 3 object mapper | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webservice | hotfix/1.0.1 | 1c49bd3 | chore(release): 1.0.1 | - | 2026-11-14 |

**trazza-webapp**

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 55555f5 | refactor(matchmaking): update matchmaking module | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | d409a01 | feat(shared): add api error | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | ec464a4 | feat(shared): add api error | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | d343b0f | feat(shared): add place value object | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | f4647bd | feat(shared): add place value object | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 5c57276 | feat(shared): add formatDateTime and formatMoney | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | c0df479 | feat(shared): add formatDateTime and formatMoney | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 0b0b506 | feat(shared): add trazza date time pipe | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | ebe6509 | feat(shared): add trazza date time pipe | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 97958fb | feat(shared): add trazza money pipe | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | e952c52 | feat(shared): add trazza money pipe | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 4b50a7c | feat(shared): add polling | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | a86320b | feat(shared): add polling | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | bb031f7 | feat(shared): add star rating | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | 5c10939 | feat(shared): add star rating | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | b6f24b5 | feat(shared): add prompt dialog | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | f3e692d | feat(shared): add prompt dialog | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 8f7d52f | feat(shared): add prompt dialog template | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | 8d7e5b4 | feat(shared): add prompt dialog template | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 164e671 | build: add leaflet dependencies to package.json | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | 83bdf7b | build: add leaflet dependencies to package.json | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | bda1745 | build: update package-lock.json for leaflet | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | 00cff3f | build: update package-lock.json for leaflet | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 70c1a99 | build: register leaflet in angular.json | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | b1c2ee1 | build: register leaflet in angular.json | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 6360fa0 | feat(shared): add map picker | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | 2980304 | feat(shared): add map picker | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 6876804 | feat(shared): add route map | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | b51740d | feat(shared): add route map | - | 2026-11-12 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 1800374 | fix(matchmaking): add shared api support | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | ebac043 | feat(shared): add platform api, api error handling and feedback attempt | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | bf575df | feat(shared): add platform api, api error handling and feedback attempt | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 840cfef | refactor(execution): update execution module | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 523f7af | refactor(billing): update billing module | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 34dee85 | refactor(reputation): update reputation module | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 2f96647 | feat(shared): link billing plans, subscriptions and settlements in side menu | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | b512c9b | fix(shared): stop loading removed billing data in layout | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 535cee7 | feat(billing): protect billing routes with iam guard | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 661d0e6 | feat(i18n): add Spanish labels for billing | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 37c1948 | feat(i18n): add English labels for billing | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/loyalty-reputation | 50db0ef | feat(reputation): add loyalty points option to side menu | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/loyalty-reputation | 9b14288 | feat(reputation): add loyalty points menu translations | - | 2026-11-13 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 96824b3 | refactor(dashboard): adapt to new stores | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 5196598 | fix(layout): load matchmaking and execution data | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | c5c0e39 | feat(i18n): add matchmaking and execution labels | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | e64e60b | refactor(iam): update domain | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | a9bba3a | refactor(iam): update domain | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 424f032 | refactor(iam): update domain | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 56f2341 | refactor(iam): update domain | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 54e2cc1 | refactor(iam): update domain | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | f242acd | refactor(iam): update domain | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | cd8377b | refactor(iam): update infrastructure | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | dcdcccc | refactor(iam): update infrastructure | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 314fed7 | refactor(iam): update infrastructure | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 2d5e9ca | refactor(iam): update infrastructure | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 6c3f7d2 | refactor(iam): update stores | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | b0284e8 | refactor(iam): update dialogs | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 567a709 | refactor(iam): update dialogs | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 5e46175 | refactor(iam): update dialogs | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 1a70452 | refactor(iam): update views | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 00d2416 | refactor(iam): update views | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 418709f | refactor(iam): update views | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 867c966 | refactor(iam): update views | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | c266ffd | refactor(iam): update views | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | b96f94a | refactor(iam): update views | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 4a969ef | refactor(iam): update routes | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | deafffe | refactor(shared): update api base classes | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 72591b2 | chore(env): add authentication endpoint path | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | 621776a | fix(iam): use platform api and base url | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | b005c74 | fix(routes): use authentication guard | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | cae747c | fix(shared): align status tag and query params | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/iam-profiles | a072653 | fix(shared): update status severities | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | 510ec6d | chore(release): 1.2.0 | - | 2026-11-14 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | d2cccbe | chore(env): point api to new backend | - | 2026-11-14 |

**trazza-report**

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/52-sprint-3 | a2a0eba | docs(chapter 5): add sprint 3 merchant screenshots | - | 2026-11-15 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/52-sprint-3 | cc1a654 | docs(chapter 5): add sprint 3 trip and carrier screenshots | - | 2026-11-15 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/52-sprint-3 | f805251 | docs(chapter 5): add sprint 3, validation interviews and about-the-product video | - | 2026-11-15 |

#### 5.2.3.5. Execution Evidence for Sprint Review

Al cierre del Sprint 3 la Web Application v1.2.0 consume los Web Services en sus cinco bounded contexts. Frente al Sprint 2 incorpora mapas con Leaflet (`MapPicker` y `RouteMap`), la actualización periódica del viaje, puntos de lealtad, conductores y direcciones guardadas, suscripciones y liquidaciones, dispositivos IoT, el panel de incidencias y mensajes de error de la API traducidos al inglés y al español.

| Evidencia | Archivo esperado | Estado |
| :--- | :--- | :--- |
| Web Application consumiendo el API: inicio de sesión y dashboard | chapter5/sprint3-webapp-dashboard.png | Pendiente |
| Matchmaking: rutas de retorno, sugerencias y ofertas | chapter5/sprint3-webapp-matchmaking.png | Pendiente |
| Execution: detalle del viaje con mapa y alertas de desvío | chapter5/sprint3-webapp-trip-detail.png | Pendiente |
| Execution: panel de incidencias | chapter5/sprint3-webapp-incidents.png | Pendiente |
| Billing: plan, suscripción y liquidaciones | chapter5/sprint3-webapp-billing.png | Pendiente |
| Reputation: calificaciones y puntos de lealtad | chapter5/sprint3-webapp-reputation.png | Pendiente |

**Video de navegación del Sprint 3:** Pendiente (se enlaza cuando esté publicado en Microsoft Stream).

#### 5.2.3.6. Services Documentation Evidence for Sprint Review

Los Web Services de Trazza exponen su documentación con springdoc-openapi: la interfaz Swagger UI en `/swagger-ui.html` y el documento OpenAPI en `/v3/api-docs` (Trazza Platform API 1.0.0). En el Sprint 3 se documentaron 74 operaciones en 61 rutas, agrupadas en 16 controladores.

| Controlador (tag) | Operaciones |
| :--- | :---: |
| Authentication | 4 |
| Cancellation compensations | 4 |
| Drivers | 4 |
| Freight settlements | 3 |
| IoT devices | 1 |
| Loyalty | 2 |
| Match proposals | 8 |
| Plans | 1 |
| Ratings | 4 |
| Return routes | 5 |
| Saved addresses | 3 |
| Shipment requests | 5 |
| Subscriptions | 4 |
| Trips | 16 |
| Users | 6 |
| Vehicles | 4 |

La siguiente tabla indica, para cada endpoint, el verbo HTTP, la ruta, los parámetros, el cuerpo de la solicitud y la respuesta exitosa. Los parámetros de ruta se escriben entre llaves.

| Controlador | Verbo | Ruta | Parámetros | Request body | Response |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Authentication | POST | `/api/v1/authentication/refresh` | — | RefreshSessionResource | 200 |
| Authentication | POST | `/api/v1/authentication/sign-in` | — | SignInResource | 200 |
| Authentication | POST | `/api/v1/authentication/sign-out` | — | RefreshSessionResource | 200 |
| Authentication | POST | `/api/v1/authentication/sign-up` | — | SignUpResource | 200 |
| Cancellation compensations | GET | `/api/v1/cancellation-compensations` | — | — | 200 |
| Cancellation compensations | POST | `/api/v1/cancellation-compensations/{tripId}/confirm-paid` | tripId (path, required) | — | 200 |
| Cancellation compensations | POST | `/api/v1/cancellation-compensations/{tripId}/dispute` | tripId (path, required) | — | 200 |
| Cancellation compensations | POST | `/api/v1/cancellation-compensations/{tripId}/waive` | tripId (path, required) | — | 200 |
| Drivers | GET | `/api/v1/drivers` | — | — | 200 |
| Drivers | POST | `/api/v1/drivers` | — | SaveDriverResource | 200 |
| Drivers | PUT | `/api/v1/drivers/{driverId}` | driverId (path, required) | SaveDriverResource | 200 |
| Drivers | DELETE | `/api/v1/drivers/{driverId}` | driverId (path, required) | — | 200 |
| Freight settlements | GET | `/api/v1/freight-settlements` | — | — | 200 |
| Freight settlements | POST | `/api/v1/freight-settlements/{tripId}/confirm` | tripId (path, required) | — | 200 |
| Freight settlements | POST | `/api/v1/freight-settlements/{tripId}/mark-paid` | tripId (path, required) | MarkFreightPaidResource | 200 |
| IoT devices | GET | `/api/v1/iot-devices` | — | — | 200 |
| Loyalty | GET | `/api/v1/loyalty/points` | — | — | 200 |
| Loyalty | POST | `/api/v1/loyalty/redemptions` | — | RedeemPointsResource | 200 |
| Match proposals | GET | `/api/v1/match-proposals` | — | — | 200 |
| Match proposals | POST | `/api/v1/match-proposals` | — | CreateMatchProposalResource | 200 |
| Match proposals | GET | `/api/v1/match-proposals/{proposalId}` | proposalId (path, required) | — | 200 |
| Match proposals | POST | `/api/v1/match-proposals/{proposalId}/accept` | proposalId (path, required) | — | 200 |
| Match proposals | POST | `/api/v1/match-proposals/{proposalId}/cancel` | proposalId (path, required) | — | 200 |
| Match proposals | GET | `/api/v1/match-proposals/{proposalId}/messages` | proposalId (path, required) | — | 200 |
| Match proposals | POST | `/api/v1/match-proposals/{proposalId}/messages` | proposalId (path, required) | SendMessageResource | 200 |
| Match proposals | POST | `/api/v1/match-proposals/{proposalId}/reject` | proposalId (path, required) | — | 200 |
| Plans | GET | `/api/v1/plans` | — | — | 200 |
| Ratings | POST | `/api/v1/ratings` | — | RateTripResource | 200 |
| Ratings | GET | `/api/v1/ratings/given` | — | — | 200 |
| Ratings | GET | `/api/v1/ratings/received` | — | — | 200 |
| Ratings | GET | `/api/v1/ratings/summary/{userId}` | userId (path, required) | — | 200 |
| Return routes | GET | `/api/v1/return-routes` | — | — | 200 |
| Return routes | POST | `/api/v1/return-routes` | — | CreateReturnRouteResource | 200 |
| Return routes | GET | `/api/v1/return-routes/{routeId}` | routeId (path, required) | — | 200 |
| Return routes | POST | `/api/v1/return-routes/{routeId}/cancel` | routeId (path, required) | — | 200 |
| Return routes | GET | `/api/v1/return-routes/{routeId}/suggested-shipments` | routeId (path, required) | — | 200 |
| Saved addresses | GET | `/api/v1/saved-addresses` | — | — | 200 |
| Saved addresses | POST | `/api/v1/saved-addresses` | — | CreateSavedAddressResource | 200 |
| Saved addresses | DELETE | `/api/v1/saved-addresses/{savedAddressId}` | savedAddressId (path, required) | — | 200 |
| Shipment requests | GET | `/api/v1/shipment-requests` | — | — | 200 |
| Shipment requests | POST | `/api/v1/shipment-requests` | — | CreateShipmentRequestResource | 200 |
| Shipment requests | POST | `/api/v1/shipment-requests/{shipmentId}/cancel` | shipmentId (path, required) | CancelWithReasonResource | 200 |
| Shipment requests | GET | `/api/v1/shipment-requests/{shipmentId}/suggested-routes` | shipmentId (path, required) | — | 200 |
| Shipment requests | GET | `/api/v1/shipment-requests/open` | — | — | 200 |
| Subscriptions | GET | `/api/v1/subscriptions` | — | — | 200 |
| Subscriptions | POST | `/api/v1/subscriptions` | — | SubscribeResource | 200 |
| Subscriptions | POST | `/api/v1/subscriptions/{subscriptionId}/cancel` | subscriptionId (path, required) | — | 200 |
| Subscriptions | POST | `/api/v1/subscriptions/{subscriptionId}/renew` | subscriptionId (path, required) | — | 200 |
| Trips | GET | `/api/v1/trips` | — | — | 200 |
| Trips | GET | `/api/v1/trips/{tripId}` | tripId (path, required) | — | 200 |
| Trips | POST | `/api/v1/trips/{tripId}/cancel` | tripId (path, required) | CancelTripResource | 200 |
| Trips | POST | `/api/v1/trips/{tripId}/confirm` | tripId (path, required) | — | 200 |
| Trips | POST | `/api/v1/trips/{tripId}/deliver` | tripId (path, required) | — | 200 |
| Trips | GET | `/api/v1/trips/{tripId}/deviation-alerts` | tripId (path, required) | — | 200 |
| Trips | POST | `/api/v1/trips/{tripId}/deviation-alerts/{alertId}/acknowledge` | tripId (path, required), alertId (path, required) | — | 200 |
| Trips | PUT | `/api/v1/trips/{tripId}/driver` | tripId (path, required) | AssignDriverResource | 200 |
| Trips | GET | `/api/v1/trips/{tripId}/incidents` | tripId (path, required) | — | 200 |
| Trips | POST | `/api/v1/trips/{tripId}/incidents` | tripId (path, required) | ReportIncidentResource | 200 |
| Trips | POST | `/api/v1/trips/{tripId}/incidents/{incidentId}/evidences` | tripId (path, required), incidentId (path, required) | AddIncidentEvidenceResource | 200 |
| Trips | POST | `/api/v1/trips/{tripId}/incidents/{incidentId}/resolve` | tripId (path, required), incidentId (path, required) | ResolveIncidentResource | 200 |
| Trips | POST | `/api/v1/trips/{tripId}/pick-up` | tripId (path, required) | — | 200 |
| Trips | GET | `/api/v1/trips/{tripId}/status-history` | tripId (path, required) | — | 200 |
| Trips | GET | `/api/v1/trips/{tripId}/tracking-points` | tripId (path, required) | — | 200 |
| Trips | POST | `/api/v1/trips/{tripId}/tracking-points` | tripId (path, required) | RecordTrackingPointResource | 200 |
| Users | GET | `/api/v1/users/me` | — | — | 200 |
| Users | PUT | `/api/v1/users/me/identity` | — | UpdateIdentityResource | 200 |
| Users | GET | `/api/v1/users/me/identity-verifications` | — | — | 200 |
| Users | POST | `/api/v1/users/me/identity-verifications` | — | SubmitIdentityVerificationResource | 200 |
| Users | PUT | `/api/v1/users/me/merchant-profile` | — | UpdateMerchantProfileResource | 200 |
| Users | POST | `/api/v1/users/me/roles` | — | AddRoleResource | 200 |
| Vehicles | GET | `/api/v1/vehicles` | — | — | 200 |
| Vehicles | POST | `/api/v1/vehicles` | — | SaveVehicleResource | 200 |
| Vehicles | PUT | `/api/v1/vehicles/{vehicleId}` | vehicleId (path, required) | SaveVehicleResource | 200 |
| Vehicles | DELETE | `/api/v1/vehicles/{vehicleId}` | vehicleId (path, required) | — | 200 |

**Ejemplos de solicitud y respuesta.** Los cuerpos de solicitud se generan a partir de los esquemas del documento OpenAPI. Las 74 respuestas exitosas declaran en el documento solo el tipo `object`, sin sus campos; por eso la columna *Response* de la tabla muestra únicamente el código HTTP. Los ejemplos de respuesta usan datos de muestra con la estructura de los recursos que la Web Application v1.2.0 recibe del API (`TripResource`, `TrackingResultResource` e `IncidentResource`). Declarar los esquemas de respuesta en los controladores queda como mejora de la documentación para el Sprint 4.

**POST `/api/v1/trips/{tripId}/tracking-points`**

Request body (estructura del esquema OpenAPI; los valores indican el tipo de cada campo):

```json
{
  "latitude": 0,
  "longitude": 0,
  "speedKmh": 0,
  "source": "string",
  "recordedAt": "2026-11-14T10:00:00Z"
}
```

Response `200` con datos de muestra. El API devuelve el punto registrado, la alerta de desvío si el punto está a más de 2 km de la ruta (o `null`) y el estado del viaje.

```json
{
  "point": {
    "id": 41,
    "latitude": -12.1,
    "longitude": -77,
    "speedKmh": 40,
    "source": "PHONE",
    "recordedAt": "2026-11-12T15:10:00Z"
  },
  "alert": {
    "id": 9,
    "latitude": -12.1,
    "longitude": -77,
    "deviationKm": 2.6,
    "detectedAt": "2026-11-12T15:10:00Z",
    "acknowledgedAt": null
  },
  "tripStatus": "IN_TRANSIT"
}
```

**POST `/api/v1/trips/{tripId}/incidents`**

Request body (estructura del esquema OpenAPI; los valores indican el tipo de cada campo):

```json
{
  "type": "string",
  "description": "string"
}
```

Response `200` con datos de muestra. El API devuelve la incidencia creada, abierta y sin evidencias.

```json
{
  "id": 3,
  "type": "DAMAGED",
  "description": "Caja rota",
  "status": "OPEN",
  "resolution": null,
  "reportedAt": "2026-11-12T16:00:00Z",
  "resolvedAt": null,
  "evidences": []
}
```

**GET `/api/v1/trips/{tripId}`**

Response `200` con datos de muestra. El API devuelve el viaje con sus lugares, las partes, el vehículo, la última posición y las fechas de cada estado.

```json
{
  "id": "3f9c2a54-7d1b-4e6a-9c1e-5b8a1d2f0a11",
  "status": "IN_TRANSIT",
  "myRole": "MERCHANT",
  "agreedRate": 120,
  "currency": "PEN",
  "matchProposalId": "8a1d0c92-2b7e-4d3f-a6c4-0e5f7b9d1c22",
  "returnRouteId": null,
  "shipmentRequestId": null,
  "description": "Cajas de ropa",
  "weightKg": 100,
  "volumeM3": 1,
  "origin": {
    "address": "Callao",
    "latitude": -12.05,
    "longitude": -77.04
  },
  "destination": {
    "address": "Surco",
    "latitude": -12.05,
    "longitude": -77.04
  },
  "pickup": {
    "address": "Lima",
    "latitude": -12.05,
    "longitude": -77.04
  },
  "delivery": {
    "address": "San Borja",
    "latitude": -12.05,
    "longitude": -77.04
  },
  "departureAt": "2026-11-12T15:00:00Z",
  "carrier": {
    "name": "Luis Ramos",
    "phone": null
  },
  "merchant": {
    "name": "Ana Torres",
    "phone": null
  },
  "vehicle": {
    "id": "v-1",
    "plate": "T5K-123"
  },
  "driverId": null,
  "driverName": null,
  "lastPoint": null,
  "openAlerts": 0,
  "totalDistanceKm": null,
  "pickedUpAt": "2026-11-12T15:10:00Z",
  "deliveredAt": null,
  "confirmedAt": null,
  "cancelledAt": null,
  "cancellationReason": null,
  "createdAt": null
}
```

**Repositorio de los Web Services:** [https://github.com/NexusLibre-1ASI0729-2620-16692/trazza-webservice](https://github.com/NexusLibre-1ASI0729-2620-16692/trazza-webservice)

**Commits relacionados con la documentación:** `77cb53b` (feat(config): add datasource and jpa settings), `8cab0ed` (build: add springdoc openapi dependency). Cada controlador se documenta con anotaciones OpenAPI en los mismos commits que lo agregan.

| Evidencia | Archivo esperado | Estado |
| :--- | :--- | :--- |
| Swagger UI: vista general de los controladores | chapter5/sprint3-swagger-overview.png | Pendiente |
| Swagger UI: operaciones de `trips` | chapter5/sprint3-swagger-trips.png | Pendiente |
| Swagger UI: ejecución de una operación con datos de muestra | chapter5/sprint3-swagger-execute.png | Pendiente |

**URL de la documentación desplegada:** Pendiente (se registra cuando se confirme el despliegue de los Web Services).

#### 5.2.3.7. Software Deployment Evidence for Sprint Review

En el Sprint 3 se etiquetaron el release v1.0.0 y el hotfix v1.0.1 de los Web Services (2026-11-14) y la versión v1.2.0 de la Web Application, que usa el API en lugar del Fake API. La configuración de los Web Services se hace con variables de entorno, descritas en la sección 5.1.4.

| Software Component | Deployment Platform | Repository / Branch | Version | URL publicada | Estado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Web Services (RESTful API) | Por confirmar | trazza-webservice / main | v1.0.1 (2026-11-14) | Pendiente | Pendiente de confirmar (TS07) |
| Frontend Web Application | AWS Amplify | trazza-webapp / main | v1.2.0 (2026-11-14) | https://main.d11tospvoprjej.amplifyapp.com | El dominio no resuelve en DNS al 2026-11-26; se vuelve a publicar en el Sprint 4 (TS07) |
| Landing Page | AWS Amplify | trazza-website / main | v1.0.0 (2026-10-08) | https://main.dop9j8vefsnfj.amplifyapp.com | El dominio no resuelve en DNS al 2026-11-26; se vuelve a publicar en el Sprint 4 (TS07) |

#### 5.2.3.8. Team Collaboration Insights during Sprint

En el Sprint 3 el equipo trabajó en tres repositorios. La siguiente tabla cuenta los commits sin merge entre el 2026-10-30 y el 2026-11-15. Todos los integrantes participaron en `trazza-webservice`. En `trazza-webapp` los commits del Sprint se concentran en tres integrantes.

| Integrante | GitHub Username | trazza-report | trazza-website | trazza-webapp | trazza-webservice | Total |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| Checalla Apaza, Emanuel Renato | Emanuelca135 | 0 | 0 | 0 | 14 | 14 |
| Lozano Quispe, Fabricio Jofred | FabricioZz15 | 0 | 0 | 5 | 53 | 58 |
| Peñaranda Caldas, Gabriel Augusto | gapc2124 | 3 | 0 | 67 | 130 | 200 |
| Pezo Castilla, Maria Jose | MariaJosePezo | 0 | 0 | 0 | 64 | 64 |
| Vite Celis, Rodrigo Matias | rodriznnn | 0 | 0 | 2 | 26 | 28 |
| **Total** |  | **3** | **0** | **74** | **287** | **364** |

<div align="center">
  <img src="../assets/images/chapter5/sprint3-insights-webservice-contributors.png" alt="GitHub Insights, contribuidores de trazza-webservice durante el Sprint 3" width="800">
  <br><br>
  <img src="../assets/images/chapter5/sprint3-insights-webservice-network.png" alt="GitHub Insights, grafo de ramas de trazza-webservice durante el Sprint 3" width="800">
  <br><br>
  <img src="../assets/images/chapter5/sprint3-insights-webapp-contributors.png" alt="GitHub Insights, contribuidores de trazza-webapp durante el Sprint 3" width="800">
  <br><br>
  <img src="../assets/images/chapter5/sprint3-insights-report-contributors.png" alt="GitHub Insights, contribuidores de trazza-report durante el Sprint 3" width="800">
</div>
