# 🏠 Indonesia Housing Price Analysis

This project focuses on predicting housing prices in Indonesia using machine learning models. We utilize property listings scraped from major Indonesian real estate websites to analyze and forecast property values based on various features such as location, size, and amenities.

## 📊 Dataset Overview

The dataset includes the following columns:

- `price` – Property price (target variable)  
- `installment` – Monthly payment (if available)  
- `title` – Listing title  
- `location` – Property location  
- `bedroom` – Number of bedrooms  
- `bathroom` – Number of bathrooms  
- `garage` – Number of garage spaces  
- `land_area` – Total land area (in m²)  
- `building_area` – Total building area (in m²)

## 🔧 Data Preprocessing

Before modeling, we performed comprehensive data cleaning and preparation:

- Standardized data formatting  
- Removed duplicate entries  
- Handled missing values  
- Fixed data type mismatches  
- Engineered new features and addressed multicollinearity  
- Encoded categorical variables  
- Scaled numerical features

## 📈 Model Evaluation

We evaluated model performance using **Mean Absolute Error (MAE)** and **R² Score**:
- **MAE** indicates the average prediction error.
- **R² Score** reflects how well the model explains the variance in property prices.

### 🧪 Model Performance Comparison

| Model                   | Metric | Training Performance | Test Performance |
|-------------------------|--------|-----------------------|------------------|
| **Ridge Regression**    | MAE    | 786.86                | 806.47           |
|                         | R²     | 0.6673                | 0.6592           |
| **Random Forest**       | MAE    | 308.11                | 624.45           |
|                         | R²     | 0.9318                | 0.7439           |
| **XGBoost**             | MAE    | 452.91                | 644.13           |
|                         | R²     | 0.8877                | 0.7472           |
| **Gradient Boosting**   | MAE    | 473.56                | 652.88           |
|                         | R²     | 0.8694                | 0.7447           |
| **LightGBM**            | MAE    | 494.79                | 645.67           |
|                         | R²     | 0.8531                | 0.7447           |

## 🔍 Key Insights

- **Location is the most critical factor** in predicting housing prices.
  - **South Jakarta** (5.5%) and **North Jakarta** (3.9%) were the most influential regions.
  - Tourist hubs like **Badung** also ranked high in importance.
- **Building and land size** follow location in importance.
- Features like **bedrooms, bathrooms, and garage spaces** matter, but their influence decreases after a certain point.
- **Space efficiency** (effective use of area) positively affects pricing.
- Even with similar specs, **prices vary widely across cities**, highlighting the need for location-aware pricing models.

## 💡 Recommendations

### 🏘️ For Real Estate Agents:
- Focus on enhancing listings with information about nearby schools, transport access, and amenities.
- Highlight neighborhood characteristics as they heavily influence buyer interest and pricing.

### 📈 For Investors & Stakeholders:
- Prioritize high-demand areas such as **South Jakarta, North Jakarta, and Bekasi**.
- Monitor **urban development and infrastructure projects** to identify emerging investment hotspots.

### 🏡 For Home Buyers:
- Prioritize **location over size**—a well-located smaller home may offer better value.
- Use **region-based price comparison tools** to ensure you're paying a fair price.

---

## 🚀 Getting Started

To run the project locally:

```bash
git clone https://github.com/yourusername/indonesia-housing-price-analysis.git
cd indonesia-housing-price-analysis
pip install -r requirements.txt
```

You can then run the model training and evaluation notebook or script in the `notebooks/` or `src/` directory.

---

## 📄 License

This project is open-source and available under the MIT License.
