# 🎯 GUÍA DE ESTUDIO - UNIDAD 6: CTI, Threat Hunting y SOC
## Método para Examen Multiple Choice

---

## 📚 PARTE 1: CYBER THREAT INTELLIGENCE (CTI)

### 🔑 ¿QUÉ ES CTI?

**DEFINICIÓN CLAVE:**
Disciplina que **recoge, analiza y contextualiza datos** sobre amenazas cibernéticas con el objetivo de **anticipar, prevenir y responder** a ciberataques.

**ENFOQUE:** **PROACTIVO** (no reactivo)

**ÁREAS DE INTERÉS:**
- Ciberdelito
- Hacktivismo
- Ciberespionaje

---

### 🔑 LOS 4 PRINCIPIOS FUNDAMENTALES DE CTI

**TABLA DE PRINCIPIOS:**

| Principio | Palabra Clave | Significado |
|-----------|---------------|-------------|
| **Relevancia** | ALINEARSE con activos y contexto | No toda información es útil |
| **Oportunidad (Timeliness)** | RÁPIDAMENTE | Información pierde valor con el tiempo |
| **Accionabilidad** | TRADUCIRSE en acciones concretas | Debe ser útil para actuar |
| **Precisión** | VERIFICADA | Debe validarse antes de difundir |

**💡 REGLA MNEMOTÉCNICA (ROAP):**
- **R**elevancia
- **O**portunidad
- **A**ccionabilidad
- **P**recisión

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Cuál NO es un principio de CTI?*
- ❌ Complejidad
- ✅ Los 4 principios son: Relevancia, Oportunidad, Accionabilidad, Precisión

---

## 📚 PARTE 2: CICLO DE INTELIGENCIA (¡MUY IMPORTANTE!)

### 🔑 LAS 5 FASES DEL CICLO CTI

**TABLA DE FASES:**

| # | Fase | Qué se hace | Pregunta clave |
|---|------|-------------|----------------|
| **1** | **Planning & Direction** | Definir objetivos y prioridades | ¿Qué necesitamos saber? ¿Qué amenazas son relevantes? |
| **2** | **Collection** | Recolectar información (fuentes internas/externas) | Logs, OSINT, feeds, foros, informes |
| **3** | **Processing** | Limpieza, normalización, estructuración | Convertir datos dispersos en información usable |
| **4** | **Analysis & Production** | Identificar patrones, TTPs, riesgos | Generar productos (informes técnicos, operacionales, estratégicos) |
| **5** | **Dissemination** | Difusión a quien lo necesita | Entregar inteligencia a SOC, dirección, técnicos |

**💡 REGLA MNEMOTÉCNICA (P-CPAD):**
- **P**lanning
- **C**ollection
- **P**rocessing
- **A**nalysis
- **D**issemination

**CONCEPTO IMPORTANTE:**
**CMF** (Collection Management Framework) = Marco de Gestión de la Recolección → Guía todo el proceso de recolección

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿En qué fase del ciclo CTI se normalizan los datos?*
- ✅ Processing
- ❌ Collection
- ❌ Analysis

> *¿Qué fase del ciclo CTI define los objetivos?*
- ✅ Planning & Direction
- ❌ Collection
- ❌ Dissemination

> *La difusión de inteligencia a los equipos técnicos corresponde a:*
- ✅ Dissemination
- ❌ Analysis
- ❌ Processing

---

### 🔑 DATA → INFORMATION → INTELLIGENCE

**CONCEPTO FUNDAMENTAL:**
No todo dato es inteligencia. Hay una transformación progresiva:

1. **DATA** (Datos) → Bruto, sin contexto
2. **INFORMATION** (Información) → Procesado, con contexto
3. **INTELLIGENCE** (Inteligencia) → Analizado, accionable

---

## 📚 PARTE 3: LOS 3 NIVELES DE CTI (¡SUPER IMPORTANTE!)

### 🔑 TABLA COMPARATIVA DE NIVELES

| Nivel | Audiencia | Pregunta | Características | Ejemplo |
|-------|-----------|----------|-----------------|---------|
| **Strategic** | Alta dirección (CISO, CTO, C-Level) | ¿Quién y por qué? | Información de alto nivel, riesgos potenciales, visión a **largo plazo** | Informe sobre APT28: motivaciones políticas, evolución de tácticas |
| **Operational** | Mandos intermedios, Threat Hunter, IR | ¿Dónde y cómo? | TTPs y campañas detalladas, término **medio** | Informe sobre campaña REvil: métodos de acceso, movimiento lateral |
| **Tactical** | Analista SOC, Blue Team | ¿Qué? | Indicadores técnicos accionables (hashes, IPs, dominios), **corto plazo** | Listado de IoCs de REvil para bloquear en firewalls |

**💡 REGLAS MNEMOTÉCNICAS:**

**STRATEGIC:**
- **S**trategic = **S**enior management
- **Largo plazo** → ¿Quién? ¿Por qué?

**OPERATIONAL:**
- **O**perational = **O**peraciones intermedias
- **Medio plazo** → ¿Dónde? ¿Cómo?

**TACTICAL:**
- **T**actical = **T**écnico detallado
- **Corto plazo** → ¿Qué? (IoCs específicos)

**❓ PREGUNTAS TIPO EXAMEN:**

> *Un listado de hashes maliciosos para bloquear en el firewall es inteligencia:*
- ✅ Tactical
- ❌ Strategic
- ❌ Operational

> *Un informe sobre motivaciones políticas de APT28 es inteligencia:*
- ✅ Strategic
- ❌ Tactical
- ❌ Operational

> *¿Qué nivel de CTI responde "¿Dónde y cómo?"*
- ✅ Operational
- ❌ Strategic
- ❌ Tactical

> *¿Qué nivel de CTI es para analistas SOC?*
- ✅ Tactical
- ❌ Strategic
- ❌ Operational

---

## 📚 PARTE 4: NOMENCLATURA DE CIBERACTORES

### 🔑 CONVENCIONES DE NOMBRES

**EJEMPLOS DE NOMBRES:**
- **Basados en malware/actividad**: Lazarus Group
- **Siglas + números**: APT28, APT10, APT33
- **Animales/insectos + adjetivo**: Fancy Bear, Stone Panda
- **Autodenominaciones**: Anonymous

**HERRAMIENTA:**
**Malpedia** → Plataforma de referencia (Fraunhofer FKIE) con información estructurada sobre malware y actores

**EJEMPLOS FAMOSOS:**

**Ciberactores:**
- **APT28** (Fancy Bear, Sofacy, Sednit, STRONTIUM) → Rusia
- **Lazarus Group** → Corea del Norte
- **APT10** (Stone Panda) → China
- **APT33** → Irán

**Malware:**
- **Chopstick** → Usado por APT28
- **Zebrocy** → Variante de APT28
- **Mimikatz** → Post-explotación para credenciales

**Campañas:**
- **Operation Honeybee** → APT37 (Corea del Norte)
- **Night Dragon** → APT chino, empresas energéticas
- **Operation Aurora** → Google atacado por APT chino
- **GhostNet** → Ciberespionaje desde China

**💡 ASOCIACIÓN PAÍSES:**
- 🐻 **BEAR** (Oso) → RUSIA
- 🐼 **PANDA** → CHINA

---

## 📚 PARTE 5: INDICATORS OF COMPROMISE (IOCs)

### 🔑 ¿QUÉ SON LOS IOCS?

**DEFINICIÓN:**
**Piezas de información** o **artefactos digitales** derivados de intrusiones, usados para detectar actividades maliciosas.

**EJEMPLOS:**
- Hashes de archivos maliciosos
- Direcciones IP sospechosas
- URLs
- Nombres de dominio
- Nombres de ejecutables o scripts

**¿PARA QUÉ SE USAN?**
- Detectar ataques en curso o pasados
- Alimentar herramientas (SIEM, EDR, IDS/IPS)
- Mejorar respuesta y contención
- Compartir información entre organizaciones

**💡 IMPORTANTE:**
IoCs **pueden cambiar rápidamente** → Su valor está limitado a corto período

---

## 📚 PARTE 6: CAMPAÑAS

### 🔑 ¿QUÉ ES UNA CAMPAÑA?

**DEFINICIÓN:**
Conjunto **coordinado y planificado** de actividades cibernéticas con objetivos específicos contra blancos definidos.

**CARACTERÍSTICAS CLAVE:**
- **Organizada en el tiempo** (días, semanas, años)
- Comparte **TTPs** (Tácticas, Técnicas, Procedimientos)
- Usa herramientas comunes, malware o infraestructura
- Persigue objetivo claro (espionaje, robo de datos)

**💡 BENEFICIO:**
Análisis de campañas → Identificar patrones y **atribuir acciones** a actores

---

## 📚 PARTE 7: PYRAMID OF PAIN (¡MUY IMPORTANTE!)

### 🔑 PIRÁMIDE DE DOLOR (DAVID BIANCO)

**CONCEPTO:**
Clasifica IoCs según el "**dolor**" o **impacto** que generan en el atacante cuando son detectados/bloqueados.

**DE FÁCIL A DIFÍCIL (abajo hacia arriba):**

| Nivel (↑) | Tipo de IoC | Facilidad de cambio | Efectividad |
|-----------|-------------|---------------------|-------------|
| **6. TTPs** ⭐⭐⭐ | Tácticas, Técnicas, Procedimientos | **MUY DIFÍCIL** | **MÁS EFECTIVO** |
| **5. Tools** | Herramientas, frameworks C2 | Difícil | Alto |
| **4. Network/Host Artifacts** | Archivos, configs, claves de registro | Medio | Medio-Alto |
| **3. Domain Names** | Dominios (pueden usar DGA) | Medio | Medio |
| **2. IP Address** | Direcciones IP (VPN, proxy, TOR) | **FÁCIL** | Bajo |
| **1. Hash Values** ⭐ | Hashes de archivos | **MUY FÁCIL** (cambio mínimo) | **MENOS EFECTIVO** |

**💡 CONCEPTO CLAVE:**
- **Arriba** = Más dolor al atacante → Más efectivo
- **Abajo** = Fácil cambiar → Menos efectivo

**DETALLES:**

**Hash Values:**
- Cambio mínimo en archivo → Hash diferente

**IP Address:**
- Fácil cambiar con proxies, VPN, TOR

**Domain Names:**
- Pueden usar **DGA** (Domain Generation Algorithms)
- DNS dinámico

**Network/Host Artifacts:**
- Claves de registro, procesos, archivos de config
- Más esfuerzo para cambiar

**Tools:**
- Scripts, frameworks C&C
- Rediseño significativo

**TTPs:**
- **NIVEL MÁS ALTO**
- **DIFÍCIL de cambiar**
- **MAYOR VALOR** en threat intelligence

**❓ PREGUNTAS TIPO EXAMEN:**

> *En la Pyramid of Pain, ¿qué es más difícil de cambiar para el atacante?*
- ✅ TTPs
- ❌ IP Address
- ❌ Hash Values

> *¿Qué tipo de IoC es el menos efectivo según la Pyramid of Pain?*
- ✅ Hash Values
- ❌ TTPs
- ❌ Tools

> *Los hashes son fáciles de cambiar porque:*
- ✅ Un cambio mínimo en el archivo altera el hash
- ❌ Son muy complejos
- ❌ Requieren herramientas especiales

> *DGA se usa para cambiar rápidamente:*
- ✅ Domain Names
- ❌ Hash Values
- ❌ TTPs

---

## 📚 PARTE 8: TTPs (TACTICS, TECHNIQUES & PROCEDURES)

### 🔑 ¿QUÉ SON LOS TTPs?

**DEFINICIÓN:**
Describen **cómo piensan, actúan y ejecutan** los ataques los Threat Actors.

**TABLA DE COMPONENTES:**

| Componente | Pregunta | Qué describe | Ejemplo |
|------------|----------|--------------|---------|
| **Tactics** | ¿Qué quiere lograr? | Objetivos generales o metas | Movimiento lateral |
| **Techniques** | ¿Cómo lo hace? | Métodos específicos | Uso de credenciales robadas para acceder a otros sistemas |
| **Procedures** | ¿Con qué herramienta? | Detalles concretos de ejecución | Mimikatz para robar credenciales + RDP para moverse |

**💡 REGLA MNEMOTÉCNICA:**
- **T**actics = **T**arget (objetivo/meta)
- **T**echniques = **T**odo el método (cómo)
- **P**rocedures = **P**articular/Preciso (herramienta específica)

**❓ PREGUNTA TIPO EXAMEN:**
> *"Movimiento lateral" es un ejemplo de:*
- ✅ Táctica (objetivo)
- ❌ Técnica
- ❌ Procedimiento

> *"Uso de Mimikatz para robar credenciales" es un ejemplo de:*
- ✅ Procedimiento
- ❌ Táctica
- ❌ Técnica solamente

---

## 📚 PARTE 9: MITRE ATT&CK (¡SUPER IMPORTANTE!)

### 🔑 ¿QUÉ ES MITRE ATT&CK?

**DEFINICIÓN:**
Framework de **uso global** que documenta **TTPs reales** utilizados por atacantes en distintos entornos.

**NOMBRE COMPLETO:**
**A**dversarial **T**actics, **T**echniques, and **C**ommon **K**nowledge

**BENEFICIOS:**
1. **Visibilidad** → Entender cómo actúan atacantes en cada etapa
2. **Estandarización** → Lenguaje común para analistas y herramientas
3. **Adaptabilidad** → Se aplica a diferentes tipos de ataques
4. **Integración** → Compatible con SIEM, EDR

**URL:** https://attack.mitre.org/

---

### 🔑 CÓMO MAPEAR CON ATT&CK

**PREGUNTAS PARA MAPEAR:**
1. ¿Qué parte del texto describe actividad del adversario?
2. ¿Qué intenta hacer el adversario? → **Táctica**
3. ¿Cómo logra sus objetivos? → **Técnicas y subtécnicas**

---

## 📚 PARTE 10: CYBER KILL CHAIN

### 🔑 ¿QUÉ ES?

**DEFINICIÓN:**
Framework desarrollado por **Lockheed Martin** que describe las **etapas** que sigue un atacante para un ciberataque exitoso.

**OBJETIVO:**
Ayudar a defensores a **entender y detener** al adversario en cada fase del ataque.

**💡 ASOCIACIÓN:**
Cyber Kill Chain = **Etapas secuenciales** del ataque

---

## 📚 PARTE 11: FUENTES DE INTELIGENCIA

### 🔑 TIPOS Y EJEMPLOS

**TIPOS:**
- **Internas**: Logs, SIEM
- **Externas**: Plataformas públicas o comerciales

**FUNCIONES:**
- Recolectar, analizar, enriquecer información
- Aportar **contexto** a IoCs
- Entender relaciones, criticidad, campañas

**EJEMPLOS POPULARES:**
- **AbuseIPDB** (https://www.abuseipdb.com/) → Reputación de IPs maliciosas
- **VirusTotal** (https://www.virustotal.com/) → Análisis de archivos y URLs
- **URL SCAN** (https://urlscan.io/) → Escaneo de sitios web sospechosos

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué herramienta se usa para verificar la reputación de IPs?*
- ✅ AbuseIPDB
- ❌ Nmap
- ❌ Wireshark

---

## 📚 PARTE 12: NIVEL DE CONFIANZA Y TLP

### 🔑 TRAFFIC LIGHT PROTOCOL (TLP)

**TABLA DE NIVELES:**

| Color | Restricción | Uso |
|-------|-------------|-----|
| **TLP RED** | Limitado a personas concretas | Impacto contra privacidad, reputación u operaciones |
| **TLP AMBER** | Limitado a la organización + clientes/proveedores | Necesitan conocerla para protegerse |
| **TLP GREEN** | Comunidad/sector | Útil para todas las organizaciones |
| **TLP WHITE** | Sin restricciones | Puede ser distribuido públicamente (puede tener Copyright) |

**💡 ASOCIACIÓN DE COLORES:**
- **RED** = Muy restringido (peligro)
- **AMBER** = Organización + socios (precaución)
- **GREEN** = Comunidad/sector (compartir)
- **WHITE** = Público (abierto)

**❓ PREGUNTA TIPO EXAMEN:**
> *Información que puede distribuirse sin restricciones es:*
- ✅ TLP WHITE
- ❌ TLP RED
- ❌ TLP AMBER

> *TLP AMBER se comparte con:*
- ✅ Organización, clientes y proveedores que necesiten protegerse
- ❌ Solo personas concretas
- ❌ Todo el público

---

## 📚 PARTE 13: TIP (THREAT INTELLIGENCE PLATFORM)

### 🔑 ¿QUÉ ES UN TIP?

**DEFINICIÓN:**
Plataforma para **recopilar, consolidar, analizar y gestionar** información sobre amenazas de forma **centralizada y automatizada**.

**FUNCIONALIDADES CLAVE:**
- Integración de múltiples fuentes (feeds, OSINT, ISACs)
- Normalización y enriquecimiento automático de IoCs
- Correlación con alertas (SIEM, EDR)
- Gestión del ciclo de vida de indicadores
- Compartición con otras organizaciones

---

### 🔑 MISP (MALWARE INFORMATION SHARING PLATFORM)

**DEFINICIÓN:**
Plataforma **open source** para **recolectar, almacenar, distribuir y compartir** IoCs de manera estructurada y colaborativa.

**CARACTERÍSTICAS:**
- Crear eventos con múltiples IoCs
- Correlación automatizada
- Intercambio entre organizaciones confiables
- Integración con SIEM, firewalls, TIPs
- Exportación en múltiples formatos

**PROYECTO:** https://www.misp-project.org/

**CASO DE USO:**
1. Campaña de phishing detectada
2. Crear evento en MISP con IoCs (URLs, IPs, archivos)
3. Correlacionar con incidentes previos
4. Compartir con organizaciones de confianza
5. Exportar al SIEM/firewall

**❓ PREGUNTA TIPO EXAMEN:**
> *MISP es una plataforma:*
- ✅ Open source para compartir IoCs
- ❌ Comercial para escaneo de vulnerabilidades
- ❌ De detección de malware solamente

---

## 📚 PARTE 14: THREAT HUNTING

### 🔑 ¿QUÉ ES THREAT HUNTING?

**CONCEPTO CLAVE:**
**Dwell Time** = Tiempo entre brecha y detección → Promedio **3 semanas** (a veces meses)

**DEFINICIÓN:**
Estrategia **PROACTIVA** basada en **hipótesis** e investigación **manual** para descubrir amenazas ocultas que herramientas automatizadas no detectan.

**OBJETIVO PRINCIPAL:**
Reducir **dwell time** detectando actores maliciosos en etapas tempranas del **Cyber Kill Chain**.

**💡 DIFERENCIA CLAVE:**
- **Threat Detection** = **REACTIVO** + **AUTOMÁTICO**
- **Threat Hunting** = **PROACTIVO** + **MANUAL**

---

### 🔑 ¿CUÁNDO HACER THREAT HUNTING?

**LISTA DE SITUACIONES:**
- Ante nueva información sobre adversario o vulnerabilidad
- Cuando aparecen nuevos IoCs de adversario conocido
- Múltiples anomalías en la red
- Durante respuesta a incidentes
- **Acciones proactivas periódicas**

**💡 IMPORTANTE:**
No debe ser **esporádica**, sino **continua y estratégica**

---

### 🔑 PROCESO DE THREAT HUNTING (EJEMPLO: EMOTET)

**CASO EMOTET:**
- Troyano bancario → Evolucionó a **plataforma modular** de distribución de malware
- Puerta de entrada para: ransomware, troyanos bancarios, infostealers
- Propagación: contraseñas débiles, exploits, PowerShell
- Vector: **Spam con documentos maliciosos** (macros)

**FASES DEL HUNTING:**

**1. PREPARACIÓN**
- Investigar TTPs del malware (MITRE ATT&CK, VirusTotal, Malpedia)
- Identificar patrones (phishing, macros, persistencia)
- Delimitar objetivos (assets críticos, usuarios susceptibles)

**2. FORMULAR HIPÓTESIS**
- Ejemplo: "Emotet usa cuentas comprometidas para enviar emails con Word malicioso"
- Hipótesis específicas y accionables

**3. DISEÑAR EL HUNT**
- Definir fuentes de datos (logs correo, EDR, firewall, SIEM)
- Diseñar consultas y filtros
- Integrar feeds de Threat Intelligence

**4. RECOPILACIÓN Y ANÁLISIS**
- Aplicar consultas sobre fuentes
- Buscar trazas (adjuntos sospechosos, tráfico C2)
- Usar herramientas: SIEM, Sandboxes, Wireshark, VirusTotal

**5. EVALUAR FINDINGS**
- Confirmar o descartar hipótesis
- Indicadores: subjects sospechosos, macros, conexiones C2
- Analizar alcance: hosts comprometidos, movimiento lateral

**6. MITIGAR AMENAZA**
- Contención: Aislar endpoints, bloquear IPs/dominios C2
- Erradicación: Eliminar malware, remover persistencia
- Restaurar: Revocar credenciales, aplicar parches

**7. DESPUÉS DEL HUNT**
- Documentar hallazgos e hipótesis
- Actualizar TIP con nuevos IoCs
- Compartir con CSIRTs (ej: MISP)
- Mejorar defensas: Ajustar reglas SIEM/EDR
- Lecciones aprendidas

**❓ PREGUNTAS TIPO EXAMEN:**

> *Threat Hunting es una estrategia:*
- ✅ Proactiva basada en hipótesis
- ❌ Reactiva automatizada
- ❌ Solo para después de incidentes

> *El "dwell time" se refiere a:*
- ✅ Tiempo entre brecha y detección
- ❌ Tiempo de respuesta del SOC
- ❌ Tiempo de análisis de malware

> *¿Cuál NO es una fase del Threat Hunting?*
- ❌ Todas son válidas (Preparación, Hipótesis, Diseño, Análisis, Evaluación, Mitigación, Documentación)

---

## 📚 PARTE 15: SECURITY OPERATION CENTER (SOC)

### 🔑 ¿QUÉ ES UN SOC?

**DEFINICIÓN:**
Equipo especializado encargado de **monitorear, prevenir, detectar, analizar y responder** a incidentes de seguridad, con tecnología y procesos adecuados.

**OBJETIVO:**
Mejora continua de la postura de seguridad y mecanismos de defensa.

---

### 🔑 SERVICIOS DE UN SOC

**LISTA DE SERVICIOS:**
- **MDR** (Managed Detection and Response) → **Servicio CORE**
- IRA (Incident Response Assistant)
- Threat Intelligence
- ASM / DRM (Attack Surface / Digital Rights Monitoring)
- Vulnerability Management
- Administración de plataformas de seguridad
- Compliance
- Threat Hunting

**💡 SERVICIO PRINCIPAL:**
**MDR** = Managed Detection and Response

---

### 🔑 LOS 3 PILARES DE UN SOC

**TABLA DE PILARES:**

| Pilar | Componentes | Detalles |
|-------|-------------|----------|
| **Tecnología** | SIEM, EDR, SOAR, TIP, SIRP | Herramientas para detección y respuesta |
| **Personas** | Operación 24x7x365, ingenieros calificados | I+D+I, educación continua |
| **Procesos** | Casos de uso, Playbooks, gestión incidentes | Certificaciones: ISO 27001, SOC 2 |

**❓ PREGUNTA TIPO EXAMEN:**
> *Los 3 pilares de un SOC son:*
- ✅ Tecnología, Personas, Procesos
- ❌ Hardware, Software, Network
- ❌ Detection, Response, Prevention

---

### 🔑 METODOLOGÍA: NIST CYBERSECURITY FRAMEWORK

**5 ETAPAS:**
1. **Identify** (Identificar)
2. **Protect** (Proteger)
3. **Detect** (Detectar)
4. **Respond** (Responder)
5. **Recover** (Recuperar)

**ENFOQUE:**
- **Visibilidad** de lo que pasa
- **Respuesta**: Qué hacer con lo detectado
- **Mejora continua** (tecnología, procesos, personas)
- Flexibilidad
- Agilidad (automatizaciones, integraciones)

**💡 REGLA MNEMOTÉCNICA (I-P-D-R-R):**
- **I**dentify
- **P**rotect
- **D**etect
- **R**espond
- **R**ecover

---

## 📚 PARTE 16: IDENTIFICACIÓN (FASE 1)

### 🔑 ¿QUÉ ESTAMOS DEFENDIENDO?

**OBJETIVO:**
Entender qué activos existen y cuáles son **críticos**.

**INVENTARIO DE ACTIVOS:**
- Jerarquía de red
- Endpoints / Servidores
- Usuarios (privilegiados, VIPs)
- Aplicaciones críticas (ERPs, CRMs)

**PREGUNTAS CLAVE:**
- ¿Qué activos son esenciales?
- ¿Cuáles generan mayor impacto si se comprometen?
- ¿Tenemos inventario actualizado?

---

### 🔑 ORÍGENES DE LOGS IMPORTANTES

**CATEGORÍAS:**

**1. ENDPOINT / SERVIDORES:**
- Eventos de SO
- Aplicaciones (nginx, apache, MySQL, SQL Server)
- Apps empresariales (SAP, CRMs)
- Endpoint Security (EDR, antivirus)

**2. NETWORK:**
- Firewalls (tráfico, bloqueos)
- IDS/IPS (detecciones por firmas)
- Proxies (navegación web)
- CASB (Cloud Apps)
- WAF (ataques a apps web)
- NAC (control de acceso)
- Honeypots

**3. INFRAESTRUCTURA Y SERVICIOS:**
- DNS (resolución de dominios)
- AAA (AD, RADIUS, LDAP, IAM)

**4. CLOUD & SAAS:**
- SaaS (Office365, Google Workspace, Salesforce)
- PaaS (AWS, Azure, GCP)
- DLP (fuga de datos)

**5. VULNERABILITY MANAGEMENT:**
- Scanners (Qualys, Nessus, Rapid7)

---

### 🔑 THREAT INTELLIGENCE EN IDENTIFICACIÓN

**NOTICIAS RELEVANTES:**
- Ciberataques en industria/región
- Vulnerabilidades críticas, exploits activos

**CIBERACTORES:**
- Seguimiento de APTs y grupos criminales
- Mapeo de TTPs (MITRE ATT&CK)

**IOCs:**
- Feeds externos (MISP, AlienVault, AbuseIPDB)
- IoCs de investigaciones internas
- Correlación con eventos locales

---

### 🔑 DIGITAL RISK (OSINT)

**MONITOREO:**
- Foros, redes sociales, sitios paste
- Mercados digitales, Deep y Dark Web

**PROTECCIÓN DE MARCA:**
- Suplantación en redes sociales
- BEC (Business Email Compromise)
- Difamación, uso indebido de marca

**LEAKS:**
- Documentos confidenciales, credenciales, código fuente, PII

**PREPARACIÓN DE ATAQUE:**
- Dominios fraudulentos
- Menciones sospechosas en foros

**TAKEDOWN:**
- Dar de baja activos maliciosos

---

### 🔑 ATTACK SURFACE MONITORING (ASM)

**OBJETIVO:**
Monitorear superficie de ataque para detectar exposición involuntaria o cambios no autorizados.

**ACTIVOS CONOCIDOS:**
- Escaneo de vulnerabilidades y puertos
- DNS, certificados, configuraciones email (SPF, DKIM, DMARC)

**ACTIVOS DESCONOCIDOS (SHADOW IT):**
- Servicios expuestos (Shodan, Censys)
- Apps móviles (stores oficiales/mercado negro)
- Repositorios públicos (GitHub, GitLab)
- Herramientas cloud (Office365, Slack, Trello)

---

## 📚 PARTE 17: PREPARACIÓN (FASE 2)

### 🔑 TECNOLOGÍA: SIEM

**DEFINICIÓN:**
**S**ecurity **I**nformation and **E**vent **M**anagement

**FUNCIÓN:**
Embudo centralizador que recolecta logs de múltiples fuentes, normaliza, correlaciona y detecta patrones sospechosos.

**¿POR QUÉ ES CLAVE?**
Visión **unificada** del entorno, detectar amenazas complejas, cumplir normativas.

**COMPONENTES A CONFIGURAR:**
- Arquitectura de recolección (agentes, syslog, APIs)
- Orígenes de logs (firewall, EDR, AD, apps, nubes)
- Timestamp (correlación efectiva)
- Parsing (extraer campos clave)
- Normalización (formato común)
- Categorización (autenticación, red, malware)
- Métricas (EPS - Events Per Second)
- Retención (tiempo de guardado)
- Compliance (ISO 27001, PCI-DSS)

**PROBLEMA PRINCIPAL:**
**FATIGA DE ALERTAS** → Abrumados por cantidad de alertas

**EJEMPLOS POPULARES:**
- Splunk
- IBM QRadar
- Microsoft Sentinel
- Elastic Security

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué significa SIEM?*
- ✅ Security Information and Event Management
- ❌ Security Internet Event Monitor
- ❌ System Information Enforcement Manager

> *El principal problema de un SIEM es:*
- ✅ Fatiga de alertas
- ❌ Alto costo de hardware
- ❌ Incompatibilidad con Linux

---

### 🔑 INTEGRACIÓN CON SIRP

**SIRP:** **S**ecurity **I**ncident **R**esponse **P**latform

**BENEFICIOS:**
- Creación automática de tickets desde SIEM
- Automatización de acciones (playbooks)
- Coordinación entre equipos
- Escalación según criticidad/SLA
- Análisis y reportes
- Documentación para auditorías

**EJEMPLO OPEN SOURCE:**
**TheHive** → Plataforma para gestión de incidentes

---

### 🔑 TECNOLOGÍA: SOAR

**DEFINICIÓN:**
**S**ecurity **O**rchestration, **A**utomation and **R**esponse

**FUNCIÓN:**
Orquestar, automatizar y responder ante incidentes, reduciendo tiempo de respuesta y carga operativa.

**BENEFICIOS:**
- Reducción de tiempo de respuesta
- Playbooks automatizados
- Integración entre herramientas (SIEM, EDR, Firewalls, CTI)
- Trazabilidad y auditoría

**❓ PREGUNTA TIPO EXAMEN:**
> *SOAR se utiliza para:*
- ✅ Orquestar, automatizar y responder ante incidentes
- ❌ Solo escanear vulnerabilidades
- ❌ Únicamente monitorear logs

---

### 🔑 CONFIGURACIÓN DE LOGS (WINDOWS/LINUX)

**WINDOWS:**
- **GPO** (Group Policy Object) → Microsoft NO habilita políticas de auditoría por defecto
- **Sysmon** → Procesos, servicios, conexiones, archivos, PowerShell

**LINUX:**
- **Auditd**

---

### 🔑 CASOS DE USO

**DEFINICIÓN:**
**Lógicas de detección** para identificar comportamientos sospechosos, ataques o violaciones de políticas.

**MODELADO:**
- **Threat Modelling** → Vectores de ataque, superficies expuestas
- **MITRE ATT&CK / Cyber Kill Chain** → Mapear y cubrir TTPs
- **Compliance** → PCI-DSS, SOX, ISO 27001
- **UEBA** (User & Entity Behavior Analytics) → Comportamientos anómalos
- Alertas de plataformas (EDR, WAF, DLP)

**CICLO DE VIDA:**
1. **Definición** → ¿Qué detectar y por qué?
2. **Desarrollo** → Diseño técnico de lógica
3. **Documentación** → SIGMA (estandarización)
4. **Testing** → Validación con logs reales/simulados
5. **Producción** → Activación con monitoreo
6. **Métricas** → ¿Cuántas alertas? ¿Son útiles? Falsos positivos
7. **Periodic Update/Fine-tuning** → Mejora continua

**EJEMPLOS DE CASOS DE USO:**
- Detectar creación/eliminación de cuenta de usuario
- Detectar cambio de password de admin
- Detectar VPN desde país no autorizado
- Detectar múltiples logins fallidos (mismo usuario, diferente IP)
- Detectar invitación externa en SharePoint/OneDrive
- Detectar conexiones a nodos TOR
- Detectar comandos PowerShell contra Windows Defender
- Detectar explotación de Log4j
- Detectar múltiples hits de firma IPS

**❓ PREGUNTA TIPO EXAMEN:**
> *SIGMA es un proyecto para:*
- ✅ Estandarizar la documentación de casos de uso
- ❌ Escanear vulnerabilidades
- ❌ Cifrar comunicaciones

---

### 🔑 PLAYBOOKS

**DEFINICIÓN:**
Guía **estructurada** que define pasos y procedimientos durante **respuesta ante incidentes**.

**OBJETIVO:**
**Estandarizar** accionar y **reducir improvisación**.

**SE DEFINEN POR:**
Tipo de incidente (phishing, ransomware, DDoS, etc.)

**MÉTODO:**
**5W1H** → Who, What, Where, When, Why, How

**❓ PREGUNTA TIPO EXAMEN:**
> *Un playbook se usa para:*
- ✅ Estandarizar la respuesta ante incidentes
- ❌ Escanear malware
- ❌ Configurar firewalls

---

### 🔑 PERSONAS

**CAPACITACIÓN:**
- Cursos y carreras
- CTF (Capture The Flag)
- Escenarios de ataque y defensa

**OPERACIÓN 24x7x365:**
- Personal suficiente (evitar burnout)
- Alta rotación (especialmente L1)
- Plan de backup
- Evaluar preferencias de turnos
- Regulaciones laborales
- Escalaciones disponibles
- Reuniones inicio/final de turno

---

## 📚 PARTE 18: DETECCIÓN (FASE 3)

### 🔑 MECANISMOS DE DETECCIÓN

**TABLA COMPARATIVA:**

| Mecanismo | Tipo | Automatización | Tecnología | Fuente |
|-----------|------|----------------|------------|--------|
| **Threat Detection** | **REACTIVO** | **AUTOMÁTICO** | SIEM (reglas, dashboards), Plataformas (firmas, alertas) | Tecnología |
| **Threat Hunting** | **PROACTIVO** | **MANUAL** | SIEM, EDR | Hipótesis (MITRE ATT&CK, CTI, investigaciones) |

**❓ PREGUNTA TIPO EXAMEN:**
> *La principal diferencia entre Threat Detection y Threat Hunting es:*
- ✅ Detection es reactivo/automático, Hunting es proactivo/manual
- ❌ Son lo mismo
- ❌ Detection es manual, Hunting es automático

---

## 📚 PARTE 19: ANÁLISIS (FASE 4)

### 🔑 ENRIQUECIMIENTO

**OBJETIVO:**
Agregar **contexto adicional** a IoCs para ayudar al analista a:
- Comprender severidad real
- Determinar si es legítima o falso positivo
- Decidir si requiere respuesta inmediata
- Priorizar según SLA

**SE HACE:** Generalmente de manera **automática**

**PREGUNTAS QUE RESPONDE:**
- ¿Este hash/IP/dominio apareció antes? ¿Qué pasó?
- ¿Está vinculado con eventos pasados?
- ¿Es parte de campaña más amplia?
- ¿Es usuario privilegiado?
- ¿Es servidor crítico?
- ¿Ese comportamiento es común en ese host?

---

### 🔑 TRIAGE (PRIORIZACIÓN)

**DEFINICIÓN:**
Proceso de **evaluación y clasificación** de alertas para determinar prioridad y necesidad de acciones inmediatas.

**TAMBIÉN ES:**
Primer filtro de **falsos positivos**

**CRITERIOS:**

**SEVERIDAD:**
- Criticidad técnica del caso de uso
- Criticidad/cantidad de activos afectados
- Incidentes pasados asociados
- Vulnerabilidades del activo

**ESCALAMIENTO:**
- Tier 2 / Tier 3 / CSIRT
- War Rooms

---

### 🔑 INVESTIGACIÓN

**OBJETIVO:**
Determinar si es **incidente real** y si es así:
- **Alcance** (hosts, usuarios, sistemas)
- **Impacto** (confidencialidad, integridad, disponibilidad)
- **Cómo se produjo** (vulnerabilidades, vectores)
- Movimiento lateral, persistencia

**RESULTADO ESPERADO:**
- Confirmación o descarte
- Identificación de causa raíz
- Visibilidad del comportamiento del atacante
- Insumos para respuesta y contención

---

## 🎯 RESUMEN ULTRA-RÁPIDO (Para 10 min antes del examen)

### 📌 CTI - 4 PRINCIPIOS:
**R**elevancia | **O**portunidad | **A**ccionabilidad | **P**recisión

### 📌 CICLO CTI (P-CPAD):
1. **P**lanning
2. **C**ollection
3. **P**rocessing
4. **A**nalysis
5. **D**issemination

### 📌 3 NIVELES CTI:
- **Strategic** → C-Level, largo plazo, ¿Quién/Por qué?
- **Operational** → Mandos medios, medio plazo, ¿Dónde/Cómo?
- **Tactical** → Analista SOC, corto plazo, ¿Qué? (IoCs)

### 📌 PYRAMID OF PAIN (↑ más efectivo):
6. **TTPs** ⭐ (más difícil cambiar)
5. Tools
4. Network/Host Artifacts
3. Domain Names
2. IP Address
1. Hash Values ⭐ (más fácil cambiar)

### 📌 TTPs:
- **T**actics = ¿Qué lograr? (objetivo)
- **T**echniques = ¿Cómo? (método)
- **P**rocedures = ¿Con qué? (herramienta)

### 📌 TLP:
- **RED** = Muy restringido
- **AMBER** = Organización + socios
- **GREEN** = Comunidad/sector
- **WHITE** = Público

### 📌 THREAT HUNTING:
- **PROACTIVO** + **MANUAL**
- Basado en **hipótesis**
- Reduce **dwell time** (≈3 semanas)

### 📌 SOC - 3 PILARES:
**T**ecnología | **P**ersonas | **P**rocesos

### 📌 NIST FRAMEWORK (I-P-D-R-R):
**I**dentify → **P**rotect → **D**etect → **R**espond → **R**ecover

### 📌 HERRAMIENTAS:
- **SIEM** = Centraliza logs, correlaciona
- **SIRP** = Gestión de incidentes (TheHive)
- **SOAR** = Orquestación y automatización
- **TIP** = Gestión de threat intelligence
- **MISP** = Open source para compartir IoCs

### 📌 CASOS FAMOSOS:
- **APT28** (Fancy Bear) = Rusia
- **APT10** (Stone Panda) = China
- **Lazarus Group** = Corea del Norte

### 📌 DETECTION vs HUNTING:
- **Detection** = Reactivo + Automático
- **Hunting** = Proactivo + Manual

---

## 🔥 ESTRATEGIA PARA EL EXAMEN

### ✅ Palabras clave en preguntas:

**Si ves:** "C-Level" / "alto nivel" → **Strategic**
**Si ves:** "IoCs" / "hashes" / "IPs" / "analista SOC" → **Tactical**
**Si ves:** "TTPs" / "campañas" / "mandos medios" → **Operational**
**Si ves:** "más difícil cambiar" → **TTPs**
**Si ves:** "más fácil cambiar" → **Hash Values** o **IP Address**
**Si ves:** "proactivo" / "hipótesis" / "manual" → **Threat Hunting**
**Si ves:** "reactivo" / "automático" → **Threat Detection**
**Si ves:** "normalizar datos" → **Processing** (ciclo CTI)
**Si ves:** "definir objetivos" → **Planning** (ciclo CTI)
**Si ves:** "difundir a equipos" → **Dissemination**
**Si ves:** "sin restricciones" → **TLP WHITE**
**Si ves:** "solo organización" → **TLP AMBER**
**Si ves:** "compartir IoCs" / "open source" → **MISP**
**Si ves:** "centralizar logs" / "correlacionar" → **SIEM**
**Si ves:** "automatizar respuesta" → **SOAR**
**Si ves:** "guía de respuesta" / "estandarizar" → **Playbook**
**Si ves:** "evaluar y clasificar alertas" → **Triage**

---

## 💪 ¡Éxito en tu examen!

**Recuerda:** Esta unidad tiene 3 grandes bloques:
1. **CTI** → Ciclo, niveles, IoCs, Pyramid of Pain, TTPs
2. **Threat Hunting** → Proactivo, hipótesis, fases
3. **SOC** → Pilares, NIST framework, herramientas (SIEM/SOAR/SIRP)

**Lo más importante:**
- **Ciclo CTI** (5 fases)
- **3 niveles de CTI** (Strategic/Operational/Tactical)
- **Pyramid of Pain** (TTPs arriba, hashes abajo)
- **Diferencia Detection vs Hunting**
- **3 pilares del SOC**
- **NIST framework** (Identify, Protect, Detect, Respond, Recover)
- **Herramientas clave** (SIEM, SOAR, SIRP, MISP)

**Practica las preguntas tipo examen y estarás listo.** 🚀


