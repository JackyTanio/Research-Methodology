
# Weather and Air Pollution Prediction

This project fetches weather data and air pollution levels for various cities using the OpenWeatherMap API and builds a machine learning model to predict air pollution levels based on weather parameters.

## Table of Contents
- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
  - [Fetching Weather and Pollution Data](#fetching-weather-and-pollution-data)
  - [Training the Model](#training-the-model)
  - [Making Predictions](#making-predictions)
- [Output](#output)
- [License](#license)

## Project Overview

This project consists of two main parts:
1. **Weather and Air Pollution Data Collection**: It retrieves weather and air pollution data from the OpenWeatherMap API for a list of cities provided in an Excel file.
2. **Air Pollution Level Prediction**: Using the fetched data, a Decision Tree Classifier is trained to predict the air pollution level based on weather conditions such as temperature, humidity, and wind speed.

The final outputs include:
- An Excel file with weather and pollution data.
- A machine learning model that predicts air pollution levels.

## Prerequisites

Before running the project, make sure you have the following dependencies installed:
- Python 3.x
- pandas
- requests
- openpyxl
- scikit-learn
- matplotlib

To install the required libraries, you can run:

```bash
pip install pandas requests openpyxl scikit-learn matplotlib
```

You will also need an API key from OpenWeatherMap. You can get one by signing up at [OpenWeatherMap](https://openweathermap.org/api).

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/weather-air-pollution-prediction.git
cd weather-air-pollution-prediction
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Ensure your cities list is available in an Excel file (`cities_list.xlsx`) with columns:
   - `lat` (Latitude)
   - `lon` (Longitude)

4. Replace the placeholder API key in the code with your actual OpenWeatherMap API key:

```python
api_key = 'your_api_key'
```

## Usage

### Fetching Weather and Pollution Data

To fetch weather and air pollution data for cities listed in `cities_list.xlsx`, run:

```bash
python fetch_weather_data.py
```

This will generate an Excel file `weather_pollution_data.xlsx` containing weather data and the corresponding air pollution levels for each city.

### Training the Model

After fetching the weather data, train a Decision Tree Classifier to predict air pollution levels:

```bash
python train_model.py
```

The classifier will be trained using temperature, humidity, and wind speed as features, and air pollution level as the target.

### Making Predictions

You can predict the air pollution level for any city by providing its latitude and longitude. For example, to predict the pollution level for Jerusalem:

```bash
python predict_pollution.py
```

The script will fetch the weather data for the specified city and use the trained model to predict its pollution level.

## Output

- **Weather and Pollution Data**: `weather_pollution_data.xlsx` (contains weather data and air pollution levels for each city).
- **Model Prediction**: Predicted air pollution level for any given city based on current weather conditions.
- **Confusion Matrix**: A plot of the confusion matrix for the model's predictions.

### Example Output
```bash
Predicted Air Pollution Level for Jerusalem: Medium
```

The confusion matrix and model accuracy will be printed in the console.

## License

This project is licensed under the MIT License.
