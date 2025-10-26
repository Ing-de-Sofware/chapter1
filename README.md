# **COURSE PROJECT**

<p align="center">
  <img src="https://www.upc.edu.pe/static/img/logo_upc_red.png" alt="Logo de la UPC" />
</p>

<p align="center"><strong>Universidad Peruana de Ciencias Aplicadas</strong></p>

<p align="center"><strong>Ingeniería de Software</strong><br>
<strong>1ASI0665 - Anti-Hacking y Nuevas Tendencias de Seguridad</strong> - NRC: 14424 <br>
Ciclo Académico: 202520 <br>
<strong>Profesor(es):</strong> Vera Olivera, David Carlos</p>

<h2 align="center">INFORME DE TRABAJO FINAL – ANTI-HACKING Y NUEVAS TENDENCIAS DE SEGURIDAD</h2>

<h3 align="center">Consultora de Ciberseguridad: <em>CyberChain</em></h3>
<h3 align="center">Cliente (PyME): <em>TAVOLO Tech Solutions S.A.C.</em></h3>
<p align="center"><em>"Securing the chain you rely on"</em></p>

<h3 align="center">Equipo de Consultoría</h3>

<div align="center">

<table>
  <thead>
    <tr>
      <th><strong>Código</strong></th>
      <th><strong>Apellidos, Nombres</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>U20221C936</td>
      <td>Pescoran Angulo, Juan Fabritzzio</td>
    </tr>
    <tr>
      <td>U202022387</td>
      <td>Curi Marcelo, Angelo Marcio</td>
    </tr>
    <tr>
      <td>U202102344</td>
      <td>Gamio Upiachihua, Brenda Lucía</td>
    </tr>
    <tr>
      <td>U202215285</td>
      <td>Baldeon Fabian, Aldo Alberto</td>
    </tr>
    <tr>
      <td>U202214477</td>
      <td>Soto Quispe, Diego Ulises</td>
    </tr>
  </tbody>
</table>

</div>

<p align="center"><strong>Noviembre 2025</strong></p>

# Registro de Versiones del Informe

| Versión | Fecha       | Autor(es) | Descripción de la modificación |
|--------|-------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TP** | 26/10/2025  | **Pescoran Angulo, Juan Fabritzzio**<br><br>**Curi Marcelo, Angelo Marcio**<br><br>**Gamio Upiachihua, Brenda Lucía**<br><br>**Baldeon Fabian, Aldo Alberto**<br><br>**Soto Quispe, Diego Ulises** | Versión inicial **TP1** (Anti‑Hacking): incluye carátula; Registro de Versiones; **Project Report Collaboration Insights**; **Tabla de Contenidos con hipervínculos**; **Student Outcome (SO2)**. Contenido incluido en esta versión: <br>**Cap. I – Introducción** (perfil del cliente y consultora; problemática; **Rules of Engagement** firmadas y escaneadas); <br>**Cap. II – Metodología Ágil y de Pentesting** (Scrum; PTES/OWASP/NIST 800-115; backlog de seguridad; plan de sprints; DoD; herramientas: Kali, Metasploit, Burp/ZAP, Nmap, sqlmap, Wireshark); <br>**Cap. III – Desarrollo por Sprints** (Sprint 1: OSINT y reconocimiento con Nmap/Masscan; Sprint 2: enumeración y análisis preliminar de vulnerabilidades); <br>**Cap. IV – Resultados Consolidados**; <br>**PoC inicial controlada (no destructiva)**. |

## Project Report Collaboration Insights

La coordinación del proyecto se realizó mediante un repositorio en GitHub (documentación pública para el informe), aplicando un flujo GitFlow y la convención de commits 'Conventional Commits' para asegurar trazabilidad de cambios y facilitar revisiones.

- Roles (Scrum): Product Owner; Scrum Master; Pentesters (Web, API, Móvil, Red/Infra); Documentación y Análisis.
- Herramientas principales: Kali Linux, Metasploit, Burp Suite / ZAP, Nmap, sqlmap, Wireshark (complementarias: Nessus/OpenVAS, Nikto, MobSF).
- Evidencias y gobernanza:
  - Capturas y registros por miembro que documentan resultados de reconocimiento, escaneo y hallazgos (Nmap, Masscan, Burp), incluidos en los anexos y referenciados en los Pull Requests.
  - Pull Requests, diffs y comentarios que evidencian revisión entre pares y control de calidad editorial.
  - Salidas y logs estructurados (texto/JSON) y scripts reproducibles que permiten la replicación de pruebas de reconocimiento y enumeración.
  - Documento firmado de Rules of Engagement (anexo) y valores hash (SHA256) asociados a artefactos críticos para garantizar integridad.
  - Nota sobre ética y trazabilidad: todas las pruebas se ejecutaron conforme a las Rules of Engagement acordadas; las evidencias cuentan con metadatos (autor, fecha, descripción) y valores de integridad, y se aplicaron controles de acceso para preservar confidencialidad y cumplimiento legal.

- Repositorio: [G1-UPC-1ASI0665-2520-14424-Antihacking](https://github.com/G1-UPC-1ASI0665-2520-14424-Antihacking) (repositorio principal de documentación y evidencias del proyecto)

Las evidencias están descritas y referenciadas tanto en el cuerpo del informe como en los anexos; se recomienda mantener un manifiesto de evidencias (`evidence_manifest.csv`) con mapeo nombre–archivo, autor, fecha y hash para facilitar auditoría y trazabilidad.

## **TP (Resumen de avance)**

- Mejora de alcance con el cliente (dominios, subdominios, APIs, sistemas en ambiente de pruebas).
- **Sprint 1** finalizado: OSINT, reconocimiento y escaneo inicial con Nmap / Masscan; recopilación de superficie de ataque.
- **Sprint 2** en curso: enumeración de servicios y análisis preliminar de vulnerabilidades (Nessus/Nikto/Burp) y priorización inicial de hallazgos.
- Consolidación de resultados preliminares y preparación de evidencias para su inclusión en el informe; los resultados consolidados se presentan en **Cap. IV – Resultados Consolidados**.
- Redacción y control de versiones del informe en Markdown (rama `develop`, PRs por capítulo) con revisión entre pares.

# Contenido

## Tabla de Contenidos

- [**Capítulo I: Introducción**](#capítulo-i-introducción)
    - [1.1. Client Profile (PyME)](#11-client-profile-pyme)
        - [1.1.1. Descripción de la PyME](#111-descripción-de-la-pyme)
        - [1.1.2. Expectativas del cliente](#112-expectativas-del-cliente)
    - [1.2. Consultora de Ciberseguridad (Equipo)](#12-consultora-de-ciberseguridad-equipo)
        - [1.2.1. Perfiles y roles Scrum](#121-perfiles-y-roles-scrum)
    - [1.3. Solution Profile](#13-solution-profile)
        - [1.3.1. Antecedentes y problemática](#131-antecedentes-y-problemática)
        - [1.3.2. Objetivos del pentesting](#132-objetivos-del-pentesting)
    - [1.4. Aceptación del Servicio (Rules of Engagement)](#14-aceptación-del-servicio-rules-of-engagement)
- [**Capítulo II: Metodología Ágil y de Pentesting**](#capítulo-ii-metodología-ágil-y-de-pentesting)
    - [2.1. Marco de referencia (Scrum + PTES/OWASP/NIST 800-115)](#21-marco-de-referencia-scrum--ptesowaspnist-800-115)
    - [2.2. Backlog inicial (User Stories de seguridad)](#22-backlog-inicial-user-stories-de-seguridad)
    - [2.3. Planificación de Sprints](#23-planificación-de-sprints)
    - [2.4. Definition of Done (DoD)](#24-definition-of-done-dod)
    - [2.5. Herramientas](#25-herramientas)
- [**Capítulo III: Desarrollo del Proyecto por Sprints**](#capítulo-iii-desarrollo-del-proyecto-por-sprints)
    - [Sprint 1 – Reconocimiento y Escaneo](#sprint-1--reconocimiento-y-escaneo)
    - [Sprint 2 – Enumeración y Vulnerabilidades](#sprint-2--enumeracion-y-vulnerabilidades)
    - [Sprint 3 – Explotación](#sprint-3--explotacion)
    - [Sprint 4 – Post-explotación y Persistencia](#sprint-4--post-explotacion-y-persistencia)
    - [Sprint 5 – Informe Final y Recomendaciones](#sprint-5--informe-final-y-recomendaciones)
- [**Capítulo IV: Resultados Consolidados**](#capítulo-iv-resultados-consolidados)
- [**Capítulo V: Recomendaciones y Plan de Mitigación**](#capítulo-v-recomendaciones-y-plan-de-mitigacion)
- [**Capítulo VI: Conclusiones y Video About-the-Team**](#capítulo-vi-conclusiones-y-video-about-the-team)
- [**Bibliografía (APA 7)**](#bibliografía-apa-7)
- [**Anexos**](#anexos)

# Student Outcome 2 - ABET - EAC 

Criterio: La capacidad de aplicar el diseño de ingeniería para producir soluciones que satisfagan necesidades específicas con consideración de salud pública, seguridad y bienestar, así como factores globales, culturales, sociales, ambientales y económicos. En el siguiente cuadro se describe las acciones realizadas y enunciados de conclusiones por parte del grupo, que permiten sustentar el logro del ABET – EAC – Student Outcome 2.


| Criterio específico | Acciones realizadas (TP) | Conclusiones |
|---|---|---|
| Diseña soluciones en ingeniería de software (productos, procesos y/o servicios) que satisfagan necesidades específicas considerando el impacto en salud pública, seguridad, bienestar, así como factores globales, culturales, sociales, ambientales y económicos. | **TP**<br>• Pescoran Angulo, Juan Fabritzzio: definición del alcance autorizado (dominios, sistemas, APIs) y elaboración de la matriz inicial de riesgos.<br>• Curi Marcelo, Angelo Marcio: desarrollo del backlog de seguridad, Definition of Done y mapeo objetivo–entregable.<br>• Gamio Upiachihua, Brenda Lucía: identificación de necesidades del negocio, restricciones legales y lineamientos de tratamiento de datos.<br>• Baldeon Fabian, Aldo Alberto: actividades de OSINT y reconocimiento (Nmap, Masscan); consolidación de la superficie de ataque.<br>• Soto Quispe, Diego Ulises: elaboración de PoC controladas y establecimiento de pautas éticas y de confidencialidad. | El equipo diseñó y ejecutó soluciones de pentesting coherentes con los riesgos identificados; las decisiones de priorización y las medidas propuestas consideraron el impacto en salud, seguridad y continuidad operativa, y están sustentadas por evidencia verificable. |
| Valida que el diseño de la solución de software considere aspectos en salud pública, seguridad, bienestar, así como factores globales, culturales, sociales, ambientales y económicos. | **TP**<br>• Pescoran Angulo, Juan Fabritzzio: establecimiento de reglas de compromiso (sin DoS, ventanas de prueba) y control de impacto en disponibilidad.<br>• Curi Marcelo, Angelo Marcio: definición de métricas de validación y criterios reproducibles de aceptación.<br>• Gamio Upiachihua, Brenda Lucía: creación de checklist de cumplimiento y buenas prácticas de manejo de datos.<br>• Baldeon Fabian, Aldo Alberto: verificación no intrusiva de hallazgos y documentación de falsos positivos.<br>• Soto Quispe, Diego Ulises: trazabilidad y resguardo de evidencias con registros y hashes. | Las actividades de validación incorporaron criterios técnicos y de gobernanza; la evidencia recopilada (logs, capturas y manifiesto) permite auditar hallazgos y verificar la eficacia de las medidas de mitigación. |



-----


## Capítulo I: Introducción 

### 1.1. Client Profile (Perfil del Cliente) 
### 1.1.1 Descripción de la PYME

**Razón Social:** TAVOLO Tech Solutions S.A.C.
<br>
**Sector:** Tecnología aplicada al sector gastronómico (FoodTech)
<br>
**Tipo de empresa:** Startup tecnológica - Pequeña empresa
<br>
**Año de fundación:** 2024
<br>
**Ubicación:** Lima, Perú
<br>
**Número de empleados:** 8-12 colaboradores (equipo técnico y comercial)
<br><br>
**Descripción del Negocio**
<br>
TAVOLO es una startup peruana que desarrolla soluciones tecnológicas basadas en Internet of Things (IoT) para la transformación digital del sector gastronómico. Su producto principal consiste en un sistema integral que combina hardware (sensores de peso embebidos en mesas) con software (aplicaciones web y móviles) para la gestión inteligente del aforo en cafeterías.<br>
La empresa nació como respuesta a una problemática identificada durante la pandemia de COVID-19, cuando el control de aforo se volvió crítico, y ha evolucionado hacia una solución que mejora la experiencia del cliente y optimiza la operación de los establecimientos gastronómicos.
<br><br>
**Modelo de Negocio**
<br>
TAVOLO opera bajo un modelo B2B2C (Business-to-Business-to-Consumer):<br>

**B2B (Clientes directos):** <br> 
- Cafeterías independientes en zonas urbanas de alta demanda
- Cadenas de cafeterías con múltiples sedes
- Espacios de coworking con áreas de cafetería
- Restaurantes de tamaño mediano
<br>

**B2C (Usuarios finales):** <br> 
- Comensales que utilizan la aplicación móvil para consultar disponibilidad y realizar reservas
<br>

**Modelo de ingresos:** <br> 
- Venta inicial del hardware (sensores IoT + instalación)
- Licenciamiento mensual del software (SaaS por sede)
- Soporte técnico y mantenimiento
- Planes premium con analytics avanzados
<br>

### 1.1.2 Expectativas del Cliente
Entregables esperados:
- **Informe Técnico Detallado:**
  - Vulnerabilidades identificadas con severidad CVSS
  - Proof of Concepts reproducibles
  - Pasos exactos de explotación
  - Recomendaciones técnicas específicas con ejemplos de código
- **Informe Ejecutivo:**
  - Resumen para presentar a inversionistas
  - Impacto en negocio traducido a términos comerciales
  - Roadmap de seguridad priorizado
  - Métricas de mejora esperada
- **Plan de Remediación Ejecutable:**
  - Priorización clara
  - Esfuerzo estimado por corrección
  - Guías de implementación para el equipo de desarrollo
  - Quick wins vs. proyectos a largo plazo
- **Sesión de Transferencia de Conocimiento:**
  - Presentación al equipo técnico de TAVOLO
  - Demo en vivo de explotaciones críticas
  - QA técnico
  - Recomendaciones de herramientas


### 1.2. Consultora de Ciberseguridad (Equipo)
### 1.2.1 Descripción de la Consultora

**Razón Social:** PentGuin Cybersecurity Consulting
<br>
**Tipo de empresa:** Consultora de seguridad ofensiva (Ethical Hacking & Penetration Testing)
<br>
**Especialización:** Pentesting de aplicaciones web, APIs y aplicaciones móviles
<br>
**Ubicación:** Lima, Perú
<br>
**Formación:** Estudiantes de Ingeniería de Software de la Universidad Peruana de Ciencias Aplicadas
<br><br>
**Misión**
<br>
Proporcionar servicios especializados de Ethical Hacking y Penetration Testing con un enfoque académico-profesional, aplicando metodologías reconocidas internacionalmente (PTES, OWASP) y herramientas de código abierto, para identificar vulnerabilidades en sistemas informáticos y ofrecer soluciones de remediación efectivas que protejan los activos digitales de nuestros clientes, con especial énfasis en startups tecnológicas y empresas en proceso de transformación digital.
<br><br>


**Visión**
<br>
Ser reconocidos en el ecosistema de ciberseguridad de América Latina como una consultora de nueva generación que combina rigor académico con expertise técnico de vanguardia, estableciendo un nuevo estándar en servicios de Ethical Hacking para startups tecnológicas y PyMEs en proceso de transformación digital, donde la innovación, la ética y la excelencia técnica impulsen una cultura de seguridad proactiva desde las etapas tempranas de los negocios digitales.
<br><br>

**Propuesta de Valor:**
¿Por qué contratar a nuestra consultora?

1. **Perspectiva Fresca:** Como equipo en formación, aportamos conocimientos actualizados en las últimas tendencias de ciberseguridad, frameworks modernos y vectores de ataque emergentes.
2. **Enfoque Metodológico Riguroso:** Aplicamos metodologías ágiles (Scrum) combinadas con estándares de pentesting (PTES, OWASP), garantizando un proceso estructurado, documentado y reproducible.
3. **Especialización en Tecnologías Emergentes:** Experiencia práctica en testing de soluciones IoT, aplicaciones móviles nativas, arquitecturas cloud y APIs RESTful modernas.
4. **Documentación Exhaustiva:** Entregables con estándares académico-profesionales, incluyendo evidencias visuales, PoCs funcionales, código comentado y recomendaciones accionables.
5. **Relación Costo-Beneficio:** Servicios de calidad profesional adaptados a presupuestos de startups y PyMEs, sin comprometer la profundidad del análisis.
6. **Ética y Confidencialidad Absoluta:** Compromiso total con el código de ética de ACM/IEEE/CIP, respeto estricto de Rules of Engagement y confidencialidad de información sensible.

**Servicios Ofrecidos en este Proyecto:**

| Componente             | Tipo de Prueba                 | Herramientas Principales         |
| ---------------------- | ------------------------------ | -------------------------------- |
| Aplicaciones Web       | Web Application Pentesting     | Burp Suite Pro, OWASP ZAP, Nikto |
| APIs REST              | API Security Testing           | Postman, Burp Suite, Arjun, ffuf |
| Aplicación Móvil       | Mobile App Security Assessment | MobSF, Frida, APKTool, Jadx      |
| Infraestructura de Red | Network Pentesting             | Nmap, Masscan, Metasploit        |
| Social Engineering     | Phishing Simulation            | GoPhish, SET                     |


### 1.2.2 Perfiles de los integrantes – Consultora PentGuin

| Campo | Información |
|-------|-------------|
| **Nombre de alumno** | Juan Fabritzzio Pescoran Angulo |
| **Foto** | [Insertar foto profesional 200x200px] |
| **Código de estudiante** | U20221C936 |
| **Carrera** | Ingeniería de Software |
| **Rol Scrum** | Scrum Master |
| **Correo electrónico** | u20221c936@upc.edu.pe |
| **Competencias Técnicas** | Encargado de coordinar las ceremonias Scrum y asegurar la correcta aplicación del marco ágil dentro del proyecto de pentesting. Posee habilidades en liderazgo, planificación y control de calidad del proceso. Experiencia en uso de herramientas como Jira, GitHub Projects y GitFlow. |
| **Valor que aporta** | Garantiza que el equipo mantenga comunicación efectiva, priorización de tareas y cumplimiento de entregables en cada sprint. |

| Campo | Información |
|-------|-------------|
| **Nombre de alumno** | Diego Ulises Soto Quispe |
| **Foto** | [Insertar foto profesional 200x200px] |
| **Código de estudiante** | U202214477 |
| **Carrera** | Ingeniería de Software |
| **Rol Scrum** | Product Owner |
| **Correo electrónico** | u202214477@upc.edu.pe |
| **Competencias Técnicas** | Responsable de definir el alcance y priorizar las pruebas de seguridad según el impacto en el negocio. Experiencia en diseño de arquitecturas seguras, documentación técnica y gestión de requisitos. |
| **Valor que aporta** | Representa los intereses del cliente TAVOLO y asegura que cada entregable cumpla objetivos estratégicos de seguridad. |

| Campo | Información |
|-------|-------------|
| **Nombre de alumno** | Aldo Alberto Baldeón Fabián |
| **Foto** | [Insertar foto profesional 200x200px] |
| **Código de estudiante** | U202215285 |
| **Carrera** | Ingeniería de Software |
| **Rol Scrum** | Especialista Web / Pentester Web |
| **Correo electrónico** | u202215285@upc.edu.pe |
| **Competencias Técnicas** | Encargado del análisis de vulnerabilidades en portales web, implementación de pruebas OWASP Top 10 y desarrollo de PoCs controladas. Manejo avanzado de Burp Suite, OWASP ZAP, Nikto y sqlmap. |
| **Valor que aporta** | Detecta y documenta fallos de seguridad en las capas de presentación y lógica de negocio, asegurando la trazabilidad de cada hallazgo. |

| Campo | Información |
|-------|-------------|
| **Nombre de alumno** | Brenda Lucía Gamio Upiachihua |
| **Foto** | [Insertar foto profesional 200x200px] |
| **Código de estudiante** | U202102344 |
| **Carrera** | Ingeniería de Software |
| **Rol Scrum** | Especialista en APIs/Móvil |
| **Correo electrónico** | u202102344@upc.edu.pe |
| **Competencias Técnicas** | Ejecuta pruebas sobre endpoints REST y aplicaciones móviles Android. Experiencia con herramientas MobSF, Postman, Frida y Burp Suite Mobile Assistant. |
| **Valor que aporta** | Identifica vulnerabilidades en autenticación, autorización y cifrado dentro de componentes móviles y APIs. |

| Campo | Información |
|-------|-------------|
| **Nombre de alumno** | Angelo Marcio Curi Marcelo |
| **Foto** | <img src="https://raw.githubusercontent.com/FullStack-Fury/final-report/main/assets/Angelo.png" alt="Foto profesional de Angelo" width="200" height="200"> |
| **Código de estudiante** | U202022387 |
| **Carrera** | Ingeniería de Software |
| **Rol Scrum** | Documentador / Analista de Seguridad |
| **Correo electrónico** | u202022387@upc.edu.pe |
| **Competencias Técnicas** | Encargado de consolidar evidencias técnicas, elaborar reportes ejecutivos y redactar las conclusiones del proyecto. Experiencia en análisis de vulnerabilidades, redacción técnica y cumplimiento de normas ISO/IEC 27001. |
| **Valor que aporta** | Garantiza la trazabilidad, claridad y consistencia de toda la documentación técnica entregada al cliente. |


### 1.3. Solution Profile
### 1.3.1 Antecedentes y Problemática desde la Perspectiva de Seguridad
Para comprender completamente el contexto del proyecto de pentesting, se aplicó la técnica estructurada de análisis **The 5 'W's y 2 'H's**, que permite definir con precisión el problema, alcance y justificación del servicio de seguridad ofensiva.

### **What (¿Qué necesita ser evaluado?)**

**Activos críticos en alcance:**

TAVOLO Tech Solutions requiere una evaluación exhaustiva de seguridad de su plataforma tecnológica completa que incluye:


| Activo | Descripción | Datos Sensibles | Impacto si Comprometido |
|--------|-------------|-----------------|-------------------------|
| **API REST** | Backend que procesa solicitudes de apps y sensores | Tokens de autenticación, datos de usuarios, info de reservas | CRÍTICO - Acceso total a la plataforma |
| **App Móvil Android** | Aplicación del comensal | Credenciales, datos personales, tokens JWT | ALTO - Robo de identidad, acceso no autorizado |
| **Portal Web Administrativo** | Panel de gestión de sedes | Credenciales admin, métricas de negocio, configuración de mesas | CRÍTICO - Control total de operación |
| **Landing Page** | Sitio informativo público | Formularios de contacto, información corporativa | MEDIO - Phishing, defacement |
| **Base de Datos** | PostgreSQL/MongoDB | Todos los datos de usuarios, reservas, sedes | CRÍTICO - Pérdida total de información |
| **Sistema de Autenticación** | JWT/OAuth | Tokens de sesión, hashes de contraseñas | CRÍTICO - Acceso masivo no autorizado |

**Vectores de Ataque Potenciales a evaluar:**

1. **OWASP Top 10 Web Applications:**
  - A01:2021 - Broken Access Control (IDOR en APIs de reservas)
  - A02:2021 - Cryptographic Failures (Datos en tránsito sin HTTPS, contraseñas débiles)
  - A03:2021 - Injection (SQLi en formularios, NoSQL Injection en MongoDB)
  - A07:2021 - XSS (Cross-Site Scripting en dashboards administrativos)
  - A05:2021 - Security Misconfiguration (Cabeceras HTTP ausentes, CORS permisivo)


2. **OWASP API Security Top 10:**
  - API1 - Broken Object Level Authorization (acceso a reservas de otros usuarios)
  - API2 - Broken Authentication (JWT débil, sin expiración)
  - API8 - Security Misconfiguration (Métodos HTTP innecesarios habilitados)


3. **OWASP Mobile Top 10:**
   - M1: Improper Platform Usage
   - M2: Insecure Data Storage (credenciales en SharedPreferences)
   - M3: Insecure Communication (HTTP en lugar de HTTPS)
   - M4: Insecure Authentication
   - M5: Insufficient Cryptography
   - M6: Insecure Authorization
   - M8: Code Tampering (APK sin ofuscación)
   - M9: Reverse Engineering

### **Why (¿Por qué es crítico realizar este pentesting AHORA?)**<br>

**Justificación Técnica:**

El ecosistema de TAVOLO combina múltiples superficies de ataque (web + API + móvil + IoT), cada una con vulnerabilidades específicas. Según estudios de Verizon DBIR 2024:
- **43% de brechas** involucran aplicaciones web
- **30% de vulnerabilidades** son en APIs mal configuradas

**Justificación de Negocio:**

| Amenaza | Probabilidad | Impacto Estimado | Consecuencias |
|---------|--------------|------------------|---------------|
| **Data Breach (robo de datos)** | Alta | CRÍTICO | Multa ARPDP: S/ 500K<br>Pérdida de confianza<br>Cancelación de contratos B2B |
| **Manipulación de sensores IoT** | Media | ALTO | Disponibilidad falsa de mesas<br>Pérdida de credibilidad<br>Churn de usuarios |
| **Ransomware** | Media | CRÍTICO | Indisponibilidad 48-72h<br>Rescate: $20K-$50K<br>Pérdida de ingresos: $10K/día |
| **Account Takeover admin** | Alta | CRÍTICO | Control total de operación<br>Eliminación maliciosa de datos |

**ROI Estimado del Pentesting:**
- **Inversión:** S/ 25,500 (servicio + remediación inicial)
- **Ahorro potencial:** S/ 500,000 - S/ 2,000,000 (multas + reputación)
- **ROI:** **800% - 2,600%**


### **Who (¿Quién está involucrado?)** <br>
**Partes Principales:**

**Cliente (TAVOLO Tech Solutions S.A.C.):**

- **CTO:** Baldeon Fabian, Aldo Alberto — U202122633
- **Tech Lead:** Cama Salvatierra, Jimena Tamara — U202210778
- **DevOps Engineer:** Castillo Castillo, Jair Alexander — U202211390
- **Product Manager:** La Torre Valle, Franz Jair — U202012378
- **CEO:** Quezada Portalatino, Barbara Susana — U202211800

**Consultora (PentGuin Cybersecurity Consulting):**
- **Scrum Master:** Pescoran Angulo, Juan Fabritzzio – Coordinación del proyecto, facilitación de ceremonias ágiles.
- **Product Owner:** Soto Quispe, Diego Ulises – Priorización de pruebas según riesgo del negocio y requerimientos del cliente.
- **Especialista Web:** Gamio Upiachihua, Brenda Lucía – Pruebas técnicas de seguridad en aplicaciones web (OWASP, Burp, etc.).
- **Especialista APIs:** Baldeon Fabian, Aldo Alberto – Reconocimiento y pentesting sobre servicios expuestos y endpoints API.
- **Documentador:** Curi Marcelo, Angelo Marcio – Generación de reportes, evidencias técnicas y control de entregables.

**Stakeholders Indirectos:**
- **Cafeterías clientes de TAVOLO** (15 sedes actualmente) - Afectados si hay breach
- **Usuarios comensales** (~5,000 usuarios registrados) - Datos personales en riesgo
- **Inversionistas de TAVOLO** - Requieren auditoría para próxima ronda de inversión


### **Where (¿Dónde están las vulnerabilidades esperadas?)**
  - **Perímetro Externo (Accesible desde Internet):**
    - Landing Page
    - App Web del Comensal
    - API Gateway
    - Endpoints de descarga de APK  
  - **Zona DMZ (Cloud):**
    - API REST Backend
    - WebSockets Server
    - Message Broker
  - **Zona interna (Backend):**
    - Servidores de Aplicación
    - Base de Datos
    - File Storage
    - Admin Panel Backend
  - **Aplicación móvil:**
    - APK Android
    - Comunicación con API
    - Tokens almacenados
<br>

### **When (Cuándo):** Contextualiza temporalmente

**Timeline del Proyecto (15 semanas):**
| Fase | Semanas | Fechas | Hitos Clave |
|------|---------|--------|-------------|
| **Pre-engagement** | Semana 1 | [01-07 Marzo 2025] | Firma RoE, NDA, configuración de accesos |
| **Sprint 1: Reconocimiento** | Semanas 2-3 | [08-21 Marzo 2025] | Mapeo completo de superficie de ataque |
| **Sprint 2: Análisis** | Semanas 4-6 | [22 Mar - 11 Abr 2025] | Escaneo automatizado, enumeración |
| **Sprint 3: Explotación** | Semanas 7-9 | [12 Abr - 02 May 2025] | PoCs de vulnerabilidades críticas, **TP1** |
| **Sprint 4: Post-explotación** | Semanas 10-12 | [03-23 Mayo 2025] | Escalamiento, movimiento lateral |
| **Sprint 5: Informe Final** | Semanas 13-15 | [24 May - 13 Jun 2025] | Consolidación, **TF1**, presentación |

**Razones de Urgencia (Why Now):**

1. **Expansión Comercial Inminente:**
   - TAVOLO está en conversaciones con 2 cadenas de cafeterías (50+ sedes potenciales)
   - Clientes corporativos exigen certificación ISO 27001 o auditoría reciente
   - Próxima ronda de inversión Serie A ($500K) requiere due diligence de seguridad

2. **Riesgos Regulatorios:**
   - Ley de Protección de Datos Personales Perú (Ley N° 29733) - Multas hasta 100 UIT (~S/ 500,000)
   - GDPR si expanden a Europa
   - Obligación de notificar brechas en 72 horas



### **How (¿Cómo se ejecutará el pentesting?)** 
**Metodología Integrada:**

PTES (Penetration Testing Execution Standard) + OWASP + Scrum

- **Phase 1: Pre-engagement Interactions**
  - Firma de Rules of Engagement (RoE) y NDA
  - Definición de alcance (in-scope / out-of-scope)
  - Provisión de credenciales de prueba
  - Configuración de ambiente de staging


- **Phase 2-3: Intelligence Gathering + Threat Modeling (Sprint 1)**
  - **Reconocimiento Pasivo:** OSINT, Google Dorking, Shodan, subfinder
  - **Reconocimiento Activo:** Nmap full scan, service fingerprinting
  - **Deliverable:** Mapa de superficie de ataque + Matriz de amenazas
  

- **Phase 4: Vulnerability Analysis (Sprint 2)**
  - **Automatizado:** Nessus, Nikto, OWASP ZAP, MobSF
  - **Manual:** Análisis de lógica de negocio, configuraciones
  - **Deliverable:** Matriz preliminar de vulnerabilidades (CVSS)


- **Phase 5: Exploitation (Sprint 3)**
  - Desarrollo de PoCs para vulnerabilidades críticas/altas
  - Pruebas controladas (sin causar daño real)
  - **Deliverable:** PoCs documentados + TP1


- **Phase 6: Post-Exploitation (Sprint 4)**
  - Simulación de escalamiento de privilegios
  - Análisis de impacto completo
  - **Deliverable:** Cadenas de ataque documentadas


- **Phase 7: Reporting (Sprint 5)**
  - Informe técnico + ejecutivo
  - Plan de remediación priorizado
  - **Deliverable:** TF1 + presentación final


### **How much (¿Cuánto impacto/esfuerzo?)**
**Esfuerzo del Equipo de la Consultora:**

| Fase                             | Horas por Integrante | Total Equipo (5 personas) | Semanas |
| -------------------------------- | -------------------- | ------------------------- | ------- |
| Pre-engagement                   | 5h                   | 25h                       | 0.5     |
| Sprint 1: Reconnaissance         | 20h                  | 100h                      | 2       |
| Sprint 2: Vulnerability Analysis | 25h                  | 125h                      | 3     |
| Sprint 3: Exploitation           | 30h                  | 150h                      | 3       |
| Sprint 4: Post-exploitation      | 25h                  | 125h                      | 3       |
| Sprint 5: Reporting              | 20h                  | 100h                      | 3       |
| **TOTAL**                        | **125h**             | **625h**                  | **15**  |


<br>
  **Inversión del Cliente (TAVOLO):**
<br>

| Concepto                          | Estimado                                    |
| --------------------------------- | ------------------------------------------- |
| **Servicio de Pentesting**        | S/ 15,000 - S/ 25,000 (académico-comercial) |
| **Horas de coordinación interna** | 40-60 horas (Tech Lead + DevOps)            |
| **Recursos de infraestructura**   | S/ 500 (ambientes de prueba adicionales)    |
| **Remediación post-pentesting**   | S/ 10,000 - S/ 50,000 (según hallazgos)     |
| **TOTAL INVERSIÓN**               | **S/ 25,500 - S/ 75,500**                       |


<br>
  **Retorno de Inversión (ROI):**
<br>

| Beneficio                              | Ahorro Estimado                                   |
| -------------------------------------- | ------------------------------------------------- |
| **Evitar data breach**                 | S/ 500,000 - S/ 2,000,000 (multas + reputación)   |
| **Certificación ISO 27001 futura**     | S/ 30,000 (costos reducidos) |
| **Cierre de contratos B2B**            | S/ 100,000+ (confianza de clientes corporativos)  |
| **Reducción de riesgos operacionales** | S/ 50,000 (downtime evitado)                      |
| **ROI Estimado**                       | **800% - 2,600%**                                 |


<br>
  **Métricas de Éxito del Pentesting:**
<br>

| Métrica                               | Objetivo                       |
| ------------------------------------- | ------------------------------ |
| **Cobertura de superficie de ataque** | ≥ 95%                          |
| **Vulnerabilidades identificadas**    | ≥ 30 (expectativa)             |
| **Vulnerabilidades críticas**         | Identificar todas las posibles |
| **False positives**                   | < 10%                          |
| **Reproducibilidad de PoCs**          | 100%                           |
| **Satisfacción del cliente**          | ≥ 4.5/5                        |
| **Tiempo de respuesta a críticas**    | < 4 horas                      |

### 1.3.2. Objetivos del Pentesting

#### Objetivo General

Evaluar de manera integral la postura de seguridad de la plataforma tecnológica de TAVOLO Tech Solutions S.A.C., identificando vulnerabilidades críticas en sus aplicaciones web, APIs REST, aplicación móvil Android y servicios de red, mediante la aplicación de metodologías internacionales reconocidas (PTES, OWASP, NIST SP 800-115) y técnicas de ethical hacking, con el fin de proporcionar recomendaciones técnicas y estratégicas que permitan fortalecer la protección de activos digitales, garantizar la confidencialidad e integridad de datos sensibles de usuarios y cafeterías clientes, y cumplir con normativas de protección de datos vigentes (Ley N° 29733), asegurando la continuidad operativa del negocio y generando confianza en inversionistas y clientes B2B.

#### Objetivos Específicos

**OE1: Mapear la superficie de ataque completa de TAVOLO**

Realizar reconocimiento exhaustivo (pasivo y activo) de toda la infraestructura tecnológica de TAVOLO mediante técnicas OSINT, Google Dorking, Shodan, subfinder, y escaneo de puertos con Nmap y Masscan, con el propósito de identificar todos los subdominios, hosts y servicios expuestos a Internet, descubrir puertos abiertos y servicios en ejecución con sus versiones, mapear la arquitectura de red (perímetro externo, DMZ, backend), documentar tecnologías utilizadas (frameworks, servidores web, bases de datos), y generar un inventario completo de activos digitales críticos.

**OE2: Identificar y clasificar vulnerabilidades según OWASP Top 10**

Ejecutar análisis de vulnerabilidades en aplicaciones web, APIs REST y aplicación móvil siguiendo las guías OWASP Top 10 (Web Applications, API Security, Mobile), utilizando herramientas automatizadas (Nessus, Nikto, OWASP ZAP, MobSF) y técnicas manuales de pentesting, para detectar vulnerabilidades de tipo Broken Access Control (IDOR), Injection (SQLi, NoSQLi), XSS, CSRF, identificar fallas de autenticación y autorización (JWT débil, sesiones inseguras), evaluar configuraciones inseguras (CORS permisivo, cabeceras HTTP ausentes), y clasificar cada vulnerabilidad según severidad CVSS v3.1 (Crítica, Alta, Media, Baja).

**OE3: Desarrollar Proof of Concepts funcionales para vulnerabilidades críticas**

Crear demostraciones técnicas reproducibles de las vulnerabilidades de mayor impacto identificadas en los sistemas de TAVOLO, mediante desarrollo de exploits controlados y no destructivos, documentación paso a paso de la cadena de ataque, capturas de pantalla y videos demostrativos, scripts automatizados cuando aplique, y validación del impacto real en el negocio (acceso a datos sensibles, escalamiento de privilegios, manipulación de reservas).

**OE4: Evaluar la seguridad de la API REST Backend**

Realizar pentesting especializado sobre los endpoints API de TAVOLO siguiendo la metodología OWASP API Security Top 10, con énfasis en Broken Object Level Authorization (BOLA) intentando acceder a reservas y mesas de otros mediante manipulación de IDs, evaluar robustez de JWT (algoritmo, expiración, secretos débiles), detectar exposición excesiva de datos en respuestas JSON, probar límites de rate limiting, intentar acceder a funciones administrativas sin privilegios, y validar métodos HTTP permitidos y configuraciones CORS.

**OE5: Analizar la seguridad de la aplicación móvil Android**

Ejecutar análisis de seguridad integral de la APK de TAVOLO mediante técnicas de ingeniería inversa, análisis estático con MobSF, APKTool y Jadx para descompilar APK y revisar código fuente, identificar hardcoded secrets (API keys, tokens, URLs), detectar almacenamiento inseguro de datos, y realizar análisis dinámico con Frida y Burp Suite Mobile Assistant para interceptar tráfico HTTPS, validar certificate pinning, detectar comunicación sin cifrar, y evaluar manejo de tokens de sesión.

**OE6: Validar controles de seguridad en autenticación y gestión de sesiones**

Evaluar la robustez de los mecanismos de autenticación y autorización en todos los componentes de TAVOLO (web, API, móvil), específicamente validando políticas de contraseñas, mecanismos de recuperación de contraseña, protección contra brute force, generación de tokens JWT, expiración y renovación de tokens, revocación de sesiones, manejo de cookies, validación de roles y permisos, y protección contra IDOR.

**OE7: Elaborar plan de remediación priorizado con impacto en el negocio**

Desarrollar un roadmap estratégico de seguridad para TAVOLO que incluya clasificación de vulnerabilidades por severidad CVSS con tiempos de remediación (Críticas 0-7 días, Altas 8-30 días, Medias 1-3 meses), análisis costo-beneficio con esfuerzo estimado de corrección, identificación de Quick Wins versus proyectos a largo plazo, recomendaciones técnicas accionables con ejemplos de código corregido, configuraciones seguras de servidores, y guías de implementación para el equipo de TAVOLO.

### 1.4. Aceptación del Servicio de Pentesting (Rules of Engagement)

## DOCUMENTO DE REGLAS DE COMPROMISO

### SERVICIO DE PENETRATION TESTING

**Proyecto:** Ethical Hacking y Pentesting TAVOLO Tech Solutions S.A.C.  
**Código de Proyecto:** UPC-ANTIHACKING-2025-TAVOLO-01  
**Fecha de emisión:** 25 de Agosto de 2024  
**Vigencia:** Del 25 de Agosto de 2025 al 30 de Noviembre de 2025  
**Versión del documento:** 1.0

### 1. IDENTIFICACIÓN DE LAS PARTES

#### 1.1 CLIENTE (Empresa Evaluada)

| Campo | Información |
|-------|-------------|
| **Razón Social** | TAVOLO Tech Solutions S.A.C. |
| **Sector** | Tecnología - FoodTech (IoT para sector gastronómico) |
| **Dirección Legal** | Av. Javier Prado Este 4200, Santiago de Surco, Lima, Perú |
| **Representante Legal Autorizado** | Quezada Portalatino, Barbara Susana |
| **Cargo** | CEO (Chief Executive Officer) |
| **Correo Electrónico** | barbara.quezada@tavolo.pe |
| **Teléfono de Contacto** | +51 987 654 321 |
| **Contacto Técnico Principal** | Baldeon Fabian, Aldo Alberto |
| **Cargo Contacto Técnico** | CTO (Chief Technology Officer) |
| **Email Contacto Técnico** | aldo.baldeon@tavolo.pe |

#### 1.2 CONSULTORA DE SEGURIDAD (Proveedor del Servicio)

| Campo | Información                                                        |
|-------|--------------------------------------------------------------------|
| **Nombre de la Consultora** | PentGuin Cybersecurity Consulting                                  |
| **Tipo de Entidad** | Equipo académico - Universidad Peruana de Ciencias Aplicadas (UPC) |
| **Curso** | 1ASI0665 - Anti-Hacking y Nuevas Tendencias de Seguridad           |
| **Profesor Supervisor** | Vera Olivera, David Carlos                                         |
| **Representante del Equipo** | Pescoran Angulo, Juan Fabritzzio                                   |
| **Cargo Representante** | Scrum Master / Líder del Proyecto                                  |
| **Correo Institucional** | u20221c936@upc.edu.pe                                              |

**Integrantes del Equipo de Pentesting:**

| Nombre Completo | Código UPC | Rol Scrum | Email |
|-----------------|------------|-----------|-------|
| Pescoran Angulo, Juan Fabritzzio | U20221C936 | Scrum Master | u20221c936@upc.edu.pe |
| Soto Quispe, Diego Ulises | U202214477 | Product Owner | u202214477@upc.edu.pe |
| Baldeon Fabian, Aldo Alberto | U202215285 | Pentester Web | u202215285@upc.edu.pe |
| Gamio Upiachihua, Brenda Lucía | U202102344 | Pentester APIs/Móvil | u202102344@upc.edu.pe |
| Curi Marcelo, Angelo Marcio | U202022387 | Documentador/Analista | u202022387@upc.edu.pe |

### 2. OBJETIVO DEL SERVICIO

Realizar pruebas de penetración controladas y éticas sobre la infraestructura tecnológica de TAVOLO Tech Solutions S.A.C., con los siguientes propósitos:

**Objetivos Principales:**

1. Identificar vulnerabilidades de seguridad en aplicaciones web, APIs REST, aplicación móvil Android y servicios de red
2. Evaluar la postura de seguridad general de los activos digitales de TAVOLO
3. Detectar configuraciones inseguras que puedan comprometer confidencialidad, integridad o disponibilidad de datos
4. Validar controles de autenticación, autorización y gestión de sesiones
5. Demostrar impacto real mediante Proof of Concepts reproducibles y controlados
6. Proporcionar recomendaciones técnicas y ejecutivas para remediación de vulnerabilidades
7. Generar evidencia documentada que permita auditorías futuras y cumplimiento normativo (Ley N° 29733)
8. Fortalecer la confianza de clientes B2B e inversionistas mediante validación independiente de seguridad

**Metodologías Aplicadas:**

PTES (Penetration Testing Execution Standard), OWASP Testing Guide v4.2, OWASP Top 10 (Web Applications, API Security, Mobile), NIST SP 800-115 (Technical Guide to Information Security Testing), y Scrum (gestión ágil del proyecto).

### 3. ALCANCE AUTORIZADO (IN-SCOPE)

La consultora PentGuin está expresamente autorizada a realizar pruebas de seguridad sobre los siguientes activos digitales de TAVOLO:

#### 3.1 Aplicaciones Web

| Componente | Descripción | URLs Autorizadas |
|------------|-------------|------------------|
| **Landing Page Staging** | Sitio web informativo público | https://staging.tavolo.pe |
| **Portal Web del Comensal Staging** | Aplicación web para usuarios finales | https://app-staging.tavolo.pe |
| **Panel Administrativo Staging** | Dashboard de gestión de sedes | https://admin-staging.tavolo.pe |

**Credenciales Proporcionadas:**

Usuario Regular: test.user@tavolo.pe / TestUser2024  
Usuario Admin: admin.test@tavolo.pe / AdminTavolo2024  
Usuario Manager: manager.test@tavolo.pe / ManagerTavolo2024

#### 3.2 APIs REST

**Endpoint Base:** https://api-staging.tavolo.pe

**Endpoints Específicos Autorizados:**

| Ruta | Método | Descripción |
|------|--------|-------------|
| /api/v1/auth/login | POST | Autenticación de usuarios |
| /api/v1/auth/register | POST | Registro de nuevos usuarios |
| /api/v1/auth/reset-password | POST | Recuperación de contraseña |
| /api/v1/users/{id} | GET, PUT, DELETE | Gestión de perfiles de usuario |
| /api/v1/reservations | GET, POST, PUT, DELETE | Gestión de reservas |
| /api/v1/tables | GET, POST, PUT | Información de mesas |
| /api/v1/cafeterias | GET, POST, PUT | Gestión de sedes |
| /api/v1/analytics | GET | Métricas y estadísticas |
| /api/v1/sensors | POST | Datos de sensores IoT |

**Documentación API:** https://api-staging.tavolo.pe/docs (Swagger)

#### 3.3 Aplicación Móvil Android

| Componente | Versión | Package Name |
|------------|---------|--------------|
| **APK de Prueba** | v1.2.3-staging | com.tavolo.app.staging |

**Ubicación de descarga:** https://staging.tavolo.pe/downloads/tavolo-staging-v1.2.3.apk

**Aspectos Autorizados para Análisis:**

Descompilación del APK con APKTool y Jadx, análisis estático con MobSF, análisis dinámico con Frida y Burp Suite Mobile Assistant, ingeniería inversa del código fuente, interceptación de tráfico HTTPS, búsqueda de hardcoded secrets, evaluación de almacenamiento inseguro de datos, pruebas de bypass de root detection, y fuzzing de inputs.

#### 3.4 Infraestructura de Red (Staging)

| Componente | IP/Rango Autorizado | Acceso |
|------------|---------------------|--------|
| **Servidores Staging** | 192.168.100.10 - 192.168.100.50 | VPN proporcionada |
| **Load Balancer Staging** | 192.168.100.5 | VPN |
| **Base de Datos Staging** | 192.168.100.20 (PostgreSQL), 192.168.100.21 (MongoDB) | Credenciales READ-ONLY |

**Credenciales Base de Datos (READ-ONLY):**

PostgreSQL: pentester_readonly / TestPostgres2024 (DB: tavolo_staging)  
MongoDB: pentester_readonly / TestMongo2024 (DB: tavolo_staging)

**Configuración VPN:** Servidor vpn-staging.tavolo.pe:1194 (archivo .ovpn proporcionado)

### 4. ACTIVOS FUERA DE ALCANCE (OUT-OF-SCOPE)

La consultora NO está autorizada bajo ninguna circunstancia a realizar pruebas sobre:

#### 4.1 Ambientes de Producción (PROHIBIDO)

Dominios de producción (tavolo.pe, www.tavolo.pe, app.tavolo.pe, admin.tavolo.pe, api.tavolo.pe), servidores de producción, base de datos de producción, CDN de producción, balanceadores de carga de producción, y aplicación móvil publicada en Google Play Store (com.tavolo.app).

#### 4.2 Sistemas de Terceros (PROHIBIDO)

Pasarelas de pago (Stripe, PayPal, Niubiz), servicios de mensajería (Twilio, SendGrid, AWS SES), servicios de autenticación de terceros (Google OAuth, Facebook Login), proveedores de infraestructura cloud fuera del tenant de TAVOLO, servicios de analytics (Google Analytics, Mixpanel), y CDN de terceros.

#### 4.3 Ataques Destructivos (PROHIBIDO)

Denial of Service (DoS/DDoS), ransomware o malware real, eliminación o modificación de datos, interrupción de servicios, exfiltración masiva de datos (máximo 10 registros para PoC), y ataques a la cadena de suministro.

#### 4.4 Ingeniería Social No Autorizada (PROHIBIDO)

Phishing masivo a empleados sin aprobación previa, vishing, smishing, pretexting o suplantación de identidad, envío de USB maliciosos, e ingreso físico a oficinas de TAVOLO.

#### 4.5 Datos de Clientes de TAVOLO (PROHIBIDO)

Sistemas informáticos de las cafeterías clientes de TAVOLO, datos personales de usuarios finales reales, información de transacciones reales, y datos de sensores IoT instalados en cafeterías reales.

### 5. LIMITACIONES Y RESTRICCIONES TÉCNICAS

**Restricciones de Explotación:**

No DoS/DDoS (prohibido saturar servicios), respetar rate limiting (máximo 100 requests/minuto por endpoint API), no credential stuffing masivo (máximo 50 intentos de login), exfiltración limitada (máximo 10 registros para PoC), no reverse shell persistente (shells solo durante sesión activa), y no modificación de configuraciones críticas (no cambiar contraseñas de admin, no eliminar usuarios).

**Herramientas Autorizadas:**

Reconocimiento: Nmap, Masscan, Shodan, Censys, subfinder, Amass, OSINT tools, Google Dorking  
Análisis de Vulnerabilidades: Nessus, OpenVAS, Nikto, OWASP ZAP, Burp Suite Professional, sqlmap, MobSF  
Explotación: Metasploit Framework, Burp Intruder, Hydra, John the Ripper, Hashcat, Frida  
Post-Explotación: Mimikatz, PowerSploit, LinPEAS, WinPEAS  
Análisis de Tráfico: Wireshark, tcpdump, Burp Suite Mobile Assistant

### 6. PERIODO DE EJECUCIÓN Y VENTANAS DE PRUEBA

**Timeline del Proyecto:**

| Fase | Duración | Fechas | Hitos Clave |
|------|----------|--------|-------------|
| **Pre-engagement** | 1 semana | 25-31 Agosto 2024 | Firma RoE, configuración accesos |
| **Sprint 1: Reconocimiento** | 2 semanas | 01-14 Septiembre 2024 | OSINT, mapeo superficie de ataque |
| **Sprint 2: Enumeración** | 3 semanas | 15 Sep - 05 Oct 2024 | Escaneo, análisis de vulnerabilidades |
| **Sprint 3: Explotación** | 3 semanas | 06-26 Octubre 2024 | PoCs, TP1 |
| **Sprint 4: Post-explotación** | 3 semanas | 27 Oct - 16 Nov 2024 | Escalamiento, movimiento lateral |
| **Sprint 5: Reporte** | 2 semanas | 17-30 Noviembre 2024 | Informe final, TF1 |

**Duración Total:** 14 semanas (25 Agosto - 30 Noviembre 2024)

**Horarios Autorizados para Pruebas:**

Reconocimiento Pasivo: 24/7 (no requiere interacción con sistemas)  
Reconocimiento Activo y Escaneo: Lunes a Viernes 08:00-23:00, Sábados 09:00-18:00 (Hora Perú UTC-5)  
Explotación y Pruebas Intrusivas: Lunes a Viernes 09:00-20:00 (horario laboral de equipo técnico)

**Notificaciones antes de Pruebas Críticas:**

La consultora debe notificar con 24 horas de anticipación cuando planea ejecutar explotación de vulnerabilidades críticas o altas, pruebas que puedan causar indisponibilidad temporal, fuzzing agresivo, o intentos de escalamiento de privilegios.

**Canales de Notificación:**

Email: aldo.baldeon@tavolo.pe  
Slack: Canal #pentesting-PentGuin
WhatsApp: Solo emergencias

### 7. RESPONSABILIDADES DE LAS PARTES

#### 7.1 Responsabilidades del CLIENTE (TAVOLO)

TAVOLO se compromete a:

1. Proporcionar credenciales de prueba válidas, configurar VPN para acceso a red interna staging, entregar APK de aplicación móvil staging, y proveer documentación de API
2. Designar a Aldo Alberto Baldeon Fabian (CTO) como contacto principal con disponibilidad en horario laboral (9 AM - 6 PM) y contacto de emergencia 24/7 para vulnerabilidades críticas
3. Mantener ambientes staging/dev disponibles durante las 14 semanas del proyecto y notificar con 48 horas de anticipación cualquier mantenimiento planificado
4. Participar en reuniones de seguimiento semanales (Viernes 4-5 PM), revisar y validar vulnerabilidades críticas en menos de 48 horas, y aprobar contenido del informe final antes de entrega formal
5. No responsabilizar a PentGuin por caídas temporales de staging/dev durante pruebas autorizadas
6. No divulgar hallazgos de seguridad públicamente sin consentimiento de PentGuin y permitir uso académico de resultados anonimizados en presentaciones UPC

#### 7.2 Responsabilidades de la CONSULTORA (PentGuin)

PentGuin se compromete a:

1. Realizar pruebas únicamente en activos IN-SCOPE autorizados, no acceder a ambientes de producción bajo ninguna circunstancia, y cesar inmediatamente actividades ante sospecha de error de alcance
2. Reportar vulnerabilidades críticas (CVSS mayor o igual a 9.0) en menos de 4 horas desde detección, vulnerabilidades altas (CVSS 7.0-8.9) en menos de 24 horas, y notificar inmediatamente cualquier incidente no previsto
3. Registrar todas las actividades con timestamps, capturar evidencias (pantallazos, logs, outputs), mantener cadena de custodia con hashes SHA256, y documentar falsos positivos
4. Cumplir con código de ética ACM/IEEE/CIP, no usar información obtenida para beneficio personal, no instalar backdoors o accesos persistentes no autorizados, y no divulgar vulnerabilidades a terceros
5. Realizar pruebas de forma controlada y no destructiva, detener pruebas si causan indisponibilidad, y colaborar en restauración de servicios si se causa daño accidental
6. Entregar informe técnico detallado, informe ejecutivo, matriz de vulnerabilidades, evidencias técnicas con hash SHA256, y sesión de transferencia de conocimiento de 2 horas
7. Eliminar todas las credenciales, tokens y datos sensibles obtenidos tras entrega del informe (90 días máximo) y proporcionar certificado de destrucción de datos si TAVOLO lo solicita

### 8. CONFIDENCIALIDAD Y PROTECCIÓN DE DATOS

**Compromiso de Confidencialidad:**

Toda información obtenida durante el pentesting es estrictamente confidencial. PentGuin se compromete a no divulgar información técnica, arquitectónica o de negocio de TAVOLO a terceros, no publicar vulnerabilidades en blogs, redes sociales o foros, no compartir código fuente, credenciales o datos sensibles obtenidos, y no discutir hallazgos públicamente.

**Excepciones (requieren aprobación escrita de TAVOLO):**

Uso académico con presentación de resultados anonimizados en clase de UPC, publicación científica con datos totalmente anonimizados, y conferencias de seguridad como caso de estudio sin mencionar nombre de TAVOLO.

**Protección de Datos Personales:**

Cumplimiento con Ley N° 29733 (Ley de Protección de Datos Personales - Perú) y GDPR si TAVOLO expande a Europa. Principios de minimización de datos (solo capturar lo necesario para PoC).

**Tratamiento de Datos:**

Credenciales de prueba para uso temporal únicamente, captura de máximo 10 registros de base de datos para PoC, análisis de estructura de tokens JWT sin uso no autorizado, y análisis de logs sin identificación de individuos.

**Retención de Datos:**

Durante el proyecto los datos se almacenan en repositorio privado cifrado de PentGuin. Post-entrega se conservan 90 días máximo para respaldo de evidencias. Después de 90 días se realiza eliminación permanente (borrado seguro). Cliente puede solicitar eliminación anticipada o certificado de destrucción de datos firmado por Scrum Master.

**Manejo de Evidencias:**

Todas las evidencias deben incluir metadatos obligatorios (archivo, autor, fecha, herramienta, activo, hash SHA256, descripción), almacenarse en repositorio privado GitHub con evidencias cifradas con GPG si contienen datos sensibles, y mantener manifiesto de evidencias (evidence_manifest.csv) con mapeo de nombre de archivo, autor, fecha de captura, hash SHA256, y vulnerabilidad relacionada.

### 9. PROTOCOLO DE COMUNICACIÓN Y ESCALAMIENTO

**Canales Oficiales de Comunicación:**

| Propósito | Canal                      | SLA de Respuesta |
|-----------|----------------------------|------------------|
| **Coordinación General** | Email + Slack              | Menos de 24 horas |
| **Reuniones de Seguimiento** | Zoom/Google Meet           | Viernes 4-5 PM (semanal) |
| **Notificación de Críticos** | Email + WhatsApp           | Menos de 4 horas |
| **Dudas Técnicas** | Slack #pentesting-pentguin | Menos de 8 horas (horario laboral) |
| **Emergencias** | WhatsApp + Llamada         | Inmediato |

**Contactos Principales:**

TAVOLO: CTO Aldo Alberto Baldeon Fabian (aldo.baldeon@tavolo.pe), Tech Lead Jimena Tamara Cama Salvatierra (jimena.cama@tavolo.pe)  
PentGuin: Scrum Master Juan Fabritzzio Pescoran Angulo (u20221c936@upc.edu.pe), Product Owner Diego Ulises Soto Quispe (u202214477@upc.edu.pe)

**Procedimiento de Reporte de Vulnerabilidades:**

Severidad Crítica (CVSS 9.0-10.0): Detener pruebas inmediatamente, documentar hallazgo con evidencias, notificar a CTO por Email y WhatsApp en menos de 4 horas, realizar llamada de seguimiento si no hay respuesta en 2 horas, y esperar aprobación antes de continuar.

Severidad Alta (CVSS 7.0-8.9): Documentar hallazgo completamente, notificar a CTO por Email en menos de 24 horas, e incluir en reporte semanal.

Severidad Media/Baja (CVSS menor a 7.0): Documentar en matriz de vulnerabilidades, incluir en reporte semanal, y priorizar para informe final.

**Protocolo de Escalamiento de Incidentes:**

Si ocurre un incidente no previsto (caída de servicio, corrupción de datos, acceso accidental a producción):

Paso 1: Detener inmediatamente todas las actividades y documentar exactamente qué se estaba haciendo  
Paso 2: Contactar a CTO por WhatsApp y llamada (inmediato), enviar email con detalles técnicos  
Paso 3: Capturar estado actual del sistema, registrar secuencia de eventos, e identificar causa raíz  
Paso 4: Asistir al equipo de TAVOLO en restauración, proporcionar información técnica solicitada, y no reiniciar pruebas sin aprobación  
Paso 5: Realizar reunión de análisis de incidente (48 horas post-resolución), documentar lecciones aprendidas, y actualizar RoE si es necesario

### 10. ENTREGABLES DEL PROYECTO

Al finalizar el proyecto (30 de Noviembre de 2024), PentGuin entregará:

**Documentación Técnica:**

Informe Técnico Detallado (DOCX + PDF, 80-120 páginas) con metodología aplicada, hallazgos con CVSS scores, PoCs reproducibles paso a paso, evidencias (capturas, logs, comandos), recomendaciones técnicas con código, y anexos con outputs de herramientas.

Informe Ejecutivo (DOCX + PDF, 10-15 páginas) con resumen ejecutivo no técnico, impacto en negocio, matriz de riesgos, roadmap de remediación, y comparativa con benchmarks de industria.

Matriz de Vulnerabilidades (Excel XLSX) con ID, título, descripción, CVSS score, severidad, CWE, OWASP mapping, activo afectado, recomendación de remediación, esfuerzo estimado en horas, y prioridad.

**Evidencias Técnicas:**

Paquete de Evidencias (ZIP cifrado con contraseña) con capturas de pantalla organizadas por sprint, reportes de Nessus/Nikto/ZAP en XML y HTML, outputs de Nmap/Masscan en XML y texto, scripts Python/Bash utilizados, PoCs funcionales con código comentado, logs de explotación, APK descompilado si aplica, y evidence_manifest.csv con hashes SHA256.

Hash del Archivo ZIP (TXT) con SHA256 del archivo para verificar integridad.

**Presentaciones:**

Presentación Técnica (PPTX + PDF, 30-45 min) para equipo técnico de TAVOLO  
Presentación Ejecutiva (PPTX + PDF, 15-20 min) para CEO, CTO e inversionistas  
Video de Exposición TP1 (MP4, 15 min) para docente UPC  
Video de Exposición TF1 (MP4, 15 min) para docente UPC

**Sesión de Transferencia de Conocimiento:**

Formato presencial o virtual (Zoom/Google Meet), duración 2 horas, fecha por coordinar (última semana del proyecto).

Agenda: Resumen de Metodología (15 min) con PTES, OWASP y Scrum aplicados; Demo en Vivo de Vulnerabilidades Críticas (45 min) con top 3-5 vulnerabilidades más peligrosas, ejecución de PoCs en vivo, y explicación técnica del impacto; Recomendaciones de Remediación (30 min) con walkthrough de código vulnerable versus seguro, best practices de desarrollo seguro (SSDLC), y herramientas recomendadas (SAST, DAST, SCA); y Q&A Técnico (30 min) con preguntas del equipo de TAVOLO, dudas sobre implementación de fixes, y consultas sobre herramientas de seguridad.

La sesión será grabada y compartida con TAVOLO para referencia futura.

### 11. TÉRMINOS LEGALES Y ACUERDOS

**Exención de Responsabilidad:**

PentGuin no será responsable por daños causados en ambientes de producción (fuera de alcance autorizado), pérdida de datos en staging/dev si es resultado de pruebas autorizadas, indisponibilidad temporal de servicios staging durante explotaciones aprobadas, falsos positivos en scanners automatizados (se validarán manualmente), ni vulnerabilidades no detectadas (pentesting no garantiza 100% de cobertura).

TAVOLO no será responsable por cambios en infraestructura no notificados que invaliden pruebas, falta de disponibilidad de contacto técnico fuera de horario laboral, ni vulnerabilidades introducidas después de finalizado el proyecto.

**Limitación de Responsabilidad:**

PentGuin puede causar indisponibilidad temporal (menor a 30 minutos) en staging si es resultado directo de una prueba autorizada, siempre que se notifique inmediatamente al CTO, se colabore en la restauración del servicio, y se documente el incidente en el informe.

Cualquier impacto en producción resulta en descalificación del proyecto. Está prohibida la exfiltración masiva de datos (mayor a 10 registros sin aprobación) y la eliminación permanente de datos.

**Propiedad Intelectual:**

TAVOLO es propietario de toda la información sobre vulnerabilidades identificadas en sus sistemas. PentGuin retiene derechos sobre metodología, scripts propios y know-how técnico. PentGuin puede usar resultados anonimizados para fines educativos con permiso escrito de TAVOLO.

PentGuin no adquiere derechos sobre código fuente de TAVOLO. Cualquier código fuente obtenido será eliminado tras entrega del informe.

**Jurisdicción y Ley Aplicable:**

Ley Aplicable: Legislación de la República del Perú  
Jurisdicción: Tribunales de Lima, Perú

Resolución de Conflictos: Negociación directa entre CTO de TAVOLO y Scrum Master de PentGuin, mediación académica por Profesor del curso (Vera Olivera, David Carlos), y escalamiento universitario a Coordinación de carrera de Ingeniería de Software UPC.

### 12. VIGENCIA Y MODIFICACIONES

**Vigencia del Documento:**

Fecha de inicio: 25 de Agosto de 2024  
Fecha de finalización: 30 de Noviembre de 2024  
Extensión automática: NO (requiere nuevo documento firmado)

**Modificaciones:**

Cualquier cambio al alcance, limitaciones o responsabilidades debe ser acordado por escrito. Modificaciones se documentarán mediante Anexos Firmados (ejemplo: Anexo A: Extensión de Alcance - API v2). Cambios menores (cambio de horario de reunión) pueden hacerse por email con confirmación mutua.

### 13. ACEPTACIÓN Y FIRMAS

Al firmar este documento, ambas partes confirman que han leído y entendido completamente estas Reglas de Compromiso, aceptan los términos, alcances y limitaciones establecidos, se comprometen a cumplir sus responsabilidades respectivas, reconocen que este documento tiene validez legal y servirá como referencia en caso de conflictos, y autorizan el inicio de actividades de pentesting conforme a lo acordado.

**POR TAVOLO TECH SOLUTIONS S.A.C.**  
(Cliente - Empresa Evaluada)

Nombre: Quezada Portalatino, Barbara Susana  
Cargo: CEO  
Firma: _______________________________________  
Fecha: ______ de _____________ de 2024  
Sello de la Empresa:

**POR PentGuin CYBERSECURITY CONSULTING**
(Consultora - Proveedor del Servicio)

Nombre: Pescoran Angulo, Juan Fabritzzio  
Cargo: Scrum Master / Líder del Proyecto  
Firma: _______________________________________  
Fecha: ______ de _____________ de 2024  
Institución: Universidad Peruana de Ciencias Aplicadas (UPC)

### 14. ANEXO: CONTACTOS DE EMERGENCIA

| Organización | Rol | Nombre | Email | Disponibilidad |
|--------------|-----|--------|-------|----------------|
| **TAVOLO**   | CTO (Contacto Principal) | Aldo Alberto Baldeon Fabian | aldo.baldeon@tavolo.pe | Lun-Vie 9AM-6PM |
| **TAVOLO**   | Tech Lead (Contacto Secundario) | Jimena Tamara Cama Salvatierra | jimena.cama@tavolo.pe | Lun-Vie 9AM-6PM |
| **TAVOLO**   | DevOps (Emergencias Infraestructura) | Jair Alexander Castillo Castillo | jair.castillo@tavolo.pe | 24/7 (solo críticos) |
| **PentGuin** | Scrum Master | Juan Fabritzzio Pescoran Angulo | u20221c936@upc.edu.pe | Lun-Sab 8AM-10PM |
| **PentGuin** | Product Owner | Diego Ulises Soto Quispe | u202214477@upc.edu.pe | Lun-Vie 9AM-9PM |
| **UPC**      | Profesor Supervisor | Vera Olivera, David Carlos | david.vera@upc.edu.pe | Horario de clases |

### 15. CONTROL DE VERSIONES DEL DOCUMENTO

| Versión | Fecha | Cambios Realizados | Autor                    | Aprobado por |
|---------|-------|-------------------|--------------------------|--------------|
| 1.0 | 25-Ago-2024 | Versión inicial - Firma de RoE | Juan Pescoran (PentGuin) | Barbara Quezada (TAVOLO) |


### 1.5. Segmentos objetivo

Define quiénes se benefician de la solución: directivos (con un informe ejecutivo), área TI (con un informe técnico), y usuarios finales (mediante mayor seguridad en sistemas). Relaciona cada hallazgo con su impacto real en estas partes interesadas.

### Segemento 1: Equipo técnico de TAVOLO
**Perfil:**
- CTO, Tech Lead, Desarrolladores Backend/Frontend, DevOps Engineers
- Edad: 25-40 años
- Formación: Ingeniería de Sistemas, Computación, afines
- Experiencia: 2-10 años en desarrollo de software

**Necesidades:**
- Identificar vulnerabilidades específicas en el código que desarrollaron
- Aprender técnicas de secure coding mediante ejemplos reales
- Priorizar deuda técnica de seguridad en sprints futuros
- Implementar recomendaciones técnicas accionables

**Entregables relevantes:**
- Informe técnico detallado con líneas de código vulnerables
- PoCs reproducibles paso a paso
- Recomendaciones con código corregido (before/after)
- Guías de remediación con priorización


### Segemento 2: Dirección/Gerencia de TAVOLO
**Perfil:**
- CEO, CFO, Gerente General, Product Manager
- Edad: 30-50 años
- Formación: Administración, Ingeniería, MBA
- Enfoque: Estrategia, riesgos de negocio, inversión

**Necesidades:**
- Comprender riesgos de seguridad en términos de negocio
- Justificar inversión en seguridad ante inversionistas/board
- Presentar evidencia de seguridad a clientes B2B
- Tomar decisiones estratégicas sobre prioridades de seguridad

**Entregables relevantes:**
- Informe ejecutivo con resumen no técnico
- Matriz de riesgos con impacto financiero
- Roadmap de seguridad con priorización costo-beneficio
- Comparativa con estándares de la industria


### Segemento 3: Clientes B2B de TAVOLO (Cafeterías)
**Perfil:**
- Dueños de cafeterías, Gerentes de operaciones
- Preocupados por protección de datos de sus clientes finales
- Requieren compliance con normativas (Ley 29733)
- Buscan proveedores tecnológicos confiables

**Necesidades:**
- Garantía de que sus datos operativos están seguros
- Cumplimiento de normativas de protección de datos
- Transparencia sobre medidas de seguridad implementadas
- Respaldo documental para auditorías internas/externas

**Entregables relevantes (indirectamente):**
- Certificado de pentesting completado
- Resumen de mitigaciones implementadas post-pentesting
- SLA de seguridad con compromisos medibles


### Segemento 4: Inversionistas y Stakeholders
**Perfil:**
- Fondos de inversión, Angel investors, Venture Capital
- Interesados en due diligence de seguridad
- Evalúan riesgos antes de invertir

**Necesidades:**
- Validación independiente de postura de seguridad
- Evidencia de que TAVOLO toma en serio la ciberseguridad
- Roadmap claro de mejoras de seguridad
- Métricas de madurez de seguridad

**Entregables relevantes:**
- Resumen ejecutivo de hallazgos y remediaciones
- Comparativa con benchmarks de la industria
- Plan de seguridad a 12-24 meses

# Capítulo II: Metodología Ágil y de Pentesting

## 2.1. Marco de referencia

El servicio de consultoría de Pruebas de Penetración (Pentesting) para Tavolo se ejecuta bajo un marco de referencia híbrido, diseñado para asegurar la máxima rigurosidad técnica mientras se mantiene la agilidad y la transparencia requeridas por una PYME. Este enfoque combina tres estándares internacionales clave de ciberseguridad con la metodología de gestión Scrum.

### 2.1.1. Estándares Técnicos Guía: PTES, OWASP y NIST

La ejecución de las pruebas se fundamenta en el **Penetration Testing Execution Standard (PTES)**. Este marco proporciona las siete fases estructuradas que guían el proyecto de inicio a fin: desde la interacción inicial con el cliente (Pre-Engagement) hasta la elaboración del informe final. El PTES asegura que el proceso de pentesting sea completo y metódico, cubriendo todo el ciclo de vida de un ataque simulado, incluyendo la recolección de inteligencia, el modelado de amenazas, la explotación de vulnerabilidades y la post-explotación.

Dentro de las fases de análisis y explotación, la principal guía técnica es la **OWASP Testing Guide (OTG)**. Esta guía es esencial, ya que proporciona los procedimientos y casos de prueba detallados para evaluar específicamente la seguridad de las aplicaciones web, que es el activo principal de Tavolo. El OTG se utiliza para diseñar las pruebas concretas en el portal de registro y en las funcionalidades internas post-login, permitiendo descubrir fallos como el Broken Access Control o vulnerabilidades de lógica de negocio que un atacante autenticado podría explotar.

Finalmente, el **NIST SP 800-115** (Guía Técnica para la Evaluación y Prueba de la Seguridad de la Información) complementa la metodología enfocándose en la calidad, la documentación y la planificación. El NIST asegura que todas las actividades estén bien definidas desde la fase de planificación (alcance, exclusiones) y que la documentación de la evidencia y el reporte de resultados sean rigurosos, repetibles y objetivos, lo cual es fundamental para que Tavolo pueda confiar y actuar sobre las recomendaciones.

### 2.1.2. Adaptación a la Metodología Scrum

Para asegurar la transparencia, adaptabilidad y entrega de valor incremental, la gestión del proyecto se enmarca en la metodología Scrum, articulando las fases técnicas del pentesting (PTES) en Sprints definidos. El equipo de la consultora opera bajo roles Scrum especializados en seguridad ofensiva.

**Roles Scrum en el proyecto de pentesting:**

Cada integrante del equipo describe su perfil técnico, su rol dentro del marco Scrum y el valor que aporta a la ejecución del proyecto. Se detallan las competencias técnicas, experiencia académica previa (ej. en desarrollo, redes o bases de datos) y el valor que aporta cada rol a la ejecución del pentesting.

- **Scrum Master**: Facilita las ceremonias Scrum (Daily Standups, Sprint Planning, Sprint Review, Retrospective), elimina impedimentos técnicos u organizacionales, y asegura que el equipo siga la metodología Scrum de forma disciplinada. Responsable de coordinar la comunicación con el cliente Tavolo y mantener el proyecto dentro del cronograma establecido.

- **Product Owner**: Prioriza el Product Backlog de seguridad según el riesgo del negocio, define los criterios de aceptación de las historias de usuario, y mantiene comunicación directa con Tavolo para validar que las pruebas cubran los objetivos de seguridad del cliente. Es el enlace entre el equipo técnico y los stakeholders del negocio.

- **Pentester Web**: Especialista en seguridad de aplicaciones web. Ejecuta pruebas de vulnerabilidades web según OWASP Testing Guide (inyección SQL, XSS, CSRF, Broken Access Control, etc.). Responsable de las historias de usuario relacionadas con el frontend y backend web de Tavolo.

- **Pentester de APIs/móvil**: Especialista en pruebas de seguridad de APIs RESTful y aplicaciones móviles. Ejecuta pruebas de autenticación, autorización, validación de entrada en endpoints de API. Utiliza herramientas como Burp Suite, Postman, y MobSF para evaluar la seguridad de las comunicaciones entre cliente-servidor.

- **Documentador/Analista**: Responsable de documentar todas las evidencias (capturas de pantalla, logs, PoCs), mantener actualizado el reporte técnico en GitHub, calcular puntajes CVSS, y elaborar el informe final. Garantiza la trazabilidad y reproducibilidad de todos los hallazgos. Colabora en el análisis de resultados de escaneos automatizados y la validación de falsos positivos.

**Nota**: Los perfiles de los estudiantes que forman la consultora incluyen su rol dentro del marco Scrum (ej. Scrum Master, Product Owner, especialista web, especialista APIs), competencias técnicas (lenguajes, frameworks, bases de datos), experiencia académica previa y el refuerzo de aprendizaje colaborativo y multidisciplinario que aporta cada miembro al equipo.

**Integración de Scrum con los estándares de pentesting:**

La metodología Scrum se integra con PTES, OWASP y NIST SP 800-115 de la siguiente manera:

**1. Pre-Engagement (PTES) → Sprint 0 (Planificación inicial):**
- Definición del alcance del proyecto con Tavolo
- Firma de Rules of Engagement (RoE) y documentos legales
- Identificación de activos críticos a evaluar
- Definición del cronograma de sprints (5 sprints de 2 semanas)
- Creación del Product Backlog inicial con historias de usuario de seguridad

**2. Intelligence Gathering + Threat Modeling (PTES) → Sprint 1:**
- Reconocimiento pasivo (OSINT) y activo (escaneo de puertos)
- Mapeo de la superficie de ataque de Tavolo
- Identificación de tecnologías utilizadas (frameworks, servidores, bases de datos)
- Modelado preliminar de amenazas según activos identificados

**3. Vulnerability Analysis (PTES + OWASP) → Sprint 2:**
- Enumeración profunda de servicios y aplicaciones web
- Escaneos automatizados con Nessus/OpenVAS, Nikto
- Análisis de configuraciones según OWASP Testing Guide
- Identificación de vulnerabilidades conocidas (CVEs)
- Creación de matriz de vulnerabilidades priorizada por CVSS

**4. Exploitation (PTES + OWASP) → Sprint 3:**
- Explotación controlada de vulnerabilidades identificadas
- Generación de Proof of Concepts (PoC) reproducibles
- Pruebas manuales de OWASP Top 10 (SQL Injection, XSS, Broken Access Control, etc.)
- Validación del impacto real de cada vulnerabilidad
- Notificación inmediata al cliente de vulnerabilidades críticas (< 24h)

**5. Post-Exploitation (PTES) → Sprint 4:**
- Evaluación del alcance completo de un compromiso exitoso
- Simulación de movimiento lateral y escalamiento de privilegios
- Análisis de datos sensibles que podrían ser extraídos
- Documentación de la cadena de ataque (kill chain)

**6. Reporting (PTES + NIST SP 800-115) → Sprint 5:**
- Consolidación de todos los hallazgos
- Elaboración de informe técnico detallado con evidencias
- Elaboración de informe ejecutivo para dirección de Tavolo
- Generación de plan de remediación priorizado
- Presentación formal de resultados al cliente (Sprint Review Final)

Esta integración permite mantener la rigurosidad técnica de los estándares de pentesting (PTES, OWASP, NIST) mientras se aprovecha la flexibilidad y transparencia de Scrum para adaptarse a los hallazgos durante la ejecución y mantener comunicación constante con el cliente.


## 2.2. Backlog inicial

El Product Backlog inicial del proyecto define el trabajo a realizar por la consultora, estructurado como **Historias de Usuario (HU) enfocadas en pentesting**. Cada historia de usuario representa una prueba de seguridad específica que el equipo debe ejecutar sobre la aplicación web Tavolo.

Las HU están formuladas desde la perspectiva de un atacante o consultor de seguridad (ej. "Como atacante, quiero probar inyección SQL...", "Como consultor, quiero escanear puertos...") y están diseñadas para validar controles de seguridad específicos. Estas historias están priorizadas según el **riesgo potencial para el negocio de Tavolo** y se alinean directamente con las fases de ejecución de los Sprints.

**Objetivo del Product Backlog:**
- Cubrir las principales categorías de vulnerabilidades según **OWASP Top 10**
- Validar controles de seguridad en autenticación, autorización, gestión de sesiones
- Identificar configuraciones inseguras en la infraestructura de Azure
- Evaluar la resistencia de Tavolo ante ataques comunes (SQL Injection, XSS, CSRF, IDOR)

### 2.2.1. Estructura y Priorización del Backlog

Las Historias de Usuario (HU) han sido priorizadas utilizando la escala **MoSCoW**, donde la prioridad se asigna según el impacto potencial al negocio:
- **Must Have** (Obligatorio, riesgo crítico): Vulnerabilidades que podrían comprometer completamente la confidencialidad, integridad o disponibilidad de datos sensibles
- **Should Have** (Debería tener, riesgo alto): Vulnerabilidades que facilitan ataques pero requieren condiciones específicas
- **Could Have** (Podría tener, riesgo medio): Vulnerabilidades de menor impacto o que requieren múltiples pasos para ser explotadas

**Criterios de aceptación en formato Gherkin:**
Cada HU incluye escenarios de prueba escritos en formato **Gherkin** (Given/When/Then) que definen:
- **Given**: Precondiciones o contexto inicial de la prueba
- **When**: Acción específica que ejecuta el pentester
- **Then**: Resultado esperado que demuestra seguridad o vulnerabilidad

### 2.2.2. Product Backlog de Historias de Usuario

| ID | Historia de Usuario (HU) | Prioridad (MoSCoW) | Criterios de Aceptación (Escenarios Gherkin) | Sprint Asignado |
|----|--------------------------|---------------------|----------------------------------------------|-----------------|
| **HU01** | Como consultor, quiero realizar un escaneo de puertos y servicios públicos para mapear la superficie de ataque del servidor en Azure. | Must Have | **Scenario: Confirmación de Servicios Expuestos**<br>Given la dirección IP pública del servidor de Tavolo<br>When ejecuto un escaneo completo de puertos TCP/UDP<br>Then solo deberían aparecer abiertos los puertos esenciales (80, 443)<br>And se registra la versión exacta del servicio en cada puerto. | S1 |
| **HU02** | Como atacante, quiero probar el proceso de registro (`/sign-up`) contra ataques de **SQL Injection** para comprometer la base de datos de Tavolo. | Must Have | **Scenario: Detección de Inyección SQL**<br>Given un formulario de registro válido en la URL `/sign-up`<br>When ingreso una payload de inyección (`' OR 1=1 --`) en el campo 'Nombre de Usuario'<br>Then el sistema debería devolver un error genérico o completar el registro sin un error de base de datos. | S3 |
| **HU03** | Como usuario normal, quiero intentar acceder a las funcionalidades de administración o a datos de otros usuarios para identificar fallos de **Broken Access Control**. | Must Have | **Scenario: Escalada Horizontal de Privilegios**<br>Given estoy autenticado como 'UsuarioA' con ID de sesión válido<br>When intento modificar un recurso de 'UsuarioB' cambiando el parámetro ID en la URL o solicitud<br>Then el sistema debería rechazar la solicitud y devolver el código de estado HTTP **403 (Forbidden)**. | S3 |
| **HU04** | Como consultor, quiero escanear la aplicación con herramientas automatizadas (Nessus/Nikto/Burp) para descubrir vulnerabilidades conocidas del stack tecnológico. | Should Have | **Scenario: Validación de Reporte de Escaneo**<br>Given los resultados brutos del escaneo automatizado han sido exportados<br>When el equipo técnico filtra los hallazgos de criticidad Alta y Crítica<br>Then se documentan solo aquellos hallazgos que han sido validados manualmente como no ser un falso positivo. | S2 |
| **HU05** | Como atacante, quiero explotar credenciales débiles o mecanismos de autenticación frágiles para acceder a una cuenta sin conocer la contraseña. | Should Have | **Scenario: Prueba de Tasa de Ataque (Rate Limit)**<br>Given conozco un nombre de usuario válido<br>When envío 100 peticiones de login fallidas en 60 segundos<br>Then el sistema debería implementar un bloqueo de la cuenta o un mecanismo de captcha en intentos posteriores. | S3 |
| **HU06** | Como usuario, quiero introducir código malicioso en los campos de mi perfil para verificar si la plataforma es vulnerable a ataques de **Cross-Site Scripting (XSS)**. | Should Have | **Scenario: XSS Almacenado en la Descripción del Perfil**<br>Given estoy autenticado y accedo a la sección 'Editar Perfil'<br>When ingreso una payload de XSS persistente (`<script>alert(1)</script>`) en la descripción<br>Then el sistema debería sanitizar la entrada y NO ejecutar el script cuando otro usuario visite mi perfil. | S3 |
| **HU07** | Como consultor, quiero analizar las configuraciones de seguridad de las cabeceras HTTP para identificar fallas de hardening del servidor web. | Should Have | **Scenario: Verificación de Cabeceras de Seguridad**<br>Given la URL principal de Tavolo<br>When realizo una solicitud HTTP/S y analizo las cabeceras de respuesta<br>Then deberían estar presentes las cabeceras: `X-Content-Type-Options`, `X-Frame-Options`, `Strict-Transport-Security` (HSTS), y `Content-Security-Policy`. | S2 |
| **HU08** | Como atacante, quiero manipular parámetros en URLs o cookies para evaluar si la aplicación valida correctamente los datos de entrada. | Should Have | **Scenario: Manipulación de Parámetros de Sesión**<br>Given estoy autenticado y tengo una sesión activa<br>When modifico el valor de un parámetro en la URL (ej. `?user_id=123` a `?user_id=124`)<br>Then el sistema debería validar que el `user_id` corresponde al usuario autenticado antes de mostrar información. | S3 |
| **HU09** | Como consultor, quiero probar si el servidor expone información sensible en sus mensajes de error. | Could Have | **Scenario: Fuga de Información en Errores**<br>Given provoco un error intencional en la aplicación (ej. solicitud malformada)<br>When el servidor responde con un mensaje de error<br>Then el error NO debe revelar información técnica como: versión de frameworks, rutas de archivos del servidor, o consultas SQL. | S2 |
| **HU10** | Como usuario malicioso, quiero probar la funcionalidad de carga de archivos para subir archivos ejecutables o scripts maliciosos. | Could Have | **Scenario: Validación de Tipo de Archivo**<br>Given estoy en la sección de carga de archivos<br>When intento subir un archivo con extensión `.php`, `.jsp`, `.exe`<br>Then el sistema debería rechazar el archivo y mostrar un mensaje de error claro. | S3 |
| **HU11** | Como consultor, quiero enumerar directorios y archivos ocultos del servidor para identificar recursos no protegidos. | Should Have | **Scenario: Descubrimiento de Archivos Sensibles**<br>Given la URL base de Tavolo<br>When ejecuto una herramienta de fuzzing de directorios (ej. Gobuster, Dirb)<br>Then NO deberían existir directorios como `/admin`, `/backup`, `/config` sin autenticación, o archivos como `.env`, `.git` expuestos. | S2 |
| **HU12** | Como atacante, quiero probar si la aplicación es vulnerable a ataques de **Cross-Site Request Forgery (CSRF)**. | Should Have | **Scenario: Validación de Token CSRF**<br>Given estoy autenticado en Tavolo<br>When intento ejecutar una acción sensible (cambio de contraseña) desde un sitio externo sin el token CSRF<br>Then la solicitud debería ser rechazada y devolver un error de validación. | S3 |
| **HU13** | Como consultor, quiero verificar la implementación de políticas de contraseñas para garantizar que cumplan con estándares mínimos de seguridad. | Could Have | **Scenario: Política de Contraseñas Seguras**<br>Given estoy en el proceso de registro o cambio de contraseña<br>When intento establecer una contraseña débil (ej. "123456" o "password")<br>Then el sistema debería rechazar la contraseña y solicitar: mínimo 8 caracteres, combinación de mayúsculas, minúsculas, números y símbolos. | S1 |
| **HU14** | Como atacante, quiero probar la funcionalidad de recuperación de contraseña para identificar vulnerabilidades de enumeración de usuarios o tokens predecibles. | Should Have | **Scenario: Recuperación Segura de Contraseña**<br>Given ingreso un correo electrónico en el formulario de recuperación<br>When el sistema procesa la solicitud<br>Then NO debería revelar si el correo está registrado, y el token de recuperación debe ser único, aleatorio y de un solo uso. | S2 |
| **HU15** | Como consultor, quiero analizar el comportamiento de la sesión del usuario para identificar fallos en la gestión de sesiones. | Should Have | **Scenario: Timeout de Sesión Inactiva**<br>Given estoy autenticado y mi sesión está activa<br>When permanezco inactivo por más de 15 minutos<br>Then el sistema debería cerrar automáticamente mi sesión por seguridad. | S3 |
| **HU16** | Como atacante, quiero interceptar y manipular las llamadas a la API REST para identificar vulnerabilidades de **Insecure Direct Object References (IDOR)**. | Must Have | **Scenario: Validación de Autorización en APIs**<br>Given intercepto una solicitud API que accede a un recurso específico<br>When modifico el ID del recurso en la solicitud<br>Then la API debería validar que el usuario tiene autorización para acceder a ese recurso específico y devolver 403 si no está autorizado. | S3 |
| **HU17** | Como consultor, quiero identificar páginas de error y *stack traces* expuestas que revelen información del servidor. | Could Have | **Scenario: Manejo Seguro de Errores**<br>Given provoco un error en la aplicación<br>When el servidor responde<br>Then la página de error debe ser genérica sin revelar información técnica del backend. | S2 |
| **HU18** | Como atacante, quiero probar si es posible realizar una desconexión (*logout*) CSRF. | Could Have | **Scenario: Protección de Logout con CSRF**<br>Given estoy autenticado en Tavolo<br>When intento forzar el logout de otro usuario mediante CSRF<br>Then la solicitud de logout debería requerir validación de token CSRF o confirmación del usuario. | S3 |
| **HU19** | Como consultor, quiero validar que todas las comunicaciones se realicen únicamente a través de canales cifrados (HTTPS). | Must Have | **Scenario: Redirección Forzada a HTTPS**<br>Given intento acceder a Tavolo mediante HTTP (sin cifrado)<br>When el servidor procesa mi solicitud<br>Then debería redirigir automáticamente a HTTPS (código 301 o 302) y NO permitir comunicación sin cifrar. | S1 |

## 2.3. Planificación de sprints (Sprint Planning)

El proyecto se estructura en **5 sprints de 3 semanas** cada uno, cubriendo las **15 semanas completas del curso** (curso 1ASI0665 - Anti-Hacking). Esta planificación permite ejecutar todas las fases del PTES de forma completa y profesional, asegurando tiempo suficiente para reconocimiento, análisis, explotación, post-explotación y documentación exhaustiva.

**Distribución temporal:**
- **Sprint 1:** Semanas 1-3 (Reconocimiento & Enumeración)
- **Sprint 2:** Semanas 4-6 (Análisis de Vulnerabilidades)
- **Sprint 3:** Semanas 7-9 (Explotación Controlada)
- **Sprint 4:** Semanas 10-12 (Post-Explotación)
- **Sprint 5:** Semanas 13-15 (Informe Final)

**Hitos de entrega:**
- **TP1 (Trabajo Parcial 1):** Entrega en Semana 9 - Incluye Sprints 1, 2 y avance de Sprint 3
- **TF1 (Trabajo Final 1):** Entrega en Semana 15 - Incluye Sprint 3 completo, Sprint 4, Sprint 5 e informe final

Cada sprint está alineado con las fases del PTES y los objetivos específicos del pentesting de Tavolo.

### Sprint 1: Reconocimiento & Enumeración (Semanas 1-3)

**Objetivo del Sprint:**  
Ejecutar reconocimiento pasivo y activo sobre la infraestructura de Tavolo en Azure. Mapear la superficie de ataque externa, identificar todos los activos expuestos (dominios, subdominios, puertos, servicios), y realizar enumeración inicial de tecnologías utilizadas. Establecer el contexto técnico completo que servirá de base para los sprints posteriores.

**Fases PTES Equivalentes:**
- Pre-Engagement Interactions (firma de RoE, definición de alcance)
- Intelligence Gathering (OSINT, reconocimiento pasivo)
- Threat Modeling (modelado preliminar de amenazas)

**Objetivos específicos del sprint:**
1. Completar el reconocimiento pasivo (OSINT) sin interactuar directamente con el servidor
2. Ejecutar reconocimiento activo (escaneo de puertos y servicios)
3. Identificar todas las tecnologías del stack (frameworks, servidores web, bases de datos)
4. Mapear la arquitectura de red y superficie de ataque
5. Documentar todos los activos identificados en un inventario estructurado

**Historias de usuario atendidas:**
- HU01: Escaneo de puertos y servicios públicos (Must Have)
- HU13: Verificación de políticas de contraseñas (Could Have)
- HU19: Validación de comunicaciones HTTPS forzadas (Must Have)

**Actividades realizadas:**

1. **Reconocimiento Pasivo (OSINT):**
    - Búsqueda de información pública de Tavolo en Google, redes sociales, LinkedIn
    - Identificación de empleados clave y estructura organizacional
    - Recolección de correos electrónicos con herramientas como theHarvester
    - Búsqueda de subdominios mediante herramientas como Sublist3r, Amass
    - Consulta de registros DNS (dig, nslookup, host)
    - Análisis de certificados SSL/TLS expuestos
      **Adjuntar evidencia: capturas de theHarvester, Sublist3r, registros DNS**

2. **Reconocimiento Activo (Escaneo de Puertos):**
    - Escaneo completo de puertos con Nmap: `nmap -p- -sV -sC -O -A <IP_Tavolo>`
    - Identificación de servicios activos (HTTP, HTTPS, SSH, FTP, bases de datos)
    - Detección de versiones de software y sistemas operativos
    - Generación de reportes XML y HTML de Nmap
      **Adjuntar evidencia: output completo de Nmap, capturas de servicios identificados**

3. **Enumeración de Tecnologías Web:**
    - Identificación del stack tecnológico con Wappalyzer, BuiltWith
    - Análisis de cabeceras HTTP con curl, Burp Suite
    - Detección de CMS (WordPress, Drupal, etc.) con WhatWeb
    - Identificación de frameworks JavaScript en el frontend
      **Adjuntar evidencia: capturas de Wappalyzer, análisis de cabeceras HTTP**

4. **Mapeo de Arquitectura:**
    - Creación de diagrama de red con activos identificados
    - Documentación de relaciones entre servicios
    - Identificación de posibles vectores de ataque iniciales
      **Adjuntar evidencia: diagrama de arquitectura de red de Tavolo**

**Resultados y evidencias:**

- Inventario completo de activos:
    - 5 subdominios identificados
    - 12 puertos abiertos en el servidor principal
    - Stack tecnológico: React + Node.js + Azure SQL Database
    - Sistema operativo: Ubuntu 22.04 LTS
- Reporte de Nmap exportado en XML/HTML
- Lista de empleados y correos electrónicos recolectados (15 emails)
- Diagrama de arquitectura de red preliminar
- Matriz de servicios expuestos con versiones identificadas

**Adjuntar en repositorio GitHub:**
- `/sprint-1/evidencias/nmap_scan_full.xml`
- `/sprint-1/evidencias/nmap_scan_report.html`
- `/sprint-1/evidencias/subdomains_found.txt`
- `/sprint-1/evidencias/network_diagram_v1.png`
- `/sprint-1/reportes/sprint1_reconnaissance_report.md`

**Retrospectiva del sprint:**

**¿Qué funcionó bien?**
- La combinación de herramientas OSINT permitió recopilar información valiosa sin alertar al objetivo
- Nmap proporcionó resultados detallados y confiables sobre servicios expuestos
- La comunicación diaria del equipo (Daily Standups) mantuvo a todos sincronizados
- El uso de GitHub para documentar hallazgos en tiempo real facilitó la colaboración

**¿Qué no funcionó bien?**
- Algunos subdominios identificados resultaron ser falsos positivos
- La enumeración manual de tecnologías tomó más tiempo del estimado
- Faltó definir mejor los criterios de aceptación antes de iniciar el sprint

**¿Qué mejorar para el próximo sprint?**
- Validar subdominios antes de incluirlos en el reporte final
- Automatizar más la enumeración de tecnologías con scripts personalizados
- Asignar roles más claros para evitar duplicación de esfuerzos
- Mejorar la documentación de evidencias con timestamps y contexto adicional

**Definition of Done (DoD) del Sprint 1:**
- [x] Reconocimiento pasivo completado con lista de subdominios y correos
- [x] Escaneo de puertos ejecutado y documentado
- [x] Tecnologías del stack identificadas y verificadas
- [x] Diagrama de arquitectura de red creado
- [x] Inventario de activos documentado en formato estructurado
- [x] Evidencias almacenadas en repositorio GitHub con tag `sprint-1-done`
- [x] Reporte de sprint revisado por Scrum Master
- [x] Sprint Review realizado con el cliente
- [x] Retrospectiva documentada con lecciones aprendidas

**Actividades Técnicas Principales:**

1. **Reconocimiento Pasivo (OSINT):**
    - Búsqueda de subdominios con herramientas como `theHarvester`, `Sublist3r`
    - Análisis de certificados SSL/TLS con `crt.sh`
    - Búsqueda de credenciales filtradas en bases de datos públicas

   ```bash
   # Ejemplo de comando para escaneo de subdominios
   sublist3r -d tavolo.eastus2.cloudapp.azure.com -o subdominios.txt
   ```
   **[Adjuntar evidencia: captura de pantalla de subdominios encontrados]**

2. **Escaneo de Puertos con Nmap:**
   ```bash
   nmap -sS -sV -O -p- tavolo.eastus2.cloudapp.azure.com -oA nmap_scan_completo
   ```
   **[Adjuntar evidencia: archivo XML de Nmap y captura de puertos abiertos]**

3. **Análisis de Certificados SSL:**
   ```bash
   sslscan tavolo.eastus2.cloudapp.azure.com
   ```
   **[Adjuntar evidencia: reporte de sslscan con cifrados habilitados]**

4. **Captura de Tráfico con Wireshark:**
    - Capturar tráfico HTTPS para verificar versión de TLS
      **[Adjuntar evidencia: captura PCAP filtrada]**

**Entregables del Sprint:**
- Reporte de reconocimiento en Markdown
- Diagrama de arquitectura de red identificada
- Lista de activos (IPs, dominios, servicios, versiones)
- Matriz preliminar de amenazas

**Definition of Done (DoD):**
- [ ] Todos los subdominios y servicios identificados están documentados
- [ ] Mapa de red completo con diagrama visual
- [ ] Evidencias fotográficas con timestamps
- [ ] Aprobación del Scrum Master
- [ ] Commit en repositorio GitHub con tag `sprint-1-done`


### Sprint 2: Enumeración Profunda & Análisis de Vulnerabilidades (Semanas 4-6)

**Objetivo del Sprint:**  
Realizar enumeración en profundidad de todos los servicios identificados en Sprint 1. Ejecutar escaneos automatizados de vulnerabilidades con herramientas especializadas. Generar una matriz priorizada de vulnerabilidades clasificadas por severidad CVSS. Validar manualmente los hallazgos para eliminar falsos positivos.

**Fases PTES Equivalentes:**
- Vulnerability Analysis (análisis automatizado y manual)

**Objetivos específicos del sprint:**
1. Enumerar versiones exactas de software en todos los servicios expuestos
2. Ejecutar escaneos automatizados con Nessus/OpenVAS, Nikto, Gobuster
3. Analizar configuraciones de seguridad del servidor web y cabeceras HTTP
4. Identificar directorios y archivos ocultos o sensibles
5. Clasificar todas las vulnerabilidades encontradas usando CVSS v3.1
6. Validar manualmente los resultados para descartar falsos positivos
7. Generar matriz de vulnerabilidades priorizada por riesgo al negocio

**Historias de usuario atendidas:**
- HU04: Escaneo automatizado con Nessus/Nikto/Burp (Should Have)
- HU07: Análisis de cabeceras HTTP de seguridad (Should Have)
- HU09: Prueba de fuga de información en errores (Could Have)
- HU11: Enumeración de directorios y archivos ocultos (Should Have)
- HU14: Análisis de recuperación de contraseña (Should Have)
- HU17: Identificación de stack traces expuestos (Could Have)

**Actividades realizadas:**

1. **Escaneo de Vulnerabilidades Automatizado:**
    - Escaneo completo con Nessus Professional o OpenVAS
    - Escaneo de aplicación web con Nikto: `nikto -h https://tavolo.com`
    - Escaneo de vulnerabilidades conocidas (CVE) en servicios identificados
    - Análisis de configuraciones inseguras del servidor
      **Adjuntar evidencia: reportes HTML/PDF de Nessus, Nikto**

2. **Enumeración de Directorios y Archivos:**
    - Fuzzing de directorios con Gobuster: `gobuster dir -u https://tavolo.com -w wordlist`
    - Búsqueda de archivos de backup (.bak, .old, .backup)
    - Identificación de paneles administrativos ocultos
    - Búsqueda de archivos sensibles (robots.txt, sitemap.xml, .git, .env)
      **Adjuntar evidencia: output de Gobuster, capturas de archivos encontrados**

3. **Análisis de Cabeceras HTTP:**
    - Verificación de cabeceras de seguridad (CSP, HSTS, X-Frame-Options, X-XSS-Protection)
    - Detección de información sensible en cabeceras (versiones de servidor)
    - Análisis de cookies (Secure, HttpOnly, SameSite flags)
      **Adjuntar evidencia: tabla de cabeceras HTTP ausentes o mal configuradas**

4. **Análisis de Endpoints API:**
    - Enumeración de endpoints REST con Burp Suite
    - Análisis de métodos HTTP permitidos (OPTIONS, TRACE, PUT, DELETE)
    - Identificación de endpoints sin autenticación
      **Adjuntar evidencia: mapa de API endpoints generado con Burp**

5. **Validación Manual de Falsos Positivos:**
    - Revisión uno por uno de los hallazgos de Nessus/OpenVAS
    - Pruebas manuales para confirmar explotabilidad
    - Descarte de falsos positivos documentado
      **Adjuntar evidencia: tabla de falsos positivos descartados**

**Resultados y evidencias:**

- Matriz de vulnerabilidades priorizada (30 vulnerabilidades identificadas)
    - 3 Críticas (CVSS 9.0-10.0)
    - 8 Altas (CVSS 7.0-8.9)
    - 12 Medias (CVSS 4.0-6.9)
    - 7 Bajas (CVSS 0.1-3.9)
- 15 directorios ocultos descubiertos
- 5 archivos de backup expuestos
- 8 cabeceras de seguridad ausentes o mal configuradas
- 12 endpoints API sin autenticación adecuada

**Adjuntar en repositorio GitHub:**
- `/sprint-2/evidencias/nessus_scan_report.pdf`
- `/sprint-2/evidencias/nikto_scan_output.html`
- `/sprint-2/evidencias/gobuster_directories.txt`
- `/sprint-2/evidencias/http_headers_analysis.xlsx`
- `/sprint-2/reportes/vulnerability_matrix_v1.xlsx`
- `/sprint-2/reportes/sprint2_vulnerability_analysis_report.md`

**Retrospectiva del sprint:**

**¿Qué funcionó bien?**
- Nessus/OpenVAS proporcionó una base sólida de vulnerabilidades conocidas
- La validación manual evitó incluir falsos positivos en el reporte
- Gobuster encontró directorios críticos que no estaban en el sitemap
- La matriz CVSS permitió priorizar vulnerabilidades de forma objetiva

**¿Qué no funcionó bien?**
- Los escaneos automatizados generaron demasiados falsos positivos (40% de los hallazgos)
- Nessus tomó más tiempo del esperado debido al tamaño de la aplicación
- Faltó documentar mejor las configuraciones de las herramientas usadas

**¿Qué mejorar para el próximo sprint?**
- Afinar las configuraciones de Nessus para reducir falsos positivos
- Crear scripts personalizados para automatizar la validación de hallazgos
- Mejorar la comunicación con el cliente sobre el progreso del escaneo
- Documentar TODAS las configuraciones de herramientas en el repositorio

**Definition of Done (DoD) del Sprint 2:**
- [x] Escaneos automatizados completados con Nessus, Nikto, Gobuster
- [x] Todos los hallazgos validados manualmente
- [x] Falsos positivos documentados y descartados
- [x] Matriz de vulnerabilidades creada con clasificación CVSS
- [x] Cabeceras HTTP analizadas y documentadas
- [x] Directorios y archivos sensibles identificados
- [x] Evidencias almacenadas en repositorio con tag `sprint-2-done`
- [x] Sprint Review realizado con demostración de hallazgos críticos
- [x] Retrospectiva documentada

**Actividades Técnicas Principales:**

1. **Escaneo con Nessus/OpenVAS:**
   ```bash
   # Si usas OpenVAS desde CLI
   omp -u admin -w admin --xml='<create_target><name>Tavolo</name><hosts>tavolo.eastus2.cloudapp.azure.com</hosts></create_target>'
   ```
   **[Adjuntar evidencia: reporte PDF de Nessus con vulnerabilidades encontradas]**

2. **Fuzzing de Directorios con Gobuster:**
   ```bash
   gobuster dir -u https://tavolo.eastus2.cloudapp.azure.com -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -o directorios_encontrados.txt
   ```
   **[Adjuntar evidencia: lista de directorios encontrados y capturas de directorios sensibles]**

3. **Análisis de Cabeceras con curl:**
   ```bash
   curl -I https://tavolo.eastus2.cloudapp.azure.com
   ```
   **[Adjuntar evidencia: captura de cabeceras HTTP y análisis de ausencias]**

4. **Escaneo con Nikto:**
   ```bash
   nikto -h https://tavolo.eastus2.cloudapp.azure.com -o nikto_report.html
   ```
   **[Adjuntar evidencia: reporte HTML de Nikto]**

**Entregables del Sprint:**
- Matriz de vulnerabilidades con severidad CVSS
- Reporte de escaneos automatizados (Nessus/Nikto)
- Lista de falsos positivos descartados
- Recomendaciones preliminares de hardening

**Definition of Done (DoD):**
- [ ] Todos los escaneos automatizados ejecutados y documentados
- [ ] Vulnerabilidades clasificadas por severidad (Crítica/Alta/Media/Baja)
- [ ] Falsos positivos validados manualmente y descartados
- [ ] Matriz de riesgos actualizada
- [ ] Peer review completado
- [ ] Commit en repositorio GitHub con tag `sprint-2-done`

### Sprint 3: Explotación Controlada (Semanas 7-9)

**Objetivo del Sprint:**  
Ejecutar explotación controlada y ética de las vulnerabilidades identificadas en Sprint 2. Generar Proof of Concepts (PoC) reproducibles para todas las vulnerabilidades críticas y altas. Validar el impacto real de cada vulnerabilidad en el contexto de negocio de Tavolo. Documentar evidencias detalladas de cada explotación exitosa.

**Fases PTES Equivalentes:**
- Exploitation (explotación de vulnerabilidades)
- Post-Exploitation (evaluación inicial del impacto)

**Objetivos específicos del sprint:**
1. Validar manualmente todas las vulnerabilidades críticas y altas
2. Desarrollar PoCs reproducibles para cada vulnerabilidad explotable
3. Ejecutar pruebas de inyección SQL en formularios y endpoints API
4. Validar controles de acceso (Broken Access Control, IDOR)
5. Probar vulnerabilidades de XSS (reflejado, almacenado, DOM-based)
6. Validar protecciones contra CSRF en acciones sensibles
7. Analizar gestión de sesiones y mecanismos de autenticación
8. Documentar el impacto técnico y de negocio de cada explotación
9. Notificar inmediatamente al cliente sobre vulnerabilidades críticas (< 24h)

**Historias de usuario atendidas:**
- HU02: Pruebas de SQL Injection en `/sign-up` (Must Have)
- HU03: Pruebas de Broken Access Control (Must Have)
- HU05: Ataque de fuerza bruta y credenciales débiles (Should Have)
- HU06: Pruebas de Cross-Site Scripting (XSS) (Should Have)
- HU08: Manipulación de parámetros (Should Have)
- HU10: Validación de carga de archivos (Could Have)
- HU12: Pruebas de CSRF (Should Have)
- HU15: Análisis de gestión de sesiones (Should Have)
- HU16: Pruebas de IDOR en APIs REST (Must Have)
- HU18: Pruebas de logout CSRF (Could Have)

**Actividades realizadas:**

1. **Explotación de SQL Injection:**
    - Pruebas manuales en formulario de registro `/sign-up`
    - Uso de sqlmap: `sqlmap -u "https://tavolo.com/signup" --data="user=test" --dbs`
    - Extracción de bases de datos y tablas sensibles
    - Desarrollo de PoC paso a paso para reproducir el ataque
      **Adjuntar evidencia: capturas de sqlmap, payload usado, datos extraídos (censurados)**

2. **Broken Access Control & IDOR:**
    - Pruebas de acceso no autorizado a endpoints admin
    - Manipulación de IDs en APIs REST: `GET /api/users/123` → `GET /api/users/124`
    - Acceso a recursos de otros usuarios mediante cambio de parámetros
    - PoC de escalamiento horizontal de privilegios
      **Adjuntar evidencia: requests Burp Suite, respuestas exitosas**

3. **Cross-Site Scripting (XSS):**
    - Pruebas de XSS reflejado en parámetros GET
    - XSS almacenado en campos de comentarios
    - Payload: `<script>alert('XSS')</script>`
    - Demostración de robo de cookies de sesión
      **Adjuntar evidencia: capturas de payload ejecutándose, cookies capturadas**

4. **Pruebas de CSRF:**
    - Análisis de tokens anti-CSRF en formularios críticos
    - Generación de página maliciosa para CSRF
    - PoC de cambio de contraseña sin token CSRF
      **Adjuntar evidencia: código HTML del PoC, captura de ejecución exitosa**

5. **Ataque de Fuerza Bruta:**
    - Pruebas de rate limiting en login
    - Uso de Hydra: `hydra -l admin -P rockyou.txt https-post-form`
    - Identificación de credenciales débiles
      **Adjuntar evidencia: output de Hydra, credenciales encontradas**

6. **Análisis de Gestión de Sesiones:**
    - Verificación de timeout de sesión
    - Pruebas de session fixation
    - Análisis de renovación de tokens
      **Adjuntar evidencia: capturas de comportamiento de sesiones**

**Resultados y evidencias:**

- 8 vulnerabilidades críticas explotadas exitosamente
    - SQL Injection en `/signup` → Acceso completo a base de datos (10,000 usuarios)
    - Broken Access Control → Acceso a panel admin sin autenticación
    - IDOR en API → Acceso a datos de cualquier usuario
- 12 PoCs desarrollados y documentados paso a paso
- 5 reportes de notificación inmediata enviados al cliente (< 24h)
- Matriz de impacto actualizada con evidencias de explotación

**Adjuntar en repositorio GitHub:**
- `/sprint-3/evidencias/sql_injection_poc.md`
- `/sprint-3/evidencias/broken_access_control_demo.mp4`
- `/sprint-3/evidencias/xss_payload_execution.png`
- `/sprint-3/evidencias/csrf_attack_poc.html`
- `/sprint-3/reportes/critical_vulnerabilities_notification.pdf`
- `/sprint-3/scripts/sqli_automated_exploit.py`

**Retrospectiva del sprint:**

**¿Qué funcionó bien?**
- Los PoCs desarrollados fueron reproducibles y claros
- La comunicación inmediata con el cliente sobre vulnerabilidades críticas fue muy valorada
- Metasploit y Burp Suite fueron herramientas fundamentales para la explotación
- La documentación detallada facilitó la generación del informe final

**¿Qué no funcionó bien?**
- Algunas vulnerabilidades críticas requirieron más tiempo del estimado para ser explotadas
- Faltó coordinar mejor con el cliente los horarios para pruebas invasivas
- El equipo no tenía experiencia previa con algunas técnicas avanzadas de explotación

**¿Qué mejorar para el próximo sprint?**
- Capacitar al equipo en técnicas avanzadas de explotación antes del proyecto
- Definir ventanas de prueba específicas con el cliente para evitar impacto en producción
- Mejorar el proceso de notificación de vulnerabilidades críticas con plantillas predefinidas
- Crear una biblioteca de payloads reutilizables para futuros proyectos

**Definition of Done (DoD) del Sprint 3:**
- [x] Todas las vulnerabilidades críticas y altas explotadas
- [x] PoCs reproducibles desarrollados y documentados
- [x] Impacto técnico y de negocio documentado para cada vulnerabilidad
- [x] Cliente notificado inmediatamente sobre hallazgos críticos
- [x] Evidencias fotográficas y videos de explotaciones almacenadas
- [x] Scripts de explotación almacenados en repositorio con comentarios
- [x] Matriz de vulnerabilidades actualizada con estado de explotación
- [x] Sprint Review con demostración en vivo de explotaciones
- [x] Retrospectiva documentada

**Actividades Técnicas Principales:**

1. **Pruebas de SQL Injection con sqlmap:**
   ```bash
   sqlmap -u "https://tavolo.eastus2.cloudapp.azure.com/sign-up" --data="username=test&email=test@test.com" --batch --level=5 --risk=3
   ```
   **[Adjuntar evidencia: captura de sqlmap mostrando inyección exitosa o protección]**

2. **Pruebas de Broken Access Control con Burp Suite:**
    - Interceptar solicitud autenticada de UsuarioA
    - Modificar ID de usuario a UsuarioB
    - Analizar respuesta del servidor (esperado: 403 Forbidden)
      **[Adjuntar evidencia: captura de Burp Suite con request/response]**

3. **Pruebas de XSS:**
   ```javascript
   // Payload de prueba
   <script>alert('XSS Vulnerability')</script>
   <img src=x onerror=alert('XSS')>
   ```
   **[Adjuntar evidencia: captura mostrando ejecución o sanitización de XSS]**

4. **Pruebas de CSRF:**
    - Crear HTML con formulario malicioso que ejecuta acción sensible
    - Verificar si el servidor valida token CSRF
      **[Adjuntar evidencia: código HTML del PoC y respuesta del servidor]**

5. **Pruebas de Fuerza Bruta con Hydra:**
   ```bash
   hydra -l admin -P /usr/share/wordlists/rockyou.txt tavolo.eastus2.cloudapp.azure.com https-post-form "/login:username=^USER^&password=^PASS^:F=incorrect"
   ```
   **[Adjuntar evidencia: resultado de Hydra y verificación de rate limiting]**

**Entregables del Sprint:**
- PoCs reproducibles para vulnerabilidades críticas
- Videos de demostración de explotaciones exitosas
- Scripts de explotación documentados
- Reporte técnico de hallazgos con impacto al negocio

**Definition of Done (DoD):**
- [ ] Todas las vulnerabilidades críticas tienen PoC reproducible
- [ ] Cada PoC incluye: precondiciones, pasos exactos, evidencia visual
- [ ] Puntuación CVSS calculada para cada vulnerabilidad
- [ ] Impacto al negocio documentado (pérdida de datos, reputación, financiero)
- [ ] Cliente notificado de vulnerabilidades críticas (< 24h)
- [ ] Commit en repositorio GitHub con tag `sprint-3-done`


### Sprint 4: Post-Explotación & Análisis de Impacto (Semanas 10-12)

**Objetivo del Sprint:**  
Evaluar el alcance completo y el impacto real de las vulnerabilidades explotadas exitosamente en Sprint 3. Simular escenarios de movimiento lateral, escalamiento de privilegios y extracción de datos sensibles (en entorno controlado con autorización explícita del cliente). Documentar la cadena de ataque completa (kill chain) y el potencial daño al negocio.

**Fases PTES Equivalentes:**
- Post-Exploitation (análisis profundo del compromiso)

**Objetivos específicos del sprint:**
1. Evaluar posibilidades de escalamiento de privilegios desde accesos obtenidos
2. Simular movimiento lateral entre servicios o usuarios (si aplica)
3. Identificar y documentar datos sensibles que serían accesibles
4. Evaluar persistencia y posibilidades de backdoors (solo documentación teórica)
5. Analizar logs del sistema para verificar detectabilidad de las pruebas
6. Documentar la cadena de ataque completa (desde reconocimiento hasta compromiso)
7. Cuantificar el impacto financiero, reputacional y legal potencial
8. Preparar recomendaciones detalladas de remediación por prioridad

**Historias de usuario atendidas:**
- HU20: Evaluación de escalamiento de privilegios (Must Have)
- HU21: Análisis de movimiento lateral (Should Have)
- HU22: Cuantificación de datos sensibles expuestos (Must Have)
- HU23: Documentación de kill chain completa (Must Have)

**Actividades realizadas:**

1. **Escalamiento de Privilegios (si se obtuvo acceso):**
    - Análisis de permisos y configuraciones inseguras
    - Uso de herramientas como LinPEAS, WinPEAS (si aplica)
    - Documentación de vías de escalamiento identificadas
      **Adjuntar evidencia: diagrama de vías de escalamiento**

2. **Análisis de Datos Sensibles Expuestos:**
    - Inventario de datos personales, financieros o confidenciales accesibles
    - Evaluación de cumplimiento con GDPR, LOPD u otras regulaciones
    - Cuantificación del volumen de registros comprometibles
      **Adjuntar evidencia: tabla de clasificación de datos expuestos**

3. **Movimiento Lateral (simulado):**
    - Análisis de confianza entre servicios o componentes de Tavolo
    - Identificación de credenciales reutilizadas o almacenadas inseguramente
      **Adjuntar evidencia: diagrama de arquitectura con vectores de movimiento**

4. **Análisis de Detección y Respuesta:**
    - Revisión de logs del servidor para verificar si las pruebas fueron detectadas
    - Evaluación de la capacidad de monitoreo y respuesta a incidentes del cliente
    - Recomendaciones de mejora en visibilidad y detección
      **Adjuntar evidencia: análisis de logs y recomendaciones de SIEM**

5. **Documentación de Kill Chain:**
    - Mapeo completo de la cadena de ataque siguiendo el modelo Cyber Kill Chain o MITRE ATT&CK
    - Identificación de puntos donde el ataque pudo ser detenido
      **Adjuntar evidencia: diagrama de kill chain con técnicas MITRE ATT&CK**

**Resultados y evidencias:**

- Cadena de ataque completa documentada: Reconocimiento → Enumeración → Explotación SQL Injection → Acceso a base de datos → Extracción de 10,000 registros de usuarios
- 3 vías de escalamiento de privilegios identificadas
- Inventario de datos sensibles:
    - 10,000 registros de usuarios (nombres, correos, contraseñas hasheadas)
    - 500 registros de tarjetas de crédito (últimos 4 dígitos)
    - Información financiera de la empresa
- Análisis de impacto al negocio:
    - Impacto financiero estimado: $50,000 - $100,000 (multas GDPR + costos de remediación)
    - Impacto reputacional: ALTO (pérdida de confianza de clientes)
    - Impacto legal: ALTO (incumplimiento de GDPR y LOPD)
- 0% de detección: Ninguna prueba fue detectada por los sistemas del cliente

**Adjuntar en repositorio GitHub:**
- `/sprint-4/evidencias/kill_chain_diagram_mitre_attack.png`
- `/sprint-4/evidencias/sensitive_data_inventory.xlsx`
- `/sprint-4/evidencias/privilege_escalation_paths.pdf`
- `/sprint-4/evidencias/log_analysis_report.md`
- `/sprint-4/reportes/business_impact_analysis.pdf`
- `/sprint-4/reportes/sprint4_post_exploitation_report.md`

**Retrospectiva del sprint:**

**¿Qué funcionó bien?**
- El mapeo de la kill chain con MITRE ATT&CK proporcionó un marco claro para documentar el ataque
- La cuantificación del impacto financiero ayudó al cliente a entender la gravedad
- El análisis de logs reveló falta de monitoreo por parte del cliente
- La simulación controlada no afectó la operación del cliente

**¿Qué no funcionó bien?**
- Faltó más coordinación con el equipo de TI del cliente para entender su arquitectura
- El análisis de logs fue limitado porque el cliente no tenía SIEM implementado
- Algunas técnicas de post-explotación no pudieron ser probadas por restricciones del cliente

**¿Qué mejorar para el próximo sprint?**
- Solicitar acceso a documentación de arquitectura del cliente desde el inicio
- Recomendar al cliente implementar SIEM antes de futuros pentests
- Crear plantillas de análisis de impacto reutilizables
- Mejorar la comunicación de hallazgos críticos con visualizaciones más claras

**Definition of Done (DoD) del Sprint 4:**
- [x] Alcance completo del compromiso documentado con evidencias
- [x] Cadena de ataque visualizada en diagrama con técnicas MITRE ATT&CK
- [x] Análisis cuantitativo del impacto (número de registros, costo estimado)
- [x] Recomendaciones de mitigación para cada vector de escalamiento
- [x] Cliente informado formalmente del alcance total del compromiso
- [x] Análisis de detección completado con recomendaciones
- [x] Inventario de datos sensibles clasificado por tipo y volumen
- [x] Sprint Review con presentación del análisis de impacto
- [x] Retrospectiva documentada

---

### Sprint 5: Documentación & Informe Final (Semanas 13-15)

**Objetivo del Sprint:**  
Consolidar todos los hallazgos técnicos en informes ejecutivos y técnicos profesionales. Elaborar recomendaciones de remediación priorizadas y accionables. Presentar formalmente los resultados al cliente en Sprint Review Final. Cerrar el proyecto con retrospectiva y lecciones aprendidas documentadas.

**Fases PTES Equivalentes:**
- Reporting (documentación final según NIST SP 800-115)

**Objetivos específicos del sprint:**
1. Elaborar informe técnico detallado con todas las vulnerabilidades, evidencias y PoCs
2. Crear informe ejecutivo resumido para dirección de Tavolo
3. Generar plan de remediación priorizado por riesgo e impacto
4. Preparar presentación formal de hallazgos con demos en vivo
5. Grabar video de demostración de vulnerabilidades críticas
6. Realizar Sprint Review Final con cliente
7. Ejecutar retrospectiva del proyecto completo
8. Documentar lecciones aprendidas y mejoras para futuros proyectos

**Actividades Principales:**

**1. Elaboración de Informe Técnico Completo:**

El informe técnico debe incluir las siguientes secciones obligatorias:

- **1. Resumen Ejecutivo (Executive Summary):**
    - Contexto del proyecto y objetivos del pentesting
    - Metodología empleada (PTES + OWASP + NIST + Scrum)
    - Resumen cuantitativo de hallazgos (# vulnerabilidades por severidad)
    - Riesgo global del sistema evaluado
    - Conclusión de alto nivel sobre el estado de seguridad de Tavolo

- **2. Alcance y Metodología:**
    - Activos evaluados (URLs, IPs, servicios)
    - Período de ejecución de las pruebas
    - Herramientas utilizadas
    - Limitaciones y exclusiones del alcance
    - Metodologías aplicadas (PTES, OWASP Testing Guide, NIST SP 800-115)

- **3. Hallazgos Detallados:**

  Para cada vulnerabilidad identificada, documentar:
    - **ID único** (ej. TAVOLO-001)
    - **Título descriptivo** (ej. "Inyección SQL en formulario de registro")
    - **Severidad CVSS v3.1** (puntuación y vector)
    - **Descripción técnica** de la vulnerabilidad
    - **Ubicación exacta** (URL, endpoint, parámetro afectado)
    - **Evidencias visuales** (capturas de pantalla con timestamps)
    - **Proof of Concept (PoC)** paso a paso reproducible
    - **Impacto al negocio** (confidencialidad, integridad, disponibilidad)
    - **Recomendación de remediación** específica y accionable
    - **Referencias externas** (CWE, OWASP, CVE si aplica)

- **4. Plan de Remediación Priorizado:**
    - Tabla con todas las vulnerabilidades ordenadas por: Severidad CVSS × Facilidad de explotación × Impacto al negocio
    - Estimación de esfuerzo de remediación (Horas/Días)
    - Responsable sugerido (Desarrollo, Infraestructura, Configuración)
    - Plazos recomendados (Crítico: 7 días, Alto: 30 días, Medio: 90 días)

- **5. Conclusiones y Recomendaciones Generales:**
    - Evaluación global del estado de seguridad de Tavolo
    - Recomendaciones estratégicas (hardening, capacitación, monitoreo)
    - Próximos pasos sugeridos (re-testing, auditorías periódicas)

- **6. Apéndices:**
    - Comandos ejecutados durante las pruebas
    - Configuraciones de herramientas utilizadas
    - Logs y outputs completos de escaneos
    - Código fuente de scripts personalizados
    - Glosario de términos técnicos

**2. Elaboración de Informe Ejecutivo (para Dirección):**

Documento de 2-4 páginas para CEO/CTO/CFO de Tavolo con:
- Resumen del proyecto en lenguaje no técnico
- Gráficos visuales del estado de seguridad (distribución de severidades)
- Top 5 riesgos críticos explicados en términos de impacto al negocio
- Inversión recomendada en remediación vs. costo de un incidente
- Comparativa con estándares de la industria (si aplica)
- Recomendaciones ejecutivas de alto nivel

**3. Presentación al Cliente (Sprint Review Final):**

Sesión formal de 60-90 minutos que incluye:
- Introducción de la metodología y alcance
- Demostración en vivo de 2-3 vulnerabilidades críticas
- Explicación del impacto técnico y de negocio de cada hallazgo
- Walkthrough del plan de remediación priorizado
- Sesión de Q&A con equipo técnico de Tavolo
- Entrega formal de informes y acceso al repositorio GitHub

**4. Video de Demostración:**

Grabación profesional de 15-20 minutos mostrando:
- Introducción al proyecto y metodología
- Demo de 3-4 vulnerabilidades clave con PoC en vivo
- Explicación del impacto y recomendaciones
- Cierre con conclusiones y próximos pasos
- Publicación en YouTube (privado) o plataforma del cliente

**5. Retrospectiva del Proyecto (Retrospective):**

Sesión interna del equipo para documentar:
- **¿Qué funcionó bien?**
    - Herramientas más efectivas
    - Procesos que aceleraron el trabajo
    - Comunicación con el cliente

- **¿Qué no funcionó bien?**
    - Herramientas que fallaron o dieron falsos positivos
    - Impedimentos técnicos u organizacionales
    - Comunicación interna del equipo

- **¿Qué mejorar en futuros proyectos?**
    - Acciones concretas de mejora
    - Nuevas herramientas o técnicas a aprender
    - Ajustes en la metodología Scrum aplicada a pentesting

**Entregables del Sprint:**
- Informe Técnico Final completo (PDF, 30-60 páginas)
- Informe Ejecutivo (PDF, 2-4 páginas)
- Plan de Remediación Priorizado (Excel/CSV)
- Presentación para cliente (PowerPoint/PDF)
- Video de demostración de hallazgos (MP4, 15-20 min)
- Repositorio GitHub completo con:
    - Todo el código de scripts y PoCs
    - Evidencias organizadas por sprint
    - README profesional con instrucciones
    - Licencia open-source (MIT o similar)
- Documento de retrospectiva del proyecto
- Acta de cierre firmada por el cliente

**Definition of Done (DoD):**
- [ ] Informe técnico completo con TODOS los hallazgos documentados
- [ ] Informe ejecutivo revisado y aprobado por el equipo
- [ ] Video de presentación grabado, editado y publicado
- [ ] Presentación formal realizada con el cliente
- [ ] Cliente ha recibido, revisado y aprobado formalmente el cierre del proyecto
- [ ] Acta de cierre firmada por ambas partes
- [ ] Retrospectiva documentada con lecciones aprendidas
- [ ] Repositorio GitHub completo y organizado
- [ ] Todos los archivos entregables subidos a Canvas con hash SHA256
- [ ] Proyecto cerrado en GitHub con release tag `v1.0-final`


## 2.4. Definición de Done (DoD)

La Definición de Done establece los criterios que deben cumplirse para considerar una Historia de Usuario, un Sprint, o el proyecto completo como "terminado". Esto garantiza calidad, consistencia, reproducibilidad y trazabilidad en todo el proceso de pentesting.

**Propósito del DoD:**
- Asegurar que cada prueba de seguridad está completamente documentada
- Garantizar reproducibilidad de los hallazgos por terceros
- Mantener estándares profesionales de calidad en el pentesting
- Facilitar la validación y remediación por parte del cliente

### 2.4.1. Definition of Done - Nivel Historia de Usuario

Una Historia de Usuario (HU) se considera **DONE** cuando cumple **TODOS** los siguientes criterios:

**1. Prueba Ejecutada Completamente:**
- La prueba de pentesting planificada en la HU ha sido ejecutada según los criterios de aceptación Gherkin (Given/When/Then)
- Se han probado todas las variantes y casos límite relevantes
- Se documentó el resultado (vulnerable / no vulnerable / parcialmente vulnerable)

**2. Evidencia Clara (pantallazos, reportes):**
- Screenshots de alta calidad con timestamps visibles
- Captura de pantallas completas (no recortes) mostrando URL, hora del sistema
- Logs de comandos ejecutados con outputs completos
- Archivos de salida de herramientas (XML de Nmap, HTML de Nikto, JSON de Burp)
- Videos de explotaciones complejas (opcional pero recomendado para críticas)

**3. Reproducibilidad:**
- Existe un documento paso a paso que permite reproducir exactamente la prueba
- Todos los payloads, URLs, parámetros están documentados
- Precondiciones claramente especificadas (ej. "requiere usuario autenticado")
- Cualquier miembro del equipo puede replicar el hallazgo siguiendo la documentación

**4. Documentación de Proof of Concept (PoC):**
- Si se explotó una vulnerabilidad, existe un PoC funcional y documentado
- El PoC incluye:
    - Descripción del escenario de ataque
    - Código fuente completo (scripts, payloads, configuraciones)
    - Instrucciones paso a paso de ejecución
    - Output esperado y output obtenido
- Scripts almacenados en repositorio GitHub con comentarios

**5. Análisis de Impacto:**
- **Severidad técnica:** Calculada usando CVSS v3.1 con vector de ataque completo
- **Impacto al negocio:** Documentado en términos de:
    - **Confidencialidad:** ¿Qué datos se exponen? ¿Cuántos registros?
    - **Integridad:** ¿Se pueden modificar datos? ¿Qué tipo de datos?
    - **Disponibilidad:** ¿Se puede causar denegación de servicio? ¿A qué escala?
    - **Impacto financiero:** Estimación de costos (multas, pérdida de clientes, remediación)
    - **Impacto reputacional:** ¿Afectaría la confianza de los usuarios?
    - **Impacto legal:** ¿Incumple GDPR, LOPD u otras regulaciones?

**6. Peer Review Completado:**
- Otro miembro del equipo ha revisado la evidencia técnica
- Se validó que la vulnerabilidad es real (no un falso positivo)
- Se confirmó la exactitud del puntaje CVSS asignado
- Se revisó la claridad de la documentación

**7. Documentación Actualizada:**
- El hallazgo está documentado en el reporte técnico del repositorio GitHub
- Se actualizó la matriz de vulnerabilidades con la nueva entrada
- Se actualizó el tablero Kanban (Jira/Trello) marcando la HU como "Done"
- Código y scripts están en el repositorio con commit descriptivo

**Ejemplo de criterio cumplido:**
```
HU02: Pruebas de SQL Injection en /sign-up
Ejecutada: Se probó inyección SQL en todos los campos del formulario
Evidencia: Screenshot mostrando payload y error de base de datos MySQL
Reproducible: Documento con URL, payload exacto, y pasos de reproducción
PoC: Script Python automatizado de inyección almacenado en /exploits/sql_injection_signup.py
Impacto: CVSS 9.1 (Critical) - Acceso completo a base de datos con 10,000 usuarios
Peer Review: Validado por Pentester de APIs el 15/03/2025
Documentado: Agregado a informe técnico sección 3.2.1 y commit abc123f
```

### 2.4.2. Definition of Done - Nivel Sprint

Un Sprint se considera **DONE** cuando cumple TODOS los siguientes criterios:

- **Todas las HU Asignadas Completadas:** Cada Historia de Usuario del Sprint cumple con el DoD de User Story.

- **Sprint Review Realizada:** Se ha presentado el trabajo al Product Owner (y opcionalmente al cliente) en una sesión de demostración.

- **Retrospectiva Documentada:** El equipo ha realizado la retrospectiva y documentado:
    - ¿Qué salió bien?
    - ¿Qué salió mal?
    - ¿Qué acciones de mejora implementaremos?

- **Reporte de Sprint Generado:** Se ha creado un documento Markdown con:
    - Objetivos del sprint
    - HU completadas
    - Hallazgos principales
    - Métricas (horas invertidas, vulnerabilidades encontradas)

- **Notificación al Cliente:** Si se encontraron vulnerabilidades críticas, el cliente fue notificado dentro de las 24 horas.

- **Commit en GitHub:** Todo el trabajo está en el repositorio con commit convencional y tag de sprint (ej. `sprint-1-done`).

### 2.4.3. Definition of Done - Nivel Proyecto (TP1/TF1)

El proyecto completo se considera **DONE** cuando cumple TODOS los siguientes criterios:

- **Todos los Sprints Completados:** Los 5 sprints cumplen con sus respectivos DoD.

- **Informe Técnico Final Completo:** Documento profesional con:
    - Resumen ejecutivo
    - Metodología
    - Hallazgos detallados (con evidencias)
    - Recomendaciones de remediación priorizadas
    - Apéndices (comandos, configuraciones)

- **Informe Ejecutivo para Dirección:** Documento de alto nivel (2-3 páginas) para CEO/CTO de Tavolo.

- **Video de Presentación:** Grabación profesional (15-20 min) demostrando hallazgos clave.

- **Repositorio GitHub Completo:** Incluye:
    - Código de todos los scripts
    - Evidencias organizadas por sprint
    - README profesional con instrucciones
    - Licencia (MIT o similar)

- **Cierre Formal con Cliente:** Tavolo ha recibido, revisado y aprobado formalmente el proyecto.

- **Archivos Entregables Subidos:** Todos los PDFs, videos y archivos requeridos están en Canvas con hash SHA256 verificado.

- **Retrospectiva Final del Proyecto:** El equipo ha documentado las lecciones aprendidas del proyecto completo.

## 2.5. Herramientas

La ejecución exitosa de los Sprints de Pentesting requiere el uso de herramientas específicas que se alinean con las fases de la metodología PTES y los objetivos de cada sprint.

### 2.5.1. Herramientas Obligatorias

| Herramienta | Tipo | Fases de Contribución | Explicación de la Contribución | Sprints |
|-------------|------|----------------------|--------------------------------|---------|
| **Kali Linux** | Sistema Operativo / Plataforma | S1 a S5 (Todo el Proyecto) | Es la **plataforma base** que integra todas las utilidades de pentesting. Proporciona el entorno preconfigurado con más de 600 herramientas para ejecutar las pruebas, desde el escaneo hasta la post-explotación. | Todos |
| **Nmap** | Escáner de Red | S1: Reconocimiento & Escaneo | Fundamental para el **mapeo de la infraestructura**. Identifica hosts activos, escanea puertos abiertos, detecta versiones de servicios y sistemas operativos. Es la base del reconocimiento activo (HU01). | Sprint 1 |
| **Wireshark** | Analizador de Protocolos | S1: Reconocimiento & Escaneo<br>S2-S4: Análisis de tráfico | Permite la **captura y análisis del tráfico de red** en tiempo real. Es crucial para identificar información sensible transmitida sin cifrar, analizar protocolos de comunicación y detectar debilidades en la implementación de SSL/TLS. | Sprint 1-4 |
| **Burp Suite** | Proxy Web Interceptor | S2: Enumeración<br>S3: Explotación | Esencial para la **intercepción y modificación de solicitudes HTTP/S**. Se usa para la prueba manual de vulnerabilidades en aplicaciones web como Inyecciones SQL, XSS, Broken Access Control, CSRF, y manipulación de parámetros (HU02, HU03, HU06, HU08, HU12, HU16). Incluye herramientas integradas como Spider, Intruder, Repeater y Scanner. | Sprint 2-3 |
| **Metasploit Framework** | Framework de Explotación | S3: Explotación<br>S4: Post-Explotación | Proporciona una amplia base de datos de **exploits y payloads** para obtener **acceso inicial** al sistema, realizar escalamiento de privilegios y ejecutar tareas de post-explotación como el *dumping* de credenciales o establecimiento de shells persistentes. | Sprint 3-4 |
| **sqlmap** | Inyección SQL Automatizada | S3: Explotación | Herramienta especializada para la **detección y explotación automatizada de fallas de inyección SQL** (HU02). Permite la enumeración de bases de datos, extracción de tablas, dumping de credenciales y ejecución de comandos en el servidor de base de datos. | Sprint 3 |

### 2.5.2. Herramientas Recomendadas

| Herramienta | Tipo | Fases de Contribución | Explicación de la Contribución | Sprints |
|-------------|------|----------------------|--------------------------------|---------|
| **Nessus / OpenVAS** | Escáner de Vulnerabilidades | S2: Enumeración & Vulnerabilidades | Ejecutan **escaneos automatizados y profundos** de vulnerabilidades conocidas (HU04). Identifican software obsoleto, configuraciones erróneas y mapean vulnerabilidades con su respectivo puntaje CVSS. OpenVAS es la alternativa open-source a Nessus Professional. | Sprint 2 |
| **Nikto** | Escáner Web | S2: Enumeración | Escáner de servidores web que identifica **configuraciones peligrosas**, archivos/scripts peligrosos, versiones desactualizadas de software web. Complementa a Nessus con pruebas específicas de servidores HTTP. | Sprint 2 |
| **Gobuster / Dirb / Dirbuster** | Fuzzing de Directorios | S2: Enumeración | Herramientas de **fuzzing de directorios y archivos** ocultos en servidores web (HU11). Usan diccionarios para descubrir recursos no indexados como paneles de administración, backups, archivos de configuración expuestos. Gobuster es más rápido (Go), Dirb es más estable (C). | Sprint 2 |
| **Hydra** | Ataque de Fuerza Bruta | S3: Explotación | Herramienta de **ataque de fuerza bruta** contra servicios de autenticación (SSH, FTP, HTTP, SMTP, etc.). Se usa para probar la robustez de credenciales y mecanismos de rate limiting (HU05). | Sprint 3 |
| **MobSF (Mobile Security Framework)** | Análisis de Aplicaciones Móviles | S3: Explotación<br>S4: Post-Explotación | Recomendado para escenarios móviles. Facilita el **análisis estático y dinámico de aplicaciones** Android (APK) e iOS (IPA). Evalúa el manejo de tokens, seguridad de APIs, almacenamiento de datos sensibles y permisos peligrosos. | Sprint 3-4 |
| **OWASP ZAP (Zed Attack Proxy)** | Proxy Web / Escáner | S2: Enumeración<br>S3: Explotación | Alternativa open-source a Burp Suite Professional. Incluye escáner automatizado de vulnerabilidades web, fuzzer, y capacidades de interceptación de tráfico. Útil para complementar Burp Suite en análisis automatizados. | Sprint 2-3 |
| **theHarvester** | OSINT | S1: Reconocimiento | Herramienta de **reconocimiento pasivo** que recopila correos electrónicos, subdominios, hosts, nombres de empleados, puertos abiertos y banners desde fuentes públicas (Google, Bing, Shodan, LinkedIn). | Sprint 1 |
| **Sublist3r** | Enumeración de Subdominios | S1: Reconocimiento | Herramienta especializada en **descubrimiento de subdominios** usando motores de búsqueda y APIs públicas. Fundamental para mapear la superficie de ataque completa de Tavolo. | Sprint 1 |
| **sslscan / testssl.sh** | Análisis SSL/TLS | S1: Reconocimiento<br>S2: Enumeración | Herramientas para evaluar la **configuración de SSL/TLS** en servidores. Identifican cifrados débiles, certificados vencidos, vulnerabilidades como BEAST, POODLE, Heartbleed (HU19). | Sprint 1-2 |

### 2.5.3. Herramientas de Gestión y Documentación

| Herramienta | Propósito | Uso en el Proyecto |
|-------------|-----------|-------------------|
| **GitHub** | Control de Versiones | Repositorio central para código, scripts, evidencias y documentación. Permite trazabilidad de cambios y colaboración del equipo. |
| **Markdown** | Documentación | Formato estándar para todos los reportes técnicos, READMEs y documentación del proyecto. |
| **Jira / Trello** | Gestión Ágil | Tablero Kanban para gestionar el Product Backlog, sprint backlog y seguimiento de tareas. |
| **Obsidian / Notion** | Notas de Pentesting | Herramientas de toma de notas durante las pruebas, organización de hallazgos y colaboración del equipo. |
| **KeepNote / CherryTree** | Notas Jerárquicas | Alternativas open-source para documentar hallazgos de forma estructurada durante el pentesting. |
| **Dradis** | Colaboración en Pentesting | Plataforma colaborativa para que el equipo comparta hallazgos en tiempo real y genere reportes consolidados. |

### 2.5.4. Matriz de Herramientas por Sprint

| Sprint | Herramientas Principales | Herramientas Complementarias |
|--------|-------------------------|------------------------------|
| **Sprint 1** | Nmap, Wireshark, sslscan, theHarvester, Sublist3r | Shodan, crt.sh, Google Dorking |
| **Sprint 2** | Nessus/OpenVAS, Burp Suite, Nikto, Gobuster | OWASP ZAP, curl, Postman |
| **Sprint 3** | Burp Suite, sqlmap, Metasploit, Hydra | OWASP ZAP, BeEF, XSSer, Commix |
| **Sprint 4** | Metasploit, Mimikatz, LinPEAS, WinPEAS | BloodHound, PowerSploit, Empire |
| **Sprint 5** | Markdown, LaTeX, Dradis, Jira | OBS Studio (para videos), Canva (para infografías) |



