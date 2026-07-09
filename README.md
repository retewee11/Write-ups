# Writeups

[![Hack The Box](https://img.shields.io/badge/Platform-Hack%20The%20Box-green?style=flat-square&logo=hackthebox)](https://www.hackthebox.com/)
[![TryHackMe](https://img.shields.io/badge/Platform-TryHackMe-red?style=flat-square&logo=tryhackme)](https://tryhackme.com/)
[![OS-Linux](https://img.shields.io/badge/OS-Linux-orange?style=flat-square&logo=linux)](https://www.linux.org/)
[![OS-Windows](https://img.shields.io/badge/OS-Windows-blue?style=flat-square&logo=windows)](https://www.microsoft.com/windows)
[![Methodology-PTES](https://img.shields.io/badge/Methodology-PTES-blueviolet?style=flat-square)](http://www.pentest-standard.org/)

Colección de resoluciones y análisis técnicos de máquinas de Hack The Box y TryHackMe organizados bajo una metodología profesional de pentesting.

## Estructura del repositorio

* `writeups/htb/` — Máquinas y retos de Hack The Box.
* `writeups/thm/` — Salas y desafíos de TryHackMe.

Cada writeup está estructurado siguiendo las fases fundamentales de un pentesting:
* **Reconocimiento y Enumeración**
* **Análisis de Vulnerabilidades**
* **Explotación**
* **Post-Explotación y Escalada de Privilegios**
* **Persistencia** *(si aplica)*

---

## Estadísticas del Repositorio

| Métrica | Cantidad |
| :--- | :--- |
| **Total de Máquinas** | 10 |
| **Hack The Box** | 2 |
| **TryHackMe** | 8 |
| **S.O. Windows** | 6 |
| **S.O. Linux** | 4 |

---

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
| [Blue](writeups/thm/Blue) | Fácil | Windows | EternalBlue (CVE-2017-0143), MS17-010, Metasploit |
| [Blaster](writeups/thm/Blaster) | Fácil | Windows | IIS, Gobuster, RDP, UAC Bypass (CVE-2019-1388), Metasploit |
| [Ice](writeups/thm/Ice) | Fácil | Windows | Icecast (CVE-2017-7659), Local Exploit Suggester, Tokenmagic |
| [Anthem](writeups/thm/anthem) | Fácil | Windows | Robots.txt, Umbraco, RDP, Backup recovery, Admin cmd |
| [Library](writeups/thm/library) | Fácil | Linux | robots.txt, SSH brute force (Hydra), Python library hijacking (bak.py) |
| [Relevant](writeups/thm/relevant) | Medio | Windows | Fuzzing, SMB client, ASPX reverse shell, PrintSpoofer (PrivEsc) |
| [Retro](writeups/thm/retro) | Fácil | Windows | IIS, Gobuster, RDP, CVE-2017-0213 (PrivEsc) |
