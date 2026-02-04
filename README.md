# 🛒 Grocea

**Smart grocery and meal planning assistant based on your actual purchases.**

Grocea transforms your grocery receipts into actionable meal planning by understanding what you buy, suggesting recipes based on available ingredients, tracking pantry inventory, and helping reduce food waste and overspending.

<!-- [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) -->

---

## 📱 What is Grocea?

Grocea is a receipt-based meal planning application that solves the age-old question: **"What's for dinner?"** by using real data from your shopping history.

### The Problem
- Food waste from forgotten ingredients
- Overspending on groceries
- Difficulty planning meals with what you have
- Not knowing when staples will run out

### The Solution
- **Scan receipts** to automatically track purchases
- **Get recipe suggestions** based on current pantry inventory
- **Reduce food waste** with expiry tracking and smart recommendations
- **Forecast stock levels** to know when to restock staples
- **Track spending** with price-per-meal analytics

---

## 🎯 Key Features

- **📸 Receipt Scanning**: OCR-powered receipt scanning with automatic item normalisation
- **🍳 Smart Recipe Recommendations**: Personalised suggestions based on available ingredients, dietary restrictions, and cooking preferences
- **📦 Pantry Management**: Real-time inventory tracking with automatic stock updates
- **📊 Usage Forecasting**: Predict when staples will run out using time-series analysis
- **⏰ Expiry Tracking**: Get notifications for items approaching expiry dates
- **💰 Cost Analytics**: Track price-per-meal and identify spending patterns
- **✍️ Custom Recipes**: Create personal recipes with NLP-powered ingredient extraction

---

## 🏗️ Project Architecture

```
┌─────────────────┐
│  Mobile App     │  React Native / Flutter
│  (iOS/Android)  │
└────────┬────────┘
         │
         │ REST API
         ▼
┌─────────────────┐
│  Backend API    │  FastAPI (Python)
│  Server         │
└────────┬────────┘
         │
         ├──────────┬──────────┬──────────┐
         ▼          ▼          ▼          ▼
    ┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐
    │Database│ │ Object │ │   ML   │ │ Cache  │
    │        │ │Storage │ │Services│ │        │
    │Postgres│ │   S3   │ │        │ │ Redis  │
    └────────┘ └────────┘ └────────┘ └────────┘
```

---

## 📦 Repositories

This organisation contains the following repositories:

### 🔧 Core Application
| Repository | Description | Tech Stack |
|------------|-------------|------------|
| [**grocea-mobile**](https://github.com/grocea-app/grocea-mobile) | iOS and Android mobile application | React Native, Redux, TypeScript |
| [**grocea-backend**](https://github.com/grocea-app/grocea-backend) | RESTful API server and business logic | FastAPI, Python, PostgreSQL |
| [**grocea-ml**](https://github.com/grocea-app/grocea-ml) | Machine learning models and training pipelines | Python, TensorFlow, scikit-learn |

### 🚀 Infrastructure & Deployment (in consideration)
| Repository | Description | Tech Stack |
|------------|-------------|------------|
| [**grocea-infrastructure**](https://github.com/grocea-app/grocea-infrastructure) | Infrastructure as Code and deployment configs | Terraform, Docker, Kubernetes |

---

## 🤖 Machine Learning Components

Grocea leverages several ML/AI techniques:

1. **Optical Character Recognition (OCR)**
   - Receipt text extraction and parsing
   - Item normalisation across different retailers

2. **Recipe Recommendation System**
   - Collaborative filtering
   - Content-based filtering using ingredient matching
   - Weighted scoring algorithm considering user preferences

3. **Time-Series Forecasting**
   - ARIMA/LSTM models for stock prediction
   - Usage pattern analysis

4. **Natural Language Processing**
   - Recipe ingredient extraction
   - Text normalisation and entity recognition
   - Fuzzy matching for product names

---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ (for mobile app)
- Python 3.11+ (for backend and ML)
- PostgreSQL 14+
- Redis 7+
- Docker (optional, recommended)

### Local Development Setup

1. **Clone the repositories**
   ```bash
   git clone https://github.com/grocea-app/grocea-mobile.git
   git clone https://github.com/grocea-app/grocea-backend.git
   git clone https://github.com/grocea-app/grocea-ml.git
   ```

2. **Start the backend**
   ```bash
   cd grocea-backend
   cp .env.example .env
   # Edit .env with your configuration
   pip install -r requirements.txt
   python src/main.py
   ```

3. **Run the mobile app**
   ```bash
   cd grocea-mobile
   cp .env.example .env
   npm install
   npm run ios    # for iOS
   npm run android # for Android
   ```

4. **Train ML models** (optional)
   ```bash
   cd grocea-ml
   pip install -r requirements.txt
   python src/training/train_recommendation.py
   ```

For detailed setup instructions, please refer to the README in each repository.

---

## 🎨 Screenshots

<div align="center">

| Receipt Scanning | Pantry View | Recipe Recommendations |
|:----------------:|:-----------:|:----------------------:|
| ![Receipt](https://via.placeholder.com/250x500?text=Receipt+Scan) | ![Pantry](https://via.placeholder.com/250x500?text=Pantry+View) | ![Recipes](https://via.placeholder.com/250x500?text=Recipes) |

</div>

> *Note: Screenshots will be updated as the project develops*

---

## 🛣️ Development Roadmap

### Phase 1: MVP (Current)
- [x] Project architecture design
- [ ] Basic receipt OCR functionality
- [ ] Pantry management (add/remove items)
- [ ] Simple recipe recommendations
- [ ] Mobile app UI/UX foundation

### Phase 2: Core Features
- [ ] Advanced recipe recommendation algorithm
- [ ] Automatic pantry stock updates
- [ ] User preference settings
- [ ] Expiry date tracking and notifications

### Phase 3: Intelligence
- [ ] Time-series forecasting for stock prediction
- [ ] Price-per-meal calculations
- [ ] Custom recipe creation with NLP
- [ ] Enhanced recommendation engine

### Phase 4: Advanced Features
- [ ] Meal photo recognition
- [ ] Shopping list generation
- [ ] Community recipe sharing
- [ ] Nutritional information tracking

---

<!-- ## 🤝 Contributing

Contributions are welcome! This project is primarily a portfolio piece demonstrating full-stack ML development, but improvements and suggestions are appreciated.

### How to Contribute

1. Fork the relevant repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes using conventional commits (`git commit -m 'feat: add amazing feature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Please read the [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and development process. -->

<!-- --- -->
<!-- 
## 📊 Project Statistics

![GitHub Stars](https://img.shields.io/github/stars/grocea-app?style=social)
![GitHub Forks](https://img.shields.io/github/forks/grocea-app?style=social)
![GitHub Issues](https://img.shields.io/github/issues/grocea-app/grocea-mobile) -->

---

## 🛠️ Technology Stack

### Mobile
- **Framework**: React Native / Flutter
- **State Management**: Redux Toolkit
- **Navigation**: React Navigation
- **API Client**: Axios + React Query

### Backend
- **Framework**: FastAPI
- **Database**: PostgreSQL
- **ORM**: SQLAlchemy
- **Caching**: Redis
- **Storage**: AWS S3 / Cloudflare R2

### Machine Learning
- **OCR**: Google Cloud Vision API / Tesseract
- **ML Frameworks**: TensorFlow, PyTorch, scikit-learn
- **Data Processing**: pandas, NumPy
- **NLP**: spaCy, Hugging Face Transformers

### Infrastructure
- **Hosting**: AWS / Google Cloud Platform
- **Containerisation**: Docker
- **Orchestration**: Kubernetes (optional)
- **CI/CD**: GitHub Actions
- **Monitoring**: Prometheus + Grafana

---

<!-- ## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

--- -->

## 👨‍💻 Author

**AmmarJ23**
<!-- - Portfolio: [yourwebsite.com](https://yourwebsite.com) -->
- LinkedIn: [linkedin.com/in/yourprofile](https://www.linkedin.com/in/ammar-jamalludin-084663269/)
- Email: ammar.jmldn@outlook.com
<!-- 
---

## 🙏 Acknowledgements

- OCR technology powered by [Google Cloud Vision API](https://cloud.google.com/vision)
- Recipe data sourced from [RecipeDB](https://cosylab.iiitd.edu.in/recipedb/) (or your data source)
- Icons from [Lucide Icons](https://lucide.dev/)
- UI inspiration from modern meal planning applications -->
<!-- 
---

## 📫 Contact & Support

- **Issues**: [Report a bug](https://github.com/grocea-app/grocea-mobile/issues)
- **Discussions**: [Join the conversation](https://github.com/grocea-app/grocea-mobile/discussions)
- **Email**: support@grocea.app (if applicable) -->

---

<div align="center">

**Built with ❤️ to reduce food waste and simplify meal planning**

[⬆ Back to Top](#-grocea)

</div>
