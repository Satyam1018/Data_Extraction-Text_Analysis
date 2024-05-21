# Data_Extraction-Text_Analysis

## Overview

This project involves extracting, cleaning, and analyzing text data from given URLs. The primary focus is on sentiment analysis and readability analysis of the extracted text. The results are compiled into a comprehensive DataFrame for further use.

## Table of Contents

- [Project Structure](#project-structure)
- [Setup and Installation](#setup-and-installation)
- [Data Extraction](#data-extraction)
- [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
- [Sentiment Analysis](#sentiment-analysis)
- [Readability Analysis](#readability-analysis)
- [Results Compilation](#results-compilation)
- [Conclusion](#conclusion)
- [Author](#author)

## Project Structure

- **data/**: Contains input data files such as URLs, positive and negative word lists.
- **notebooks/**: Contains the Jupyter notebook files for data processing and analysis.
- **output/**: Contains the final output files, including the cleaned data and results.
- **README.md**: This file, providing an overview of the project and instructions.

## Setup and Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/text-analysis-project.git
    cd text-analysis-project
    ```

2. **Install required libraries**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Download the data**:
    - Place the URLs, positive-words.txt, and negative-words.txt files in the `data/` directory.

## Data Extraction

- **Define Extraction Function**:
    - **Function**: `extract_text_from_url(url)`
    - **Action**: Fetches and parses HTML content from the URL, extracts text from `<p>` tags, and returns the combined text.

- **Apply Function**:
    - **Action**: Applied the function to each URL in the DataFrame's `URL` column.
    - **Result**: Stored the extracted text in a new column named `Text`.

- **Verify and Save**:
    - **Verify**: Displayed the first few rows of the DataFrame to ensure text extraction.
    - **Save**: Optionally saved the DataFrame to an Excel file (`extracted_text.xlsx`).

## Data Cleaning and Preprocessing

- **Load Stop Words**:
    - Created a function to load stop words from multiple text files.
    - Combined stop words into a set, handling different file encodings.

- **Data Cleaning Function**:
    - Developed a function to clean text by:
        - Removing URLs.
        - Removing punctuation.
        - Converting text to lowercase.
        - Tokenizing text into words.
        - Converting words to their base form.
        - Removing stop words.
        - Joining cleaned words back into a single string.

- **Apply Cleaning Function**:
    - Loaded stop words using the defined function.
    - Applied the cleaning function to the `Text` column of the DataFrame.
    - Stored cleaned text in a new column `Cleaned_Text`.

## Sentiment Analysis

Using predefined lists of positive and negative words, we calculated:
- **Positive Score**: The number of positive words in the text.
- **Negative Score**: The number of negative words in the text.
- **Polarity Score**: A measure of the overall sentiment of the text, calculated as the normalized difference between positive and negative scores.
- **Subjectivity Score**: The proportion of the text that is subjective, based on the presence of both positive and negative words.

## Readability Analysis

We computed various readability metrics to assess the complexity and readability of the text:
- **Average Sentence Length**: The average number of words per sentence.
- **Percentage of Complex Words**: The proportion of words with more than two syllables.
- **Fog Index**: A readability test that estimates the years of formal education needed to understand the text.
- **Complex Word Count**: The number of complex words in the text.
- **Word Count**: The total number of words in the text.
- **Syllables per Word**: The average number of syllables per word.
- **Personal Pronouns**: The count of personal pronouns in the text.

- **Average Word Length**: The average number of characters per word.

## Results Compilation

We compiled the calculated metrics into a comprehensive DataFrame, aligning with the expected output format. This included columns for URL_ID, URL, sentiment scores, readability scores, and other relevant metrics.

**The final DataFrame contains the following columns**:

- **URL_ID**: The unique identifier for each URL.
- **URL**: The URL from which the text was extracted.
- **Positive Score**: The count of positive words.
- **Negative Score**: The count of negative words.
- **Polarity Score**: The normalized difference between positive and negative scores.
- **Subjectivity Score**: The proportion of the text that is subjective.
- **Average Sentence Length**: The average number of words per sentence.
- **Percentage of Complex Words**: The proportion of words with more than two syllables.
- **Fog Index**: A readability test score.
- **Complex Word Count**: The count of complex words.
- **Word Count**: The total number of words.
- **Syllables per Word**: The average number of syllables per word.
- **Personal Pronouns**: The count of personal pronouns.
- **Average Word Length**: The average number of characters per word.

## Conclusion

This project successfully demonstrates the process of extracting, cleaning, and analyzing text data from URLs. The sentiment and readability analyses provide valuable insights into the content, allowing us to understand both the emotional tone and the complexity of the text. The final DataFrame, with all calculated metrics, serves as a robust dataset for further analysis or reporting.

## Author

- **Name** - Satyam Ojha
 
-  **Contact Detail** 
  - **LinkedIN** - https://www.linkedin.com/in/ojha-satyam
  - **Email**    - ojhasatyam10@gmail.com
    
- **Skills**  
  - PYTHON
  - SQL
  - Power BI / Tableau
  - Machine learning
  - Deep learning
  - Natural language processing (NLP)
  - Neural Network
