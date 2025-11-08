# CAMA Simulator — Cost, Income & Auto Method

**CAMA Simulator** es un proyecto (notebook-first) que estima el valor de mercado usando lógica de **avaluación masiva (CAMA)**. Implementa:
- **Enfoque por Costos (RCNLD)**
- **Enfoque por Ingresos (Cap Rate)** y **EGIM**
- **PSF proxy** (precio por ft²)
- Un **auto-selector** que elige el método óptimo según los datos disponibles

> Ideal para pruebas, docencia y prototipos de *Computer Assisted Mass Appraisal*.

---

## ✨ Características
- **Cost**: Replacement Cost New – Depreciación + Terreno
- **Income (Direct Cap)**: `value = NOI / cap_rate`
- **EGIM**: `value = EGI × EGIM`
- **PSF**: `value = bldg_sf × market_psf`
- **Auto-selector** de método según columnas presentes
- Vectorizable con **pandas/numpy**; resultados listos para BI

---
En el simulador final, solo debes ingresar diferentes parámetros. 

1. PropertyType
2. Submarket [Downtown/Suburban/Airport]
3. GBA_SF
4. YearBuilt
5. MarketRent_perSF
6. OccupancyRate
7. ExpenseRatio
8. NOI
9. CapRate (%)
10. Land_SF
11. SiteImpr_Dep

Al final, el simulador buscará el approach adecuado y dará el valor avaluado según CAMA.
## 📦 Requisitos
- Python 3.10+
- Paquetes: `pandas`, `numpy`, `plotly` (opcional), `dataclasses`, `typing`

Instalación rápida:
```bash
pip install pandas numpy plotly
