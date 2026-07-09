# [Nombre de la Máquina] - Writeup

| Plataforma | S.O. | Dificultad | IP Objetivo | Temas Clave |
| :--- | :--- | :--- | :--- | :--- |
| [TryHackMe / Hack The Box] | [Windows / Linux] | [Fácil / Medio / Difícil] | `X.X.X.X` | [Tema 1, Tema 2, ...] |

## Reconocimiento y Enumeración

### Escaneo de puertos

```bash
nmap -sC -sV -Pn -p- [IP]
```

### Enumeración de servicios
*Describir aquí los hallazgos en servicios específicos (ej. directorios descubiertos con Gobuster, análisis de recursos compartidos con smbclient, banner grabbing de servicios, etc.). Incluir capturas de pantalla de la carpeta `assets/` si es necesario.*

---

## Análisis de Vulnerabilidades

*Detallar las posibles vulnerabilidades identificadas (como CVEs conocidos, configuraciones inseguras, credenciales por defecto o de prueba, formularios sin saneamiento, etc.) y la justificación de por qué son explotables.*

---

## Explotación

### Acceso Inicial
*Explicar el paso a paso del exploit o técnica empleada para conseguir la primera shell o acceso remoto (SSH, RDP, reversa en puerto específico, etc.).*

---

## Post-Explotación y Escalada de Privilegios

### Elevación de Privilegios
*Explicar la enumeración local del sistema (ej. búsqueda de archivos SUID, Capabilities, permisos débiles en servicios, vulnerabilidades del Kernel) y los pasos seguidos para escalar privilegios a NT AUTHORITY\SYSTEM (Windows) o root (Linux).*

---

## Persistencia (Si aplica)
*Describir el método utilizado para garantizar el acceso recurrente al sistema objetivo.*

---

## Mitigación y Recomendaciones

1. **[Mitigación 1]**: *Descripción clara y concisa de cómo solucionar el vector de entrada o vulnerabilidad explotada.*
2. **[Mitigación 2]**: *Descripción de la recomendación de endurecimiento para evitar la escalada de privilegios.*
3. **[Mitigación 3]**: *Buenas prácticas generales de administración del sistema afectado (ej. desactivación de protocolos obsoletos, MFA).*
