# 🎯 GUÍA DE ESTUDIO - UNIDAD 4: Vulnerabilidades y SDLC
## Método para Examen Multiple Choice

---

## 📚 PARTE 1: DEFINICIÓN DE VULNERABILIDADES

### 🔑 ¿QUÉ ES UNA VULNERABILIDAD?

**DEFINICIÓN CLAVE:**
Una vulnerabilidad es una **debilidad** en un sistema, aplicación, proceso o control que **puede ser explotada** por una amenaza para causar daño o realizar acciones no autorizadas.

**💡 IMPORTANTE:**
Las vulnerabilidades NO siempre están en el código → También en hardware, red o procesos humanos/organizacionales

---

## 📚 PARTE 2: TIPOS DE VULNERABILIDADES

### 🔑 TABLA COMPARATIVA DE TIPOS (¡MUY IMPORTANTE!)

| Tipo | Dónde está | Ejemplos | Caso Real Famoso |
|------|------------|----------|------------------|
| **Software** | CÓDIGO, configuraciones | Bugs, software desactualizado, configuraciones inseguras | **Log4Shell** (CVE-2021-44228) |
| **Hardware** | COMPONENTES FÍSICOS | Firmware desactualizado, backdoors, defectos de diseño | **Meltdown & Spectre** (2018) |
| **Red** | INFRAESTRUCTURA de red | Protocolos no cifrados, firewalls mal configurados, WiFi débil | **Heartbleed** (CVE-2014-0160) |
| **Proceso** | PROCEDIMIENTOS, políticas | Ausencia de políticas, autenticación débil, falta de capacitación | **Equifax** (2017) |

**💡 REGLAS MNEMOTÉCNICAS:**

**SOFTWARE:**
- **CÓDIGO** tiene bugs
- Ejemplo: Log4Shell → Librería Log4j de **Java**

**HARDWARE:**
- **FÍSICO** → Procesadores, firmware
- Ejemplo: Meltdown & Spectre → **Procesadores Intel/AMD/ARM**

**RED:**
- **INFRAESTRUCTURA** de comunicación
- Ejemplo: Heartbleed → Falla en **OpenSSL**

**PROCESO:**
- **HUMANO/ORGANIZACIONAL** → Políticas, capacitación
- Ejemplo: Equifax → No aplicaron **PARCHE a tiempo**

---

### 🔑 CASOS REALES IMPORTANTES

**LOG4SHELL (CVE-2021-44228) - 2021**
- Librería **Log4j** de Java
- Permitía **RCE** (Remote Code Execution)
- **Una de las vulnerabilidades más graves de la década**

**MELTDOWN & SPECTRE - 2018**
- Fallas en **procesadores** Intel, AMD, ARM
- Explotaban **ejecución especulativa**
- Acceso a **memoria sensible**

**HEARTBLEED (CVE-2014-0160) - 2014**
- Falla en **OpenSSL** (protocolo TLS/SSL)
- Permitía leer **memoria del servidor**
- Afectó: claves privadas, contraseñas, tokens
- Impacto: **Millones** de servidores web, VPNs, routers

**EQUIFAX BREACH - 2017**
- **NO aplicaron parche** a tiempo (Apache Struts, CVE-2017-5638)
- Exposición de: SSN, tarjetas, licencias
- Costo: **+700 millones** de dólares

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Qué vulnerabilidad afectó a la librería Log4j de Java?*
- ✅ Log4Shell (CVE-2021-44228)
- ❌ Heartbleed
- ❌ Spectre

> *Meltdown y Spectre afectaron principalmente a:*
- ✅ Procesadores (Intel, AMD, ARM)
- ❌ Librerías de software
- ❌ Routers

> *¿Qué caso fue causado por NO aplicar un parche a tiempo?*
- ✅ Equifax (2017)
- ❌ Heartbleed
- ❌ Log4Shell

> *Heartbleed afectó a:*
- ✅ OpenSSL (protocolo TLS/SSL)
- ❌ Procesadores
- ❌ Log4j

---

## 📚 PARTE 3: ZERO-DAY Y CVE

### 🔑 ZERO-DAY

**DEFINICIÓN:**
Vulnerabilidad **desconocida públicamente** que **aún NO tiene parche** ni solución oficial disponible.

**NOMBRE:**
"Zero-Day" = El desarrollador tiene **CERO días** desde su descubrimiento para corregirla.

**¿POR QUÉ SON TAN PELIGROSOS?**
- ❌ No hay firmas de detección en antivirus/IDS
- ❌ Las organizaciones NO pueden protegerse proactivamente
- 💰 Muy valiosos en mercado negro (hasta **millones de dólares**)
- 🎯 Usados en APT, ciberespionaje, campañas gubernamentales

**💡 FRASE:**
> "Los Zero-Days no solo son puertas abiertas, son puertas que **nadie sabe que existen**"

---

### 🔑 CVE (COMMON VULNERABILITIES AND EXPOSURES)

**DEFINICIÓN:**
Sistema de registro **público** que asigna **identificadores únicos** a vulnerabilidades conocidas.

**MANTENIDO POR:** MITRE

**FORMATO:** `CVE-<AÑO>-<4/5/7 dígitos>`

**EJEMPLO:** CVE-2021-44228 (Log4Shell)

**ESTADÍSTICA 2024:**
- **40.700+ CVEs** publicados
- Promedio: **108 CVEs POR DÍA**
- Aumento del **≈39%** respecto a 2023

**FUENTES:**
- https://nvd.nist.gov/vuln/search (Base NVD con CVSS y parches)
- https://www.cve.org/ (Repositorio oficial MITRE)

**💡 ASOCIACIÓN:**
CVE = **Lenguaje común** para identificar vulnerabilidades

---

### 🔑 EXPLOIT DATABASE

**DEFINICIÓN:**
Repositorio **público y gratuito** de exploits conocidos para vulnerabilidades reales.

**MANTENIDO POR:** **Offensive Security** (creadores de Kali Linux)

**URL:** https://www.exploit-db.com/

**HERRAMIENTA:** `searchsploit` (búsqueda en terminal)

**💡 ASOCIACIÓN:**
Exploit Database = Vincula **CVE con código de explotación**

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Qué es un Zero-Day?*
- ✅ Vulnerabilidad sin parche conocido
- ❌ Vulnerabilidad antigua
- ❌ Exploit público

> *El formato de CVE es:*
- ✅ CVE-<AÑO>-<DÍGITOS>
- ❌ CVE-<EMPRESA>-<NÚMERO>
- ❌ VUL-<AÑO>-<ID>

> *¿Quién mantiene el sistema CVE?*
- ✅ MITRE
- ❌ NIST
- ❌ OWASP

> *Exploit Database es mantenido por:*
- ✅ Offensive Security
- ❌ MITRE
- ❌ Microsoft

---

## 📚 PARTE 4: CVSS (COMMON VULNERABILITY SCORING SYSTEM)

### 🔑 ¿QUÉ ES CVSS?

**DEFINICIÓN:**
Sistema **estándar** para asignar nivel de severidad **numérico** (0.0 – 10.0) a vulnerabilidades conocidas.

**¿PARA QUÉ SIRVE?**
- Estimar **impacto técnico**
- **Priorizar** parches o mitigaciones
- **Comparar** vulnerabilidades

---

### 🔑 CVSS v3.1

**COMPONENTES (8 MÉTRICAS BASE):**

**1) Vector de Ataque:**
- **AV** (Attack Vector): Red / Local / Físico
- **AC** (Attack Complexity): Alta / Baja
- **PR** (Privileges Required): Ninguno / Bajo / Alto
- **UI** (User Interaction): Requiere o no intervención del usuario

**2) Impacto:**
- **C**: Confidencialidad
- **I**: Integridad
- **A**: Availability (Disponibilidad)

**3) Alcance (Scope):**
- Si el impacto afecta más allá del componente vulnerable

**RESULTADO:** Base Score de **0.0 a 10.0**
- 0.0-3.9 → **Bajo**
- 4.0-6.9 → **Medio**
- 7.0-8.9 → **Alto**
- 9.0-10.0 → **Crítico**

**EJEMPLO CVSS 3.1:**
`CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:H/A:H`

---

### 🔑 CRÍTICAS A CVSS v3.1

**LIMITACIONES:**

1. **Falta de contexto real**
   - No refleja riesgo específico de la organización
   - No distingue si está explotada activamente

2. **Inconsistencia en puntuación**
   - Vulnerabilidades poco explotables → scores altos
   - Casos críticos → pueden no parecerlo

3. **Transparencia y manipulación**
   - Puede estar influenciada por intereses comerciales

4. **Escasez de métricas contextuales**
   - No considera: ¿Está expuesto a Internet? ¿Hay exploit público?

**💡 CLAVE:**
CVSS NO es suficiente → Necesita **CONTEXTO**

---

### 🔑 CVSS v4.0 (NOVIEMBRE 2023)

**MEJORAS:**

**Eliminación de Scope** → Absorbido por otras métricas

**NUEVAS MÉTRICAS:**
1. **Safety** → ¿Puede causar daño físico a personas?
2. **Automation** → ¿Qué tan fácil es automatizar la explotación?
3. **Recovery** → ¿Qué tan difícil es restaurar el sistema?
4. **Exploitation Status** → ¿Está siendo explotada activamente?

**NO BASARSE SOLO EN BASE SCORE:**
- **Threat Score** → Contexto de amenaza real
- **Environmental Score** → Ajustado al entorno y criticidad

**EJEMPLO CVSS 4.0:**
`CVSS:4.0/AV:L/AC:L/AT:P/PR:L/UI:N/VC:H/VI:H/VA:H/SC:N/SI:N/SA:N`

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Qué rango indica una vulnerabilidad CRÍTICA en CVSS?*
- ✅ 9.0-10.0
- ❌ 7.0-8.9
- ❌ 4.0-6.9

> *¿Qué métrica fue eliminada en CVSS v4.0?*
- ✅ Scope (Alcance)
- ❌ Confidencialidad
- ❌ Integridad

> *La métrica "Safety" en CVSS v4.0 evalúa:*
- ✅ Si puede causar daño físico a personas
- ❌ La complejidad del ataque
- ❌ Los privilegios requeridos

> *¿Qué versión de CVSS introdujo "Exploitation Status"?*
- ✅ CVSS v4.0
- ❌ CVSS v3.1
- ❌ CVSS v2.0

---

## 📚 PARTE 5: PRIORIZACIÓN SEGÚN CONTEXTO

### 🔑 CONTEXTUALIZACIÓN (MÁS ALLÁ DE CVSS)

**EVALUAR:**
1. ✅ Gravedad técnica (CVSS)
2. ✅ **Exposición** del sistema (¿Internet? ¿Crítico?)
3. ✅ **Dificultad de explotación** (¿Requiere interacción?)
4. ✅ Disponibilidad de **PoC** (Proof of Concept)
5. ✅ **Impacto** en el negocio
6. ✅ Usuarios y datos afectados

---

### 🔑 APOYO DE CIBERINTELIGENCIA

**PERMITE:**
- **Aumentar/disminuir criticidad** según:
  - Explotación activa por ciberactores
  - Inclusión en campañas recientes
  - Uso en ransomware, APTs

- **Enfocar recursos**:
  - Priorizar con explotación inminente

- **Reducir riesgo operacional**:
  - Decisiones basadas en amenazas reales

---

## 📚 PARTE 6: CICLO OODA

### 🔑 ¿QUÉ ES OODA?

**DEFINICIÓN:**
Ciclo desarrollado por coronel John Boyd para **toma de decisiones rápidas** en entornos dinámicos.

**OODA = Observe - Orient - Decide - Act**

---

### 🔑 OODA PARA GESTIÓN DE VULNERABILIDADES

**TABLA DE LAS 4 FASES:**

| Fase | Pregunta | Qué se hace | Ejemplo |
|------|----------|-------------|---------|
| **1. Observe** | ¿Qué está pasando? | Monitorear CVEs, exploits, threat intelligence | "Se publica CVE-2024-12345 con CVSS 9.8" |
| **2. Orient** | ¿Cómo nos afecta? | ¿Tenemos activos vulnerables? ¿Están expuestos? | "Afecta nuestro Apache expuesto en producción" |
| **3. Decide** | ¿Qué vamos a hacer? | Parchear, workaround, mitigar, posponer | "Aplicar parche esta noche" |
| **4. Act** | Ejecutar y validar | Implementar, verificar, documentar | "Parcheado con éxito, monitoreando" |

**💡 REGLA MNEMOTÉCNICA (OODA):**
- **O**bserve → Monitorear
- **O**rient → Analizar impacto
- **D**ecide → Decidir acción
- **A**ct → Ejecutar

**❓ PREGUNTA TIPO EXAMEN:**

> *En el ciclo OODA, la fase donde se decide si parchear o aplicar workaround es:*
- ✅ Decide
- ❌ Orient
- ❌ Act

> *La fase "Orient" del ciclo OODA responde:*
- ✅ ¿Cómo nos afecta esta vulnerabilidad?
- ❌ ¿Qué está pasando?
- ❌ ¿Qué vamos a hacer?

---

## 📚 PARTE 7: TÉCNICAS DE DETECCIÓN

### 🔑 HERRAMIENTAS Y TÉCNICAS

**TABLA COMPARATIVA:**

| Técnica/Herramienta | Qué hace | Ejemplos |
|---------------------|----------|----------|
| **Escáneres de Vulnerabilidades** | Detectan vulnerabilidades conocidas (firmas CVE) | Nessus, OpenVAS, Qualys, Rapid7 |
| **Escaneo de Configuraciones** | Analizan configuraciones inseguras | MBSA, Azure Defender, AWS Inspector |
| **Gestión de Parches** | Automatizan detección y aplicación de parches | WSUS, SCCM |
| **SAST** | Analiza código **SIN ejecutar** | SonarQube, Checkmarx, Veracode |
| **DAST** | Evalúa aplicación **EN EJECUCIÓN** | OWASP ZAP, Burp Suite, Acunetix |
| **Dependency Scanners** | Detectan bibliotecas con vulnerabilidades | Snyk, OWASP Dependency-Check |

---

### 🔑 SAST vs DAST (¡SUPER IMPORTANTE!)

**DIFERENCIAS CLAVE:**

| Aspecto | SAST | DAST |
|---------|------|------|
| **Nombre completo** | **S**tatic **A**pplication **S**ecurity **T**esting | **D**ynamic **A**pplication **S**ecurity **T**esting |
| **Cuándo** | Tiempo de **DESARROLLO** | Aplicación **EN EJECUCIÓN** |
| **Acceso** | Requiere **CÓDIGO FUENTE** | **NO requiere** código |
| **Análisis** | **Estático** (sin ejecutar) | **Dinámico** (ejecutando) |
| **Detecta** | Inyecciones, validación débil, manejo inseguro | SQL Injection, XSS, errores de autenticación |
| **Integración** | Pipelines **CI/CD**, **DevSecOps** | Testing en ambiente de pruebas |
| **Perspectiva** | Como **DESARROLLADOR** (código) | Como **ATACANTE** (caja negra) |

**💡 REGLAS MNEMOTÉCNICAS:**

**SAST:**
- **S**tatic = **S**in ejecutar
- Analiza **código fuente**
- Fase de **desarrollo**

**DAST:**
- **D**ynamic = **E**jecutando
- **NO** requiere código
- Como un **atacante externo**

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Qué herramienta analiza el código sin ejecutarlo?*
- ✅ SAST
- ❌ DAST
- ❌ IAST

> *¿Qué técnica evalúa la aplicación desde la perspectiva de un atacante externo?*
- ✅ DAST
- ❌ SAST
- ❌ Manual Code Review

> *SAST se integra típicamente en:*
- ✅ Pipelines CI/CD
- ❌ Solo en producción
- ❌ Solo testing manual

> *¿Qué herramienta NO requiere acceso al código fuente?*
- ✅ DAST
- ❌ SAST
- ❌ Ninguna

> *OWASP ZAP es un ejemplo de:*
- ✅ DAST
- ❌ SAST
- ❌ Escáner de red

---

## 📚 PARTE 8: DIFICULTADES PARA REMEDIAR

### 🔑 BARRERAS COMUNES

**LISTA DE DIFICULTADES:**

1. **Limitaciones operativas**
   - Parchear requiere **reinicios**
   - Riesgo de **interrupción** de servicios críticos

2. **Infraestructura obsoleta**
   - Sistemas **legacy** sin soporte
   - Aplicaciones críticas sin entornos de **testing**

3. **Falta de visibilidad**
   - Nadie "**dueño**" de algunos sistemas
   - Inventario **incompleto**

4. **Procesos lentos**
   - Requiere **aprobaciones múltiples**
   - No hay procesos **automatizados**

**💡 FRASE:**
> "Saber qué parchear no es suficiente. El verdadero reto es **cuándo, cómo y si podemos hacerlo**."

---

## 📚 PARTE 9: SDLC (SOFTWARE DEVELOPMENT LIFE CYCLE)

### 🔑 ¿QUÉ ES SDLC?

**DEFINICIÓN:**
Marco **estructurado** que define las fases necesarias para desarrollar, entregar y mantener software de manera **ordenada y eficiente**.

**OBJETIVO:**
Software funcional, de calidad, mantenible y alineado al negocio.

---

### 🔑 LAS 7 ETAPAS DEL SDLC (¡MEMORÍZALAS!)

**TABLA DE ETAPAS:**

| # | Etapa | Qué se hace |
|---|-------|-------------|
| **1** | **Planificación** | Objetivos, alcance, cronograma, recursos |
| **2** | **Análisis de Requisitos** | Relevar necesidades del usuario/cliente |
| **3** | **Diseño** | Arquitectura, interfaces, bases de datos, tecnologías |
| **4** | **Desarrollo (Coding)** | Construcción del software |
| **5** | **Pruebas (Testing)** | Validar funcionamiento (funcional, seguridad, rendimiento) |
| **6** | **Implementación (Deployment)** | Paso a producción |
| **7** | **Mantenimiento** | Corrección de errores, mejoras, actualizaciones |

**💡 REGLA MNEMOTÉCNICA (PAD-DPiM):**
- **P**lanificación
- **A**nálisis
- **D**iseño
- **D**esarrollo
- **P**ruebas
- **I**mplementación
- **M**antenimiento

---

## 📚 PARTE 10: SECURE SDLC

### 🔑 ¿QUÉ ES SECURE SDLC?

**DEFINICIÓN:**
Busca **integrar controles y buenas prácticas de seguridad** en **CADA ETAPA** del desarrollo, para **prevenir vulnerabilidades desde el diseño**, no solo corregirlas al final.

**FRASE CLAVE:**
> "El SDLC define cómo se construye el software. El **Secure SDLC** define cómo se construye **con seguridad desde el primer día**."

---

### 🔑 ¿POR QUÉ ES NECESARIO?

**ERROR COMÚN:**
Postergar seguridad hasta las pruebas finales cuando:
- ❌ La mayor parte del código ya fue escrita
- ❌ El diseño NO se puede modificar fácilmente
- ❌ El costo de corregir fallas es **MUCHO MAYOR**

**💡 CONCEPTO:**
> "Integrar seguridad en cada fase NO es una opción: es una **NECESIDAD**"

---

### 🔑 BENEFICIOS DE SECURE SDLC

**LISTA DE BENEFICIOS:**
1. ✅ Fallas detectadas y corregidas **MÁS TEMPRANO**
2. ✅ Se evitan **retrabajos** y retrasos
3. ✅ Fortalece **cultura** de desarrollo seguro
4. ✅ Reducción de vulnerabilidades en **producción**
5. ✅ Gana **confianza** del usuario final
6. ✅ **Menor costo** de remediación
7. ✅ Menor exposición al **riesgo**

---

## 📚 PARTE 11: SEGURIDAD EN CADA ETAPA DEL SDLC

### 🔑 TABLA COMPLETA (¡MUY IMPORTANTE!)

| Etapa | Actividades de Seguridad Clave |
|-------|--------------------------------|
| **1. Planificación** | • Evaluar riesgo y panorama de amenazas<br>• ¿Qué datos manejará?<br>• ¿Dónde se almacenarán?<br>• Evaluar impacto de incidentes |
| **2. Análisis de Requisitos** | • Incorporar requisitos de seguridad<br>• Autenticación fuerte<br>• Control de accesos (RBAC)<br>• Requisitos legales (GDPR, HIPAA) |
| **3. Diseño** | • **Threat Modeling** (Modelado de amenazas)<br>• Seguridad como parte de arquitectura<br>• Principios: Least Privilege, Defense in Depth<br>• Evaluar impacto de decisiones |
| **4. Desarrollo** | • Capacitación en **OWASP Top 10**, CWE<br>• Integración de **SAST**<br>• **Dependency Scanners** (Snyk, OWASP Dependency-Check)<br>• Control de versiones, secretos en variables de entorno |
| **5. Testing** | • Revisión de código (manual/por pares)<br>• **SAST** (estático)<br>• **DAST** (dinámico)<br>• Pentesting<br>• Validar cumplimiento normativo |
| **6. Implementación** | • Evaluar seguridad del entorno<br>• Revisar configuraciones<br>• Cifrado en tránsito y reposo<br>• Backups antes de deploy<br>• Rollback plan |
| **7. Mantenimiento** | • Gestión continua de vulnerabilidades<br>• **Monitoreo** y detección de incidentes<br>• Control de cambios<br>• Retroalimentación y mejora continua |

---

### 🔑 CONCEPTOS CLAVE POR ETAPA

**1. PLANIFICACIÓN:**
- Pregunta: ¿Qué datos manejará? ¿Son críticos?

**2. ANÁLISIS:**
- Requisitos **funcionales** Y de **seguridad**
- Cumplimiento: GDPR, HIPAA, PCI DSS

**3. DISEÑO:**
- **Threat Modeling** (Modelado de amenazas) ⭐
- Principios: **Least Privilege**, **Defense in Depth**

**4. DESARROLLO:**
- **OWASP Top 10** (vulnerabilidades web más comunes)
- **SAST** en pipelines CI/CD
- **Dependency Scanners** → Detectar bibliotecas vulnerables
- Nunca hardcodear secretos

**5. TESTING:**
- **SAST** + **DAST** ⭐
- Code Review
- Pentesting

**6. IMPLEMENTACIÓN:**
- Configuraciones seguras
- **Cifrado** (en tránsito y reposo)
- **Backups** antes de deploy
- **Rollback plan**

**7. MANTENIMIENTO:**
- **Monitoreo continuo**
- Gestión de vulnerabilidades
- Respuesta a incidentes

---

### 🔑 TÉRMINOS IMPORTANTES

**THREAT MODELING:**
Modelado de amenazas → Identificar amenazas potenciales en fase de diseño

**OWASP TOP 10:**
Lista de las 10 vulnerabilidades web más críticas

**DEVSECOPS:**
Integración de seguridad en DevOps (Development + Security + Operations)

**CI/CD:**
Continuous Integration / Continuous Deployment → Automatización de desarrollo y despliegue

**DEPENDENCY SCANNER:**
Herramienta que detecta bibliotecas con vulnerabilidades conocidas

**LEAST PRIVILEGE:**
Principio de mínimos privilegios

**DEFENSE IN DEPTH:**
Defensa en profundidad → Múltiples capas de seguridad

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿En qué etapa del SDLC se debe hacer Threat Modeling?*
- ✅ Diseño
- ❌ Desarrollo
- ❌ Mantenimiento

> *¿Qué herramienta detecta bibliotecas con vulnerabilidades conocidas?*
- ✅ Dependency Scanner (ej: Snyk)
- ❌ SAST
- ❌ DAST

> *OWASP Top 10 lista:*
- ✅ Las 10 vulnerabilidades web más críticas
- ❌ Los 10 mejores escáneres
- ❌ Los 10 mejores frameworks

> *¿En qué etapa se integra SAST?*
- ✅ Desarrollo (en pipelines CI/CD)
- ❌ Solo en producción
- ❌ Solo en planificación

> *¿En qué etapa se debe evaluar "¿Qué datos manejará la aplicación?"*
- ✅ Planificación
- ❌ Desarrollo
- ❌ Testing

> *El principio de Least Privilege significa:*
- ✅ Otorgar solo los permisos mínimos necesarios
- ❌ Dar acceso completo
- ❌ No dar permisos a nadie

> *DevSecOps integra:*
- ✅ Development + Security + Operations
- ❌ Solo Development y Security
- ❌ Solo Operations

---

## 🎯 RESUMEN ULTRA-RÁPIDO (Para 10 min antes del examen)

### 📌 TIPOS DE VULNERABILIDADES:
- **Software** = Código (Log4Shell)
- **Hardware** = Físico (Meltdown/Spectre)
- **Red** = Infraestructura (Heartbleed)
- **Proceso** = Humano (Equifax - no parche)

### 📌 CONCEPTOS CLAVE:
- **Zero-Day** = Sin parche conocido
- **CVE** = Identificador único (MITRE)
- **CVSS** = Score 0.0-10.0 (pero necesita contexto)
- **CVSS v4.0** eliminó Scope, agregó Safety/Automation/Recovery

### 📌 CICLO OODA:
1. **O**bserve → Monitorear
2. **O**rient → ¿Nos afecta?
3. **D**ecide → ¿Qué hacer?
4. **A**ct → Ejecutar

### 📌 DETECCIÓN:
- **SAST** = Estático, SIN ejecutar, código fuente
- **DAST** = Dinámico, EN EJECUCIÓN, como atacante
- **Dependency Scanner** = Bibliotecas vulnerables

### 📌 SDLC - 7 ETAPAS (PAD-DPiM):
1. **P**lanificación
2. **A**nálisis
3. **D**iseño
4. **D**esarrollo
5. **P**ruebas
6. **I**mplementación
7. **M**antenimiento

### 📌 SECURE SDLC - POR ETAPA:
1. **Planificación** → ¿Qué datos? ¿Impacto?
2. **Análisis** → Requisitos de seguridad, cumplimiento
3. **Diseño** → **Threat Modeling** ⭐
4. **Desarrollo** → **OWASP Top 10**, **SAST**, **Dependency Scanner** ⭐
5. **Testing** → **SAST + DAST**, Pentesting ⭐
6. **Implementación** → Cifrado, backups, rollback
7. **Mantenimiento** → Monitoreo, gestión vulnerabilidades

### 📌 CASOS REALES:
- **Log4Shell** = Log4j, Java, RCE
- **Meltdown/Spectre** = Procesadores
- **Heartbleed** = OpenSSL
- **Equifax** = No parche, 700M pérdida

---

## 🔥 ESTRATEGIA PARA EL EXAMEN

### ✅ Palabras clave en preguntas:

**Si ves:** "sin parche conocido" → **Zero-Day**
**Si ves:** "identificador único de vulnerabilidad" → **CVE**
**Si ves:** "0.0-10.0" / "severidad numérica" → **CVSS**
**Si ves:** "analiza código sin ejecutar" → **SAST**
**Si ves:** "evalúa aplicación en ejecución" → **DAST**
**Si ves:** "bibliotecas vulnerables" → **Dependency Scanner**
**Si ves:** "Log4j" → **Log4Shell**
**Si ves:** "procesadores Intel/AMD" → **Meltdown/Spectre**
**Si ves:** "OpenSSL" → **Heartbleed**
**Si ves:** "no aplicó parche a tiempo" → **Equifax**
**Si ves:** "modelado de amenazas" → **Threat Modeling** (Diseño)
**Si ves:** "10 vulnerabilidades web" → **OWASP Top 10**
**Si ves:** "¿Cómo nos afecta?" → **Orient** (OODA)
**Si ves:** "Observe-Orient-Decide-Act" → **Ciclo OODA**

---

## 💪 ¡Éxito en tu examen!

**Recuerda:** Esta unidad tiene 2 partes grandes:
1. **VULNERABILIDADES**: Tipos, CVE, CVSS, detección (SAST/DAST)
2. **SDLC**: 7 etapas + Secure SDLC (seguridad en cada etapa)

**Lo más importante:**
- Diferencia **SAST vs DAST**
- Las **7 etapas del SDLC**
- **Seguridad en cada etapa** (especialmente Threat Modeling en Diseño)
- **Casos reales** (Log4Shell, Meltdown/Spectre, Heartbleed, Equifax)
- **Ciclo OODA** para gestión de vulnerabilidades

**Practica las preguntas tipo examen y estarás listo.** 🚀

