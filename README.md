# Fuzzy Logic Project: Intelligent EV Charging Station Selection

## Project Overview

Finding a suitable charging station is important for electric vehicle users, especially when distance, charging-slot availability, and charging prices vary. This project develops a Python-based fuzzy logic system that evaluates these factors and provides a score indicating how suitable a charging station may be.

The system takes three inputs—distance, availability, and charging cost—and processes them using fuzzy sets and predefined rules. It then generates a recommendation score from 0 to 100. This allows users to compare different charging situations through a simple, interactive interface.

## Features and Working Logic

### Input Parameters

The system considers the following parameters:

- **Distance from the user:** Ranges from 0 to 15 km and is represented by the fuzzy categories Near, Moderate, and Far.
- **Charging-slot availability:** Ranges from 0% to 100%, with the categories Low, Medium, and High.
- **Charging cost:** Ranges from $0 to $20 per kWh and is divided into Cheap, Moderate, and Expensive categories.

### Output Parameter

- **Station recommendation score:** A value between 0 and 100, represented by the fuzzy categories Low, Medium, and High. A higher score generally indicates a more suitable charging option according to the defined rules.

### Fuzzy Logic Implementation

- **Membership functions:** Triangular membership functions are used to describe how input and output values belong to different fuzzy categories.
- **Rule base:** Eight IF–THEN rules evaluate combinations of distance, availability, and cost. For instance, a station that is nearby, has high availability, and offers a low charging cost can receive a high recommendation.
- **Inference method:** The minimum operator is used to evaluate the AND conditions in the fuzzy rules.
- **Defuzzification:** The centroid method converts the combined fuzzy output into a single numerical score.
- **Interactive operation:** Users can change the input values through controls in the Jupyter Notebook and observe the resulting recommendation.
- **Performance testing:** Different combinations of input values are tested to study how the system responds to favourable and unfavourable charging conditions.

## Prerequisites and Installation

The project is developed in Python and is designed to run in Jupyter Notebook or JupyterLab.

The following libraries are required:

- `NumPy` for mathematical and numerical calculations.
- `Pandas` for organizing and processing data.
- `Matplotlib` for displaying graphs and membership functions.
- `scikit-fuzzy` for defining fuzzy sets and implementing the inference system.
- `ipywidgets` for interactive controls within the notebook.

Install the required packages by running the following command in a terminal or notebook cell:

```bash
pip install numpy pandas matplotlib scikit-fuzzy ipywidgets
```

## Steps to Execute the Project

1. Install Python and set up Jupyter Notebook or JupyterLab.
2. Install all the required Python libraries.
3. Open the `EV_Charging_Station_Recommendation_PBL.ipynb` notebook.
4. Execute the notebook cells sequentially to initialize the fuzzy system
