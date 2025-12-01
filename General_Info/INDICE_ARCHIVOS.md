# 📂 Índice de Archivos - Trading View Scripts

**Directorio Raíz**: `d:\martin\Trading view`  
**Fecha**: 2025-12-01  
**Estructura**: Organizada por Estrategias

---

## 1. 🟢 IFVG Strategy (Inversion Fair Value Gaps)
Carpeta: `\IFVG_Strategy\`

### **Scripts (`\Scripts`)**
| Archivo | Descripción | Estado |
|---------|-------------|--------|
| **`IFVG_ULTIMATE.pine`** ⭐ | **SUITE DEFINITIVA**. Integra: IFVG + EMAs + Dynamic Heatmap/VP + Señales de Liquidación. | ✅ **USAR ESTE** |
| `IFVG_PRO.pine` | Versión anterior (Solo IFVG + Heatmap). | ⚠️ Alternativa |
| `IFVG_2.0_CLEAN.pine` | Versión ligera (Solo IFVG). | ℹ️ Ligero |
| `Dynamic heatmap.pine` | Componente Heatmap standalone (v6). | ℹ️ Componente |

### **Documentación (`\Documentation`)**
| Archivo | Contenido |
|---------|-----------|
| `IFVG_PRO_RESUMEN.md` | Guía rápida y resumen ejecutivo. |
| `ANALISIS_MATEMATICO.md` | Análisis de fórmulas y optimización. |
| `IFVG_2.0_DOCUMENTACION.md` | Manual completo de usuario. |
| `IFVG_2.0_VERIFICACION.md` | Reporte de validación de código. |
| `IFVG_CARACTERES_ESPECIALES.md` | Nota técnica sobre tildes en Pine. |
| `ANALISIS_*.md` | Otros análisis técnicos. |

### **Legacy (`\Legacy`)**
*Contiene versiones antiguas (`IFVG 2.0`, `IFVG.pine`, etc.) que no se deben usar.*

---

## 2. 🔵 Smart Signals Strategy
Carpeta: `\Smart_Signals_Strategy\`

### **Scripts (`\Scripts`)**
| Archivo | Descripción | Estado |
|---------|-------------|--------|
| **`smart_signals_assistant.pine`** | Asistente de señales completo (EMAs, ADX). | ✅ Listo |
| `liquid.pine` | Señales de reversión por liquidación (Integrado en IFVG Ultimate). | ℹ️ Componente |

### **Documentación (`\Documentation`)**
| Archivo | Contenido |
|---------|-----------|
| `VERIFICATION_REPORT.md` | Reporte de verificación del script. |

---

## 3. 🟠 Volume Profile Strategy
Carpeta: `\Volume_Profile_Strategy\`

### **Scripts (`\Scripts`)**
| Archivo | Descripción |
|---------|-------------|
| `VP.pine` | Volume Profile estándar. |
| `Volumen-profile.pine` | Versión alternativa. |

---

## 4. 🟣 Otras Estrategias
Carpeta: `\Other_Strategies\`

| Archivo | Descripción |
|---------|-------------|
| `STRAT-Comb.pine` | Estrategia combinada (The Strat). |
| `Estacionalidad.pine` | Análisis de estacionalidad. |
| `SGT_PROFESSIONAL.pine` | SGT Professional script. |
| `tradingview_script_corrected.pine` | Script corregido misceláneo. |

---

## 5. ℹ️ Información General
Carpeta: `\General_Info\`

| Archivo | Descripción |
|---------|-------------|
| `INDICE_ARCHIVOS.md` | **Este archivo**. Mapa del proyecto. |
| `Readme.md` | Información general del repositorio. |
| `CLAUDE.md` | Guía de uso del asistente. |

---

## 🚀 Recomendación de Uso

1.  **Para Análisis Completo (Institucional)**: Ve a `IFVG_Strategy\Scripts` y usa **`IFVG_ULTIMATE.pine`**. Es la herramienta más potente que incluye Gaps, Tendencia, Liquidez Dinámica y Señales de Reversión.
2.  **Para Señales Simples**: Ve a `Smart_Signals_Strategy\Scripts` y usa `smart_signals_assistant.pine`.
3.  **Para leer guías**: Revisa la carpeta `Documentation` dentro de cada estrategia.

---
**Organización completada el 2025-12-01**
