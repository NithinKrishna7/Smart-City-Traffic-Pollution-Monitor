# Real-Time Multimodal Urban Air Quality Visualization and Anomaly Prediction System

A comprehensive real-time dashboard for monitoring urban air quality across Tamil Nadu with advanced forecasting, anomaly detection, and explainable AI capabilities. This project integrates multiple data sources, machine learning models, and novel visualization techniques to deliver actionable insights for smart city development and public health.

## 🌟 Key Features

### 1. **Real-Time Multi-Pollutant Monitoring**
- Live data ingestion from OpenWeatherMap API (PM2.5, PM10, NO₂, SO₂, CO, O₃)
- Multi-pollutant spatio-temporal visualization
- Dynamic updates with configurable refresh intervals
- Fallback to simulated data when API is unavailable

### 2. **Prophet Forecasting Models**
- Time-series forecasting using pre-trained Prophet models
- 7-14 day air quality predictions
- Confidence intervals and trend analysis
- City-specific models for accurate predictions

### 3. **Isolation Forest Anomaly Detection**
- Real-time anomaly detection using Isolation Forest
- Anomaly scoring and severity classification
- Visual anomaly heatmaps
- Alert system for unusual pollution patterns

### 4. **Explainable AI (SHAP/LIME)**
- Feature importance analysis
- SHAP values for model interpretability
- LIME explanations for predictions
- Visual explanations of influential pollutants

### 5. **Pollution Sensitivity Index (PSI)**
- Novel health-based pollution index
- Public health interpretation and recommendations
- Risk categorization (Low, Moderate, High, Very High)
- Actionable health guidance

### 6. **Advanced Visualizations**
- **Spatio-Temporal Evolution**: Animated pollution flow across regions
- **Pollutant Flow Vectors**: Visual representation of pollution movement
- **Multi-Pollutant Comparison**: Side-by-side pollutant analysis
- **Anomaly Heatmaps**: Temporal anomaly patterns
- **Forecast Charts**: Predictive visualizations with confidence bands

### 7. **Geographic Coverage**
- 15 major Tamil Nadu districts
- Real-time monitoring for each location
- Interactive maps with multiple visualization modes
- Choropleth and heatmap representations

## 🚀 Installation

```bash
# Clone the repository
git clone <repository-url>
cd Smart-City-Traffic-Pollution-Monitor-main

# Install dependencies
pip install -r requirements.txt

# Ensure models are in the models/ directory
# - Prophet models: prophet_*.pkl
# - Isolation Forest: isolation_forest.pkl

# Run the application
streamlit run main.py
```

## 📋 Requirements

### Core Dependencies
- `streamlit` - Web framework
- `pandas`, `numpy` - Data processing
- `plotly` - Interactive visualizations
- `folium` - Geospatial mapping
- `requests` - API integration
- `prophet` - Time-series forecasting
- `scikit-learn` - Machine learning (Isolation Forest)

### Optional Dependencies
- `shap` - SHAP explainability
- `lime` - LIME explainability

### API Configuration
The application uses OpenWeatherMap Air Pollution API. Update the `API_KEY` in `main.py`:
```python
API_KEY = "your-api-key-here"
```

## 🎯 Usage

### Dashboard Pages

1. **Dashboard** 📊
   - Real-time AQI and multi-pollutant monitoring
   - Current PSI and health recommendations
   - Anomaly alerts
   - Recent trends

2. **Multi-Pollutant View** 🌬️
   - Spatio-temporal pollutant distribution
   - Multi-pollutant comparison charts
   - Interactive pollutant selection

3. **Forecasting** 🔮
   - Prophet-based air quality forecasts
   - Confidence intervals
   - Trend analysis
   - Forecast summaries

4. **Anomaly Detection** ⚠️
   - Real-time anomaly identification
   - Anomaly scoring
   - Temporal anomaly patterns
   - Anomaly statistics

5. **Explainable AI** 🤖
   - Feature importance analysis
   - SHAP/LIME explanations
   - Top contributor identification

6. **Spatio-Temporal** 🗺️
   - Animated pollution evolution
   - Time-lapse visualizations
   - Regional pollution movement

7. **Pollution Flow** 🌊
   - Flow vectors between cities
   - Pollution transport visualization
   - Inter-city pollution patterns

8. **Health Index** 🏥
   - PSI calculation and mapping
   - Health risk categorization
   - City-wise PSI ranking
   - Health recommendations

9. **Traffic Heatmap** 🔥
   - Traffic density visualization
   - Congestion hotspots

10. **Time Trends** 📈
    - Historical time-series analysis
    - Multi-pollutant trends

## 🔬 Novelty Components

### 1. Dual-Stage Prediction Architecture
- **Stage 1**: Prophet forecasting for future trends
- **Stage 2**: Isolation Forest for anomaly detection
- Combined insights for comprehensive air quality intelligence

### 2. Pollution Sensitivity Index (PSI)
- Novel health-based metric combining multiple pollutants
- Weighted by health impact (PM2.5 and PM10 prioritized)
- Public health interpretation and recommendations

### 3. Dynamic Multi-Pollutant Spatio-Temporal Visualization
- Real-time multi-pollutant mapping
- Animated pollution flow
- Temporal evolution patterns

### 4. Explainable Visualization
- SHAP/LIME integration for model interpretability
- Feature importance visualization
- Transparent AI decision-making

### 5. Animated Pollutant Flow Vectors
- Visual representation of pollution transport
- Inter-city pollution flow patterns
- Flow strength visualization

## 📊 Model Architecture

### Prophet Models
- Pre-trained models for major cities
- Handles seasonality, trends, and holidays
- Provides uncertainty estimates

### Isolation Forest
- Unsupervised anomaly detection
- Handles multi-dimensional pollutant data
- Configurable contamination rate

### Explainability
- SHAP: Shapley Additive Explanations
- LIME: Local Interpretable Model-agnostic Explanations
- Feature importance ranking

## 🎨 Visualization Techniques

1. **Interactive Maps**: Folium and Plotly Mapbox
2. **Time-Series Charts**: Plotly with dual y-axes
3. **Heatmaps**: Temporal and spatial heatmaps
4. **Bar Charts**: Multi-pollutant comparisons
5. **Scatter Plots**: Correlation analysis
6. **Animated Visualizations**: Time-lapse pollution evolution
7. **Flow Vectors**: Pollution transport visualization

## 🔧 Configuration

### API Settings
- Update `API_KEY` in `main.py`
- Configure API endpoints if needed
- Set fallback behavior for API failures

### Model Settings
- Prophet models: `models/prophet_*.pkl`
- Isolation Forest: `models/isolation_forest.pkl`
- Model loading is cached for performance

### Refresh Settings
- Auto-refresh toggle in sidebar
- Configurable refresh interval (5-60 seconds)
- Manual refresh available

## 📈 Expected Outputs

1. **Real-Time AQI Dashboard**: Live multi-pollutant monitoring
2. **Predictive Charts**: Forecast visualizations with confidence bands
3. **Anomaly Heatmaps**: Temporal anomaly patterns
4. **Spatio-Temporal Animations**: Pollution evolution over time
5. **Explainable ML Insights**: Feature importance and explanations
6. **Health Recommendations**: PSI-based public health guidance

## 🎓 Research Applications

This system supports research publication with:
- Comparative analysis of forecasting models
- Novel PSI metric for public health
- Dual-stage prediction architecture
- Explainable AI integration
- Comprehensive visualization techniques

## 🤝 Contributing

Contributions are welcome! Please ensure:
- Code follows PEP 8 style guidelines
- New features include documentation
- Models are properly saved and loaded
- API keys are not committed

## 📝 License

[Specify your license here]

## 🙏 Acknowledgments

- OpenWeatherMap for air quality API
- Prophet by Facebook for time-series forecasting
- SHAP and LIME for explainability
- Streamlit for the web framework

## 📧 Contact

[Your contact information]

---

**Last Updated**: 2024
**Version**: 2.0 - Enhanced with Forecasting, Anomaly Detection, and Explainable AI
