# Portafolio GitHub: Análisis de Datos

> Cómo usarlo: crea un repositorio público con el mismo nombre que tu usuario de GitHub y pega la sección "README de perfil" como README.md. Luego crea cada repo de la lista y usa la plantilla del final.
> Lo marcado con **[confirmar]** debes validarlo antes de publicar.

---

## README de perfil

# Hola, soy Germán León Galdos 👋

Administrador de Redes y Comunicaciones que convierte datos de campo en decisiones. Trabajo con información de infraestructura de telecomunicaciones en hospitales y postas de salud de la región Ica, Perú: consolido, limpio, valido y presento datos para informes técnicos y toma de decisiones.

### Qué hago
- Limpieza y consolidación de datos desde Excel y JSON
- Dashboards con indicadores (KPI) por provincia y por sede
- Validación y auditoría de presupuestos y metrados
- Análisis de disponibilidad de red a partir de métricas de monitoreo

### Herramientas
`Python` `pandas` `openpyxl` `Excel avanzado` `SQL` `Zabbix`
**[confirmar: Power BI, Power Query, matplotlib, plotly u otras que uses]**

### Proyectos destacados
| Repo | Qué demuestra |
|---|---|
| [dashboard-conectividad-postas](#) | Dashboard con KPI por provincia |
| [cruce-datos-clave-compuesta](#) | Unión de datos con duplicados |
| [auditoria-precios-unitarios](#) | Validación entre múltiples sedes |
| [analisis-disponibilidad-zabbix](#) | Métricas de red (uptime, tiempo de reparación) |
| [generador-etiquetas-cableado](#) | Automatización con estándar TIA-606-B |
| [etl-excel-json](#) | Limpieza y normalización de datos |

📍 Arequipa, Perú · 🔗 LinkedIn: **[tu enlace]** · ✉️ **[tu correo profesional]**

---

## Repos a crear

> Todos con **datos sintéticos** que imiten la estructura real. No subas datos del GORE ICA ni de clientes.

### 1. `dashboard-conectividad-postas`
**Problema:** consolidar el estado de conectividad de más de 100 establecimientos en cinco provincias para saber dónde actuar primero.
**Solución:** script que lee un Excel de visitas, calcula indicadores por provincia (porcentaje con internet, proveedor, estado del equipo) y genera un dashboard.
**Contenido:** `datos_sinteticos.xlsx`, `generar_dashboard.py`, captura del resultado.
**Resultado a mostrar:** tabla resumen por provincia y gráfico de barras.

### 2. `cruce-datos-clave-compuesta`
**Problema:** al cruzar dos tablas por nombre de establecimiento, los nombres repetidos en distintas provincias mezclaban datos.
**Solución:** clave compuesta (provincia + nombre normalizado) y validación de relación uno a uno.

```python
import pandas as pd

def clave(df):
    return df["provincia"].str.strip().str.upper() + "|" + df["establecimiento"].str.strip().str.upper()

a["clave"], b["clave"] = clave(a), clave(b)
resultado = a.merge(b[["clave", "cantidad"]], on="clave", how="left", validate="one_to_one")
```

**Detalle que suma:** reporte de filas sin coincidencia, para revisarlas a mano.

### 3. `auditoria-precios-unitarios`
**Problema:** garantizar que los precios unitarios sean iguales entre varias sedes y que las diferencias estén justificadas.
**Solución:** script que compara partidas entre libros de presupuesto y marca desviaciones.
**Contenido:** `comparar_presupuestos.py`, ejemplo con partidas ficticias, reporte de discrepancias en Excel.

### 4. `analisis-disponibilidad-zabbix`
**Problema:** saber qué sedes fallan más y cuánto tardan en recuperarse.
**Solución:** análisis de eventos exportados (CSV o JSON) para calcular disponibilidad porcentual, número de caídas y tiempo medio de reparación por sede.
**Contenido:** `eventos_ejemplo.json`, `analisis.py`, gráficos de disponibilidad.
**[confirmar]:** si exportas desde la API de Zabbix o desde la interfaz.

### 5. `generador-etiquetas-cableado`
**Problema:** etiquetar cientos de puntos de red de forma consistente.
**Solución:** generador de etiquetas con el formato `[SEDE]-[GDS-ID]-[SW##]-[##PS]-[J##]`, alineado a TIA-606-B, que produce un libro de Excel listo para imprimir.
**Contenido:** `generar_etiquetas.py`, plantilla de entrada, libro de salida de ejemplo.

### 6. `etl-excel-json`
**Problema:** datos de varias fuentes con formatos distintos.
**Solución:** pipeline que lee Excel y JSON, normaliza nombres y fechas, elimina duplicados y exporta un archivo limpio.
**Contenido:** `etl.py`, datos de ejemplo, pruebas básicas con `pytest`.

---

## Plantilla de README para cada repo

```markdown
# Nombre del proyecto

## Problema
Qué había que resolver y por qué importaba (1 o 2 frases).

## Datos
Origen y estructura (sintéticos, imitan el caso real).

## Solución
- Paso 1
- Paso 2
- Paso 3

## Herramientas
`Python` `pandas` `openpyxl`

## Resultados
Captura del dashboard o tabla final. Si puedes, una métrica: "Reduje de 2 horas a 5 minutos la consolidación mensual".

## Cómo reproducirlo
pip install -r requirements.txt
python script.py

## Aprendizajes
Qué mejorarías.
```

---

## Antes de publicar

1. **Confidencialidad:** nada de nombres reales de postas, informes oficiales ni presupuestos del GORE ICA o de clientes. Datos sintéticos con la misma estructura.
2. **Una métrica por proyecto.** Horas ahorradas o errores evitados, solo si son reales **[confirmar]**.
3. **Captura de resultado en cada README.** Quien revise tu perfil no va a correr tu código.
4. **Incluye `requirements.txt`** y datos de ejemplo para que cualquiera pueda reproducirlo.
