# 🚗 Car Price Prediction System

A comprehensive Machine Learning-based web application for predicting car prices based on various parameters like brand, model, year, fuel type, distance travelled, and city.

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Dataset Information](#dataset-information)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Machine Learning Model](#machine-learning-model)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Project Overview

This project is a Django-based web application that uses Machine Learning to predict car prices. It provides an intuitive interface where users can input car specifications and receive accurate price predictions based on a trained ML model.

### Key Highlights
- **5,175+ car records** from various brands and models
- **Real-time price prediction** using trained ML model
- **Responsive web interface** optimized for all devices
- **Professional design** with modern UI/UX
- **Form validation** with real-time feedback

## ✨ Features

### 🎨 User Interface
- **Modern Design**: Professional gradient backgrounds and clean layouts
- **Responsive Layout**: Optimized for desktop, tablet, and mobile devices
- **Interactive Forms**: Real-time validation and error handling
- **Visual Feedback**: Success/error states with color-coded indicators

### 🔧 Functionality
- **Car Brand Selection**: 31 unique car brands with count information
- **Model Selection**: 168+ car models across different brands
- **Year Range**: Support for cars from 1990-2021
- **Fuel Types**: Petrol, Diesel, CNG + 1, Hybrid, Petrol + 1
- **City Selection**: 15 major Indian cities
- **Distance Input**: Kilometers travelled (0-500,000 range)

### 📊 Data Management
- **CSV Dataset**: Comprehensive car data with 7 columns
- **Dynamic Dropdowns**: Populated with actual dataset values
- **Data Validation**: Input validation and error handling
- **Real-time Updates**: Form updates based on user input

## 🛠️ Technology Stack

### Backend
- **Python 3.x**
- **Django 4.x** - Web framework
- **scikit-learn** - Machine Learning library
- **pandas** - Data manipulation
- **numpy** - Numerical computing

### Frontend
- **HTML5** - Semantic markup
- **CSS3** - Styling and animations
- **JavaScript** - Interactive functionality
- **jQuery** - DOM manipulation
- **Responsive Design** - Mobile-first approach

### Database
- **SQLite** - Development database
- **CSV Files** - Data storage and ML training

### Machine Learning
- **Joblib** - Model serialization
- **Pickle** - Model storage
- **Supervised Learning** - Regression model

## 📊 Dataset Information

### Dataset Overview
- **Total Records**: 5,175 cars
- **Columns**: 7 features
- **Year Range**: 1990-2021
- **Geographic Coverage**: 15 major Indian cities

### Data Columns
1. **year** - Manufacturing year (1990-2021)
2. **brand** - Car brand (31 unique brands)
3. **model_name** - Car model (168+ models)
4. **price** - Car price in INR
5. **distance_travelled(kms)** - Kilometers driven
6. **fuel_type** - Fuel type (5 types)
7. **city** - City location (15 cities)

### Popular Brands
- Maruti Suzuki (221 cars)
- Hyundai (214 cars)
- Honda (117 cars)
- Mercedes-Benz (107 cars)
- Toyota (88 cars)
- BMW (79 cars)
- Audi (72 cars)

## 🚀 Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Git (for cloning)

### Step-by-Step Installation

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd car-price-prediction
   ```

2. **Create Virtual Environment**
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Database Setup**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Run the Application**
   ```bash
   python manage.py runserver
   ```

6. **Access the Application**
   Open your browser and navigate to `http://127.0.0.1:8000/`

## 📱 Usage

### 1. Access the Application
- Navigate to the car price prediction page
- You'll see a professional form interface

### 2. Fill the Form
- **Select Brand**: Choose from 31 available car brands
- **Select Model**: Pick from available models for the selected brand
- **Enter Year**: Input manufacturing year (1990-2021)
- **Select Fuel Type**: Choose fuel type (Petrol/Diesel/CNG/Hybrid)
- **Enter Distance**: Input kilometers travelled (0-500,000)
- **Select City**: Choose from 15 major Indian cities

### 3. Get Prediction
- Click "🔮 Predict Price" button
- View the predicted car price in INR
- Results are displayed in a professional format

### 4. Form Validation
- All fields are required
- Real-time validation feedback
- Error messages for invalid inputs
- Success states for valid inputs

## 📁 Project Structure

```
carpredict/
├── car_data.csv                 # Dataset file
├── car_price_prediction.pkl     # Trained ML model
├── manage.py                    # Django management script
├── db.sqlite3                   # SQLite database
├── carpredict/                  # Django project settings
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── predict/                     # Main Django app
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── static/                  # Static files
│   │   ├── css/
│   │   ├── image/
│   │   └── scripts.js
│   └── templates/               # HTML templates
│       ├── car_price_prediction.html
│       ├── home.html
│       ├── login.html
│       └── signup.html
└── ml_model/                    # ML model files
    ├── car_data.csv
    └── car_price_prediction.pkl
```

## 🔌 API Endpoints

### Main Endpoints
- **Home**: `/` - Landing page
- **Car Price Prediction**: `/predict/` - Main prediction form
- **Login**: `/login/` - User authentication
- **Signup**: `/signup/` - User registration

### API Response Format
```json
{
    "predicted_price": 850000,
    "status": "success"
}
```

## 🤖 Machine Learning Model

### Model Details
- **Algorithm**: Regression-based prediction
- **Features**: 6 input parameters
- **Output**: Car price in INR
- **Training Data**: 5,175 car records
- **Model Format**: Pickle (.pkl) file

### Feature Engineering
- Year normalization
- Brand encoding
- Model encoding
- Fuel type encoding
- City encoding
- Distance scaling

### Model Performance
- **Accuracy**: Optimized for Indian car market
- **Training**: Supervised learning approach
- **Validation**: Cross-validation techniques
- **Deployment**: Production-ready model

## 📸 Screenshots

### Desktop View
- Professional form layout
- Gradient background design
- Responsive grid system

### Mobile View
- Mobile-optimized interface
- Touch-friendly inputs
- Adaptive typography

### Form Validation
- Real-time error feedback
- Success state indicators
- Professional styling

## 🤝 Contributing

We welcome contributions to improve this project! Here's how you can help:

### Contribution Guidelines
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Areas for Improvement
- Enhanced ML model accuracy
- Additional car brands/models
- More prediction features
- UI/UX improvements
- Performance optimization

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

If you have any questions or need support:

- **Issues**: Create an issue on GitHub
- **Documentation**: Check the project wiki
- **Contact**: Reach out to the development team

## 🙏 Acknowledgments

- **Dataset Sources**: Car market data collection
- **ML Libraries**: scikit-learn community
- **Web Framework**: Django development team
- **UI Components**: Modern web design inspiration

---

**Made with ❤️ for the Indian car market**

*This project demonstrates the power of Machine Learning in real-world applications, providing accurate car price predictions to help users make informed decisions.*

