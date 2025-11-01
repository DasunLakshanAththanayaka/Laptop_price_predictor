# Laptop Price Predictor

A machine learning web application that predicts laptop prices based on various specifications using Flask and scikit-learn.

## 🚀 Features

- **Machine Learning Model**: Random Forest Regressor with GridSearchCV optimization
- **Web Interface**: Clean and responsive Flask web application
- **Real-time Predictions**: Input laptop specifications and get instant price predictions
- **Multiple Features**: Considers RAM, weight, company, type, OS, CPU, GPU, touchscreen, and IPS display

## 📊 Dataset

The model is trained on a laptop pricing dataset (`laptop_price.csv`) with the following features:
- **RAM**: Memory in GB
- **Weight**: Laptop weight in kg
- **Company**: Manufacturer (Acer, Apple, Asus, Dell, HP, Lenovo, MSI, etc.)
- **TypeName**: Laptop category (Gaming, Notebook, Ultrabook, etc.)
- **Operating System**: Windows, Mac, Linux, Other
- **CPU**: Processor type (Intel Core i3/i5/i7, AMD, Other)
- **GPU**: Graphics card (AMD, Intel, Nvidia)
- **Touchscreen**: Yes/No
- **IPS Display**: Yes/No

## 🛠️ Technologies Used

- **Python 3.x**
- **Flask** - Web framework
- **scikit-learn** - Machine learning library
- **pandas** - Data manipulation
- **numpy** - Numerical computing
- **pickle** - Model serialization
- **HTML/CSS** - Frontend

## 📁 Project Structure

```
Laptop_price_predictor/
│
├── laptop_price.csv        # Dataset
├── model.ipynb            # Jupyter notebook with ML model training
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
│
└── website/
    ├── app.py            # Flask application
    ├── Procfile          # Heroku deployment file
    ├── model/
    │   └── predictor.pickle  # Trained model file
    ├── static/
    │   └── style.css     # CSS styling
    └── templates/
        └── index.html    # HTML template
```

## 🔧 Installation

1. **Clone the repository**
```bash
git clone https://github.com/DasunLakshanAththanayaka/Laptop_price_predictor.git
cd Laptop_price_predictor
```

2. **Install required packages**
```bash
pip install -r requirements.txt
```

3. **Run the Jupyter notebook** (if you want to retrain the model)
```bash
jupyter notebook model.ipynb
```

4. **Start the Flask application**
```bash
cd website
python app.py
```

5. **Open your browser** and navigate to `http://127.0.0.1:5000`

## 🤖 Model Performance

The model uses Random Forest Regressor with the following optimized parameters:
- **n_estimators**: [10, 50, 100]
- **criterion**: ['squared_error', 'absolute_error', 'poisson']

Model achieves good accuracy through:
- Feature engineering (extracting touchscreen, IPS features)
- Categorical encoding using one-hot encoding
- Company grouping (less frequent brands grouped as 'Other')
- GridSearchCV for hyperparameter tuning

## 💻 Usage

1. **Access the web interface** at `http://127.0.0.1:5000`
2. **Fill in the laptop specifications**:
   - RAM (GB)
   - Weight (kg)
   - Select company, type, OS, CPU, GPU
   - Check touchscreen/IPS if applicable
3. **Click predict** to get the estimated price in LKR

## 📈 Model Training Process

1. **Data Loading**: Load CSV with latin-1 encoding
2. **Data Cleaning**: Handle missing values, convert data types
3. **Feature Engineering**: 
   - Extract touchscreen and IPS features from screen resolution
   - Simplify CPU names to major categories
   - Group less frequent companies
4. **Preprocessing**: One-hot encoding for categorical variables
5. **Model Training**: Compare multiple algorithms (Linear Regression, Lasso, Decision Tree, Random Forest)
6. **Optimization**: GridSearchCV for best parameters
7. **Model Serialization**: Save trained model using pickle

## 🔮 Future Enhancements

- [ ] Add more laptop specifications (storage, screen size, etc.)
- [ ] Implement more advanced ML algorithms
- [ ] Add model performance metrics visualization
- [ ] Deploy to cloud platform (Heroku, AWS, etc.)
- [ ] Add user feedback system
- [ ] Implement API endpoints for integration

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Dasun Lakshan Aththanayaka**
- GitHub: [@DasunLakshanAththanayaka](https://github.com/DasunLakshanAththanayaka)

## 🙏 Acknowledgments

- Dataset source: Various laptop specification databases
- Inspiration from various laptop pricing prediction projects
- Flask documentation and tutorials
- scikit-learn community

---

⭐ **Star this repo if you found it helpful!**