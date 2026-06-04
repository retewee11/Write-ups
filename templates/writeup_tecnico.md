# BITÁCORA TÉCNICA DE EXPLOTACIÓN (WRITEUP)

---

## FICHA DE INFORMACIÓN DEL OBJETIVO

*   **Identificador del Target:** [Nombre del host / Reto]
*   **Dirección IP:** [X.X.X.X]
*   **Nombre de Dominio (FQDN):** [target.local / sub.target.local]
*   **Sistema Operativo:** [Linux (distro / kernel) / Windows (versión / build)]
*   **Entorno:** [Interno / Perimetral / CTF (HTB/THM)]

---

## RESUMEN DE LA RUTA DE INTRUSIÓN

*   **Punto de Acceso Inicial:** [Definir vector de acceso inicial, ej: Inyección SQL, credenciales expuestas]
*   **Usuario Inicial:** [Nombre del usuario obtenido inicialmente]
*   **Escalada de Privilegios:** [Definir vector de escalada local]
*   **Privilegios Logrados:** [root / NT AUTHORITY\SYSTEM / Administrador]

---

## BITÁCORA PASO A PASO (REPRODUCIBILIDAD)

### 1. Reconocimiento y Enumeración

#### 1.1 Descubrimiento de Puertos Activos
Ejecución del escaneo inicial de puertos para identificar la superficie expuesta:

```bash
# [Insertar comandos de escaneo de puertos ejecutados (ej: nmap)]
```

**Puertos Detectados:**
*   **Port [Número]/[Protocolo]:** [Nombre de Servicio] - [Versión] - [Breves observaciones].

#### 1.2 Enumeración de Servicios y Aplicaciones
(Documentar hallazgos de herramientas de escaneo web, subdominios o directorios).

```bash
# [Insertar comandos de fuerza bruta de directorios o DNS (ej: gobuster, dirsearch)]
```

**Resultados de interés:**
*   `[URL / Recurso]` - [Código de estado y descripción de lo identificado].

---

### 2. Acceso Inicial (Initial Foothold)

#### 2.1 Vector de Explotación
Explicación detallada del fallo explotado para conseguir ejecución de código en la máquina objetivo.

#### 2.2 Ejecución del Exploit / Payload
Detalle de comandos o scripts utilizados para forzar la intrusión:

```bash
# [Insertar comando de ejecución del exploit o payload de acceso inicial]
```

**Escucha en máquina atacante (si aplica):**
```bash
# [Insertar comando empleado para recibir la conexión (ej: netcat listener)]
```

**Sesión establecida:**
```text
# [Evidencia de consola interactiva y usuario obtenido (ej: output de id, whoami)]
```

---

### 3. Post-Explotación Local y Movimiento Lateral

#### 3.1 Estabilización de la Consola
Comandos utilizados para estabilizar la sesión interactiva (TTY):

```bash
# [Insertar secuencia de comandos para tratamiento de TTY]
```

#### 3.2 Enumeración Interna de Credenciales y Secretos
Comandos ejecutados para auditar el sistema local y recolectar secretos:

```bash
# [Insertar comandos de enumeración manual o automatizada (ej: búsqueda de configs, sudo -l)]
```

#### 3.3 Movimiento Lateral y Pivoting (Si aplica)
Documentar la configuración de túneles o saltos para acceder a otros segmentos de red:

```bash
# [Insertar comandos de redirección de puertos, proxies o túneles (ej: chisel, ligolo-ng)]
```

---

### 4. Escalada de Privilegios

#### 4.1 Identificación del Vector de Escalada
Descripción de la vulnerabilidad local, tarea cron, binario SUID, capacidad o privilegio abusado.

#### 4.2 Explotación del Vector local
Comandos ejecutados para la elevación de privilegios:

```bash
# [Insertar comandos ejecutados para abusar del vector de escalada local]
```

**Confirmación de privilegios de Administrador / Root:**
```bash
# [Evidencia de privilegios elevados (ej: whoami, id)]
```

---

### 5. Indicadores de Compromiso (IoCs) e Información Obtenida

#### 5.1 Secretos Extraídos (Flags)
*   **User Flag / Hash:** [Hash o secreto de usuario]
*   **Root Flag / Hash:** [Hash o secreto de administrador/root]

#### 5.2 Registro de Limpieza (Post-Audit CleanUp)
Listado de archivos transferidos, cuentas creadas o configuraciones modificadas que deben ser eliminadas o revertidas:

| Ruta Absoluta / Recurso | Usuario Propietario | Hash SHA-256 o Detalle | Acción Requerida |
| :--- | :--- | :--- | :--- |
| [Ej: /tmp/script.sh] | [Usuario] | [Hash] | [Eliminar / Revertir] |

---

### 6. NOTAS Y REFERENCIAS
*   [Notas y lecciones aprendidas durante la resolución].
*   [Enlaces a recursos externos, GTFOBins, LOLBAS o CVEs].
