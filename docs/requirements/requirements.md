# 📄 Requerimientos del Sistema

## 1. Lista general de requerimientos

El sistema de TechCup tiene los siguientes requerimientos (descripción a alto nivel):

### 1.1 Requerimientos funcionales

El sistema de TechCup debe tener la capacidad de:

1. <mark> **Creación de torneos:** la aplicación debe permitir a los organizadores crear torneos especificando su información básica, incluyendo fechas, cuota de inscripción y reglas establecidas</mark>
2. <mark> **Registro en torneos:** la aplicación debe permitir a los usuarios registrar sus equipos en el torneo que se encuentre activo, de acuerdo con las reglas establecidas.</mark>
3. **Autenticación de usuarios:** el sistema debe permitir a los usuarios acceder mediante correo electrónico y contraseña, protegiendo sus credenciales de acceso.
4. **Pago de inscripción:** el sistema debe permitir a los capitanes realizar el pago correspondiente a la inscripción de sus equipos mediante PSE.
5. <mark> **Reporte de equipos inscritos:** la aplicación debe permitir a los organizadores generar un reporte con la información de los equipos inscritos en un torneo.</mark>

### 1.2 Requerimientos no funcionales

El sistema de Bankify debe tener:

1. **Seguridad:** las contraseñas de los usuarios deben ser almacenadas de forma segura mediante mecanismos de cifrado o hashing, con el fin de proteger sus cuentas.
2. **Usabilidad:** la interfaz de usuario debe ser clara e intuitiva, permitiendo identificar fácilmente las opciones disponibles según el rol del usuario y la información de los torneos.
3. **Gestión de torneos:** el sistema debe permitir gestionar diferentes torneos y mostrar claramente el estado correspondiente de cada uno, de acuerdo con los estados definidos para los torneos.
4. **Confirmación de pagos:** la aplicación debe mostrar un mensaje de confirmación al usuario después de realizar un pago de inscripción.
5. **Rendimiento:** la aplicación debe responder a las solicitudes de los usuarios en un tiempo adecuado, evitando demoras que afecten la interacción con la plataforma.

## 2. Diagramas de caso de uso

### 2.1 Requerimiento Funcional 1

| Campo | Descripción |
|------|-------------|
| **ID** | RF-01 |
| **Nombre del requerimiento** | Creación de torneos |
| **Descripción** | La aplicación debe permitir a los organizadores crear torneos especificando su información básica, incluyendo un código único de cinco dígitos basado en el año y el semestre académico, fechas, cuota de inscripción y reglas establecidas. |
| **Precondiciones** | El organizador debe estar autenticado en el sistema y contar con autorización para gestionar torneos, de acuerdo con su rol de organizador. |
| **Actor** | Organizador |
| **Flujo principal** | 1. El organizador selecciona la opción para crear un torneo.<br> 2. El sistema solicita la información básica del torneo.<br>3. El organizador ingresa el código, fechas, cuota de inscripción y reglas del torneo.<br>4. El sistema verifica que el código tenga cinco dígitos y sea único.<br>5. El sistema verifica que la duración del torneo no sea superior a un día.<br>6. El sistema registra el torneo. |
| **Diagrama de caso de uso** | [Use Case Create Tournament Diagram](./../images/UseCaseCreateTournament.png)|
| **Poscondiciones** | El torneo queda registrado en el sistema con la información proporcionada y puede ser gestionado por el organizador. |


### 2.2 Requerimiento Funcional 2

| Campo | Descripción |
|------|-------------|
| **ID** | RF-02 |
| **Nombre del requerimiento** | Registro de equipo en torneo activo |
| **Descripción** | El sistema debe permitir a un capitán registrar su equipo en el torneo que se encuentre actualmente en estado *Activo*. |
| **Precondiciones** | TechCup debe tener previamente un torneo en estado *Activo* y el usuario debe estar autenticado como capitán. |
| **Actor** | Capitán |
| **Flujo principal** | 1. El capitán selecciona la opción de registrar su equipo.<br>2. El sistema muestra el torneo actualmente activo.<br>3. El sistema valida que el equipo no esté ya registrado y confirma la inscripción, quedando pendiente del pago. |
| **Diagrama de caso de uso** |  [Use Case Register Diagram](./../images/UseCaseRegister.png)|
| **Poscondiciones** | El equipo queda vinculado al torneo activo, en estado pendiente de pago de la inscripción. |

### 2.3 Requerimiento Funcional 3

| Campo | Descripción |
|------|-------------|
| **ID** | RF-03 |
| **Nombre del requerimiento** | Generación de reporte de equipos inscritos |
| **Descripción** | El sistema debe permitirle a un usuario con el rol de organizador, generar un reporte con la información de los equipos inscritos hasta el momento en el que se realiza la solicitud. |
| **Precondiciones** | El usuario debe tener permisos de organizador y el sistema debe estar conectado con Power BI para generar el informe con los datos de los equipos registrados en el torneo |
| **Actor** | Organizador |
| **Flujo principal** | 1. El organizador selecciona la opción de generar reporte. <br>2. El Sistema emite un mensaje indicando que el reporte se está preparando.  <br>3. El sistema se conecta con PowerBI y envía los datos de los equipos registrados al momento. <br>4. PowerBI le envía un archivo al sistema con el informe consolidado. <br>5. El sistema se conecta con el correo institucional para enviarle el reporte al organizador. <br>6. El sistema emite un mensaje de notificación indicandole al organizador que ya tiene el reporte en su correo. |
| **Diagrama de caso de uso** | [Use Case Report Diagram](./../images/UseCaseReport.png) |
| **Poscondiciones** | El organizador recibe un documento en su correo institucional, con la toda información consolidada de los equipos registrados al momento de hacer la solicitud. |

## 3. Preguntas
1. Do you identify any requirement that needs to be further detailed? Which one(s)?
    - Sí. Principalmente el requerimiento 5. No especificamos el formato del reporte, sus campos, filtros, etc.
    - Otro requerimiento que podríamos especificar un poco más es el 4 (Pago por PSE), no decimos qué pasa en caso de que el pago falle o sea rechazado.

2. Are there any requirements that contradict each other? Which one(s)?
    - Actualmente el requerimiento no funcional 3 dice que deben poder existir varios torneos simultáneamente, sin embargo, se contradice con el contexto del caso, donde se pide un solo torneo activo a la vez.

3. If you had to prioritize the requirements, which 2 requirements should be considered the most important and implemented in the first iteration of the project?
    - El RF-01 y RF-02. Estos 2 son esenciales debido a que, si no podemos crear torneos ni registrarnos a los mismos, la aplicación no cumpliría con su propósito y no aportaría valor al negocio.
  
4. Is there any requirement that should not be implemented?

    - Creemos que ninguno de los requerimientos está demás. Necesitamos crear un torneo, registrar a un equipo, pagar la inscripción y reportar lo sucedido para aportar valor al negocio, y cada uno de los requerimientos expuestos aporta algo a cumplir con ese objetivo. No obstante, podríamos decir que el requerimiento de generación de reportes no influye directamente en las dinámicas "operativas", siendo más una herramienta para el análisis gerencial.
