# 📄 Requerimientos del Sistema

## 1. Lista general de requerimientos

El sistema de TechCup tiene los siguientes requerimientos (descripción a alto nivel):

### 1.1 Requerimientos funcionales

El sistema de TechCup debe tener la capacidad de:

1. <mark> **Creación de torneos:**la aplicación debe permitir a los organizadores crear torneos especificando su información básica, incluyendo fechas, cuota de inscripción y reglas establecidas</mark>
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
| **Nombre del requerimiento** | |
| **Descripción** | *El sistema debe …* |
| **Precondiciones** | *Para que el sistema cumpla con este requerimiento, Bankify debe tener previamente …* |
| **Actor** | *(El actor debe estar definido en el diagrama de contexto)* |
| **Flujo principal** | 1. El actor …<br>2. El sistema …<br>3. El sistema … |
| **Diagrama de caso de uso** | *imagen y link*|
| **Poscondiciones** | *Se espera como resultado …* |


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
| **Nombre del requerimiento** | |
| **Descripción** | *El sistema debe …* |
| **Precondiciones** | *Para que el sistema cumpla con este requerimiento, Bankify debe tener previamente …* |
| **Actor** | *(El actor debe estar definido en el diagrama de contexto)* |
| **Flujo principal** | 1. El actor …<br>2. El sistema …<br>3. El sistema … |
| **Diagrama de caso de uso** | *imagen y link*|
| **Poscondiciones** | *Se espera como resultado …* |

## 3. Preguntas
1. Do you identify any requirement that needs to be further detailed? Which one(s)?
    - Sí. Principalmente el requerimiento 5. No especificamos el formato del reporte, sus campos, filtros, etc.
    - Otro requerimiento que podríamos especificar un poco más es el 4 (Pago por PSE), no decimos qué pasa en caso de que el pago falle o sea rechazado.

2. Are there any requirements that contradict each other? Which one(s)?
    - Actualmente el requerimiento no funcional 3 dice que deben poder haber varios torneos simultáneamente, pero al ver el contexto del caso, se pide un solo torneo activo a la vez.

3. If you had to prioritize the requirements, which 2 requirements should be considered the most important and implemented in the first iteration of the project?
    - El RF-01 y RF-02. Estos 2 son esenciales. Sin poder crear torneos ni registrarnos a los mismos la aplicación no serviría de nada y no aportaría valor al negocio.
4. Is there any requirement that should not be implemented?

    - Creemos que ninguno de los requisitos sobra. Necesitamos crear un torneo, registrar a un equipo, pagar la inscripción y reportar lo sucedido para aportar valor al negocio. Podríamos decir que el requerimiento de generación de reportes es el menos necesario, pero puede ser útil.
