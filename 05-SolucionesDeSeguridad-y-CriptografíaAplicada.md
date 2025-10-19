# 🎯 GUÍA DE ESTUDIO - UNIDAD 5: Soluciones de Seguridad y Criptografía Aplicada
## Método para Examen Multiple Choice

---

## 📚 PARTE 1: CONCEPTOS FUNDAMENTALES

### 🔑 DEFENSE IN DEPTH (Defensa en Profundidad)

**DEFINICIÓN:**
Enfoque de "**seguridad en capas**" que aplica **múltiples controles defensivos** en distintos puntos del sistema (red, endpoint, usuario, datos, apps).

**CONCEPTO CLAVE:**
Si una capa falla, **otra actúa como barrera secundaria**.

**💡 ASOCIACIÓN:**
Defense in Depth = **CAPAS** de seguridad (como una cebolla)

---

### 🔑 MODELO ZERO TRUST

**PRINCIPIO FUNDAMENTAL:**
> "**Nunca confíes, siempre verifica**"

**DEFINICIÓN:**
Modelo de seguridad donde **nada ni nadie es confiable por defecto**, incluso si el acceso proviene de dentro de la red.

**¿POR QUÉ EXISTE?**
- El perímetro de red tradicional ya **NO existe** (cloud, BYOD, trabajo remoto)
- Muchos ataques son desde **ADENTRO** (insiders)

**PRINCIPIOS CLAVE (5):**
1. **Verificación continua** → Cada solicitud debe autenticarse
2. **Mínimos privilegios** → Solo acceso estrictamente necesario
3. **Contexto y ubicación** → Dispositivo, ubicación, riesgo, hora
4. **Segmentación** → Red dividida en zonas seguras
5. **Monitoreo constante** → Registrar y analizar todo el tiempo

**💡 ASOCIACIÓN:**
Zero Trust = **DESCONFIAR** de TODO, siempre verificar

**❓ PREGUNTA TIPO EXAMEN:**
> *El modelo Zero Trust se basa en:*
- ✅ Nunca confiar, siempre verificar
- ❌ Confiar en usuarios internos
- ❌ Solo proteger el perímetro

> *¿Por qué surge Zero Trust?*
- ✅ El perímetro tradicional ya no existe (cloud, remoto)
- ❌ Los firewalls son obsoletos
- ❌ Para reducir costos

---

## 📚 PARTE 2: SEGURIDAD EN REDES (NETWORK SECURITY)

### 🔑 SSL/TLS

**TLS (TRANSPORT LAYER SECURITY):**
Protocolo **criptográfico** que proporciona seguridad en comunicaciones a través de redes.

**3 OBJETIVOS:**
1. **Confidencialidad** → Nadie puede leer la información
2. **Integridad** → Datos no modificados en el camino
3. **Autenticación** → Verificar con quién hablamos

**HISTORIA:**
- **SSL** → Creado por Netscape en los 90s, **OBSOLETO** (inseguro)
- **TLS** → Sucesor de SSL, mantenido por IETF desde 1999
- **TLS 1.3** → Versión actual (agosto 2018)

**FASES DE TLS:**
1. **Handshake** → Cliente y servidor acuerdan algoritmos, intercambian certificados y claves
2. **Cifrado de datos** → Todo el tráfico cifrado con claves de sesión

**PUERTOS COMUNES:**
- HTTP → Puerto **80** (sin cifrado)
- **HTTPS** (HTTP sobre TLS) → Puerto **443** (cifrado)
- SMTP → Puerto **25** (sin cifrado)
- **SMTPS** → Puerto **465** (con TLS)

**💡 ASOCIACIÓN:**
- TLS = Sucesor de SSL (más moderno y seguro)
- HTTPS = HTTP + TLS (puerto 443)

**❓ PREGUNTAS TIPO EXAMEN:**
> *¿Qué protocolo reemplazó a SSL?*
- ✅ TLS
- ❌ SSH
- ❌ IPSec

> *El puerto estándar para HTTPS es:*
- ✅ 443
- ❌ 80
- ❌ 8080

> *TLS garantiza: (seleccione todas)*
- ✅ Confidencialidad
- ✅ Integridad
- ✅ Autenticación

---

### 🔑 FIREWALLS - TABLA COMPARATIVA (¡MUY IMPORTANTE!)

| Tipo de Firewall | Capa OSI | Qué analiza | Características | Ejemplos |
|------------------|----------|-------------|-----------------|----------|
| **Packet Filtering** | 3-4 (Red/Transporte) | Solo HEADERS | Más simple, rápido, NO analiza contenido | iptables, AWS Security Groups |
| **Stateful Inspection** | 3-4 | Headers + ESTADO de conexión | Recuerda conexiones activas | Fortinet FortiGate, Palo Alto, Cisco Firepower |
| **Proxy** | 7 (Aplicación) | INTERMEDIARIO completo | Recibe y retransmite solicitudes | Squid, Zscaler |
| **WAF** | 7 (Aplicación) | Tráfico HTTP/HTTPS | Protege apps web, mitiga OWASP Top 10 | Cloudflare WAF, AWS WAF, Azure WAF |
| **NGFW** | 3-7 (Múltiples) | DPI, apps, URL, IPS, AV | Combina funciones avanzadas | Fortinet, Palo Alto, Check Point |
| **Cloud-based** | Variable | Gestionado desde la nube | FWaaS, escalable | AWS Network Firewall, Cloudflare |

**💡 REGLAS MNEMOTÉCNICAS:**

**PACKET FILTERING:**
- Solo **HEADERS** (IP, puerto, protocolo)
- NO mira **CONTENIDO**

**STATEFUL:**
- **STATE** = Estado → Recuerda conexiones activas

**PROXY:**
- **INTERMEDIARIO** → Cliente nunca se conecta directo al destino

**WAF:**
- **W**eb **A**pplication **F**irewall
- Capa **7** → Protege **aplicaciones web**
- Mitiga **OWASP Top 10** (SQL Injection, XSS)

**NGFW:**
- **N**ext-**G**eneration → Combina TODO
- DPI (Deep Packet Inspection)
- IPS integrado
- Antivirus/Antimalware

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Qué firewall analiza solo headers sin ver el contenido?*
- ✅ Packet Filtering
- ❌ Stateful Inspection
- ❌ WAF

> *¿Qué firewall protege específicamente aplicaciones web?*
- ✅ WAF
- ❌ Packet Filtering
- ❌ Proxy

> *¿Qué firewall opera en Capa 7 (Aplicación)?*
- ✅ Proxy y WAF
- ❌ Packet Filtering
- ❌ Stateful Inspection

> *Un NGFW combina:*
- ✅ Filtrado + IPS + AV + DPI
- ❌ Solo filtrado de paquetes
- ❌ Solo proxy

---

### 🔑 DMZ (DEMILITARIZED ZONE)

**DEFINICIÓN:**
**Subred aislada** ubicada entre la **red interna** (protegida) y una **red externa** no confiable (Internet).

**PROPÓSITO:**
Alojar servicios accesibles desde el exterior (web, correo, DNS) **sin exponer** la red interna.

**CARACTERÍSTICAS:**
- **Aislamiento** → Separada de la red interna
- **Accesibilidad controlada** → Servicios públicos disponibles
- **Reglas estrictas** → Tráfico DMZ ↔ Red interna fuertemente regulado

**CONFIGURACIONES:**
- **Firewall único** → 1 firewall con 3 interfaces (Internet, DMZ, LAN)
- **Doble firewall** → 2 firewalls (más seguro)

**💡 ASOCIACIÓN:**
DMZ = **ZONA DE NADIE** entre Internet y red interna

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué es una DMZ?*
- ✅ Subred aislada entre red interna e Internet
- ❌ Una VPN
- ❌ Un tipo de firewall

---

### 🔑 VLANs (VIRTUAL LOCAL AREA NETWORKS)

**DEFINICIÓN:**
Permiten **dividir una red física** en **múltiples redes lógicas independientes**.

**¿PARA QUÉ SIRVEN?**
1. **Seguridad** → Separar dispositivos por función
2. **Eficiencia** → Reducir tráfico broadcast
3. **Control** → Políticas distintas por VLAN
4. **Cumplimiento** → Aislar áreas sensibles

**¿CÓMO FUNCIONAN?**
- Cada paquete se etiqueta con **VLAN ID** (IEEE 802.1Q)
- Los switches gestionan etiquetas
- Cada VLAN = dominio de broadcast propio

**EJEMPLOS:**
- VLAN 100 → Management
- VLAN 200 → Servers
- VLAN 300 → LAN Users

**💡 ASOCIACIÓN:**
VLAN = **Segmentación lógica** de la red

---

### 🔑 IDS vs IPS (¡SUPER IMPORTANTE!)

**DIFERENCIA CLAVE:**

| Aspecto | IDS (Detection) | IPS (Prevention) |
|---------|-----------------|------------------|
| **Nombre completo** | Intrusion Detection System | Intrusion Prevention System |
| **Acción** | Solo DETECTA y ALERTA | Detecta Y BLOQUEA automáticamente |
| **Despliegue** | Modo PASIVO | En línea, INTERCEPTA tráfico |
| **Riesgo** | Bajo | Cuidado con falsos positivos |

**TÉCNICAS DE DETECCIÓN:**

**1. Basado en FIRMAS:**
- Detecta patrones **CONOCIDOS**
- Bajo falsos positivos
- ❌ NO detecta ataques desconocidos

**2. Basado en ANOMALÍAS (behavioral, AI):**
- Detecta **DESVIACIONES** del comportamiento normal
- ✅ Puede detectar amenazas nuevas o zero-day
- ⚠️ Mayor riesgo de falsos positivos

**TIPOS DE IMPLEMENTACIÓN:**
- **NIDS/NIPS** → Network-based (monitorean red)
- **HIDS/HIPS** → Host-based (monitorean sistema operativo)

**EJEMPLOS:**
- **Snort** → Open source, basado en firmas
- **Suricata** → Open source, más moderno
- **OSSEC** → HIDS basado en logs

**💡 REGLAS MNEMOTÉCNICAS:**
- **IDS** = **D**etecta = **Solo alerta**
- **IPS** = **P**reviene = **Bloquea**

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Cuál es la diferencia entre IDS e IPS?*
- ✅ IDS solo detecta, IPS detecta y bloquea
- ❌ IDS es más moderno
- ❌ No hay diferencia

> *¿Qué técnica detecta amenazas desconocidas o zero-day?*
- ✅ Basado en anomalías
- ❌ Basado en firmas
- ❌ Ninguna

> *Snort es un ejemplo de:*
- ✅ IDS/IPS open source
- ❌ Firewall
- ❌ EDR

---

### 🔑 NAC (NETWORK ACCESS CONTROL)

**DEFINICIÓN:**
Solución que controla **quién y qué puede conectarse** a una red.

**EVALÚA:**
- **Identidad** del usuario
- **Tipo de dispositivo**
- **Estado de seguridad** (antivirus, parches, firewall)

**FUNCIONAMIENTO:**
1. **Conexión inicial** → Dispositivo intenta conectarse
2. **Autenticación** → Valida identidad (802.1X, certificados, AD)
3. **Evaluación de postura** → ¿Antivirus actualizado? ¿Parcheado?
4. **Decisión** → Permite/Deniega o redirige a cuarentena

**EJEMPLOS:**
- Cisco ISE
- Fortinet FortiNAC
- Aruba ClearPass

**💡 ASOCIACIÓN:**
NAC = Control de **ACCESO** basado en **POSTURA** de seguridad

---

### 🔑 CASB (CLOUD ACCESS SECURITY BROKER)

**DEFINICIÓN:**
Solución que proporciona **visibilidad y control** sobre datos que fluyen hacia y desde **aplicaciones en la nube**.

**¿POR QUÉ EXISTE?**
- Organizaciones usan apps cloud sin que IT lo sepa (**Shadow IT**)

**QUÉ HACE:**
- Saber **qué cloud apps** se usan y por quién
- Aplicar **políticas de seguridad**
- Detectar **comportamientos anómalos** (UEBA)
- **Prevenir fuga de datos** (DLP)
- **Cumplir regulaciones**

**CASOS DE USO:**
- Detectar uso de apps no autorizadas (Shadow IT)
- Prevenir descarga de archivos sensibles desde M365
- Bloquear acceso desde países no permitidos
- Aplicar DLP sobre Gmail o Dropbox

**EJEMPLOS:**
- Netskope
- Microsoft Defender for Cloud Apps
- McAfee MVISION

**💡 ASOCIACIÓN:**
CASB = **BROKER** entre usuarios y aplicaciones **CLOUD**

---

### 🔑 ANTI-DOS / ANTI-DDOS

**DOS (DENIAL OF SERVICE):**
- Desde una **ÚNICA fuente**
- Satura recursos (ancho de banda, CPU, memoria)

**TIPOS:**
1. **Volumen** → UDP Flood, Ping Flood
2. **Protocolo** → SYN Flood, Ping of Death
3. **Aplicación** → HTTP Flood, Slowloris

**DDOS (DISTRIBUTED DENIAL OF SERVICE):**
- Desde **MÚLTIPLES** dispositivos (botnet)
- Mucho más difícil de detener
- Millones de IPs

**CASO REAL:**
**Ataque Dyn (2016)** → Botnet Mirai, afectó Twitter, Spotify, Netflix, **+1 Tbps** de tráfico

**BOTNET:**
- Red de dispositivos **infectados** (bots/zombies)
- Controlados por **C2** (Command and Control)

**ARQUITECTURAS DE BOTNET:**
- **Centralizada** → Un servidor C2 (fácil de derribar)
- **P2P** → Bots se comunican entre sí (más resiliente)

**PROTECCIÓN:**
- Detectar picos inusuales
- Filtrar tráfico malicioso
- **Scrubbing center** → Centro de limpieza
- **Rate Limiting** → Limitar solicitudes por IP
- **Balanceadores** → Distribuir carga

**EJEMPLOS:**
- Cloudflare
- AWS Shield
- Akamai Kona

**💡 ASOCIACIÓN:**
- DoS = **UNO** ataca
- **D**DoS = **D**istribuido = **MUCHOS** atacan
- Botnet = Red de **ZOMBIES**

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Cuál es la diferencia entre DoS y DDoS?*
- ✅ DoS desde una fuente, DDoS desde múltiples
- ❌ DoS es más peligroso
- ❌ No hay diferencia

> *¿Qué es una botnet?*
- ✅ Red de dispositivos infectados controlados remotamente
- ❌ Un tipo de firewall
- ❌ Un protocolo de red

> *La botnet Mirai atacó a:*
- ✅ Dyn (2016), afectó Twitter, Spotify, Netflix
- ❌ Capital One
- ❌ Equifax

---

## 📚 PARTE 3: SEGURIDAD EN ENDPOINTS

### 🔑 ANTIVIRUS vs EDR vs XDR (¡MUY IMPORTANTE!)

**TABLA COMPARATIVA:**

| Aspecto | Antivirus | EDR | XDR |
|---------|-----------|-----|-----|
| **Detección** | Amenazas CONOCIDAS | Conocidas + COMPORTAMIENTO | Múltiples fuentes correlacionadas |
| **Método** | FIRMAS estáticas | Firmas + Heurística + ML | Correlación entre endpoint, red, cloud |
| **Visibilidad** | Baja | Alta (contexto endpoint) | Extremo a extremo |
| **Respuesta** | Sin automatización | Automática (aislar, eliminar) | Unificada desde consola central |
| **Alcance** | Solo endpoint | Solo endpoint | Endpoint + Red + Cloud + Email |
| **Zero-Day** | ❌ NO detecta | ✅ Puede detectar | ✅ Puede detectar |

**ANTIVIRUS:**
- **Escaneo de archivos** → Busca malware conocido
- **Firmas estáticas** → Base de datos de patrones
- Requiere **actualizaciones frecuentes**
- ❌ NO detecta zero-day
- Ejemplos: Windows Defender, Norton, Kaspersky

**EDR (ENDPOINT DETECTION AND RESPONSE):**
- **Monitoreo continuo** del endpoint
- **Detección avanzada** → Firmas + heurística + ML
- **Alertas detalladas** con contexto
- **Respuesta automática** → Aislar, eliminar, detener procesos
- **Telemetría y forense**
- Ejemplos: CrowdStrike Falcon, Microsoft Defender for Endpoint

**XDR (EXTENDED DETECTION AND RESPONSE):**
- **Más allá del endpoint** → Red + Cloud + Email + Identidad
- **Correlación automática** de eventos
- **Contexto completo** del ataque
- **Respuesta unificada** desde una consola
- Ejemplos: Palo Alto Cortex XDR, Microsoft 365 Defender

**💡 REGLAS MNEMOTÉCNICAS:**
- Antivirus = **FIRMAS** (solo conocidos)
- **E**DR = **E**ndpoint (solo endpoint)
- **X**DR = e**X**tendido (múltiples fuentes)

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Qué solución detecta amenazas solo conocidas?*
- ✅ Antivirus
- ❌ EDR
- ❌ XDR

> *¿Qué solución monitorea múltiples capas (endpoint, red, cloud)?*
- ✅ XDR
- ❌ EDR
- ❌ Antivirus

> *EDR permite:*
- ✅ Respuesta automática y telemetría
- ❌ Solo detección de malware conocido
- ❌ Solo monitoreo de red

> *¿Qué solución correlaciona eventos entre distintos sistemas?*
- ✅ XDR
- ❌ EDR
- ❌ Antivirus

---

## 📚 PARTE 4: SEGURIDAD EN DATOS (DATA SECURITY)

### 🔑 DLP (DATA LOSS PREVENTION)

**DEFINICIÓN:**
Solución para **detectar, monitorear y prevenir** la exposición no autorizada de información sensible.

**PROTEGE:**
- Datos **en reposo** (almacenados)
- Datos **en tránsito** (comunicación)
- Datos **en uso** (procesamiento)

**DETECCIÓN:**
Reglas basadas en **expresiones regulares**

**EJEMPLOS:**
- Netskope
- Microsoft Purview
- Symantec DLP
- Trellix DLP

**💡 ASOCIACIÓN:**
DLP = Previene **FUGA** de datos

---

### 🔑 FULL DISK ENCRYPTION

**DEFINICIÓN:**
Técnica que usa **criptografía simétrica** para cifrar **todos los datos** en un disco.

**PROTEGE:**
Datos **en reposo** (data at rest)

**CUÁNDO PROTEGE:**
Solo cuando el sistema está **APAGADO**

**EVITA:**
- Robo de laptop
- Extracción física del disco

**TRANSPARENTE:**
Usuario no nota el cifrado/descifrado

**EJEMPLOS:**
- **Windows**: BitLocker
- **Linux**: LUKS
- **Multiplataforma**: VeraCrypt

**💡 ASOCIACIÓN:**
Full Disk Encryption = Protege disco cuando está **APAGADO**

---

### 🔑 BACKUPS

**DEFINICIÓN:**
**Copia de datos originales** para recuperarlos en caso de pérdida.

**TIPOS:**
1. **Completo** → Copia TODO (lento, fácil de restaurar)
2. **Incremental** → Solo lo que cambió desde último backup
3. **Diferencial** → Cambios desde último backup completo

**REGLA 3-2-1:**
- **3** copias de los datos
- En **2** tipos de medios diferentes
- **1** copia fuera del sitio (off-site o cloud)

**DÓNDE GUARDAR:**
- Discos externos / NAS
- Cloud (OneDrive, Google Drive, Azure, AWS)
- Dispositivos separados de la red

**BUENAS PRÁCTICAS:**
- Planificar frecuencia según criticidad
- **Pruebas periódicas** de restauración
- **Cifrar** backups si contienen info sensible
- **Automatizar** y monitorear

**💡 ASOCIACIÓN:**
Backups = **DISPONIBILIDAD** (uno de los pilares CIA)

**❓ PREGUNTA TIPO EXAMEN:**
> *La regla 3-2-1 de backups significa:*
- ✅ 3 copias, 2 medios, 1 off-site
- ❌ 3 servidores, 2 redes, 1 firewall
- ❌ 3 usuarios, 2 contraseñas, 1 admin

---

## 📚 PARTE 5: SEGURIDAD EN LA NUBE (CLOUD SECURITY)

### 🔑 RIESGOS COMUNES EN LA NUBE

**LISTA DE RIESGOS:**
1. **Misconfigurations** → Configuraciones incorrectas
   - Ejemplo: Buckets S3 públicos (accesibles sin autenticación)

2. **IAM Weaknesses** → Gestión deficiente de identidades
   - Cuentas admin sin MFA
   - API Keys compartidas

3. **Exposición de credenciales** → Claves en código
   - Claves AWS hardcodeadas en Git público

4. **Data Leakage** → Fuga de datos
   - Archivos con links públicos en OneDrive/Google Drive

5. **Desconocimiento del Shared Responsibility Model**

---

### 🔑 SHARED RESPONSIBILITY MODEL

**DEFINICIÓN:**
Define **qué es responsabilidad del Cloud Provider** y **qué es responsabilidad del Cliente**.

**DEPENDE DEL TIPO DE SERVICIO:**
- **IaaS** (Infrastructure as a Service) → Cliente gestiona más
- **PaaS** (Platform as a Service) → Responsabilidad compartida
- **SaaS** (Software as a Service) → Provider gestiona más

**GENERAL:**
- **Provider** → Seguridad **DE** la nube (hardware, red física, datacenters)
- **Cliente** → Seguridad **EN** la nube (datos, apps, configuraciones, IAM)

**💡 ASOCIACIÓN:**
Shared Responsibility = **Provider** cuida la infraestructura, **Cliente** cuida lo que pone encima

---

### 🔑 CSPM (CLOUD SECURITY POSTURE MANAGEMENT)

**DEFINICIÓN:**
Tecnología para **detectar configuraciones incorrectas** y vulnerabilidades en entornos cloud.

**QUÉ HACE:**
- **Visibilidad centralizada** de configuraciones
- **Evaluación continua** de riesgos
- **Recomendaciones** de remediación
- **Integración** con frameworks (CIS, NIST, ISO 27001)

**💡 FRASE:**
> "La seguridad en la nube no es solo responsabilidad del proveedor, sino también de cómo **configuramos y monitoreamos**"

---

### 🔑 CASO REAL: CAPITAL ONE (2019)

**QUÉ PASÓ:**
- **Fuga de +100 millones** de clientes
- Atacante explotó **mala configuración** en WAF en AWS
- Usó **SSRF** (Server-Side Request Forgery)
- Obtuvo credenciales de **rol IAM**
- Listó y copió **buckets S3**

**CONSECUENCIAS:**
- Multa: **80 millones** de dólares
- Acuerdo: **190 millones** adicionales
- Daño reputacional grave
- Atacante arrestada y condenada

**💡 LECCIÓN:**
**Misconfigurations** en cloud pueden ser devastadoras

**❓ PREGUNTA TIPO EXAMEN:**
> *El ataque a Capital One (2019) fue causado por:*
- ✅ Mala configuración en WAF (SSRF)
- ❌ Phishing
- ❌ Ransomware

---

## 📚 PARTE 6: CRIPTOGRAFÍA APLICADA

### 🔑 ¿QUÉ ES LA CRIPTOGRAFÍA?

**DEFINICIÓN:**
Disciplina que estudia técnicas para **proteger información** frente a accesos no autorizados.

**EN SIMPLE:**
Arte de **transformar información** para que solo quien tenga la **clave correcta** pueda leerla.

**4 PILARES:**
1. **Confidencialidad** → Solo autorizados leen
2. **Integridad** → Información no alterada
3. **Autenticación** → Verificar identidad
4. **No repudio** → No negar acción realizada

---

### 🔑 ELEMENTOS DE UN CRIPTOSISTEMA

**COMPONENTES:**
1. **Texto plano** → Información original
2. **Cifrado (Encryption)** → Transforma a ilegible
3. **Texto cifrado (Criptograma)** → Resultado del cifrado
4. **Descifrado (Decryption)** → Recupera texto plano
5. **Algoritmo de cifrado/descifrado** → Pasos matemáticos
6. **Clave** → Puede ser la misma (simétrica) o distinta (asimétrica)
7. **Adversario** → Atacante que intercepta

**💡 REGLA:**
El atacante puede conocer el **ALGORITMO**, pero NUNCA debe conocer la **CLAVE**

---

### 🔑 CRIPTOGRAFÍA SIMÉTRICA vs ASIMÉTRICA

**TABLA COMPARATIVA:**

| Aspecto | Simétrica | Asimétrica |
|---------|-----------|------------|
| **Claves** | **UNA clave** (misma para cifrar y descifrar) | **DOS claves** (pública y privada) |
| **Velocidad** | ✅ RÁPIDA | ❌ LENTA |
| **Uso principal** | Cifrar GRANDES cantidades de datos | Intercambio de claves, firmas digitales |
| **Problema** | Distribución de clave secreta | - |
| **Ejemplos** | AES, DES, 3DES, ChaCha20 | RSA, ECC, Diffie-Hellman |

**CRIPTOGRAFÍA SIMÉTRICA:**
- **Misma clave** para cifrar y descifrar
- Emisor y receptor deben conocer la clave
- **Problema**: ¿Cómo compartir la clave de forma segura?

**TIPOS:**
- **Stream Ciphers** → Bit a bit o byte a byte
- **Block Ciphers** → Bloques fijos de bits

**STREAM CIPHERS:**
- **RC4** → Obsoleto (roto desde 2015)
- **E0** → Bluetooth
- **ChaCha20** → Más robusto, recomendado (SSL/TLS, OpenSSH)

**💡 REGLAS MNEMOTÉCNICAS:**
- **Simétrica** = **UNA** clave = **RÁPIDA** = Cifrar DATOS
- **Asimétrica** = **DOS** claves = **LENTA** = Intercambio de claves

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Cuántas claves usa la criptografía simétrica?*
- ✅ Una (la misma para cifrar y descifrar)
- ❌ Dos (pública y privada)
- ❌ Tres

> *¿Qué tipo de criptografía es más rápida?*
- ✅ Simétrica
- ❌ Asimétrica
- ❌ Ambas igual

> *ChaCha20 es un ejemplo de:*
- ✅ Stream Cipher (criptografía simétrica)
- ❌ Block Cipher
- ❌ Criptografía asimétrica

> *¿Cuál está obsoleto?*
- ✅ RC4
- ❌ ChaCha20
- ❌ AES

---

## 🎯 RESUMEN ULTRA-RÁPIDO (Para 10 min antes del examen)

### 📌 CONCEPTOS FUNDAMENTALES:
- **Defense in Depth** = Múltiples capas de seguridad
- **Zero Trust** = Nunca confiar, siempre verificar

### 📌 PROTOCOLOS:
- **TLS** = Sucesor de SSL (puerto 443 para HTTPS)
- **SSL** = Obsoleto

### 📌 FIREWALLS (TABLA):
- **Packet Filtering** = Solo headers, Capa 3-4
- **Stateful** = Headers + Estado
- **Proxy** = Intermediario, Capa 7
- **WAF** = Apps web, OWASP Top 10, Capa 7
- **NGFW** = Combina todo (DPI, IPS, AV)

### 📌 IDS vs IPS:
- **IDS** = Solo **D**etecta
- **IPS** = **P**reviene (bloquea)

### 📌 CONCEPTOS DE RED:
- **DMZ** = Zona entre Internet y red interna
- **VLAN** = Segmentación lógica
- **NAC** = Control de acceso por postura
- **CASB** = Broker para apps cloud

### 📌 DoS vs DDoS:
- **DoS** = Una fuente
- **DDoS** = Múltiples (botnet)
- **Botnet** = Red de zombies + C2

### 📌 ENDPOINT:
- **Antivirus** = Solo firmas (conocidos)
- **EDR** = Endpoint + comportamiento + respuesta
- **XDR** = Múltiples fuentes + correlación

### 📌 DATOS:
- **DLP** = Previene fuga de datos
- **Full Disk Encryption** = Protege en reposo (apagado)
- **Backups** = Regla 3-2-1

### 📌 CLOUD:
- **Shared Responsibility** = Provider cuida infra, Cliente cuida config
- **CSPM** = Detecta misconfigurations
- **Capital One** = Mala config WAF + SSRF + S3

### 📌 CRIPTOGRAFÍA:
- **Simétrica** = 1 clave, rápida, cifrar datos
- **Asimétrica** = 2 claves, lenta, intercambio
- **Stream Cipher** = Bit a bit (ChaCha20 ✅, RC4 ❌)
- **Block Cipher** = Bloques

### 📌 CASOS REALES:
- **Dyn (2016)** = Botnet Mirai, +1 Tbps
- **Capital One (2019)** = 100M clientes, mala config

---

## 🔥 ESTRATEGIA PARA EL EXAMEN

### ✅ Palabras clave en preguntas:

**Si ves:** "nunca confiar" → **Zero Trust**
**Si ves:** "múltiples capas" → **Defense in Depth**
**Si ves:** "puerto 443" → **HTTPS (TLS)**
**Si ves:** "solo headers" → **Packet Filtering**
**Si ves:** "aplicaciones web" / "OWASP Top 10" → **WAF**
**Si ves:** "solo detecta" → **IDS**
**Si ves:** "detecta y bloquea" → **IPS**
**Si ves:** "zona entre Internet y LAN" → **DMZ**
**Si ves:** "apps cloud" / "Shadow IT" → **CASB**
**Si ves:** "una fuente" → **DoS**
**Si ves:** "múltiples fuentes" / "botnet" → **DDoS**
**Si ves:** "solo firmas" → **Antivirus**
**Si ves:** "comportamiento" / "respuesta automática" → **EDR**
**Si ves:** "múltiples fuentes" / "correlación" → **XDR**
**Si ves:** "3-2-1" → **Regla de Backups**
**Si ves:** "mala configuración" / "S3 público" → **Misconfiguration cloud**
**Si ves:** "Capital One" → **Mala config WAF + SSRF**
**Si ves:** "una clave" / "rápida" → **Criptografía Simétrica**
**Si ves:** "dos claves" / "lenta" → **Criptografía Asimétrica**

---

## 💪 ¡Éxito en tu examen!

**Recuerda:** Esta unidad cubre **4 áreas grandes**:
1. **Seguridad en Redes** (Firewalls, IDS/IPS, DMZ, etc.)
2. **Seguridad en Endpoints** (Antivirus, EDR, XDR)
3. **Seguridad en Datos** (DLP, Encryption, Backups)
4. **Seguridad en Cloud** + **Criptografía**

**Lo más importante:**
- **Tabla de Firewalls** (tipos y diferencias)
- **IDS vs IPS**
- **EDR vs XDR**
- **Simétrica vs Asimétrica**
- **Zero Trust** y **Defense in Depth**
- **Caso Capital One**

**Practica las preguntas tipo examen y estarás listo.** 🚀

