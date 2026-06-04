# INFORME DE SIMULACIÓN DE ADVERSARIOS (RED TEAM)

---

## CONTROL DOCUMENTAL

### Detalles del Proyecto
*   **Identificador de Proyecto:** SEC-2026-XXXX
*   **Cliente / Organización:** [Nombre de la Empresa / Organización]
*   **Clasificación de Seguridad:** CONFIDENCIAL / TLP:AMBER (Restringido para uso interno del cliente y el equipo evaluador)
*   **Fecha de Emisión:** DD/MM/AAAA
*   **Equipo Evaluador (Red Team):**
    *   [Nombre del Consultor] - Lead Red Team Consultant
    *   [Nombre del Consultor] - Security Researcher

### Historial de Versiones
| Versión | Fecha | Autor | Descripción de Modificaciones |
| :--- | :---: | :--- | :--- |
| 1.0 | DD/MM/AAAA | [Nombre] | Versión inicial entregable para revisión técnica. |

### Firmas y Aprobaciones
| Rol | Nombre | Firma / Estado | Fecha |
| :--- | :--- | :---: | :---: |
| Preparado por (Red Team) | [Nombre] | Aprobado | DD/MM/AAAA |
| Revisado por (QA) | [Nombre] | Aprobado | DD/MM/AAAA |
| Aceptado por (Cliente) | [Nombre] | Pendiente | DD/MM/AAAA |

---

## 1. RESUMEN EJECUTIVO

### 1.1 Objetivos de la Evaluación
El principal objetivo de esta simulación de adversarios es evaluar la capacidad de prevención, detección y respuesta de la infraestructura tecnológica, así como el nivel de madurez del equipo de defensa (**Blue Team**) frente a tácticas y técnicas de ataques dirigidos del mundo real.

### 1.2 Calificación de Riesgo Global
El nivel de riesgo general determinado tras el ejercicio se clasifica como: **[CRÍTICO / ALTO / MEDIO / BAJO]**

*   **Impacto de Negocio:** Alto. Se logró acceder a datos confidenciales del negocio y comprometer controladores de dominio.
*   **Capacidad de Detección:** Baja. Los sistemas de monitorización (SIEM/EDR) detectaron de forma parcial las fases tempranas, pero no bloquearon la escalada.

### 1.3 Resumen del Vector de Ataque (Kill Chain)
1.  **Acceso Inicial:** Explotación de una vulnerabilidad expuesta en [Servicio / Aplicación Web] que permitió la ejecución remota de comandos (RCE).
2.  **Persistencia:** Instalación de una puerta trasera en memoria y configuración de tareas programadas persistentes.
3.  **Movimiento Lateral:** Pivoteo desde el segmento DMZ hacia la red interna corporativa a través de túneles de red cifrados.
4.  **Escalada de Privilegios:** Explotación de configuraciones débiles en políticas locales y abuso de capacidades del sistema operativo, logrando acceso de Administrador / Root.

---

## 2. ESCENARIO Y REGLAS DE COMPROMISO (ROE)

### 2.1 Activos en Alcance
| IP / FQDN | Segmento de Red | Entorno | Descripción |
| :--- | :--- | :---: | :--- |
| [IP / Rango] | DMZ | Producción | Servidor Web de Aplicaciones |
| [IP / Rango] | Interna | Producción | Directorio Activo / Base de Datos |

### 2.2 Exclusiones y Restricciones
*   **Denegación de Servicio (DoS/DDoS):** Excluida explícitamente para evitar impacto en la continuidad de negocio.
*   **Ingeniería Social (Phishing):** [Permitida / Excluida] según los acuerdos iniciales del proyecto.
*   **Ventana de Pruebas:** Las actividades de explotación activa se limitaron a la ventana horaria de [00:00] a [06:00] (hora local).

---

## 3. METODOLOGÍA Y ESTÁNDARES

Esta simulación se ha realizado siguiendo las fases descritas en la metodología **PTES** (Penetration Testing Execution Standard) y mapeando las técnicas utilizadas bajo el marco **MITRE ATT&CK**:

*   **Reconocimiento [TA0043]**: Recopilación de información pasiva y activa de los objetivos expuestos.
*   **Acceso Inicial [TA0001]**: Explotación de fallos de configuración o vulnerabilidades para obtener ejecución en el objetivo.
*   **Ejecución [TA0002]**: Ejecución de herramientas y scripts maliciosos dentro del sistema.
*   **Persistencia [TA0003]**: Configuración de mecanismos para mantener el acceso tras reinicios.
*   **Escalada de Privilegios [TA0004]**: Elevación de permisos de usuario básico a privilegios administrativos.

---

## 4. CRONOLOGÍA DE ACTIVIDADES E INDICADORES DE COMPROMISO (IoCs)

Con el fin de facilitar la correlación de logs en los sistemas de detección del cliente, se detalla la cronología exacta de las acciones más críticas realizadas por el Red Team:

| Marca Temporal (UTC) | IP Origen | Acción Realizada / Herramienta | IP/Host Destino | Detalle de IoC (Ruta / Hash SHA-256) | Detectado por Blue Team |
| :---: | :---: | :--- | :---: | :--- | :---: |
| [Fecha / Hora] | [IP Origen] | [Acción / Herramienta] | [IP Destino] | [Ej: /ruta/script | SHA-256] | [Sí / No / Parcial] |

---

## 5. MATRIZ DE RIESGO DE HALLAZGOS

Los hallazgos se clasifican cruzando la **Probabilidad Técnica** de explotación y el **Impacto de Negocio** resultante:

| Probabilidad \ Impacto | Bajo | Medio | Alto | Crítico |
| :--- | :---: | :---: | :---: | :---: |
| **Muy Alta** | Medio | Alto | Crítico | Crítico |
| **Alta** | Bajo | Medio | Alto | Crítico |
| **Media** | Bajo | Bajo | Medio | Alto |
| **Baja** | Informativo | Bajo | Bajo | Medio |

---

## 6. DETALLE DE HALLAZGOS

### 6.1 [ID-HALLAZGO] — [Título Descriptivo del Hallazgo / Vulnerabilidad]
*   **Severidad:** [Crítico / Alto / Medio / Bajo]
*   **Puntuación CVSSv3.1:** [Especificar puntuación y vector CVSS, ej: AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H]
*   **Activos Afectados:** [IP / Hostname / Servicio]
*   **Vector de Explotación:** [Definir vector general, ej: Inyección SQL, Deserialización insegura]

#### Descripción Técnica
[Explicación clara y concisa de la vulnerabilidad identificada, cómo funciona y qué impacto tiene en el sistema].

#### Prueba de Concepto (PoC)
1.  **Fase de Enumeración / Detección:**
    ```bash
    # [Insertar comandos ejecutados para detectar o diagnosticar el servicio vulnerable]
    ```
2.  **Explotación:**
    ```bash
    # [Insertar comandos, scripts o peticiones empleados para comprometer el servicio]
    ```
3.  **Evidencia de Compromiso:**
    ```text
    # [Insertar capturas de texto, hashes, outputs de consola o flags obtenidos como prueba]
    ```

#### Impacto Asociado
[Descripción de las consecuencias reales sobre el negocio (ej: fuga de datos, pérdida de disponibilidad, control del segmento de red)].

#### Recomendaciones de Mitigación
*   **Inmediata (Workaround):** [Medidas provisionales para mitigar el riesgo temporalmente].
*   **Corto Plazo (Remediación):** [Solución definitiva, ej: aplicar parches o actualizar componentes].
*   **Largo Plazo (Preventiva):** [Políticas, hardening general, monitorización].
*   **Estado:** [Abierto / Mitigado]

---

## 7. ANEXOS Y REFERENCIAS
*   **Estándares de Seguridad:** [Links o referencias a OWASP, guías de endurecimiento CIS].
*   **Repositorios de Exploits Utilizados:** [URLs de confianza a PoCs públicos].
