# Mobile Price Classification

## Project Overview

Bob, the founder of a mobile company, wants to predict the price range of his mobile phones based on their specifications. This project aims to develop a machine learning model that can predict the price range of a mobile phone based on various features like battery power, screen size, RAM, camera megapixels, and more.

The goal is to build an accurate model that helps Bob make informed pricing decisions to compete with established players like Apple and Samsung.

## Problem Statement

Bob gathered data from different companies to understand the relationship between the specifications of mobile phones and their selling prices. He needs assistance in analyzing this data and building a model that can predict the price range for mobile phones. This will help Bob set competitive prices for his phones.

## Solution

The main objective of this project is to predict the price range of mobile phones based on their specifications. We will explore different classification algorithms, train models using the data, and evaluate the models based on their accuracy. After evaluating the models, we will select the most accurate one for price prediction.

## Data Description

The dataset consists of 21 features, with each row representing a mobile phone and its specifications. The features include:

- `battery_power`: Battery capacity in milliampere hours (mAh)
- `blue`: Bluetooth availability (1 if present, 0 if absent)
- `clock_speed`: Microprocessor speed in gigahertz (GHz)
- `dual_sim`: Dual SIM support (1 if supported, 0 if not)
- `fc`: Front camera megapixels
- `four_g`: 4G connectivity support (1 if supported, 0 if not)
- `int_memory`: Internal memory capacity in gigabytes (GB)
- `m_dep`: Mobile depth in cm
- `mobile_wt`: Weight of mobile phone in grams
- `n_cores`: Number of cores of the processor
- `pc`: Primary camera megapixels
- `px_height`: Pixel resolution height
- `px_width`: Pixel resolution width
- `ram`: RAM capacity in megabytes (MB)
- `sc_h`: Screen height in cm
- `sc_w`: Screen width in cm
- `talk_time`: Maximum talk time on a single charge
- `three_g`: 3G connectivity support (1 if supported, 0 if not)
- `touch_screen`: Touchscreen availability (1 if present, 0 if absent)
- `wifi`: Wi-Fi support (1 if supported, 0 if not)
- `price_range`: Target variable indicating the price range of the mobile phone

The dataset is split into two parts:

- **Training Dataset**: Used to train the machine learning models.
- **Test Dataset**: Used to evaluate the performance of the trained models.

Both datasets are stored in the `data` folder of the repository. The data is sourced from Kaggle.

## Machine Learning Models Used

We evaluated several machine learning models to classify the price range of mobile phones:

1. **Logistic Regression**
2. **MLPClassifier (Multi-layer Perceptron)**
3. **RandomForestClassifier**
4. **HistGradientBoostingClassifier**

## Best Model and Evaluation

The evaluation results for different models showed that **Logistic Regression** provided the best accuracy:

- **Logistic Regression**: 0.979462
- **MLPClassifier**: 0.901794
- **RandomForestClassifier**: 0.886373
- **HistGradientBoostingClassifier**: 0.915545

Based on the performance metrics, we recommend **Logistic Regression** as the best model for predicting mobile phone price ranges.

## Installation and Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/mobile-price-classification.git
    cd mobile-price-classification
    ```

2. Install dependencies using `pip`:

    ```bash
    pip install -r requirements.txt
    ```

3. Before running the model, make sure to set the correct file paths in the configuration files.

    - **Data**: Ensure that the path to the training and test datasets in the `data` folder is correctly specified in the code. The data is available in the `data` folder.
    - **Notebook Configuration**: The libraries for running the model are uploaded in the `notebook_configuration` folder. Make sure all necessary libraries are installed and correctly referenced in the notebook configuration.
    - **Code**: The whole code for running the model is uploaded in the `finalproject.ipynb` file.

4. Run the code:

    ```bash
    python main.py
    ```

## Usage

The script loads the dataset, processes the data (handling missing values, encoding categorical features, etc.), and trains various classification models. The results, including accuracy scores, are displayed, and the best-performing model (Logistic Regression) is used for predicting the price range of mobile phones based on their specifications.

Ensure you change the path to the dataset files and configuration folder if needed before running the script.

## Conclusion

The project successfully predicted mobile phone price ranges using machine learning classification algorithms. Logistic Regression proved to be the most accurate model, achieving an accuracy of 97.95%.

## References

1. [Tree-Based Models Case Study - Yuxiaohuang](https://yuxiaohuang/teaching/p2_c2_s5_tree_based_models/case_study)
2. [Kaggle Mobile Price Classification](https://www.kaggle.com/competitions/mobile-price-classification)
