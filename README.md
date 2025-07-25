Name Finder
A Python tool to find phonetically similar names to your favorite name, using a dataset of approximately 48,200 Iranian village names. You can input a name (preferably in Farsi, but English is also supported) and the tool will suggest 10 names from the dataset that are phonetically similar.
Features

Accepts a name input in Farsi or English.
Converts names to phonetic representations for comparison.
Uses TF-IDF vectorization and cosine similarity to find the closest matches.
Currently uses a dataset of Iranian village names, but supports any list with a 'name' column.
Outputs the top 10 phonetically similar names.

Example Input
Enter a name, preferably in Farsi (e.g., زاو، اوریم، نیما، اسنپ). For example:
What is your favorite name in Farsi: اسنپ

Requirements
The following Python libraries are required:

pandas
regex
gdown
scikit-learn

Install them using:
pip install pandas regex gdown scikit-learn

Data Source
The tool downloads a dataset of Iranian village names from Google Drive:

File ID: 1diRpnHII0HCeemkZhdXxQTG94JvM54_g
Download URL: https://drive.google.com/uc?export=download&id=1diRpnHII0HCeemkZhdXxQTG94JvM54_g
The dataset is an Excel file (data.xlsx) containing columns: provinces, cities, villages_names, and names.

How It Works

Input: The user provides a name (preferably in Farsi).
Data Loading: The tool downloads and loads the dataset into a pandas DataFrame.
Phonetic Conversion: Names are converted to phonetic representations, mapping Farsi characters to phonetic equivalents (e.g., 'ا' to 'æ' or 'ɑ').
TF-IDF Vectorization: The phonetic representations are transformed into a TF-IDF matrix for similarity comparison.
Cosine Similarity: The input name is converted to phonetics, vectorized, and compared to the dataset using cosine similarity.
Output: The top 10 phonetically similar names are displayed.

Usage

Run the script.
Enter a name when prompted (e.g., اسنپ).
The script downloads the dataset, processes the names, and outputs the 10 most phonetically similar names.

Notes

The dataset must have a names column for the tool to work.
You can replace the dataset with any other Excel or CSV file containing a names column.
The phonetic conversion is tailored for Farsi; English names may produce less accurate results.
The tool is case-sensitive for English inputs.

Example Output
For input اسنپ:
1. اسنپ
2. اسناب
3. اسنوب
...
