# 💎 Matriz de Criticidad de Activos: Asset Tiering Standard

**Versión:** 2.0
**Objetivo:** Priorización de recursos defensivos y definición de SLAs de recuperación.

La protección uniforme es ineficiente y costosa. **Sesecpro** aplica una metodología de "Defensa en Profundidad" basada en la criticidad del activo para la supervivencia de la organización. Esta matriz define dónde debemos concentrar las inversiones de ciberseguridad más agresivas.

---

## 1. Clasificación por Niveles (Asset Tiers)

Dividimos el ecosistema tecnológico en cuatro niveles jerárquicos basados en la tolerancia al fallo.

### 🔴 Tier 0: "Joyas de la Corona" (Mission Critical)
Activos cuya confidencialidad, integridad o disponibilidad es **existencial** para la compañía. Su compromiso implica pérdidas catastróficas inmediatas o responsabilidad penal.
* **Tolerancia al riesgo:** CERO.
* **RTO (Tiempo máx. caída):** < 1 Hora.
* **RPO (Pérdida de datos máx.):** < 15 Minutos.
* **Ejemplos:**
    * Controladores de Dominio (Identidad).
    * Core Bancario / ERP de Producción en tiempo real.
    * Propiedad Intelectual (Fórmulas, Código Fuente Propietario).
    * Sistemas SCADA/OT de seguridad física.

### 🟠 Tier 1: Críticos de Negocio (Business Critical)
Sistemas necesarios para la generación de ingresos o el cumplimiento regulatorio. Su caída detiene la facturación, pero no amenaza la supervivencia inmediata.
* **Tolerancia al riesgo:** BAJA.
* **RTO:** < 4 Horas.
* **Ejemplos:**
    * CRM (Ventas), E-commerce, Plataforma de Facturación.
    * Correo Electrónico (Exchange Online).
    * Bases de Datos de Clientes (PII - GDPR).

### 🔵 Tier 2: Operativos (Business Operational)
Sistemas de soporte interno. Su caída reduce la eficiencia, pero existen procesos manuales alternativos.
* **Tolerancia al riesgo:** MEDIA.
* **RTO:** < 24 Horas.
* **Ejemplos:**
    * Portal de RRHH, Intranet, Servidores de Ficheros departamentales.
    * Herramientas de colaboración no críticas.

### ⚪ Tier 3: Soporte y No Productivos (Support & Lab)
Entornos de pruebas, desarrollo o sistemas heredados (Legacy) no conectados a producción.
* **Tolerancia al riesgo:** ALTA.
* **RTO:** "Best Effort" (Sin garantía).

---

## 2. Estándar de Protección por Nivel

La clasificación dicta la arquitectura de seguridad requerida. Esto asegura que el presupuesto se gasta donde más importa.

| Control de Seguridad | Tier 0 (Joyas) | Tier 1 (Crítico) | Tier 2 (Operativo) | Tier 3 (Soporte) |
| :--- | :---: | :---: | :---: | :---: |
| **Identidad (MFA)** | Físico (YubiKey) | App (Number Match) | App Standard | Password Compleja |
| **Monitorización (SOC)** | 24/7/365 Real-Time | 24/7 Alertas Críticas | Horario Laboral | Logs Retenidos |
| **Respuesta (EDR)** | Bloqueo Automático | Bloqueo Automático | Detección | Antivirus Base |
| **Red** | Segmentación Total (Air Gap/VLAN) | Zero Trust (SASE) | VPN Corporativa | Acceso Restringido |
| **Backups** | Inmutables + Offsite | Inmutables | Diario | Semanal |
| **Auditoría (Pentest)** | Trimestral + Red Team | Semestral | Anual | N/A |

---

## 3. Matriz de Evaluación Rápida (CIA)

Utilice esta guía para clasificar nuevos activos:

| Tipo de Activo | Confidencialidad | Integridad | Disponibilidad | Clasificación Final |
| :--- | :--- | :--- | :--- | :--- |
| **Datos Financieros/Tesorería** | **Crítica** | **Crítica** | Alta | **TIER 0** |
| **Propiedad Intelectual (R&D)** | **Crítica** | Alta | Media | **TIER 0** |
| **Línea de Producción (OT)** | Baja | Alta | **Crítica** | **TIER 0** |
| **Servidor de Impresión** | Baja | Baja | Media | **TIER 2** |
| **Web Corporativa (Informativa)** | Baja | Alta | Alta | **TIER 1** |

---

### 💡 Nota Estratégica
*El error más común en las organizaciones es tratar todos los activos como Tier 1. Esto diluye el presupuesto y deja las "Joyas de la Corona" insuficientemente protegidas. En Sesecpro, priorizamos la **supervivencia** sobre la comodidad.*

*© 2026 Sesecpro Strategic Resilience.*
