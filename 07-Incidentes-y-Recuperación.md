# 🎯 GUÍA DE ESTUDIO - UNIDAD 7: Respuesta ante Incidentes y Recuperación
## Método para Examen Multiple Choice

---

## 📚 PARTE 1: IMPORTANCIA DE LA PREPARACIÓN ANTICIPADA

### 🔑 ¿POR QUÉ PREPARARSE ANTES?

**FRASE CLAVE:**
> Los ciberataques **NO son cuestión de SI ocurrirán, sino de CUÁNDO**

**CONSECUENCIAS DE RESPUESTA IMPROVISADA:**
1. ❌ Agrava el **IMPACTO**
2. ❌ Demora la **CONTENCIÓN**
3. ❌ Genera **PÉRDIDAS** económicas y reputacionales
4. ❌ Complica obligaciones **LEGALES** y regulatorias

**REQUIERE:**
- ✅ **Políticas** definidas
- ✅ **Procedimientos** documentados
- ✅ **Roles** y responsables asignados
- ✅ **Capacitación** constante
- ✅ **Simulacros** y ejercicios
- ✅ **Comunicación** efectiva
- ✅ Integración con planes de **continuidad** (BCP/DRP)

**💡 ASOCIACIÓN:**
Preparación = **ANTES** del incidente, no después

**❓ PREGUNTA TIPO EXAMEN:**
> *Una respuesta improvisada ante un incidente puede:*
- ✅ Agravar el impacto y demorar la contención
- ❌ Mejorar la respuesta
- ❌ Reducir costos

---

## 📚 PARTE 2: PLAN DE RESPUESTA ANTE INCIDENTES

### 🔑 DEFINICIÓN

**QUÉ ES:**
Conjunto **documentado** de procedimientos y responsabilidades que guía para **detectar, contener, erradicar, comunicar y recuperarse** ante un incidente de ciberseguridad.

**DEBE SER DINÁMICO:**
Evoluciona según:
- Amenazas **EMERGENTES**
- **Lecciones aprendidas** de incidentes anteriores
- **Cambios** en infraestructura, personal o negocio

**COMPONENTES CLAVE (6):**
1. Definición de **escenarios de riesgo**
2. Asignación de **roles y recursos**
3. Procedimientos de **escalamiento** y decisión
4. **Comunicación** interna y externa
5. **Checklist** por tipo de incidente
6. **Revisión** y actualización periódica

**💡 ASOCIACIÓN:**
Plan de Respuesta = **GUÍA** para manejar incidentes

---

### 🔑 1. DEFINICIÓN DE ESCENARIOS DE RIESGO

**IDENTIFICACIÓN DE ESCENARIOS POTENCIALES:**
- **Spear phishing**
- Infección por **malware o ransomware**
- **Data Breach** (fuga de datos)
- Ataques **DDoS**

**ANÁLISIS DE IMPACTO:**
- ¿Qué sistemas críticos serían afectados?
- ¿Qué impacto en operación, reputación, legalidad?

**PRIORIZACIÓN BASADA EN:**
1. **Probabilidad** de ocurrencia
2. **Gravedad** e impacto potencial
3. **Capacidad** de respuesta actual

---

### 🔑 2. ASIGNACIÓN DE RECURSOS

**TABLA DE RECURSOS:**

| Tipo de Recurso | Qué incluye | Ejemplos |
|-----------------|-------------|----------|
| **Humanos** | Equipos especializados + Roles definidos | Líder IR, Analista de Seguridad, Coordinador Comunicaciones |
| **Técnicos** | Herramientas + Sistemas + Entornos | SIEM, EDR, SOAR, backups, sandbox |
| **Financieros** | Presupuesto específico + Fondo emergencia | Licencias, consultorías, análisis forense |

**ROLES CLAVE:**
- **Líder del Equipo de Respuesta**
- **Analista de Seguridad**
- **Coordinador de Comunicaciones**
- **Enlace con áreas legales / Alta Dirección / RRHH**

**💡 FRASE:**
> "La planificación efectiva implica tener recursos **previamente definidos, asignados y disponibles**"

---

### 🔑 3. CAPACITACIÓN Y EJERCICIOS

**TIPOS DE CAPACITACIÓN:**

**A) ENTRENAMIENTO CONTINUO:**
- Capacitación técnica periódica (nuevas amenazas, TTPs)
- Simulaciones de incidentes reales (ransomware, phishing, DDoS)
- Revisión de tiempo de respuesta y efectividad

**B) EJERCICIOS TABLETOP:**
- **Reuniones simuladas** (no técnicas)
- Se analiza **cómo responder** ante escenarios
- Evalúan **decisiones, escalamiento, comunicación**
- **Evaluaciones post-ejercicio** → ¿Qué funcionó? ¿Qué falló?

**💡 DIFERENCIA:**
- **Simulaciones** = Técnicas, prácticas
- **Tabletop** = Reuniones, análisis de procesos

**❓ PREGUNTA TIPO EXAMEN:**
> *¿Qué son los ejercicios Tabletop?*
- ✅ Reuniones simuladas para analizar respuesta a escenarios
- ❌ Simulaciones técnicas de ataques reales
- ❌ Pruebas de penetración

---

### 🔑 4. PROCEDIMIENTOS DE ESCALADO

**NIVELES DE ESCALADO (3):**

| Nivel | Nombre | Características | Ejemplo |
|-------|--------|-----------------|---------|
| **Nivel 1** | **MENOR** | Sin impacto significativo | Malware contenido en 1 endpoint aislado |
| **Nivel 2** | **MODERADO** | Afecta varios usuarios/sistemas, NO interrumpe críticos | Phishing masivo sin éxito |
| **Nivel 3** | **CRÍTICO** | Alto impacto en operación, reputación, cumplimiento | Ransomware extendido, fuga de datos |

**CRITERIOS DE ESCALADO:**
- Impacto en **CIA** (Confidencialidad, Integridad, Disponibilidad)
- Afectación a **servicios críticos**
- **Cumplimiento** de normativas

**PROCESO DE ESCALADO:**
1. **Notificación inicial** al equipo
2. **Evaluación rápida** de severidad y alcance
3. **Activación progresiva** de niveles superiores (CISO/CSIRT, Alta Dirección)
4. **Comunicación clara** y trazable

**💡 ASOCIACIÓN:**
Niveles: **1=Menor, 2=Moderado, 3=Crítico**

**❓ PREGUNTA TIPO EXAMEN:**
> *Un ransomware extendido a múltiples sistemas es un incidente de nivel:*
- ✅ Nivel 3 (Crítico)
- ❌ Nivel 1 (Menor)
- ❌ Nivel 2 (Moderado)

---

### 🔑 5. REVISIÓN Y ACTUALIZACIÓN

**EVALUACIONES PERIÓDICAS:**
- Revisiones **trimestrales o anuales**
- Validar si procesos siguen **alineados**
- **Simulacros** y auditorías internas

**APRENDIZAJE DE INCIDENTES:**
- Analizar incidentes **reales o simulados**
- Documentar **lecciones aprendidas**
- Incorporar **mejoras**

**ACTUALIZACIÓN CONTINUA - REVISAR ANTE:**
- Cambios en **infraestructura, personal, procesos**
- Nuevas **vulnerabilidades** o tácticas de ataque
- Nuevas **herramientas** de respuesta

**💡 FRASE:**
> "Un plan que no se actualiza, **pierde efectividad**. La mejora continua es parte de la ciberresiliencia"

---

## 📚 PARTE 3: NIST SP 800-61 R2 (¡MUY IMPORTANTE!)

### 🔑 LAS 4 FASES DEL NIST

**TABLA DE FASES:**

| # | Fase | Qué se hace | Palabra Clave |
|---|------|-------------|---------------|
| **1** | **Preparation** | Establecer políticas, roles, herramientas, procedimientos | **ANTES** del incidente |
| **2** | **Detection and Analysis** | Identificar signos, clasificar, determinar impacto | **DETECTAR** |
| **3** | **Containment, Eradication and Recovery** | Limitar daño, eliminar, restaurar | **CONTENER-ERRADICAR-RECUPERAR** |
| **4** | **Post-Incident Activity** | Lecciones aprendidas, reportes, actualizar | **DESPUÉS** - Aprender |

**💡 REGLA MNEMOTÉCNICA (PDCP):**
- **P**reparation → **Prepararse**
- **D**etection → **Detectar**
- **C**ontainment → **Contener/Erradicar/Recuperar**
- **P**ost-incident → **Post-mortem**

**❓ PREGUNTAS TIPO EXAMEN:**

> *¿En qué fase del NIST se establecen políticas y procedimientos?*
- ✅ Preparation (Fase 1)
- ❌ Detection and Analysis
- ❌ Post-Incident Activity

> *La fase de "Detection and Analysis" del NIST incluye:*
- ✅ Identificar signos de incidente y clasificarlos
- ❌ Establecer políticas de seguridad
- ❌ Realizar lecciones aprendidas

> *¿Qué fase del NIST viene después de la recuperación?*
- ✅ Post-Incident Activity
- ❌ Preparation
- ❌ Detection

---

## 📚 PARTE 4: CONTENCIÓN, ERRADICACIÓN Y MITIGACIÓN

### 🔑 1. CONTENCIÓN DEL INCIDENTE

**OBJETIVO:**
**Evitar propagación** y mitigar impacto inicial mientras se prepara la erradicación.

**ACCIONES COMUNES:**

**A) BLOQUEO DE ELEMENTOS MALICIOSOS:**
- IPs, URLs, dominios, puertos

**B) DESACTIVACIÓN DE CUENTAS:**
- Cambiar credenciales
- Deshabilitar usuarios comprometidos

**C) AISLAMIENTO:**
- Aislar host (desconectar de red)
- Cuarentena de archivos sospechosos
- Detener procesos/servicios

**D) CONTROLES TEMPORALES:**
- Reglas en firewall
- Políticas NAC / Zero Trust
- Restricciones por GPO (Group Policy Object)

**💡 ASOCIACIÓN:**
Contención = **STOP** la propagación (como poner un incendio en cuarentena)

---

### 🔑 2. ERRADICACIÓN DE LA AMENAZA

**OBJETIVO:**
**Eliminar completamente** la amenaza y todos sus elementos.

**ACCIONES COMUNES:**

**A) ELIMINAR ARCHIVOS Y CONFIGURACIONES:**
- Archivos maliciosos
- Servicios, procesos
- Claves de registro
- Aplicaciones no autorizadas

**B) REMOVER OBJETOS DEL ENTORNO:**
- Correos maliciosos
- Dispositivos "rogue" (no autorizados)
- Usuarios o accesos creados por atacante

**C) REVOCAR ACCESOS COMPROMETIDOS:**
- Borrado de usuarios
- Reset de credenciales
- Anulación de tokens

**D) REPARACIÓN DE SISTEMAS:**
- Reinstalación limpia
- Parcheo de vulnerabilidades

**💡 ASOCIACIÓN:**
Erradicación = **ELIMINAR TODO** rastro del atacante

---

### 🔑 3. MITIGACIÓN DE DAÑOS

**OBJETIVO:**
**Reducir impacto residual** y prevenir recurrencias.

**A) FORTALECIMIENTO DE DEFENSAS:**
- Reglas de firewall más **restrictivas**
- Implementar **MFA**
- Auditorías de seguridad post-incidente
- Validación de configuración segura

**B) EDUCACIÓN Y CONCIENTIZACIÓN:**
- Capacitación sobre **lecciones aprendidas**
- Reforzar **buenas prácticas**
- Simulacros de escenarios similares
- Pruebas de detección y respuesta

**C) LECCIONES APRENDIDAS:**
- Documentar qué se hizo **bien** y **mal**
- Feedback interno y externo
- **Resiliencia** a largo plazo:
  - Hardening
  - Mejoras técnicas
  - Cambios en arquitectura de seguridad

**💡 ASOCIACIÓN:**
Mitigación = **PREVENIR** que vuelva a pasar

---

### 🔑 TABLA RESUMEN: CONTENCIÓN vs ERRADICACIÓN vs MITIGACIÓN

| Fase | Objetivo | Cuándo | Acciones Clave |
|------|----------|--------|----------------|
| **Contención** | Evitar propagación | **DURANTE** el incidente | Bloquear, aislar, deshabilitar |
| **Erradicación** | Eliminar amenaza | **DESPUÉS** de contener | Eliminar, remover, revocar, reparar |
| **Mitigación** | Reducir impacto y prevenir | **POST-INCIDENTE** | Fortalecer defensas, capacitar, aprender |

**❓ PREGUNTAS TIPO EXAMEN:**

> *Aislar un host de la red es una acción de:*
- ✅ Contención
- ❌ Erradicación
- ❌ Mitigación

> *Eliminar archivos maliciosos y revocar accesos es parte de:*
- ✅ Erradicación
- ❌ Contención
- ❌ Preparación

> *Implementar MFA después de un incidente es parte de:*
- ✅ Mitigación
- ❌ Contención
- ❌ Erradicación

---

## 📚 PARTE 5: COMUNICACIÓN DURANTE UN INCIDENTE

### 🔑 IMPORTANCIA

**PLANEAMIENTO ESTRATÉGICO:**
- Cada incidente es **único**, pero el plan debe estar **predefinido**
- Ser **PROACTIVOS** → Facilita coordinación y evita errores
- Contemplar comunicaciones **INTERNAS** y **EXTERNAS**

**💡 FRASE:**
> "Un mal manejo comunicacional puede **agravar** el impacto técnico, legal y reputacional"

---

### 🔑 ELEMENTOS CLAVE DEL PLAN DE COMUNICACIÓN

**3 ELEMENTOS FUNDAMENTALES:**

**1. CLARIDAD EN EL MENSAJE:**
- Lenguaje **simple** y sin ambigüedades
- Evitar suposiciones y tecnicismos innecesarios

**2. COMUNICAR A TIEMPO:**
- Enviar **actualizaciones regulares**
- Notificar **apenas se confirme** el incidente

**3. TRANSPARENCIA Y HONESTIDAD:**
- Reconocer el incidente con **seriedad**
- **NO ocultar** ni minimizar el impacto

**💡 ASOCIACIÓN:**
Comunicación = **Claro, A tiempo, Transparente** (CAT)

---

### 🔑 AUDIENCIAS Y NIVELES DE INFORMACIÓN

**COMUNICACIÓN INTERNA:**
- Equipos **técnicos** y **ejecutivos**
- Toda la **organización** (si es necesario)

**COMUNICACIÓN EXTERNA:**
- **Clientes**, proveedores, partners
- Autoridades **regulatorias**
- **Prensa** (si aplica)

**PREGUNTA CLAVE:**
> ¿Qué información compartir y con quién?
> Evaluar: **Confidencialidad, impacto legal y reputacional**

**❓ PREGUNTA TIPO EXAMEN:**
> *Un plan de comunicación durante incidentes debe ser:*
- ✅ Predefinido antes del incidente
- ❌ Improvisado según la situación
- ❌ Solo para comunicación externa

---

## 📚 PARTE 6: RECUPERACIÓN POST-INCIDENTE

### 🔑 OBJETIVO

**ESTABLECER ESTRATEGIAS PARA:**
1. Restablecer **operaciones críticas**
2. Minimizar **impacto** en procesos del negocio
3. Garantizar **resiliencia** y sostenibilidad a largo plazo

**DOS PLANES PRINCIPALES:**
- **BCP** (Business Continuity Plan)
- **DRP** (Disaster Recovery Plan)

---

### 🔑 BCP vs DRP (¡SUPER IMPORTANTE!)

**TABLA COMPARATIVA:**

| Aspecto | BCP (Business Continuity Plan) | DRP (Disaster Recovery Plan) |
|---------|--------------------------------|------------------------------|
| **Enfoque** | Mantener **OPERACIÓN** del negocio | Restaurar **SISTEMAS y DATOS** |
| **Objetivo** | Continuidad mínima viable | Recuperar infraestructura IT |
| **Alcance** | **PROCESOS DE NEGOCIO** | **TECNOLOGÍA** (IT) |
| **Qué preserva** | Funciones críticas del negocio | Sistemas, datos, infraestructura |
| **Incluye** | Trabajo remoto, proveedores alternativos, operación degradada | Backups, recuperación de servidores, reinstalación |
| **Métricas** | Operación mínima | **RTO** y **RPO** |

**💡 REGLAS MNEMOTÉCNICAS:**

**BCP:**
- **B**usiness = **NEGOCIO**
- Mantiene **OPERACIÓN** (el negocio sigue funcionando)

**DRP:**
- **D**isaster **R**ecovery = **RECUPERAR TECNOLOGÍA**
- Restaura **SISTEMAS** y **DATOS**

**RELACIÓN:**
> "El BCP mantiene la **continuidad**, el DRP acelera la **recuperación técnica**"

---

### 🔑 BCP (BUSINESS CONTINUITY PLAN)

**DEFINICIÓN:**
Procesos y procedimientos que aseguran que funciones **críticas del negocio** continúen durante y después de un incidente.

**OBJETIVOS:**
- Mantener **operación mínima** viable
- Minimizar interrupción de **servicios esenciales**
- Preservar **continuidad** de procesos

**COMPONENTES CLAVE:**
- Estrategias de **trabajo remoto**
- **Redundancia** de sistemas y enlaces críticos
- Proveedores **alternativos** y planes de contingencia
- Procedimientos para **operación en modo degradado**

**💡 EJEMPLO:**
Si el edificio no es accesible → BCP dice cómo seguir trabajando desde casa

---

### 🔑 DRP (DISASTER RECOVERY PLAN)

**DEFINICIÓN:**
Estrategias y acciones específicas para **restaurar sistemas, datos e infraestructura tecnológica** después de un desastre.

**OBJETIVOS:**
- Restaurar servicios críticos de **IT** rápidamente
- Garantizar **recuperación** de datos e infraestructura
- Reducir **downtime** (tiempo de inactividad)

**COMPONENTES CLAVE:**
- **Inventario** de activos tecnológicos
- Clasificación por **prioridad de recuperación**
- Procedimientos para:
  - Recuperación de **bases de datos**
  - Restauración de **backups**
  - Reinstalación de **servicios críticos**
- Definición de **RTO** y **RPO**

---

### 🔑 RTO y RPO (¡MUY IMPORTANTE!)

**TABLA DE MÉTRICAS:**

| Métrica | Nombre Completo | Qué mide | Pregunta clave | Ejemplo |
|---------|-----------------|----------|----------------|---------|
| **RTO** | **R**ecovery **T**ime **O**bjective | Tiempo MÁXIMO para restaurar | ¿Cuánto tiempo podemos estar **SIN** el servicio? | 4 horas |
| **RPO** | **R**ecovery **P**oint **O**bjective | Pérdida de datos MÁXIMA aceptable | ¿Cuánta **PÉRDIDA** de datos toleramos? | 1 hora de datos |

**💡 REGLAS MNEMOTÉCNICAS:**

**RTO:**
- **T**ime = **TIEMPO** para recuperar
- ¿Cuánto tiempo **ABAJO**?
- Ejemplo: Sistema debe estar UP en máximo 4 horas

**RPO:**
- **P**oint = **PUNTO** en el tiempo
- ¿Cuántos datos **PERDEMOS**?
- Ejemplo: Backup cada hora → Perdemos máximo 1 hora de datos

**DIFERENCIA CRÍTICA:**
- **RTO** = ¿Cuánto tiempo **TARDA** la recuperación?
- **RPO** = ¿Cuántos **DATOS PERDEMOS**?

**❓ PREGUNTAS TIPO EXAMEN:**

> *RTO (Recovery Time Objective) mide:*
- ✅ Tiempo máximo para restaurar un servicio
- ❌ Pérdida de datos máxima aceptable
- ❌ Frecuencia de backups

> *RPO (Recovery Point Objective) mide:*
- ✅ Pérdida de datos máxima aceptable
- ❌ Tiempo para restaurar un servicio
- ❌ Costo de recuperación

> *Si hacemos backup cada 2 horas, el RPO es:*
- ✅ 2 horas
- ❌ 4 horas
- ❌ 1 hora

> *BCP se enfoca en:*
- ✅ Mantener operación del negocio
- ❌ Restaurar sistemas IT
- ❌ Solo backups

> *DRP se enfoca en:*
- ✅ Recuperar sistemas y datos IT
- ❌ Mantener operación del negocio
- ❌ Solo comunicaciones

> *¿Qué plan incluye estrategias de trabajo remoto?*
- ✅ BCP
- ❌ DRP
- ❌ Ninguno

---

### 🔑 SINERGIA ENTRE BCP Y DRP

**CÓMO SE COMPLEMENTAN:**
- **BCP** → Mantiene la operación durante la crisis
- **DRP** → Restaura la tecnología rápidamente

**RESILIENCIA ORGANIZACIONAL:**
- Fortalece capacidad de **resistir y recuperarse**
- Reduce impacto **económico, operativo y reputacional**

**💡 FRASE:**
> "Mientras el BCP mantiene la **continuidad**, el DRP acelera la **recuperación técnica**"

---

## 🎯 RESUMEN ULTRA-RÁPIDO (Para 10 min antes del examen)

### 📌 PREPARACIÓN:
- Ataques = **CUÁNDO**, no SI
- Requiere: Políticas, procedimientos, roles, capacitación, simulacros

### 📌 PLAN DE RESPUESTA - 6 COMPONENTES:
1. Escenarios de riesgo
2. Roles y recursos
3. Escalamiento (3 niveles: Menor, Moderado, Crítico)
4. Comunicación
5. Checklist
6. Revisión

### 📌 CAPACITACIÓN:
- **Simulaciones** = Técnicas
- **Tabletop** = Reuniones simuladas

### 📌 NIST SP 800-61 (PDCP):
1. **P**reparation → Antes
2. **D**etection → Detectar
3. **C**ontainment → Contener/Erradicar/Recuperar
4. **P**ost-incident → Aprender

### 📌 CONTENCIÓN-ERRADICACIÓN-MITIGACIÓN:
- **Contención** = Evitar propagación (bloquear, aislar)
- **Erradicación** = Eliminar TODO (remover, revocar, reparar)
- **Mitigación** = Prevenir recurrencia (fortalecer, capacitar)

### 📌 COMUNICACIÓN (CAT):
- **C**lara
- **A** tiempo
- **T**ransparente
- Interna Y Externa

### 📌 BCP vs DRP:
- **BCP** = **NEGOCIO** (mantener operación)
- **DRP** = **TECNOLOGÍA** (restaurar sistemas)

### 📌 RTO vs RPO:
- **RTO** = **TIEMPO** para recuperar (¿Cuánto ABAJO?)
- **RPO** = **DATOS** perdidos (¿Cuánto PERDEMOS?)

### 📌 NIVELES DE ESCALADO:
1. Menor
2. Moderado
3. Crítico

---

## 🔥 ESTRATEGIA PARA EL EXAMEN

### ✅ Palabras clave en preguntas:

**Si ves:** "antes del incidente" → **Preparation**
**Si ves:** "identificar signos" → **Detection and Analysis**
**Si ves:** "lecciones aprendidas" → **Post-Incident Activity**
**Si ves:** "evitar propagación" → **Contención**
**Si ves:** "eliminar completamente" → **Erradicación**
**Si ves:** "prevenir recurrencia" → **Mitigación**
**Si ves:** "reuniones simuladas" → **Tabletop**
**Si ves:** "simulaciones técnicas" → **Entrenamiento técnico**
**Si ves:** "ransomware extendido" → **Nivel 3 (Crítico)**
**Si ves:** "mantener operación del negocio" → **BCP**
**Si ves:** "restaurar sistemas IT" → **DRP**
**Si ves:** "tiempo para recuperar" → **RTO**
**Si ves:** "pérdida de datos" → **RPO**
**Si ves:** "comunicación predefinida" → **Plan de comunicación**

---

## 💪 ¡Éxito en tu examen!

**Recuerda:** Esta unidad es sobre **PREPARACIÓN** y **RESPUESTA**:
1. **Prepararse ANTES** (políticas, roles, capacitación)
2. **NIST SP 800-61** (las 4 fases)
3. **Contención-Erradicación-Mitigación** (diferencias)
4. **Comunicación** efectiva
5. **BCP vs DRP** (negocio vs tecnología)
6. **RTO vs RPO** (tiempo vs datos)

**Lo más importante:**
- **NIST 4 fases** (Preparation, Detection, Containment, Post-incident)
- **Contención vs Erradicación vs Mitigación** (cuándo y qué)
- **BCP vs DRP** (negocio vs IT)
- **RTO vs RPO** (tiempo vs pérdida de datos)
- **Niveles de escalado** (1-2-3)
- **Tabletop** vs Simulaciones

**Practica las preguntas tipo examen y estarás listo.** 🚀

