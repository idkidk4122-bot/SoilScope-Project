# 🌱 SoilScope - NASA-Powered Agricultural Intelligence

![SoilScope](https://img.shields.io/badge/SoilScope-NASA%20Powered-green)
![Flask](https://img.shields.io/badge/Backend-Flask-blue)
![Google Earth Engine](https://img.shields.io/badge/Satellite%20Data-Google%20Earth%20Engine-orange)
![Real-time](https://img.shields.io/badge/Data-Real--time-brightgreen)

A comprehensive agricultural intelligence platform that leverages NASA satellite data and Google Earth Engine to provide real-time soil, water, and air analysis for farmers and agricultural professionals.

## 🛰️ Features

### 🌍 Real-time Satellite Data Integration
- **NDVI Analysis** - Vegetation health monitoring using Sentinel-2 satellite imagery
- **Soil Moisture Tracking** - Surface and root zone moisture levels
- **Climate Data** - Temperature, precipitation, and humidity from NASA POWER
- **Live Map Integration** - Interactive farm location mapping

### 📊 Advanced Analytics
- **Soil Health Dashboard** - pH levels, organic matter, and nutrient analysis
- **Water Quality Monitoring** - TDS, nitrates, and bacterial quality
- **Air Quality Index** - Real-time environmental conditions
- **Crop Recommendations** - AI-powered crop suggestions based on soil conditions

### 🤖 AI Assistant
- **CropLens AI** - Intelligent agricultural assistant
- **Real-time Q&A** - Get answers to farming questions
- **NASA Data Insights** - Satellite-enhanced recommendations

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Google Earth Engine Account
- Sentinel-2 Data Access

### Backend Setup

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/soilsope.git
cd soilscope
```

2. **Set up Python environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Set up Google Earth Engine**
```bash
# Download service account key file and save as service-account.json
earthengine authenticate
```

5. **Configure environment variables**
```bash
export GEE_KEYFILE="service-account.json"
export FLASK_ENV=development
```

6. **Run the backend server**
```bash
python server.py
```
Backend will run on `http://localhost:8080`

### Frontend Setup

1. **Serve the frontend**
```bash
# Using Python HTTP server
python -m http.server 8000

# Or using Node.js serve
npx serve .
```

2. **Open your browser**
```
http://localhost:8000
```

## 📁 Project Structure

```
soilscope/
├── server.py                 # Flask backend with GEE integration
├── service-account.json      # Google Earth Engine credentials
├── index.html               # Main frontend application
├── requirements.txt         # Python dependencies
└── README.md               # This file
```

## 🔧 API Endpoints

### Satellite Data Endpoints
- `GET /api/ndvi?lat={lat}&lng={lng}` - Get NDVI vegetation index
- `GET /api/soil-moisture?lat={lat}&lng={lng}` - Soil moisture data
- `GET /api/climate?lat={lat}&lng={lng}` - Climate and weather data
- `GET /api/health` - Service health check

### Example API Call
```javascript
// Fetch NDVI data for a location
const response = await fetch('/api/ndvi?lat=40.7128&lng=-74.0060');
const data = await response.json();
console.log(data.ndvi_value); // 0.72
```

## 🛠️ Technology Stack

### Backend
- **Flask** - Python web framework
- **Google Earth Engine** - Satellite data processing
- **Sentinel-2** - European satellite imagery
- **NASA POWER** - Climate data API

### Frontend
- **HTML5/CSS3** - Responsive design
- **JavaScript ES6+** - Interactive features
- **Chart.js** - Data visualization
- **Google Maps API** - Location services
- **Tailwind CSS** - Modern UI components

### Data Sources
- 🌍 **Sentinel-2** - High-resolution satellite imagery
- 🔬 **NASA POWER** - Climate and solar data
- 💧 **Soil Moisture** - Agricultural hydration data
- 🌡️ **Weather Data** - Real-time environmental conditions

## 🌟 Key Features

### Real-time Monitoring
- Live NDVI vegetation indices
- Current soil moisture levels
- Environmental condition tracking
- Historical data comparison

### Smart Analytics
- Crop suitability analysis
- Growth stage monitoring
- Yield prediction models
- Pest and disease risk assessment

### User Experience
- Dark/Light theme toggle
- Responsive mobile design
- Interactive data visualizations
- Intuitive farm management

## 📊 Sample Data Output

```json
{
  "ndvi_value": 0.72,
  "vegetation_health": "Excellent",
  "surface_moisture": 0.38,
  "temperature": 24.5,
  "crop_recommendation": "Corn (94% match)"
}
```

## 🎯 Use Cases

- **Precision Agriculture** - Data-driven farming decisions
- **Crop Monitoring** - Real-time growth tracking
- **Resource Optimization** - Efficient water and fertilizer use
- **Yield Prediction** - Data-informed harvest forecasts
- **Environmental Compliance** - Sustainable farming practices

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **NASA** - For satellite data and POWER API
- **Google Earth Engine** - For geospatial data processing
- **European Space Agency** - For Sentinel-2 imagery
- **Flask Community** - For the excellent web framework

## 📞 Support

For support and questions:
- 📧 Email: araadh3111@gmail.com
- 📍 Location: Nagala, Zirakpur, Punjab, India
- 📱 Phone: +91 62841 59714

## 🚀 Deployment

### Production Deployment
```bash
# Set production environment
export FLASK_ENV=production
export GEE_KEYFILE="/path/to/service-account.json"

# Run with production server
gunicorn -w 4 -b 0.0.0.0:8080 server:app
```

### Docker Deployment
```dockerfile
FROM python:3.9-slim
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
EXPOSE 8080
CMD ["python", "server.py"]
```

---

<div align="center">

**Built with ❤️ for the future of agriculture**

*Empowering farmers with NASA satellite technology*

</div>
