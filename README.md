# Harveston Solar Radiation Forecasting

**Team RainMakers**  
*Data_Crunch_025 | University of Moratuwa*

---

## 🌟 Key Innovations

1. **Geospatial Group Forecasting**  
   - 23 region-specific models based on latitude/longitude clusters  
   - Shared architecture with group-wise normalization

2. **Hybrid Prediction System**  
   - Combines deep learning patterns with physical constraints  
   - Integrates seasonal baselines and noise-controlled projections

3. **Agricultural-Focused Features**  
   - Wind impact vectors (North/East components)  
   - Dry spell duration tracking  
   - Clear sky radiation benchmarks

---

## 🚀 Core Features

- 7-day radiation forecasts for 23 regions  
- Temporal attention on critical weather patterns  
- Stability-enhanced predictions via:  
  - 5-day smoothing windows  
  - Outlier-resilient preprocessing  
  - Cyclical time encoding

---

## 📥 Installation & Usage

1. Install dependencies:  
   `pip install -r requirements.txt`  
2. Train region-specific models:  
   `python train.py --groups [1-23]`  
3. Generate forecasts:  
   `python predict.py --date [YYYY-MM-DD]`

---

## 🌱 Agricultural Impact

- Optimize protective cover deployment  
- Compare regional radiation trends  
- Plan solar-dependent operations  

*MIT Licensed | Maintained by Team RainMakers*
