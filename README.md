# Classification of Wont-Fix Issues in GitHub

This is a classification tool for categorizing GitHub issues as "wont-fix" or "non-wont-fix." It uses the GitHub API to fetch issues from repositories marked with relevant labels. 

## Features

- Integration with the GitHub API to fetch issues and repository details.
- Converts issue details into structured datasets in CSV format for analysis.
- Classifies issues using TF-IDF vectorization combined with Random Forest and Multinomial Naive Bayes models.
- Evaluates model performance using accuracy scores and confusion matrices.
- Validates results with K-Fold Cross-Validation.

## Project Structure

- **Classification Code**:
  - `project_code.ipynb`: Contains the implementation for classification without the additional feature.
  - `project_code_additional_feature.ipynb`: Extends the classification with an additional feature and includes 10-fold cross-validation to validate performance.

- **Dataset Collection (Optional)**:
  - Requires a GitHub personal access token and the **Perceval** library.
  - **Note**: If you wish to generate your own dataset, use `issue_fetch.ipynb` to retrieve repositories, followed by `dataset_collection.ipynb` to collect issue details. Skip this step if you want to use a pre-existing dataset.

## Installation

### Prerequisites

- Python 3.x
- pip (Python package installer)
- Jupyter Notebook (optional for running `.ipynb` files)

### Steps

1. Clone the repository:

    ```bash
    git clone https://github.com/jaishmau39/classification_wont-fix_issues_github.git
    ```

2. Navigate to the project directory:

    ```bash
    cd classification_wont-fix_issues_github
    ```

3. Install the required Python dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Ensure that you have a valid GitHub personal access token.

5. Execute the relevant notebooks using Jupyter Notebook or your preferred Python environment.

## Usage

1. **Dataset Collection (Optional)**:
   - Run `issue_fetch.ipynb` to retrieve a list of repositories.
   - Use `dataset_collection.ipynb` to collect issue details and save as CSV. A valid GitHub token is required.
     
2. **Classification**:
   - Run `project_code.ipynb` to classify issues without the additional feature.
   - Run `project_code_additional_feature.ipynb` for classification using the additional feature and 10-fold cross-validation.

3. Analyze the outputs in the respective notebooks for classification accuracy and validation results.

## Acknowledgements

- **Perceval**: Data was fetched using the [Perceval tool](https://github.com/chaoss/grimoirelab-perceval), which simplifies the process of retrieving data from GitHub.
- GitHub API documentation for fetching issues.




