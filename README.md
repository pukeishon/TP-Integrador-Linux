# Trabajo Práctico Integrador – GNU/Linux

Repositorio de entrega del TP Integrador para la materia de GNU/Linux (Ingeniería en Inteligencia Artificial – Universidad de Palermo).

---

## Integrantes del grupo

- Bruno Jecheln 
- Isabella Mordeaglia
- Adam Martinez
---

## Contenido entregado

Se incluyen los siguientes archivos comprimidos:

- `root.tar.gz`
- `etc.tar.gz`
- `opt.tar.gz`
- `proc.tar.gz`
- `www_dir.tar.gz`
- `backup_dir.tar.gz`
- `var.tar.gz` dividido en partes:
  - `var_part_aa` a `var_part_ae`

---

## Detalles técnicos

- Configuración de red estática con IP `192.168.1.200`
- Servicios instalados y configurados:
  - Apache con PHP y DocumentRoot en `/www_dir`
  - SSH con clave pública/privada
  - MariaDB cargando `db.sql`
- Dos particiones montadas automáticamente:
  - `/www_dir` (3GB)
  - `/backup_dir` (6GB)
- Script `/opt/scripts/backup_full.sh` que permite:
  - Backups comprimidos con fecha en nombre
  - Validación de origen/destino
  - Opción `-help`
- Tareas programadas en `crontab`:
  - Todos los días 00:00 ➜ `/var/log`
  - Lunes, miércoles y viernes 23:00 ➜ `/www_dir`

---

##  Observaciones

- El archivo `proc.tar.gz` contiene una copia parcial representativa (no el `/proc` completo).
- El backup de `/var` se dividió en partes menores a 100 MB para cumplir con las restricciones de GitHub.

---

## Link del Repositorio

[https://github.com/pukeishon/TP-Integrador-Linux](https://github.com/pukeishon/TP-Integrador-Linux)
