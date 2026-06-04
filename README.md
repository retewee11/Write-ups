# Writeups

Colección de resoluciones y análisis técnicos de máquinas de Hack The Box y TryHackMe.

## Estructura del repositorio

* `writeups/htb/` — Máquinas y retos de Hack The Box.
* `writeups/thm/` — Salas y desafíos de TryHackMe.
* `templates/` — Plantillas de reportes técnicos y ejecutivos.

## Soluciones

### Hack The Box

| Máquina | Dificultad | S.O. | Temas clave |
| :--- | :--- | :--- | :--- |
| [Cap](writeups/htb/cap) | Fácil | Linux | IDOR, PCAP Analysis, Capabilities |
| [DevArea](writeups/htb/DevArea) | Medio | Linux | JWT Bypass, XXE, Capabilities |

### TryHackMe

| Sala | Dificultad | S.O. | Temas clave |
| :--- | :--- | :--- | :--- |
| [BountyHacker](writeups/thm/BountyHacker) | Fácil | Linux | FTP Anonymous, SSH Brute Force, SUID |

---

## Plantillas de reporte

En el directorio [templates/](templates) se encuentran los formatos utilizados para documentar las pruebas:

* [Informe Red Team / Stakeholders](templates/informe_redteam.md): Resumen ejecutivo, impacto en negocio, matriz de riesgo y plan de mitigación.
* [Writeup Técnico / Interno](templates/writeup_tecnico.md): Paso a paso de explotación detallada (reconocimiento, intrusión y escalada).
