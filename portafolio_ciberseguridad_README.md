# Portafolio GitHub: Ciberseguridad

> Cómo usarlo: crea un repositorio público con el mismo nombre que tu usuario de GitHub y pega la sección "README de perfil" como README.md. Luego crea cada repo de la lista y usa la plantilla del final.
> Lo marcado con **[confirmar]** debes validarlo antes de publicar.

---

## README de perfil

# Hola, soy Germán León Galdos 👋

Administrador de Redes y Comunicaciones con enfoque en ciberseguridad. Trabajo en transformación digital del sector público, con proyectos de conectividad en hospitales y postas de salud de la región Ica, Perú.

**Certificación:** Google Cybersecurity Professional Certificate **[confirmar: año y enlace de Credly]**

### Qué hago
- Análisis de incidentes y de tráfico de red
- Evaluación de riesgos y vulnerabilidades
- Automatización de tareas de seguridad con Python y SQL
- Redes seguras en entornos hospitalarios (cableado estructurado, segmentación, monitoreo con Zabbix)

### Herramientas
`Linux` `Bash` `Python` `SQL` `Wireshark` `tcpdump` `Zabbix` `Fortinet` `Cisco`
**[confirmar: SIEM usado en el curso, por ejemplo Splunk o Chronicle]**

### Marcos y normas
NIST CSF · ISO/IEC 27001 · TIA-942 (data center) · Ley 29733 (protección de datos personales, Perú)

### Proyectos destacados
| Repo | Qué demuestra |
|---|---|
| [incident-report-ransomware-clinica](#) | Respuesta a incidentes con NIST |
| [risk-assessment-hospital-regional](#) | Evaluación de riesgos en red hospitalaria |
| [python-lista-acceso-automatizada](#) | Automatización con Python |
| [sql-filtrado-logs-seguridad](#) | Investigación de logs con SQL |
| [wireshark-analisis-trafico](#) | Análisis de paquetes |
| [linux-auditoria-permisos](#) | Hardening de permisos en Linux |
| [vulnerability-assessment-red-hospital](#) | Escaneo y priorización de vulnerabilidades |

📍 Arequipa, Perú · 🔗 LinkedIn: **[tu enlace]** · ✉️ **[tu correo profesional]**

---

## Repos a crear

### 1. `incident-report-ransomware-clinica`
**Qué es:** informe de un incidente simulado (ransomware en una clínica) siguiendo las fases de NIST: preparación, detección, contención, erradicación, recuperación y lecciones aprendidas.
**Contenido:** `informe.md`, `linea-de-tiempo.md`, `indicadores-de-compromiso.csv`, `plan-de-comunicacion.md`.
**Por qué importa:** en salud, un incidente afecta atención al paciente. Incluye impacto operativo, no solo técnico.

### 2. `risk-assessment-hospital-regional`
**Qué es:** evaluación de riesgos de una red hospitalaria genérica (no uses datos reales del GORE ICA).
**Contenido:** inventario de activos, matriz probabilidad × impacto, controles recomendados, mapeo a NIST CSF e ISO 27001, nota sobre Ley 29733 para datos de pacientes.
**Entregable visual:** matriz de riesgo en imagen y tabla en Markdown.

### 3. `python-lista-acceso-automatizada`
**Qué es:** script que lee una lista de IPs o usuarios permitidos, elimina los que están en una lista de revocados y actualiza el archivo.
**Contenido:** `actualizar_acceso.py`, `allow_list.txt`, `revocados.txt`, `tests/`.
**Detalle que suma:** manejo de errores y registro (logging) de cada cambio.

### 4. `sql-filtrado-logs-seguridad`
**Qué es:** consultas SQL para investigar intentos de login fallidos, accesos fuera de horario y equipos de un área específica.
**Contenido:** `consultas.sql`, `datos_ejemplo.csv` (sintéticos), explicación de cada consulta.

### 5. `wireshark-analisis-trafico`
**Qué es:** análisis de una captura de red para identificar tráfico sospechoso (escaneo de puertos, DNS anómalo, credenciales en texto plano).
**Contenido:** capturas de pantalla con filtros usados, hallazgos y recomendaciones. Usa un `.pcap` público o generado por ti, nunca de una red real de cliente.

### 6. `linux-auditoria-permisos`
**Qué es:** guía y script en Bash que revisa permisos de archivos y directorios sensibles y propone correcciones con `chmod` y `chown`.
**Contenido:** `auditar_permisos.sh`, ejemplos antes y después, principio de mínimo privilegio explicado.

### 7. `vulnerability-assessment-red-hospital`
**Qué es:** informe de escaneo de vulnerabilidades en un laboratorio propio (máquinas virtuales), con priorización por severidad (CVSS).
**Contenido:** resumen ejecutivo, hallazgos, plan de remediación por prioridad.
**Herramienta:** **[confirmar: OpenVAS, Nessus Essentials u otra]**

---

## Plantilla de README para cada repo

```markdown
# Nombre del proyecto

## Contexto
Qué problema se resuelve y en qué escenario (1 o 2 frases).

## Qué hice
- Paso 1
- Paso 2
- Paso 3

## Herramientas
`Python` `SQL` `Wireshark`

## Resultados
Hallazgos, capturas o métricas. Ejemplo: "Identifiqué 12 intentos de login fallidos desde 3 IPs".

## Recomendaciones
Qué se debería corregir y en qué orden.

## Cómo reproducirlo
Pasos para correr el script o repetir el análisis.

## Aprendizajes
Qué mejorarías si lo repitieras.
```

---

## Antes de publicar

1. **Confidencialidad:** no subas nombres de postas, IPs, planos, presupuestos ni informes oficiales del GORE ICA ni de clientes de Mercurio. Usa datos sintéticos o laboratorio propio.
2. **Cada repo con una captura o resultado visible.** Un repo con solo código convence poco.
3. **Fija (pin) los 6 mejores** en tu perfil de GitHub.
4. **Commits claros y en orden**, no un solo commit gigante.
