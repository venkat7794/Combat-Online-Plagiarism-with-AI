## Text Similarity Computation

This Python script computes the text similarity between a set of files using the TF-IDF (Term Frequency-Inverse Document Frequency) and cosine similarity algorithms.

### Features

- Reads text content from a list of file paths
- Computes the TF-IDF matrix for the text content
- Calculates the cosine similarity between each pair of files
- Outputs the file pairs and their corresponding similarity scores

### Usage

1. Ensure you have the following dependencies installed:
   - `os`
   - `sklearn.feature_extraction.text.TfidfVectorizer`
   - `sklearn.metrics.pairwise.cosine_similarity`

2. Update the `file_paths` list in the `main()` function to include the paths to the files you want to analyze.

3. Run the script using the following command:

   ```
   python text_similarity.py
   ```

4. The script will output the file pairs and their corresponding similarity scores.

### Example Output

```
('/content/drive/MyDrive/john.txt', '/content/drive/MyDrive/juma.txt', 0.5)
('/content/drive/MyDrive/john.txt', '/content/drive/MyDrive/fatma.txt', 0.3)
('/content/drive/MyDrive/juma.txt', '/content/drive/MyDrive/fatma.txt', 0.7)
```

### Functions

#### `read_files(file_paths)`

- Reads the text content from the provided file paths and returns a list of the text content.

#### `compute_similarity(file_paths)`

- Computes the TF-IDF matrix for the text content.
- Calculates the cosine similarity between each pair of files.
- Returns a list of tuples, where each tuple contains the file paths and the corresponding similarity score.

#### `main()`

- Defines the list of file paths.
- Calls the `compute_similarity()` function and prints the results.

### Limitations

- The script assumes that the text content is encoded in UTF-8.
- The script does not handle any preprocessing or cleaning of the text content.
- The script does not provide any visualization or further analysis of the similarity results.

### Future Improvements

- Implement text preprocessing steps, such as stopword removal, stemming, or lemmatization, to improve the quality of the similarity computation.
- Add support for handling different file formats (e.g., PDF, Word documents) or text extraction from various sources.
- Provide options for customizing the TF-IDF parameters or the similarity metric.
- Integrate the script into a larger application or provide a user-friendly interface.
