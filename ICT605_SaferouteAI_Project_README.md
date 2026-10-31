# SAFEROUTE AI – INTELLIGENT ROAD ACCIDENT SEVERITY & HOTSPOT ANALYSIS

##1. PROJECT TITLE & OVERVIEW

SafeRoute AI – Intelligent Road Accident Severity & Hotspot Analysis

SafeRoute AI is an AI-supported road accident analysis and decision-support project. It uses the US Accidents (March 2023) dataset to explore accident patterns based on temporal, environmental, road, and contextual factors. The project applies a Random Forest machine learning model to classify accident traffic-impact severity into four levels (Severity 1–4).

The project includes interactive visualisations to help users explore accident trends, severity distributions, geographic accident concentrations, road and weather indicators, and model performance. It also provides a web-based interface with an interactive What-if predictor, allowing users to change selected conditions and view the predicted severity class and estimated probabilities for the four severity levels.

The main purpose of SafeRoute AI is to transform large-scale accident data into useful insights and support users in investigating historical accident patterns and hypothetical traffic conditions.

The project is intended for educational and exploratory analysis. The predicted severity represents traffic impact in the dataset, not injury or fatality severity. Model predictions are estimates and should not be treated as guaranteed real-world outcomes.

##2. INSTALLATION GUIDE

Prerequisites:

- Python environment with Jupyter Notebook, JupyterLab, or Google Colab
- Internet access for installing libraries or downloading the dataset
- The project notebook and required dataset
- A compatible Python environment for the libraries listed in `requirements.txt`

Step 1: Open the notebook

Open the SafeRoute AI notebook using Jupyter Notebook, JupyterLab, or Google Colab.

Step 2: Install the required libraries

Install the required Python libraries using the provided `requirements.txt` file:

```bash
pip install -r requirements.txt
```

The project uses libraries such as Pandas, NumPy, Scikit-learn, Plotly, and Gradio, along with other packages required by the notebook.

Step 3: Obtain the dataset

Download the US Accidents (March 2023) dataset from Kaggle:

https://www.kaggle.com/datasets/joytuntonny/us-accidents-march23

Place the dataset in the appropriate project data directory or update the dataset-loading path in the notebook.

Dataset file used in the project:

`US_Accidents_March23_sampled_500k.csv`

Ensure that the dataset is accessible before running the notebook. The notebook's original file path may need to be changed when running it on another computer or in a different environment.

Step 4: Run the notebook

Run the notebook cells sequentially from the beginning to the end.

The notebook performs:

- Dataset loading and data-quality checks
- Exploratory data analysis
- Feature engineering and data preparation
- Missing-value handling and data preprocessing
- Training, validation, and test data preparation
- Baseline and Random Forest model comparison
- Class-weight experiments to address class imbalance
- Model evaluation and confusion matrix analysis
- Error analysis and feature importance visualisation
- Prediction probability analysis and uncertainty-related assessment
- Geographic accident concentration mapping
- Interactive What-if predictor and dashboard generation

Step 5: Launch the web application

After running the required data preparation, model training, and evaluation cells, execute the web application cell in the notebook.

The application provides two main sections:

-AI What-if Predictor:Allows users to change available scenario inputs and view the predicted severity and estimated class probabilities.
-Historical Analytics Dashboard:Allows users to filter historical accident records and explore interactive charts.

When launched with Gradio sharing enabled, the application may generate a temporary web link that can be opened in a browser. The notebook runtime must remain active for the temporary link to continue working.

##3. USAGE EXAMPLES

Example 1:Run the complete analysis

Open the SafeRoute AI Jupyter Notebook and execute all cells sequentially.

The notebook loads the accident dataset, prepares the data, trains and evaluates the Random Forest classifier, compares model configurations, and generates the project's visualisations and application.

Example 2:Explore accident severity

Open the Historical Analytics Dashboard in the web application.

Users can filter historical accident records based on:

- Severity
- Time of Day
- Season
- Rush Hour
- Weekend

The dashboard provides visualisations and summaries such as:

- Filtered accident record count
- Average recorded severity
- Severity 4 case count
- Accident distribution by severity
- Accident patterns by time of day
- Road and weather indicator percentages
- Final model evaluation scores

The dashboard filters update the historical visualisations. They do not retrain the machine learning model.

Example 3: Generate an AI severity prediction

Open the AI What-if Predictor tab in the web application.

Users can change the available numerical, categorical, weather, state, and road-condition inputs and select the prediction button.

The application produces:

- Predicted traffic-impact severity (Severity 1–4)
- Estimated probability for each severity class
- A probability chart showing the model's output

The State dropdown displays full US state names alongside their abbreviations, while the application passes the original state codes to the trained model.

The prediction probabilities are model estimates and should not be interpreted as guaranteed or necessarily calibrated real-world probabilities.

Example 4: Explore geographic accident concentrations

Use the geographic visualisation in the notebook to examine where accident records are concentrated.

The map groups accident coordinates into approximate geographic cells and displays the number of recorded accidents in those areas. The displayed map may use a selected subset of geographic cells to improve visualisation performance.

Accident concentration does not automatically indicate a higher underlying accident risk because traffic volume, road-user exposure, and other contextual factors are not fully accounted for.

Example 5: Evaluate model performance

Review the model evaluation sections in the notebook.

The project compares a baseline model with Random Forest configurations using class-weight experiments. Evaluation includes accuracy, balanced accuracy, precision, recall, macro F1-score, confusion matrices, and class-specific error analysis.

These results help identify the effects of class imbalance and the trade-offs between overall accuracy and minority-class recognition.

##4. CONTRIBUTION GUIDELINES

This project was developed as a university group project.

Contributors should follow these guidelines:

- Clearly describe any changes made to the project.
- Ensure that code changes do not introduce errors into the notebook, predictor, or dashboard.
- Test the notebook from a fresh kernel before submitting changes.
- Keep dataset paths, feature definitions, and file references consistent.
- Ensure that the preprocessing and engineered features used by the predictor match those used during model training.
- Verify that reported metrics match the final notebook outputs.
- Do not upload private information, passwords, API keys, or other confidential credentials.
- Clearly acknowledge external datasets, libraries, software, services, and AI assistance according to university requirements.
- Report errors or issues with enough information to reproduce the problem where possible.

For future development, contributors may explore improvements to:

- Interactive What-if scenario functionality
- Recognition of minority severity classes
- Probability calibration and uncertainty communication
- Model explainability
- Geographic hotspot analysis using additional road-network and traffic-exposure data
- Updated data integration and deployment of a persistent web application
- Graph-based approaches where suitable road-network data is available

##5. LICENSE INFORMATION

The US Accidents (March 2023) dataset is obtained from Kaggle and is based on the countrywide traffic accident dataset developed by Moosavi et al.

Dataset source:

Joytuntonny. (2023). US Accidents (March 23) [Data set]. Kaggle.

https://www.kaggle.com/datasets/joytuntonny/us-accidents-march23

Users of this project must comply with the applicable terms, conditions, attribution requirements, and licence restrictions of the original dataset and any third-party software or libraries used.

The Python libraries used in this project are subject to their respective licences.

This project is intended for educational and research purposes. SafeRoute AI is an academic prototype and is not a validated real-time accident prediction or emergency response system. Its outputs should not be used as the sole basis for professional road-safety or traffic-management decisions.

No private API keys, passwords, or other confidential credentials should be included in the submitted project files.

##6. PROJECT EVIDENCE AND REPRODUCIBILITY

The Project Evidence and Source folder contains the materials required to inspect and reproduce the implemented system.

These materials should include:

- The final Jupyter Notebook
- README and dependency information
- Dataset or dataset access instructions
- Architecture diagram and source file
- Baseline and model comparison results
- Model evaluation and error analysis evidence
- Geographic map and dashboard screenshots
- What-if predictor examples
- Other relevant implementation and assessment evidence

To reproduce the project, users should install the required dependencies, ensure that the dataset is accessible, and run the notebook cells in order. The web application should be launched only after the required model and dataset objects have been prepared.

The submitted evidence should reflect the final implementation and should not contain outdated results or descriptions of features that are no longer present.