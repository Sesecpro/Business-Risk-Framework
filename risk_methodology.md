# 📐 Metodología de Cuantificación de Riesgo Corporativo (CRQ)

**Versión:** 2.0 (Enterprise Standard)
**Enfoque:** Traducción de CVSS (Técnico) a Riesgo Financiero (EBITDA).

Esta metodología establece el marco estándar de **Sesecpro** para evaluar riesgos cibernéticos. Su objetivo es proporcionar al Consejo de Administración una visión clara de la exposición al riesgo, permitiendo comparar el ciberriesgo en igualdad de condiciones con riesgos financieros, legales o de mercado.

---

## 1. Filosofía: Del "CVSS" al Impacto de Negocio
En la gestión tradicional, un servidor con una vulnerabilidad crítica (CVSS 10) se considera una emergencia. En el **Framework Sesecpro**, esa vulnerabilidad es irrelevante si el servidor no soporta un proceso de negocio crítico.

**La Ecuación del Riesgo Sesecpro:**
$$Riesgo = (Impacto \ Financiero \times Probabilidad \ de \ Amenaza) \times Contexto \ del \ Activo$$

---

## 2. Taxonomía de Impacto (Las 4 Dimensiones)

Clasificamos cada hallazgo según su capacidad para dañar los cuatro pilares de valor de la compañía.

| Dimensión | Definición Estratégica | KRI (Indicador Clave de Riesgo) |
| :--- | :--- | :--- |
| **💵 Financiera** | Impacto directo en P&L (Pérdidas y Ganancias), salida de caja y costes de recuperación. | Impacto > 0.5% del EBITDA anual. |
| **⚙️ Operativa** | Interrupción de la cadena de valor, logística o capacidad productiva. | Tiempo de Inactividad (Downtime) > RTO establecido. |
| **⚖️ Legal / Compliance** | Sanciones regulatorias (NIS2, GDPR, DORA) y responsabilidad civil/penal de los administradores. | Materialización de Sanciones > 2% Facturación Global. |
| **📢 Reputacional** | Erosión de confianza, pérdida de valor de marca y fuga de clientes. | Cobertura mediática negativa en prensa nacional/sectorial. |

---

## 3. Escala de Severidad Financiera (Materialidad)

Para eliminar la subjetividad, Sesecpro define los niveles de riesgo basándose en umbrales financieros preacordados con la Dirección Financiera (CFO).

| Nivel | Severidad | Impacto Financiero Est. | Impacto Operativo | Acción Requerida |
| :--- | :--- | :--- | :--- | :--- |
| **L5** | **Catastrófico** | **> 10% EBITDA** | Parada total (> 24h). Amenaza a la viabilidad de la empresa. | **War Room Inmediato.** Comunicación a CNMV/Reguladores. |
| **L4** | **Crítico** | **5% - 10% EBITDA** | Parada de procesos core (> 4h). Incumplimiento contractual grave. | **Corrección < 24h.** Reporte al Comité de Dirección. |
| **L3** | **Alto** | **1% - 5% EBITDA** | Degradación severa de servicio. Impacto en SLA de clientes. | Plan de remediación prioritaria (< 7 días). |
| **L2** | **Medio** | **< 1% EBITDA** | Interrupción menor interna. Sin impacto visible al cliente. | Gestión en ciclo de mantenimiento estándar (30 días). |
| **L1** | **Bajo** | **Insignificante** | Mantenimiento rutinario o costes operativos absorbibles. | Aceptación del riesgo o remediación a largo plazo. |

---

## 4. Matriz de Probabilidad (Threat Intel Driven)

No usamos "frecuencia histórica" (lo que pasó ayer), sino **Inteligencia de Amenazas** (lo que está pasando hoy en el sector).

* **P5 - Inminente:** Grupo de amenazas activo atacando el sector/región actual (Campañas activas).
* **P4 - Probable:** Vulnerabilidad ("Exploit") pública disponible y automatizable.
* **P3 - Posible:** Requiere condiciones específicas o acceso interno previo.
* **P2 - Improbable:** Existen controles compensatorios fuertes (MFA, Segmentación).
* **P1 - Raro:** Teóricamente posible, pero requiere recursos de estado-nación o complejidad extrema.

---

### ⚠️ Nota de Aplicación
Esta metodología debe ser calibrada anualmente junto con el **CFO** para ajustar los umbrales de materialidad financiera según la facturación del ejercicio corriente.

*© 2026 Sesecpro Strategic Resilience.*
