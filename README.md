# Kenya Violence Prediction Prototype

## Project Overview

This project develops a prototype AI system for analyzing political statements in Kenya and predicting the likelihood of post-election violence. Leveraging Natural Language Processing (NLP) techniques, this system aims to identify potentially inciteful language and assign a "risk score" to statements, demonstrating a pipeline for early warning systems.

**Important Note:** This is a *prototype* developed for demonstration purposes. It utilizes dummy data and a simplified rule-based model. Its primary goal is to showcase the analytical workflow, not to provide perfectly accurate predictions or be used in real-world sensitive contexts without significant further development, validation, and ethical considerations.

## Features

* **Data Loading & Preprocessing:** Handles ingestion of text data and performs cleaning (lowercasing, punctuation removal, whitespace normalization).
* **NLP Analysis:**
    * **Tokenization:** Breaks down statements into individual words/phrases.
    * **Sentiment Analysis:** Calculates sentiment scores using NLTK's VADER lexicon.
    * **Keyword Identification:** Identifies 'inciteful' keywords from a predefined list.
* **Feature Extraction:** Generates numerical features from NLP outputs (e.g., sentiment score, inciteful keyword frequency, statement length).
* **Probability Score Calculation:** Applies a rule-based tiered leader weighting system to calculate a "probability of violence" score for each statement, considering speaker influence and statement characteristics.
* **Output & Visualization:** Displays detailed analysis results per statement and visualizes the distribution of probability scores using a histogram.
* **Experimentation Module:** Allows for easy modification of parameters (e.g., keyword lists, weighting schemes) to observe their impact on the predictions.

## Getting Started

Follow these steps to set up and run the prototype on your local machine.

### Prerequisites

* Python 3.8+
* `pip` (Python package installer)

### Installation

1.  **Clone the repository:**

    ```bash
    git clone [https://github.com/your-username/Kenya-Violence-Prediction-Prototype.git](https://github.com/your-username/Kenya-Violence-Prediction-Prototype.git)
    cd Kenya-Violence-Prediction-Prototype
    ```

    *(Replace `your-username` with your actual GitHub username or the repository's path.)*

2.  **Create a virtual environment (recommended):**

    ```bash
    python -m venv venv
    # On Windows
    .\venv\Scripts\activate
    # On macOS/Linux
    source venv/bin/activate
    ```

3.  **Install the required dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

    *The `requirements.txt` file is generated later in this documentation.*

4.  **Download NLTK data:**
    The notebook will attempt to download necessary NLTK data (`vader_lexicon`, `punkt`) automatically. If you encounter issues, you can run this manually in a Python interpreter or within a Jupyter cell:

    ```python
    import nltk
    nltk.download('vader_lexicon')
    nltk.download('punkt')
    ```

### Running the Prototype

1.  **Start Jupyter Notebook:**

    ```bash
    jupyter notebook
    ```

2.  **Open the Notebook:**
    In your web browser, navigate to `Kenya_Violence_Prediction_Prototype.ipynb` and open it.

3.  **Run All Cells:**
    Execute all cells in the notebook sequentially (Cell -> Run All). The notebook will:
    * Create a `data.txt` file with dummy political statements.
    * Perform NLP analysis.
    * Calculate probability scores.
    * Display results and a visualization.

## Project Structure
