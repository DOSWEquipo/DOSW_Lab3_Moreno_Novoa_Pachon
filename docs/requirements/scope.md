# 📄 Requerimientos del Sistema

## 1. Sistema

* Nombre del sistema: **TechCup**
* Objetivo: El objetivo del sistema es **garantizar que los torneos y las inscripciones cumplan con reglas específicas**, al tiempo que permite a los usuarios interactuar con la plataforma de forma sencilla y segura.

## 2. Problema a resolver
Actualmente, la Escuela Colombiana de Ingeniería Julio Garavito no cuenta con un sistema centralizado para gestionar de manera sencilla y segura los torneos de fútbol semestrales de los programas de Ingeniería de Sistemas, Ingeniería de Inteligencia Artificial, Ingeniería de Ciberseguridad e Ingeniería Estadística.

Esta situación dificulta la gestión de los torneos y el proceso de inscripción de los equipos, incluyendo el registro de equipos, el procesamiento y validación de los pagos, la consulta de los equipos inscritos y la generación de informes relacionados con las inscripciones y los ingresos.

Por lo tanto, se requiere una plataforma digital que permita centralizar y facilitar la gestión de los torneos, equipos, inscripciones y pagos, garantizando el cumplimiento de las reglas establecidas por la Escuela.

## 3. Diagrama de Contexto
![Diagram](docs/images/ContextDiagram-LAB03-DOSW.png)
### 3.1 Diagrama

Relacionar imagen del diagrama de contexto realizado

### 3.2 Actores

<En el siguiente cuadro, mapee los actores o roles identificados del sistema>
<El primer rol es de ejemplo>

| Actor / Rol                        |          Descripción              |
|------------------------------------|:---------------------------------:|
| Usuario final                      | Cliente del sistema de Bankify    |
|                                    |                                   |

### 3.3 Sistemas externos

<En el siguiente cuadro, mapee los sistemas externos que interactúan con el sistema de Bankify>
<El primer sistema es de ejemplo>

| Sistema                            |                                    Descripción                                        |
|------------------------------------|:-------------------------------------------------------------------------------------:|
| Reportes                           | Sistema que genera los reportes tributarios de cada cliente del sistema de Bankify    |
|                                    |                                                                                       |

## 4. Alcance del sistema
   
### 4.1 Dentro del sistema
1. Autenticación de roles (organizadores, estudiantes, capitanes) utilizando usuario y contraseña.
2. Creación y administración de torneos.
3. Registro de equipos en el torneo activo.  
4. Procesamiento y validación de pagos de inscripción usando PSE.
5. Generación de reportes de equipos registrados.
6. Envío de reportes a la decanatura. 
Funciones que el sistema sí realiza (Relacione al menos 4).

### 4.2 Fuera del sistema
1. Gestión de partidos y calendario de encuentros.
2. Proceso de transacciones bancarias. (Se hace a través de PSE).
3. Gestión de jugadores individuales.
4. Notificaciones a equipos.
Funciones que no realiza (Relacione al menos 3).

