## Installation

To get started with this project, clone the repository and install the required dependencies.

1. Clone the repository:

    bash
    git clone <repository_url>
    cd Booking-Volume-Prediction
    

2. Install dependencies:

    It is recommended to use a virtual environment (e.g., venv or conda) to manage dependencies. Install the required libraries using the requirements.txt file:

    bash
    pip install -r requirements.txt
    

## Dataset

The dataset used in this project, lux_hot_8.xlsx, contains booking details from luxury hotels, including features such as:

- Booking status
- Number of adults
- Number of children
- Booking lead time
- Room type, and more

## Data Preprocessing

1. *Data Cleaning*: 
   - Missing values in the Booking Status column were removed to ensure the dataset is clean.
   
2. *Feature Engineering*: 
   - Normalization using MinMax scaling was applied to numerical features to improve model performance.

## Model Selection

The following models were used to predict the booking volume:

1. *Recurrent Neural Network (RNN)*: Used for its suitability in handling sequential data such as time series.
2. *Random Forest*: Used for comparison to evaluate the model’s performance.
3. *Linear Regression*: Another model used for comparison.

The models were trained and evaluated using a hyperparameter tuning process to improve their accuracy.

## Deployment

The trained models were deployed via a *Streamlit* application that allows users to input data and get real-time booking volume predictions. This interface provides a simple way to interact with the model.

## Running the Application

To run the application locally:

1. Ensure that all dependencies are installed.
2. Run the following command to start the application:

    bash
    streamlit run app/app.py
    

3. The application will be available at http://localhost:8501 in your browser.

## Hyperparameter Tuning

Hyperparameter tuning was conducted using GridSearchCV and RandomizedSearchCV to find the optimal settings for each model.

## Saving and Loading Models

The trained models are saved using the h5 format for the booking volume model and pkl format for the scaler used during feature normalization. These models are saved in the models/ folder.

## Cloud Deployment

The project was deployed to a cloud platform (e.g., Heroku, AWS, or Render) for real-time predictions. Users can interact with the model through the deployed web application.

## Conclusion

This project demonstrates how machine learning models can be used for time series forecasting and hotel booking volume prediction. The RNN model performed the best, providing solid forecasting capabilities. The deployment of the model through Streamlit allows users to interact with the model in real-time.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
