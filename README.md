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


### 1.2.2 Perfiles de los integrantes y roles Scrum

| Campo | Información |
|-------|-------------|
|**Nombre de alumno**|  |
| **Foto** | [Insertar foto profesional 200x200px] |
| **Código de estudiante** | UXXXXXXXXX |
| **Carrera** | Ingeniería de Software |
| **Rol Scrum** | Scrum Master |
| **Correo electrónico** | UXXXXXXX@upc.edu.pe |

| Campo | Información |
|-------|-------------|
|**Nombre de alumno**|  |
| **Foto** | [Insertar foto profesional 200x200px] |
| **Código de estudiante** | UXXXXXXXXX |
| **Carrera** | Ingeniería de Software |
| **Rol Scrum** | Product Owner |
| **Correo electrónico** | UXXXXXXX@upc.edu.pe |

| Campo | Información |
|-------|-------------|
|**Nombre de alumno**|  |
| **Foto** | [Insertar foto profesional 200x200px] |
| **Código de estudiante** | UXXXXXXXXX |
| **Carrera** | Ingeniería de Software |
| **Rol Scrum** | Pentester Web |
| **Correo electrónico** | UXXXXXXX@upc.edu.pe |

| Campo | Información |
|-------|-------------|
|**Nombre de alumno**| Brenda Gamio |
| **Foto** | [Insertar foto profesional 200x200px] |
| **Código de estudiante** | U202120344 |
| **Carrera** | Ingeniería de Software |
| **Rol Scrum** | Pentester de APIs/Móvil |
| **Correo electrónico** | u202120344@upc.edu.pe |

| Campo | Información |
|-------|-------------|
|**Nombre de alumno**| Angelo Curi  |
| **Foto** | <img src="https://raw.githubusercontent.com/FullStack-Fury/final-report/main/assets/Angelo.png" alt="Foto profesional de Angelo" width="200" height="200">
| **Código de estudiante** | U202022387 |
| **Carrera** | Ingeniería de Software |
| **Rol Scrum** | Documentador/Analista |
| **Correo electrónico** | U202022387@upc.edu.pe |


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
| Sprint 5: Reporting              | 20h                  | 100h                      | 3     |
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


### 1.4. Aceptación del Servicio de Pentesting (Rules of Engagement)

**Identificación de las partes:** [COMPLETAR]

**Alcance autorizado:** [COMPLETAR]

**Limitaciones:** [COMPLETAR]

**Ventanas de prueba:** [COMPLETAR]

**Responsabilidades:** [COMPLETAR]

**Confidencialidad:** [COMPLETAR]

**Protocolo de comunicación:** [COMPLETAR]

**Aceptación y Firmas:** [COMPLETAR]


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
