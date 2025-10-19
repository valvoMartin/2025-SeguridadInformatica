# 🎯 GUÍA DE ESTUDIO - UNIDAD 2: Seguridad Informática en la Empresa
## Método para Examen Multiple Choice

---

## 📚 PARTE 1: ¿CÓMO EMPEZAR? - LOS 4 PASOS FUNDAMENTALES

### 🔑 ESTRUCTURA GENERAL (MEMORIZA ESTE ORDEN)

**Los 4 Pasos para Implementar Seguridad en la Empresa:**

1. **PASO 1: Evaluación Inicial** → Auditoría + Análisis de Riesgos
2. **PASO 2: Estrategia** → Política de Seguridad + Normativas
3. **PASO 3: Implementación** → Controles + Herramientas + Procedimientos
4. **PASO 4: Concientización** → Capacitación del personal

**💡 REGLA MNEMOTÉCNICA (AEIC):**
- **A**uditoría y Evaluación
- **E**strategia y Políticas
- **I**mplementación de Controles
- **C**oncientización

---

## 📚 PARTE 2: PASO 1 - EVALUACIÓN INICIAL

### 🔑 A. AUDITORÍA DE SEGURIDAD

**DEFINICIÓN CLAVE:**
Proceso **objetivo y sistemático** que evalúa la efectividad de los controles de seguridad.

**COMPONENTES PRINCIPALES:**

| Componente | Palabra Clave | Qué se hace |
|------------|---------------|-------------|
| **Inventario de Activos** | CMDB, listado completo | Identificar TODO el hardware, software, datos |
| **Activos Críticos** | IMPACTO en operaciones | Recursos cuya pérdida afecta significativamente |
| **Mapeo de Flujos (DFD)** | MOVIMIENTO de información | Cómo fluyen los datos entre sistemas |

**💡 ASOCIACIÓN:**
- **Auditoría** = Fotografía completa del estado actual
- **Inventario** = ¿Qué tenemos?
- **Activos Críticos** = ¿Qué es MÁS importante?
- **DFD** = ¿Cómo SE MUEVE la información?

---

### 🔑 INVENTARIO DE ACTIVOS

**PALABRAS CLAVE:**
- **CMDB** (Configuration Management Database)
- Ejemplos de herramientas: **SolarWinds**, **Lansweeper**

**BENEFICIOS DEL INVENTARIO:**
1. Visión **CLARA** de todos los activos
2. **PRIORIZAR** recursos y medidas de seguridad
3. Gestión de **LICENCIAS** y actualizaciones
4. **CUMPLIMIENTO** normativo
5. Respuesta rápida a **INCIDENTES**

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué es una CMDB?*
- ✅ Configuration Management Database - base de datos de gestión de configuración
- ❌ Control Management Data Backup
- ❌ Cyber Management Database

> *¿Cuál es un beneficio del inventario de activos?*
- ✅ Facilita la respuesta rápida a incidentes
- ❌ Elimina todos los riesgos
- ❌ Reemplaza la necesidad de auditorías

---

### 🔑 CLASIFICACIÓN DE ACTIVOS

**PROCESO:**
1. **Inventario** → Listar todos los activos
2. **Clasificación** → Categorizar según importancia
3. **Valoración** → Evaluar impacto de pérdida/compromiso

**MÉTODOS DE VALORACIÓN:**
- **Cualitativo**: Juicios expertos, categorías (Alto/Medio/Bajo)
- **Cuantitativo**: Métricas financieras, valores numéricos

---

### 🔑 MAPEO DE FLUJOS DE DATOS (DFD)

**PALABRAS CLAVE:**
- **Puntos de entrada**: Correos, formularios web
- **Tránsito**: Servidores, bases de datos
- **Salida**: Informes, exportaciones, reportes

**OBJETIVO:**
Identificar **puntos críticos y vulnerables** donde fluye la información.

**VERIFICAR EN CADA PUNTO:**
- ¿Hay **cifrado**?
- ¿Hay **autenticación**?
- ¿Hay **escaneo de código**?
- ¿Se aplica **mínimos privilegios**?

**❓ PREGUNTA TIPO EXAMEN:**
> *El mapeo de flujos de datos (DFD) ayuda a:*
- ✅ Identificar puntos críticos y vulnerables
- ❌ Eliminar la necesidad de cifrado
- ❌ Reemplazar el inventario de activos

---

### 🔑 B. ANÁLISIS DE RIESGOS

**COMPONENTES DEL ANÁLISIS:**

| Paso | Palabra Clave | Qué se identifica |
|------|---------------|-------------------|
| **Identificar Amenazas** | EXTERNAS | Malware, ciberataques, desastres naturales |
| **Identificar Vulnerabilidades** | INTERNAS/DEBILIDADES | Software sin parches, contraseñas débiles, configuraciones incorrectas |
| **Evaluar Impacto** | CONSECUENCIAS | Pérdidas financieras, daño reputacional, interrupciones |
| **Evaluar Probabilidad** | FRECUENCIA | Qué tan probable es que ocurra |

**💡 DIFERENCIA CLAVE:**
- **Amenaza** = Lo que PUEDE atacarnos (externo)
- **Vulnerabilidad** = Nuestra DEBILIDAD (interno)
- **Riesgo** = Amenaza + Vulnerabilidad + Impacto + Probabilidad

---

### 🔑 EJEMPLOS DE AMENAZAS vs VULNERABILIDADES

**AMENAZAS POTENCIALES:**
- Malware
- Ciberataque
- Errores humanos
- Desastres naturales
- Fallos de hardware
- Fugas de datos

**VULNERABILIDADES EXISTENTES:**
- Debilidades en software
- Configuraciones incorrectas
- Falta de parches
- Contraseñas débiles
- Falta de formación
- Procedimientos inadecuados

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Cuál es una vulnerabilidad?*
- ✅ Contraseñas débiles
- ❌ Malware
- ❌ Ciberataque

> *¿Cuál es una amenaza?*
- ✅ Desastre natural
- ❌ Falta de parches
- ❌ Configuración incorrecta

---

### 🔑 EVALUACIÓN DE IMPACTO Y PROBABILIDAD

**TIPOS DE IMPACTO:**
1. **Económico** → Pérdidas FINANCIERAS
2. **Legal** → Incumplimiento NORMATIVAS
3. **Reputacional** → Pérdida de CONFIANZA
4. **Operativo** → Interrupción de PROCESOS
5. **Humano** → Seguridad FÍSICA de personas
6. **Político/Geopolítico** → Relaciones INTERNACIONALES

**FACTORES DE PROBABILIDAD:**
- Frecuencia **HISTÓRICA**
- Nivel de **EXPOSICIÓN**
- Efectividad de **CONTROLES** existentes
- **CONTEXTO** operativo

**💡 MATRIZ DE RIESGOS:**
```
PROBABILIDAD ↑
        │  MEDIO  │  ALTO  │
        │  BAJO   │ MEDIO  │
        └─────────────────→ IMPACTO
```

---

### 🔑 GESTIÓN DE RIESGOS (4 OPCIONES)

**TABLA COMPARATIVA - ¡MUY IMPORTANTE!**

| Estrategia | Palabra Clave | Acción | Ejemplo |
|------------|---------------|--------|---------|
| **ACEPTAR** | COSTO vs BENEFICIO | Documentar y **NO mitigar** | Riesgo bajo, mitigación muy cara |
| **EVITAR** | ELIMINAR la actividad | **CANCELAR** proyecto/proceso | Cancelar proyecto con riesgo inaceptable |
| **MITIGAR** | REDUCIR el riesgo | Implementar **CONTROLES** | Firewalls, MFA, parches, capacitación |
| **TRANSFERIR** | DELEGAR el riesgo | **SEGURO** o contrato | Seguro de ciberseguridad |

**💡 REGLA MNEMOTÉCNICA (AEMT):**
- **A**ceptar → Asumir
- **E**vitar → Eliminar
- **M**itigar → Minimizar
- **T**ransferir → Tercerizar

**❓ PREGUNTAS TIPO EXAMEN:**

> *Contratar un seguro de ciberseguridad es una estrategia de:*
- ✅ Transferir el riesgo
- ❌ Mitigar el riesgo
- ❌ Evitar el riesgo

> *Implementar MFA es una estrategia de:*
- ✅ Mitigar el riesgo
- ❌ Transferir el riesgo
- ❌ Aceptar el riesgo

> *Cancelar un proyecto que presenta riesgos inaceptables es:*
- ✅ Evitar el riesgo
- ❌ Aceptar el riesgo
- ❌ Mitigar el riesgo

> *Documentar un riesgo sin tomar acción porque el costo de mitigarlo es muy alto es:*
- ✅ Aceptar el riesgo
- ❌ Evitar el riesgo
- ❌ Transferir el riesgo

---

## 📚 PARTE 3: PASO 2 - POLÍTICA DE SEGURIDAD INFORMÁTICA

### 🔑 ¿QUÉ ES UNA POLÍTICA DE SEGURIDAD?

**DEFINICIÓN CLAVE:**
Documento que establece **reglas claras** sobre uso de recursos de TI, contraseñas, acceso a datos y dispositivos.

**ELEMENTOS FUNDAMENTALES:**
1. **Compromiso de Alta Dirección** ← ¡LA CLAVE!
2. **Equipo Multidisciplinario** (TI, Legal, RRHH, Procesos)
3. **Alcance y Objetivos** definidos
4. **Análisis de Riesgos**
5. **Políticas Específicas**

**💡 ASOCIACIÓN:**
Sin apoyo de **ALTA DIRECCIÓN** → La política fracasa

---

### 🔑 ISO 27001

**PALABRAS CLAVE:**
- Estándar **INTERNACIONAL**
- Marco para **SGSI** (Sistema de Gestión de Seguridad de la Información)
- Ciclo **PDCA** (Plan-Do-Check-Act)
- **Anexo A**: Controles de seguridad

**CICLO PDCA:**
1. **Plan** → Planificar
2. **Do** → Hacer/Implementar
3. **Check** → Verificar/Auditar
4. **Act** → Actuar/Mejorar

**💡 ASOCIACIÓN:**
ISO 27001 = Marco de **MEJORA CONTINUA**

**CONTROLES ISO 27001 - NUEVOS EN 2022:**
- Inteligencia de amenazas (5.7)
- Preparación TIC para continuidad (5.30)
- Supervisión física (7.4)
- Gestión de configuración (8.9)
- Eliminación de información (8.10)
- Enmascaramiento de datos (8.11)
- Prevención de fuga de datos (8.12)
- Actividades de monitoreo (8.16)
- Filtrado web (8.23)
- Codificación segura (8.28)

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué significa PDCA?*
- ✅ Plan-Do-Check-Act
- ❌ Protect-Detect-Correct-Analyze
- ❌ Prepare-Deploy-Control-Audit

> *ISO 27001 proporciona un marco para:*
- ✅ Sistema de Gestión de Seguridad de la Información (SGSI)
- ❌ Solo protección de tarjetas de crédito
- ❌ Solo gestión de personal

---

### 🔑 EJEMPLOS DE POLÍTICAS ESPECÍFICAS

**LISTA DE POLÍTICAS COMUNES:**
1. **Política de Contraseñas** → Complejidad, cambios, bloqueos
2. **Política de Acceso a Datos** → RBAC (Control basado en roles)
3. **Política de Uso de Recursos TI** → Uso aceptable de equipos
4. **Política de Dispositivos Móviles** → MDM, cifrado
5. **Política de Trabajo Remoto** → VPN, seguridad del entorno
6. **Política de Clasificación de Datos** → Público, Confidencial, Secreto
7. **Política de Gestión de Vulnerabilidades** → Parches, actualizaciones

---

## 📚 PARTE 4: NORMATIVAS LEGALES Y ESTÁNDARES

### 🔑 TABLA COMPARATIVA DE NORMATIVAS (¡MEMORÍZALA!)

| Normativa | Ubicación | Qué Protege | Palabra Clave Principal |
|-----------|-----------|-------------|-------------------------|
| **GDPR** | Unión Europea | Datos PERSONALES de ciudadanos UE | **DERECHO AL OLVIDO** |
| **HIPAA** | EE.UU. | Información de SALUD (PHI) | **DATOS MÉDICOS** |
| **SOX** | EE.UU. | Registros FINANCIEROS | **EMPRESAS EN BOLSA** |
| **PCI DSS** | Internacional | Datos de TARJETAS de crédito | **PAN (número tarjeta)** |
| **NIST** | EE.UU. | Marco de CIBERSEGURIDAD | **GESTIÓN DE RIESGO** |
| **Ley 26.388** | Argentina | Delitos INFORMÁTICOS | **CÓDIGO PENAL** |

**💡 REGLAS MNEMOTÉCNICAS:**

**GDPR:**
- **G**eneral → Protección de **D**atos **P**ersonales en **R**egión europea
- Derecho al **OLVIDO** (supresión de datos)

**HIPAA:**
- **H**ealth → **H**ospitales y **Salud**
- Protege **PHI** (Protected Health Information)

**SOX:**
- **S**arbanes-**O**xley → Empre**S**as en B**O**lsa, Finanza**S**
- Informes **FINANCIEROS**

**PCI DSS:**
- **P**ayment **C**ard **I**ndustry
- Protege el **PAN** (Primary Account Number = número de tarjeta)

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Qué normativa protege datos personales en la UE?*
- ✅ GDPR
- ❌ HIPAA
- ❌ PCI DSS

> *¿Qué normativa regula la información de salud en EE.UU.?*
- ✅ HIPAA
- ❌ GDPR
- ❌ SOX

> *¿Qué estándar protege datos de tarjetas de crédito?*
- ✅ PCI DSS
- ❌ SOX
- ❌ HIPAA

> *La Ley Sarbanes-Oxley (SOX) se aplica a:*
- ✅ Empresas cotizadas en bolsa
- ❌ Solo hospitales
- ❌ Solo bancos

> *La Ley 26.388 en Argentina regula:*
- ✅ Delitos informáticos
- ❌ Solo protección de datos personales
- ❌ Solo tarjetas de crédito

---

### 🔑 GDPR - PRINCIPIOS CLAVE

**PALABRAS CLAVE:**
- **Transparencia** en tratamiento
- **Minimización** de datos
- **Derecho al olvido** (supresión)
- **Portabilidad** de datos
- **Consentimiento explícito**
- **Notificación** de violaciones

**💡 DERECHOS DEL USUARIO:**
- **A**cceso
- **R**ectificación
- **S**upresión (olvido)
- **P**ortabilidad
- **L**imitación del tratamiento
- **O**posición

---

### 🔑 HIPAA - PHI (Protected Health Information)

**EJEMPLOS DE PHI:**
- Historial médico
- Resultados de laboratorio
- Radiografías e imágenes
- Diagnósticos
- Tratamientos
- Medicamentos prescritos
- Registros de hospitalización

**PRINCIPIOS:**
- **Integridad**: PHI no alterada
- **Disponibilidad**: Accesible cuando se necesita
- **Salvaguardias**: Administrativas, físicas y técnicas

---

### 🔑 PCI DSS - DATOS PROTEGIDOS

**INFORMACIÓN DE TARJETA:**
- **PAN** (Primary Account Number) → Número de 16 dígitos
- Nombre del titular
- Fecha de vencimiento
- Código de seguridad (CVV2/CVC2/CID)

**DATOS SENSIBLES DE AUTENTICACIÓN:**
- Banda magnética / Chip
- PIN / PIN Block
- Códigos de verificación

**REGLAS CRÍTICAS:**
- **PAN** solo almacenado si está **CIFRADO**
- **CVV/CVC NO se almacena** después de autorización
- **Banda magnética NO se almacena** después de autorización
- **Segmentación de red** (CDE - Cardholder Data Environment)

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué es el PAN en PCI DSS?*
- ✅ Primary Account Number (número de tarjeta)
- ❌ Personal Account Name
- ❌ Payment Authorization Number

> *¿Se puede almacenar el CVV después de la autorización?*
- ✅ No, está prohibido
- ❌ Sí, si está cifrado
- ❌ Sí, siempre

> *El CDE en PCI DSS es:*
- ✅ Cardholder Data Environment (entorno de datos del titular)
- ❌ Credit Data Encryption
- ❌ Card Detection Environment

---

### 🔑 LEY 26.388 (ARGENTINA)

**DELITOS TIPIFICADOS:**
1. **Acceso indebido** (Art. 153 bis) → Sistemas sin autorización
2. **Daño a sistemas** (Art. 183) → Destrucción/alteración de datos
3. **Fraude informático** (Art. 173 inc. 16) → Manipulación para beneficio
4. **Distribución de malware** (Art. 197 bis) → Crear/difundir programas dañinos
5. **Pornografía infantil** → Producción, difusión, tenencia

**💡 ASOCIACIÓN:**
Ley 26.388 = Modificación del **CÓDIGO PENAL** argentino (2008)

---

## 📚 PARTE 5: PASO 3 - IMPLEMENTACIÓN

### 🔑 ESTRUCTURA Y ORGANIGRAMA

**ROLES CLAVE:**

| Rol | Responsabilidad | Palabra Clave |
|-----|-----------------|---------------|
| **CISO** | Chief Information Security Officer | Líder de TODA la seguridad |
| **Comité de Riesgos** | Supervisar y gestionar riesgos | Grupo MULTIDISCIPLINARIO |

**💡 CLAVE:**
- **CISO** debe ser **INDEPENDIENTE** del CIO/CTO (área de Sistemas)
- **Comité de Riesgos**: Finanzas, Sistemas, Auditoría, RRHH, Marketing, Seguridad, etc.

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué significa CISO?*
- ✅ Chief Information Security Officer
- ❌ Chief Internet Security Operations
- ❌ Cybersecurity Information Systems Officer

> *¿Por qué el CISO debe ser independiente del CIO?*
- ✅ Para evitar conflictos de interés
- ❌ Para reducir costos
- ❌ No necesita ser independiente

---

### 🔑 HERRAMIENTAS DE SEGURIDAD (12 PRINCIPALES)

**LISTA PARA MEMORIZAR:**

1. **Firewall** → Filtro de red
2. **IDS/IPS** → Detección/Prevención de Intrusiones
3. **Antivirus/Antimalware** → Protección contra malware
4. **Cifrado** → Protección de datos
5. **SIEM** → Gestión de Información y Eventos de Seguridad
6. **MFA** → Multi-Factor Authentication
7. **Gestor de Parches** → Actualizaciones
8. **IAM** → Gestión de Identidades y Accesos
9. **DLP** → Prevención de Pérdida de Datos
10. **Protección contra Phishing** → Email security
11. **Monitoreo de Redes** → Vigilancia continua
12. **Concientización** → Capacitación de usuarios

**💡 DIFERENCIAS CLAVE:**

**IDS vs IPS:**
- **IDS** (Intrusion Detection System) → Solo **DETECTA** y alerta
- **IPS** (Intrusion Prevention System) → **DETECTA Y BLOQUEA**

**SIEM:**
- **S**ecurity **I**nformation and **E**vent **M**anagement
- Centraliza logs y eventos, correlaciona información

**DLP:**
- **D**ata **L**oss **P**revention
- Previene fuga de datos sensibles

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿Cuál es la diferencia entre IDS e IPS?*
- ✅ IDS solo detecta, IPS detecta y bloquea
- ❌ IDS es más moderno que IPS
- ❌ No hay diferencia

> *¿Qué herramienta centraliza logs y eventos de seguridad?*
- ✅ SIEM
- ❌ DLP
- ❌ MFA

> *¿Qué significa DLP?*
- ✅ Data Loss Prevention
- ❌ Data Link Protocol
- ❌ Digital License Protection

---

## 📚 PARTE 6: GESTIÓN DE IDENTIDADES Y ACCESOS (IAM)

### 🔑 CONCEPTOS FUNDAMENTALES DE IAM

**COMPONENTES PRINCIPALES:**

| Componente | Qué hace | Palabra Clave |
|------------|----------|---------------|
| **Autenticación** | Verificar IDENTIDAD | ¿Quién eres? (login) |
| **Autorización** | Gestionar PERMISOS | ¿Qué puedes hacer? (roles) |
| **Provisión/Deprovisión** | Crear/Eliminar usuarios | Ciclo de vida |
| **RBAC** | Control basado en ROLES | Permisos por puesto |

**💡 DIFERENCIA CRÍTICA:**
- **Autenticación** = Probar quién eres → Usuario + contraseña
- **Autorización** = Qué puedes acceder → Permisos y roles

**❓ PREGUNTA TIPO EXAMEN:**
> *La autenticación se refiere a:*
- ✅ Verificar la identidad del usuario
- ❌ Definir los permisos del usuario
- ❌ Crear una cuenta de usuario

> *La autorización se refiere a:*
- ✅ Gestionar los permisos de acceso
- ❌ Verificar la contraseña
- ❌ Crear copias de seguridad

---

### 🔑 MÉTODOS DE AUTENTICACIÓN

**TABLA COMPARATIVA:**

| Método | Qué es | Ejemplo |
|--------|--------|---------|
| **MFA** | Multi-Factor Authentication | Contraseña + SMS/App |
| **SSO** | Single Sign-On | Un login para múltiples apps |
| **Biometría** | Características físicas | Huella, reconocimiento facial |

**MFA - FACTORES:**
1. **Algo que SABES** → Contraseña, PIN
2. **Algo que TIENES** → Teléfono, token
3. **Algo que ERES** → Huella, iris

**SSO - BENEFICIO:**
- **Una sola sesión** para acceder a múltiples aplicaciones
- Mejora experiencia de usuario
- Reduce fatiga de contraseñas

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué es SSO?*
- ✅ Single Sign-On - una sesión para múltiples aplicaciones
- ❌ Security System Operations
- ❌ Secure Socket Online

> *MFA combina:*
- ✅ Múltiples factores de autenticación
- ❌ Solo contraseñas complejas
- ❌ Solo biometría

---

### 🔑 RBAC (Role-Based Access Control)

**DEFINICIÓN:**
Control de acceso basado en **ROLES** → Los permisos se asignan según el puesto/función.

**EJEMPLO:**
- **Contador** → Acceso a sistema contable
- **Vendedor** → Acceso a CRM
- **Admin** → Acceso a todo

**BENEFICIO:**
- Simplifica gestión de permisos
- Facilita altas/bajas de usuarios
- Cumple con SoD (Segregación de Responsabilidades)

---

### 🔑 SoD (Segregation of Duties)

**DEFINICIÓN CLAVE:**
**Ninguna persona** debe tener control total sobre **todas las fases** de un proceso crítico.

**OBJETIVO:**
Reducir riesgo de **fraude**, **errores** y **actividades maliciosas**.

**EJEMPLOS PRÁCTICOS:**

| Separación | Razón |
|------------|-------|
| Desarrollador ≠ Tester | Quien crea no debe validar |
| Desarrollador ≠ Deploy a producción | Quien programa no debe desplegar |
| Commit ≠ Revisión de código | Quien modifica no debe aprobar solo |
| Desarrollador ≠ Auditor | Quien crea no debe auditar |
| Desarrollador ≠ Gestor de accesos | No debe gestionar sus propios permisos |

**💡 REGLA MNEMOTÉCNICA:**
SoD = **Separar para proteger**

**❓ PREGUNTA TIPO EXAMEN:**
> *La Segregación de Responsabilidades (SoD) busca:*
- ✅ Evitar que una persona controle todo un proceso crítico
- ❌ Reducir la cantidad de empleados
- ❌ Aumentar la velocidad de desarrollo

> *Según SoD, el desarrollador que hace cambios en el código:*
- ✅ No debe ser el único que revisa y aprueba esos cambios
- ❌ Debe aprobar sus propios cambios
- ❌ Debe tener acceso de administrador

---

### 🔑 MODELO ZERO-TRUST

**PRINCIPIO FUNDAMENTAL:**
**"Never trust, always verify"** → Nunca confiar, siempre verificar

**DEFINICIÓN:**
Ninguna entidad (dentro o fuera de la red) es **confiable por defecto**. Todo acceso debe ser **verificado y autenticado**.

**CONCEPTOS CLAVE:**
- No hay "perímetro confiable"
- Verificación continua
- Microsegmentación de red
- Least Privilege

**💡 ASOCIACIÓN:**
Zero-Trust = **Desconfiar de TODO**, incluso dentro de la red

**❓ PREGUNTA TIPO EXAMEN:**
> *El modelo Zero-Trust se basa en:*
- ✅ Nunca confiar, siempre verificar
- ❌ Confiar en usuarios internos automáticamente
- ❌ Solo proteger el perímetro de red

---

### 🔑 LEAST PRIVILEGED ACCESS (Mínimos Privilegios)

**DEFINICIÓN:**
Usuarios deben tener **solo el mínimo acceso necesario** para realizar sus tareas.

**CARACTERÍSTICAS:**
- Permisos mínimos necesarios
- **Accesos temporales** para tareas específicas
- Revocación automática cuando ya no se necesita

**PAM (Privileged Access Management):**
- Gestiona acceso de usuarios **PRIVILEGIADOS**
- Control de cuentas con **altos permisos** (admin, root, etc.)
- Monitoreo de sesiones privilegiadas

**💡 DIFERENCIA:**
- **Least Privilege** = Principio general para TODOS
- **PAM** = Herramienta específica para usuarios PRIVILEGIADOS

**❓ PREGUNTA TIPO EXAMEN:**
> *Least Privileged Access significa:*
- ✅ Otorgar solo los permisos mínimos necesarios
- ❌ Dar acceso completo a todos los usuarios
- ❌ Bloquear todos los accesos

> *PAM se enfoca en:*
- ✅ Gestionar usuarios con altos privilegios
- ❌ Gestionar solo usuarios estándar
- ❌ Solo crear contraseñas

---

### 🔑 BUENAS PRÁCTICAS DE IAM

**LISTA DE VERIFICACIÓN:**

✅ **Revisión periódica** de permisos
✅ **Proceso de baja** al cambiar de sector
✅ **Evitar usuarios compartidos/genéricos**
✅ **Política de contraseñas robustas**
✅ **Reportes de usuarios** (inicios, permisos, cambios)
✅ **Autogestión de credenciales** con validación robusta

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Por qué se deben evitar usuarios compartidos?*
- ✅ No se sabe qué usuario real está detrás
- ❌ Son más seguros que usuarios individuales
- ❌ Son más fáciles de gestionar

---

## 📚 PARTE 7: SEGURIDAD FÍSICA

### 🔑 ¿QUÉ ES SEGURIDAD FÍSICA?

**DEFINICIÓN:**
Protección de **elementos físicos** del sistema contra daños, acceso no autorizado o interferencia.

**INCLUYE:**
1. **Instalaciones y edificios**
2. **Equipos y hardware**
3. **Protección contra desastres naturales**
4. **Protección contra robo y vandalismo**
5. **Supervisión y vigilancia**
6. **Controles de acceso físico**

---

### 🔑 EJEMPLOS DE CONTROLES FÍSICOS

**TABLA DE MEDIDAS:**

| Control | Tecnología/Método | Objetivo |
|---------|-------------------|----------|
| **Control de acceso** | Tarjetas de proximidad, biometría, PIN | Acceso solo a autorizados |
| **Vigilancia CCTV** | Cámaras de seguridad | Monitoreo continuo |
| **Guardias** | Personal de seguridad | Control y patrullaje |
| **Barreras físicas** | Puertas, barras de seguridad | Restringir acceso a áreas sensibles |
| **Cerraduras** | Electrónicas y mecánicas | Proteger oficinas críticas |
| **Protección contra incendios** | Detectores, supresores | Prevenir daños por fuego |
| **Control ambiental** | Temperatura, humedad | Proteger salas de servidores |
| **UPS y generadores** | Respaldo de energía | Continuidad ante fallos eléctricos |
| **Cajas fuertes** | Almacenamiento seguro | Proteger discos y backups |
| **Sensores de intrusión** | Alarmas, movimiento | Detectar accesos no autorizados |
| **Etiquetas antimanipulación** | Sellos de seguridad | Evitar manipulación de equipos |
| **Zonas restringidas** | Niveles de acceso | Áreas solo para personal autorizado |
| **Protección perimetral** | Vallas, detectores | Seguridad alrededor de instalaciones |

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Cuál es un ejemplo de control de seguridad física?*
- ✅ Tarjetas de proximidad para acceso
- ❌ Firewall
- ❌ Antivirus

> *Las UPS y generadores sirven para:*
- ✅ Garantizar continuidad ante fallos eléctricos
- ❌ Proteger contra malware
- ❌ Cifrar datos

> *CCTV es:*
- ✅ Sistema de vigilancia con cámaras
- ❌ Control de acceso biométrico
- ❌ Cifrado de datos

---

## 📚 PARTE 8: PASO 4 - CONCIENTIZACIÓN

### 🔑 PLAN DE CONCIENTIZACIÓN

**OBJETIVO:**
Educar y sensibilizar al personal sobre **buenas prácticas de seguridad**.

**RAZONES:**
1. Crear **cultura de seguridad**
2. Reducir **errores humanos** (phishing, malware)
3. Cumplir con **normativas**

**💡 RECORDATORIO DE KEVIN MITNICK:**
> "Los humanos son el **eslabón más débil** en la seguridad"

**TEMAS DE CAPACITACIÓN:**
- Phishing y ingeniería social
- Contraseñas seguras
- Uso seguro de dispositivos
- Políticas de la empresa
- Respuesta a incidentes

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Por qué es importante la concientización en seguridad?*
- ✅ Los humanos son el eslabón más débil
- ❌ Es un requisito opcional
- ❌ Solo aplica al área de TI

---

## 🎯 RESUMEN ULTRA-RÁPIDO (Para 10 min antes del examen)

### 📌 LOS 4 PASOS:
1. **Evaluación** → Auditoría + Riesgos
2. **Estrategia** → Políticas + Normativas
3. **Implementación** → Controles + Herramientas
4. **Concientización** → Capacitación

### 📌 GESTIÓN DE RIESGOS (AEMT):
- **A**ceptar → Documentar
- **E**vitar → Cancelar
- **M**itigar → Controles
- **T**ransferir → Seguro

### 📌 NORMATIVAS:
- **GDPR** → Datos personales UE
- **HIPAA** → Salud EE.UU.
- **SOX** → Finanzas, empresas en bolsa
- **PCI DSS** → Tarjetas de crédito (PAN, no almacenar CVV)
- **Ley 26.388** → Delitos informáticos Argentina

### 📌 IAM CLAVE:
- **Autenticación** = ¿Quién eres?
- **Autorización** = ¿Qué puedes hacer?
- **RBAC** = Roles
- **SoD** = Separar responsabilidades
- **Zero-Trust** = Nunca confiar
- **Least Privilege** = Mínimos permisos
- **PAM** = Gestión de privilegiados

### 📌 HERRAMIENTAS:
- **IDS** = Detecta
- **IPS** = Detecta + Bloquea
- **SIEM** = Centraliza eventos
- **DLP** = Previene fuga de datos
- **MFA** = Múltiples factores
- **SSO** = Un login para todo

### 📌 ISO 27001:
- **SGSI** = Sistema de Gestión
- **PDCA** = Plan-Do-Check-Act
- Marco de mejora continua

### 📌 ROLES:
- **CISO** = Chief Information Security Officer (independiente de CIO)
- **Comité de Riesgos** = Multidisciplinario

### 📌 SEGURIDAD FÍSICA:
- Controles de acceso
- CCTV
- UPS/Generadores
- Protección ambiental

---

## 🔥 ESTRATEGIA PARA EL EXAMEN

### ✅ Identifica PALABRAS CLAVE en la pregunta:

- **Si ves:** "datos personales UE" → Piensa: **GDPR**
- **Si ves:** "información de salud" → Piensa: **HIPAA**
- **Si ves:** "tarjetas de crédito" → Piensa: **PCI DSS**
- **Si ves:** "empresas en bolsa" → Piensa: **SOX**
- **Si ves:** "¿Quién eres?" → Piensa: **Autenticación**
- **Si ves:** "¿Qué puedes hacer?" → Piensa: **Autorización**
- **Si ves:** "una persona no debe controlar todo" → Piensa: **SoD**
- **Si ves:** "mínimos permisos" → Piensa: **Least Privilege**
- **Si ves:** "nunca confiar" → Piensa: **Zero-Trust**
- **Si ves:** "seguro de ciberseguridad" → Piensa: **Transferir riesgo**
- **Si ves:** "implementar firewall" → Piensa: **Mitigar riesgo**
- **Si ves:** "cancelar proyecto" → Piensa: **Evitar riesgo**
- **Si ves:** "detecta y alerta" → Piensa: **IDS**
- **Si ves:** "detecta y bloquea" → Piensa: **IPS**

---

## 💪 ¡Éxito en tu examen!

**Recuerda:** Este método de **palabras clave + asociaciones** es perfecto para exámenes multiple choice. No necesitas memorizar textos completos, solo las **conexiones clave** entre conceptos.

**Practica las preguntas tipo examen** y estarás listo. 🚀

