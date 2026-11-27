### 5.2.2. Sprint 2

En esta sección se registra el avance en producto y en trabajo colaborativo del Sprint 2, cuyo alcance fue la primera versión funcional de la Frontend Web Application sobre un Fake API y una nueva versión del Landing Page.

#### 5.2.2.1. Sprint Planning 2

En el Sprint Planning 2 el equipo definió el objetivo del Sprint y seleccionó las User Stories de la Web Application de acuerdo con su prioridad en el Product Backlog.

| Sprint # | Sprint 2 |
| :--- | :--- |
| **Sprint Planning Background** | |
| Date | 2026-10-05 |
| Time | 10:00 PM |
| Location | Reunión virtual vía Discord |
| Prepared By | Peñaranda Caldas, Gabriel Augusto |
| Attendees (to planning meeting) | Checalla Apaza, Emanuel Renato / Lozano Quispe, Fabricio Jofred / Pezo Castilla, Maria Jose / Peñaranda Caldas, Gabriel Augusto / Vite Celis, Rodrigo Matias |
| Sprint 1 Review Summary | En este sprint, el equipo avanzó en la primera versión funcional de Trazza, desarrollando la Landing Page y las funcionalidades iniciales de registro y autenticación. También se establecieron las bases para la integración y despliegue de los componentes del sistema. Como mejora, identificamos la necesidad de seguir refinando la experiencia de usuario y fortalecer la integración entre los diferentes módulos. |
| Sprint 1 Retrospective Summary | Durante este sprint, el equipo mantuvo una colaboración constante mediante la distribución de responsabilidades y el uso de GitHub para integrar los avances. Sin embargo, se identificaron oportunidades de mejora en la coordinación de tareas, comunicación e integración de cambios entre ramas. Para el siguiente sprint, buscaremos mejorar la organización del trabajo y mantener una comunicación más constante entre los integrantes. |
| **Sprint Goal & User Stories** | |
| Sprint 2 Goal | **Nuestro enfoque está en** desplegar la primera versión funcional de la Web Application de Trazza, con los cinco bounded contexts navegables sobre un Fake API, y en publicar una nueva versión del Landing Page que lleve al registro de la aplicación. **Creemos que esto entrega** a transportistas y comerciantes MYPE una experiencia interactiva para registrarse, publicar rutas o solicitudes de flete, negociar tarifas y seguir un envío antes de contar con los Web Services. **Esto se confirmará cuando** un usuario complete en la aplicación desplegada en AWS Amplify el flujo principal de su rol (registro, inicio de sesión, publicación de ruta o solicitud, negociación, seguimiento y calificación) sin errores bloqueantes, las **14 historias comprometidas (53 SP)** estén cerradas, y los botones de autenticación del Landing Page v1.0.0 lleven a las vistas de registro e inicio de sesión de la aplicación. |
| Sprint 2 Velocity | 53 Story Points |
| Sum of Story Points | 53 Story Points (US01: 3, US02: 3, US03: 3, US23: 3, US08: 5, US09: 5, US10: 5, US11: 5, US12: 5, US13: 5, US19: 2, US20: 2, US21: 2, US24: 5) |

#### 5.2.2.2. Aspect Leaders and Collaborators

Los aspectos del Sprint 2 corresponden a los bounded contexts de la Web Application, a la nueva versión del Landing Page y a la internacionalización. Cada integrante lideró el contexto en el que concentró sus commits.

| Team Member (Last Name, First Name) | GitHub Username | Landing Page v1.0.0 (L/C) | IAM & Profiles (L/C) | Shared Kernel y despliegue (L/C) | Matchmaking & Routing (L/C) | Payment & Billing (L/C) | Service Execution & Monitoring (L/C) | Loyalty & Reputation e i18n (L/C) |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Checalla Apaza, Emanuel Renato | Emanuelca135 | C | C | C | C | L | C | C |
| Lozano Quispe, Fabricio Jofred | FabricioZz15 | L | C | C | L | C | C | C |
| Peñaranda Caldas, Gabriel Augusto | gapc2124 | C | L | L | C | C | C | C |
| Pezo Castilla, Maria Jose | MariaJosePezo | C | C | C | C | C | L | C |
| Vite Celis, Rodrigo Matias | rodriznnn | C | C | C | C | C | C | L |

#### 5.2.2.3. Sprint Backlog 2

El Sprint 2 comprometió 14 User Stories de la Web Application y cuatro tareas transversales. Cada User Story se descompuso en tareas de 4 a 8 horas. Al cierre del Sprint, 18 tareas: 18 en **Done**, 0 en **In-Process**, 0 en **To-Review** y 0 en **To-do**.

**URL público del Board:** [https://trazza.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog](https://trazza.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog)

| Sprint # | Sprint 2 | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **User Story** | | **Work-Item / Task** | | | | | |
| **Id** | **Title** | **Id** | **Title** | **Description** | **Estimation (Hours)** | **Assigned To** | **Status (To-do / In-Process / To-Review / Done)** |
| US01 | Registro de Transportista | T01 | Sign up del transportista | Implementar el registro con DNI, el perfil del transportista y sus validaciones. | 6 | Peñaranda Caldas, Gabriel Augusto | Done |
| US02 | Registro de Emprendedor | T02 | Sign up del comerciante | Implementar el registro con RUC y el perfil del comerciante. | 5 | Peñaranda Caldas, Gabriel Augusto | Done |
| US03 | Inicio de Sesión de Usuario | T03 | Sign in, guards e interceptor | Implementar el inicio de sesión, la protección de rutas por autenticación y rol y el interceptor HTTP. | 6 | Peñaranda Caldas, Gabriel Augusto | Done |
| US23 | Registro de Nuevo Vehículo | T04 | Vehículos del transportista | Implementar el listado, la tarjeta y el formulario de vehículos con placa y capacidad de carga. | 5 | Peñaranda Caldas, Gabriel Augusto | Done |
| US08 | Publicación de Ruta de Retorno | T05 | Publicación y listado de rutas de retorno | Implementar el formulario y el listado de rutas de retorno con ventana horaria y tipo de carga. | 8 | Lozano Quispe, Fabricio Jofred | Done |
| US09 | Solicitud de Envío de Mercadería | T06 | Solicitud de envío de mercadería | Implementar el formulario y el listado de solicitudes de flete con peso, volumen y destino. | 8 | Lozano Quispe, Fabricio Jofred | Done |
| US10 | Sugerencias Automáticas de Carga | T07 | Sugerencias automáticas de carga | Implementar el servicio de dominio `RouteMatchingService` y la vista de sugerencias con desvío estimado. | 8 | Lozano Quispe, Fabricio Jofred | Done |
| US11 | Búsqueda Manual de Transportistas | T08 | Búsqueda manual de transportistas | Implementar la búsqueda de transportistas con envío de oferta. | 6 | Lozano Quispe, Fabricio Jofred | Done |
| US12 | Aceptar Solicitud de Carga | T09 | Aceptar una solicitud de carga | Implementar el detalle de la carga y la aceptación de la tarifa. | 4 | Lozano Quispe, Fabricio Jofred | Done |
| US13 | Negociación y Propuesta de Tarifa | T10 | Negociación de tarifa | Implementar la contraoferta y la lista de ofertas con sus estados. | 6 | Lozano Quispe, Fabricio Jofred | Done |
| US19 | Calificación del Transportista | T11 | Calificación del transportista | Implementar el diálogo de calificación de 1 a 5 estrellas y el componente de estrellas. | 4 | Vite Celis, Rodrigo Matias | Done |
| US20 | Calificación del Cliente | T12 | Calificación del cliente | Implementar la calificación del emprendedor y la lista de calificaciones recibidas. | 4 | Vite Celis, Rodrigo Matias | Done |
| US21 | Reportar Problemas con la Carga | T13 | Reportar problemas con la carga | Implementar el reporte de incidencias sobre un envío. | 5 | Pezo Castilla, Maria Jose | Done |
| US24 | Historial de Envíos | T14 | Historial de envíos | Implementar el seguimiento y los historiales de viajes y envíos con filtro por rol. | 6 | Pezo Castilla, Maria Jose | Done |
| — | Constraint | T15 | Shared kernel y estructura base | Configurar el proyecto Angular, el shared kernel (`Money`, `Address`, `GeoLocation`), el layout y el enrutamiento base. | 8 | Peñaranda Caldas, Gabriel Augusto | Done |
| — | Constraint | T16 | Planes y facturación | Implementar la vista de planes, el diálogo de pago con validación de tarjeta y el comprobante electrónico. | 8 | Checalla Apaza, Emanuel Renato | Done |
| — | Constraint | T17 | Internacionalización y landing v1.0.0 | Traducir los mensajes de validación (EN / ES) y publicar la nueva versión del Landing Page con el selector de idioma. | 6 | Vite Celis, Rodrigo Matias | Done |
| — | Constraint | T18 | Despliegue del frontend | Desplegar la aplicación web en AWS Amplify conectada a un entorno de prueba público. | 4 | Pezo Castilla, Maria Jose | Done |

#### 5.2.2.4. Development Evidence for Sprint Review

En el Sprint 2 se implementó la Web Application con Angular y una arquitectura DDD por bounded context, se publicó una nueva versión del Landing Page y se actualizó el informe. Las tablas muestran los commits sin merge de los tres repositorios entre el 2026-10-05 y el 2026-10-29: 116 de `trazza-webapp`, 50 de `trazza-website` y 29 de `trazza-report`.

**trazza-webapp**

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 35dcb92 | Initial commit | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | e11e8ba | feat(matchmaking): add party type for negotiation turns | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | a655857 | feat(matchmaking): add time-window value object | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | a07f17f | feat(matchmaking): add cargo-type value object | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | acf378e | feat(matchmaking): add cargo value object | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 683063d | feat(matchmaking): add detour value object | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 689960a | feat(matchmaking): add route-status value object | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | bb039e0 | feat(matchmaking): add request-status value object | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 6b63f48 | feat(matchmaking): add proposal-status value object | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | af0b928 | feat(matchmaking): add route-matching domain service | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 590c3cf | feat(matchmaking): add return-route aggregate | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | aee88c6 | feat(matchmaking): add freight-request aggregate | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 6cc2057 | feat(matchmaking): add match-proposal aggregate | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 85a3b9c | test(matchmaking): add route-matching service unit tests | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | f89295c | feat(matchmaking): add return-route resource and response | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 2c0b106 | feat(matchmaking): add freight-request resource and response | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 33d4779 | feat(matchmaking): add match-proposal resource and response | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | adbd97d | feat(matchmaking): add return-route assembler | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 4cd5747 | feat(matchmaking): add freight-request assembler | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 27bc0b1 | feat(matchmaking): add match-proposal assembler | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 611f290 | feat(matchmaking): add return-routes api endpoint | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 6d02ad5 | feat(matchmaking): add freight-requests api endpoint | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 3477c49 | feat(matchmaking): add match-proposals api endpoint | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | c8d2357 | feat(matchmaking): add matchmaking api facade | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 28c4fad | feat(matchmaking): add matchmaking signal store | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 7337170 | feat(matchmaking): add route-preview component | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | fddf0f2 | feat(matchmaking): add counter-offer-panel component | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 0c4638a | feat(matchmaking): add offer-amount dialog | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 6a7290f | feat(matchmaking): add load-suggestion-card component | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | afefd4e | feat(matchmaking): add carrier-card component | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | f164df4 | feat(matchmaking): add return-route list view | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | df18e9b | feat(matchmaking): add return-route form view | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | acc886e | feat(matchmaking): add load-suggestions view | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | aa4b30b | feat(matchmaking): add load-detail view | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | f015024 | feat(matchmaking): add freight-request list view | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 0f04504 | feat(matchmaking): add freight-request form view | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | d1f1faa | feat(matchmaking): add find-carriers view | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | 5c634ea | feat(matchmaking): add offer list view | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | bf03274 | feat(matchmaking): add offer-detail view | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/matchmaking-routing | b284b81 | feat(matchmaking): add matchmaking routes | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 644a0bc | feat(reputation): add score value object | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 3a8049f | feat(reputation): add rating-target value object | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 54ca594 | feat(reputation): add rating aggregate | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 9ebda84 | feat(reputation): add rating resource and response | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 73d352e | feat(reputation): add rating assembler | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | a8586c9 | feat(reputation): add ratings api endpoint | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 8952f29 | feat(reputation): add reputation api facade | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | f65b20d | feat(reputation): add reputation signal store | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 4e36fab | feat(reputation): add star-rating component | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | e5149cf | feat(reputation): add rating dialog | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | bc23729 | feat(reputation): add rating-list view | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 12e5434 | feat(reputation): add reputation routes | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 25eb611 | feat(execution): add shipment domain model | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 8aa74ce | feat(execution): implement service execution monitoring | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | cbcc5b7 | feat(iam): scaffold domain-driven design directory structure | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 5651d4e | feat(iam): implement domain models and infrastructure assemblers | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 62462a6 | chore: update package-lock | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 3382491 | feat(iam): implement api services, interceptor and authentication guard | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | ccd3508 | feat(iam): implement application stores with Angular Signals | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | f91c5e7 | feat(iam): add sign-in component and setup routes | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 5c5cdd9 | feat(iam): add sign-up component | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 38bc29d | feat(execution): integrate shipment filtering with IAM | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | fb8cb9b | feat(execution): filter shipments by user role | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 23cc0f6 | refactor(execution): centralize cancelled shipment status | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | e8c9490 | feat(billing): add PaymentTransactionResponse DTO | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | cb4426e | feat(billing): add ReceiptResponse DTO | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | bdc90f5 | feat(billing): add PaymentTransactionAssembler (DTO <-> Entity) | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 986e3d2 | feat(billing): add ReceiptAssembler (DTO <-> Entity) | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 1bfcf78 | feat(execution): validate active shipment actions | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 3dc5725 | fix(execution): reset loading state after fetch failure | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 875624c | feat(billing): add SubscriptionPlan value object | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 438e1e8 | refactor(execution): simplify shipment state updates | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 3ca11dc | feat(billing): add PaymentStatus value object | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 299b207 | feat(billing): add ReceiptType value object | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 1539870 | feat(billing): add PaymentMethod value object with Luhn validation | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | efc5896 | test(billing): add PaymentMethod unit tests | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 1c20967 | feat(billing): add PaymentTransaction entity | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | c125fa0 | feat(billing): add Receipt entity | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 5774ada | feat(billing): add BillingStore application service | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 3d5b633 | feat(billing): add CheckoutDialog component | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 1e0ac84 | feat(billing): add CheckoutDialog template | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | ccf0ddc | feat(billing): add CheckoutDialog styles | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 4599476 | feat(billing): add ReceiptDialog component | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 7de4755 | feat(billing): add ReceiptDialog styles | - feat(billing): add ReceiptDialog template | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | a71221b | feat(billing): add PlanBilling styles | - feat(billing): add PlanBilling template - feat(billing): add PlanBilling view | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 7775dc6 | feat(billing): add BillingApi HTTP service | - feat(billing): add PaymentGateway mock service | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 73d8916 | feat(iam): add profile view component | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 3b4605d | feat(iam): add vehicle list, card and form components | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 75fa96c | fix(iam): rename guard to match app.routes.ts import | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | b6788e8 | chore(env): prepare production environment for EC2 deployment | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | 243ed9d | chore(env): set EC2 public IP for production | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | 894ed06 | fix(core): resolve typescript compilation errors across modules | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | 1d4cee1 | chore(env): remove port 3000 from EC2 API base url | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | cf716a7 | chore(env): update EC2 API base url to 16.59.43.35 | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | 5950ab2 | chore(env): restore port 3000 to API base url | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | fca0d49 | chore(env): point to 18.116.52.45 via Nginx | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | 8406ce8 | chore(env): use duckdns domain for API | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | 7ce0426 | chore(env): use relative url for amplify proxy | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | 0b29987 | chore(env): revert to direct EC2 IP due to AWS proxy limitations | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | main | a7f3b97 | chore(env): update API base url to https duckdns as per instructions | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | 6b239df | fix(iam): translate sign-in validation messages and remove duplicated asterisks | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 748eab4 | fix(iam): translate sign-in validation messages and remove duplicated asterisks | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | 783648c | fix(iam): translate profile validation messages and remove duplicated asterisks | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 2c26f7c | fix(iam): translate profile validation messages and remove duplicated asterisks | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | 53701b1 | fix(iam): translate vehicle form validation messages and remove duplicated asterisks | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 87eed98 | fix(iam): translate vehicle form validation messages and remove duplicated asterisks | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | 55756c1 | feat(i18n): add English labels for terms and privacy links | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | ed6164d | feat(i18n): add English labels for terms and privacy links | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | ba8dd15 | feat(i18n): add Spanish labels for terms and privacy links | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 3ef17e3 | feat(i18n): add Spanish labels for terms and privacy links | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | 41b5bdf | feat(iam): add terms link to sign-up and translate its validation messages | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 488ecb0 | feat(iam): add terms link to sign-up and translate its validation messages | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | fc265ab | feat(seo): add keywords and author meta tags | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | b23a9cf | feat(seo): add keywords and author meta tags | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/shared | ceb3ab7 | feat(shared): add terms and privacy links to footer | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-webapp | feature/payment-billing | 66bff68 | feat(shared): add terms and privacy links to footer | - | 2026-10-08 |

**trazza-website**

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/header-navegation | abab0d0 | chore: initial repository structure | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/i18n-translations | bce4e5b | chore(setup): add base HTML structure | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/i18n-translations | d761c39 | style(setup): add global variables, reset and base components | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/i18n-translations | a37205a | chore(setup): add gitignore | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/i18n-translations | 082165a | feat(segments): add how it works, carriers and merchants sections | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/i18n-translations | aa0e6ef | feat(segments): add carrier and merchant images | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/i18n-translations | 840e62d | style(segments): add styles for how it works, carriers and merchants | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/i18n-translations | 9e89547 | feat(segments): add profile tabs in how it works | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/i18n-translations | 718efca | feat(i18n): add language engine and base translations | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/i18n-translations | 470da4a | feat(i18n): load i18n script | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 2eee42b | feat/cta-redirection | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | db8fcec | feat/footer-and-terms | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 94ae261 | fix(cta): correct-asset-paths-to-assets-folder | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 630aea4 | fix(cta): remove-login-and-registration-pages | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | aaf5025 | feat(header): add navbar structure and logo | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 86e1df7 | feat(header): add navigation links and mobile sign-in | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 0515c26 | feat(header): add language switch, sign-in and burger button | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | db109ac | style(header): add logo styles | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 3b86216 | style(header): add language switch styles | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | cde8744 | style(header): add navbar and navigation links styles | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | a3babcc | style(header): add burger menu styles | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 5797c0b | style(header): add responsive navigation styles | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | f7f641d | style(header): add nav-menu | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 8bfde8c | chore(hero): hero section | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 6a1641a | feat(hero): add hero structure, title and description | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 6faf336 | feat(hero): add call-to-action buttons and trust chips | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 912d3ef | style(hero): add hero content styles | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | c3a9a6d | feat(hero): add load suggestion card with route map | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 74cd367 | feat(hero): add merchant, rate and detour details to load card | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 0645dc8 | style(hero): add load suggestion card styles | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 973ccb8 | docs(readme): add project overview and folder structure | Added a description of the Trazza platform and its purpose. | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | 2806178 | Clear existing README content | Removed the initial content of the README file. | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/readme-and-setup | b578684 | docs(readme): reset readme and add gitattributes | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/readme-and-setup | 94fddde | docs(readme): add project overview and folder structure | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/readme-and-setup | 411837f | docs(readme): add project overview and folder structure | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/readme-and-setup | 2b85929 | docs(readme): add project overview and folder structure | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/readme-and-setup | 083dd64 | docs(readme): document setup, i18n and UI components | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/readme-and-setup | 1741a47 | docs(readme): add design system, sections, conventions and roadmap | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/project-setup-and-styles | abdc44b | feat(seo): add keywords and author meta tags | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/footer-and-terms | 1baf56a | feat(footer): add terms page and link legal section, rename startup to NexusLibre | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/footer-and-terms | a925c85 | feat(footer): add terms page translations and legal page styles | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/cta-redirection | 5a00b0f | docs(cta): document main landing actions | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/target-segments-content | eeaee37 | feat(content): set Pro plan price and add validation testimonials | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/cta-redirection | d750468 | docs(cta): document carrier and merchant actions | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/cta-redirection | 26b4b44 | fix(hero): remove duplicated hero block | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/hero-section | 64875de | fix(hero): place load suggestion card beside hero content | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | release/v1.1.0 | 5cc2381 | feat: add registration page | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | release/v1.1.0 | 5ddbe67 | feat: add login and register form UI | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | feature/header-navegation | d5a92ef | feat: redirect all auth actions to external web application and fix asset paths | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-website | HEAD | f6885e1 | chore: update web app links to use IAM bounded context routes | - | 2026-10-08 |

**trazza-report**

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/update-startup-profile | 4a669c9 | doc: adding new changes | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/update-startup-profile | c2342a0 | doc: adding new changes | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/update-startup-profile | 80ca896 | feat/update-startup-profile | - | 2026-10-06 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/update-22-entrevistas | 2395c64 | feat/update-22-entrevistas | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/03-collaboration-insights | 1435c3e | feat/update-05-student-outcome | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/03-collaboration-insights | 42478d0 | feat/update-03-collaboration-insights | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/02-version-register | 13584f5 | feat/update-02-version-register | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/13-segmentos-objetivo | b46a5f0 | feat/update-52-landing-page-services-applications-implementation | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/05-student-outcome | 0765f23 | docs: update course name and team in front page | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/11-startup-profile | e00b379 | docs: update student outcome section | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/11-startup-profile | b68bb5c | docs(chapter 1): update startup profile | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/42-information-architecture | e1576e3 | docs(chapter 4): update information architecture | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/44-web-applications-ux-ui-design | db14f7a | docs(chapter 4): update web applications ux ui design | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/05-student-outcome | 01472c6 | docs(chapter 5): updating software configuration management | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/05-student-outcome | acbf768 | docs(student-outcome): update Rodrigo Vite TB1 contributions | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/05-student-outcome | 032cf6d | docs(student-outcome): align Rodrigo Vite entries with ABET SO3 and fix typos | - | 2026-10-07 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | release/3.0 | fe40d9b | docs: actualizar imágenes y referencias del modelo C4 en arquitectura | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | release/3.0 | a60828a | doc: updating references | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | release/3.0 | 7a26ec8 | doc: add tb1 presentation and sprint 2 videos | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | release/3.0 | 16e4ea0 | doc: update deployment urls for web app and landing page | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | release/3.0 | 0199f2b | doc: fill deployment configuration table in 5.1.4 with live URLs and repo names | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | release/3.0 | 6e4525e | doc: add sprint 2 user story execution evidence and remove empty swagger table | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | release/3.0 | 50de5cb | doc: preparing export | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/11-startup-profile | 4bfd2ff | docs(chapter 1): update startup profile | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/12-solution-profile | bd79f08 | docs(chapter 2): update solution profile | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/22-entrevistas | be158d9 | docs(chapter 2): update interviews | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/51-software-configuration-management | 38599c0 | docs(chapter 5): update software configuration management | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/61-conclusiones | c6332d5 | docs: update conclusions | - | 2026-10-08 |
| NexusLibre-1ASI0729-2620-16692/trazza-report | feature/52-landing-page-services-applications-implementation | 5a5a9e7 | docs(chapter 5): update landing page services application | - | 2026-10-08 |

#### 5.2.2.5. Execution Evidence for Sprint Review

Al cierre del Sprint 2 la Web Application permitía a un transportista publicar rutas de retorno, recibir sugerencias de carga y negociar tarifas, y a un comerciante crear solicitudes de flete, buscar transportistas y seguir sus envíos, con sus calificaciones, su plan y sus comprobantes. Los datos provenían de un Fake API.

| Bounded context | Vistas implementadas |
| :--- | :--- |
| IAM & Profiles | Sign in, sign up, perfil, lista y formulario de vehículos |
| Matchmaking & Routing | Rutas de retorno, solicitudes de flete, sugerencias de carga, detalle de carga, búsqueda de transportistas y ofertas |
| Service Execution & Monitoring | Viaje activo, historial de viajes, seguimiento de envío e historial de envíos |
| Payment & Billing | Plan y facturación, diálogo de pago y comprobante |
| Loyalty & Reputation | Lista de calificaciones y diálogo de calificación |

| Evidencia | Archivo esperado | Estado |
| :--- | :--- | :--- |
| Landing Page v1.0.0, vista de escritorio y móvil | chapter5/sprint2-landing-desktop.png, chapter5/sprint2-landing-mobile.png | Pendiente |
| Web Application: dashboard del transportista | chapter5/sprint2-webapp-carrier-dashboard.png | Pendiente |
| Web Application: rutas de retorno y sugerencias de carga | chapter5/sprint2-webapp-matchmaking.png | Pendiente |
| Web Application: viaje activo | chapter5/sprint2-webapp-active-trip.png | Pendiente |
| Web Application: plan y facturación | chapter5/sprint2-webapp-billing.png | Pendiente |

Las capturas anteriores del Sprint 2 se retiraron porque corresponden a una versión con otra biblioteca de componentes (muestran un aviso de licencia de PrimeUI) y no a la aplicación Angular Material de este repositorio.

**Video de navegación del Sprint 2:** [upc-pre-202620-1asi0729-16692-NexusLibre-keynote-tb1.mp4](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202210836_upc_edu_pe/IQB4iIieEXLgTY0NDGDKdOCWAffPuq2jSt2JscaEYz-EMaQ?e=R1rXS0&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)

#### 5.2.2.6. Services Documentation Evidence for Sprint Review

En el Sprint 2 no existían los Web Services. La Web Application consumió un Fake API creado con json-server (`server/db.json` y `server/routes.json` de `trazza-webapp`, etiqueta `v1.1.0`), que expone cada colección bajo el prefijo `/api/v1`. Los Web Services con OpenAPI se implementaron en el Sprint 3 (sección 5.2.3.6).

| Endpoint | Acciones soportadas | Registros de muestra |
| :--- | :--- | :---: |
| `/api/v1/users` | GET, POST, PUT, PATCH, DELETE | 6 |
| `/api/v1/carrier-profiles` | GET, POST, PUT, PATCH, DELETE | 3 |
| `/api/v1/merchant-profiles` | GET, POST, PUT, PATCH, DELETE | 3 |
| `/api/v1/return-routes` | GET, POST, PUT, PATCH, DELETE | 4 |
| `/api/v1/freight-requests` | GET, POST, PUT, PATCH, DELETE | 6 |
| `/api/v1/match-proposals` | GET, POST, PUT, PATCH, DELETE | 4 |
| `/api/v1/shipments` | GET, POST, PUT, PATCH, DELETE | 5 |
| `/api/v1/payment-transactions` | GET, POST, PUT, PATCH, DELETE | 1 |
| `/api/v1/receipts` | GET, POST, PUT, PATCH, DELETE | 1 |
| `/api/v1/ratings` | GET, POST, PUT, PATCH, DELETE | 9 |

#### 5.2.2.7. Software Deployment Evidence for Sprint Review

En el Sprint 2 se desplegaron la nueva versión del Landing Page, la Web Application y el Fake API. Los pasos se describen en la sección 5.1.4.

| Software Component | Deployment Platform | Repository / Branch | Version | URL publicada | Estado al 2026-11-26 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Landing Page | AWS Amplify | trazza-website / main | v1.0.0 (2026-10-08) | https://main.dop9j8vefsnfj.amplifyapp.com | El dominio no resuelve en DNS; se vuelve a publicar en el Sprint 4 (TS07) |
| Frontend Web Application | AWS Amplify | trazza-webapp / main | v1.1.0 (2026-10-08) | https://main.d11tospvoprjej.amplifyapp.com | El dominio no resuelve en DNS; se vuelve a publicar en el Sprint 4 (TS07) |
| Fake API (json-server) | AWS EC2 | trazza-webapp / carpeta `server` | — | https://trazza-api2.duckdns.org/api/v1 | No responde (tiempo de espera agotado); reemplazado por los Web Services en el Sprint 3 |

#### 5.2.2.8. Team Collaboration Insights during Sprint

En el Sprint 2 el equipo trabajó en tres repositorios. En `trazza-webapp` cada bounded context se desarrolló en su propia rama `feature/*` y se integró a `develop` mediante Pull Request. La siguiente tabla cuenta los commits sin merge entre el 2026-10-05 y el 2026-10-29.

| Integrante | GitHub Username | trazza-report | trazza-website | trazza-webapp | trazza-webservice | Total |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| Checalla Apaza, Emanuel Renato | Emanuelca135 | 0 | 8 | 19 | 0 | 27 |
| Lozano Quispe, Fabricio Jofred | FabricioZz15 | 12 | 16 | 39 | 0 | 67 |
| Peñaranda Caldas, Gabriel Augusto | gapc2124 | 9 | 4 | 21 | 0 | 34 |
| Pezo Castilla, Maria Jose | MariaJosePezo | 6 | 6 | 8 | 0 | 20 |
| Vite Celis, Rodrigo Matias | rodriznnn | 2 | 16 | 29 | 0 | 47 |
| **Total** |  | **29** | **50** | **116** | **0** | **195** |

<div align="center">
  <img src="../assets/images/chapter5/sprint2-insights-webapp-contributors.png" alt="GitHub Insights, contribuidores de trazza-webapp durante el Sprint 2" width="800">
  <br><br>
  <img src="../assets/images/chapter5/sprint2-insights-webapp-network.png" alt="GitHub Insights, grafo de ramas de trazza-webapp durante el Sprint 2" width="800">
  <br><br>
  <img src="../assets/images/chapter5/sprint2-insights-website-contributors.png" alt="GitHub Insights, contribuidores de trazza-website durante el Sprint 2" width="800">
  <br><br>
  <img src="../assets/images/chapter5/sprint2-insights-report-contributors.png" alt="GitHub Insights, contribuidores de trazza-report durante el Sprint 2" width="800">
</div>
