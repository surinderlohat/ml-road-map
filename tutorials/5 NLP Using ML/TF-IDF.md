# TF-IDF (Term Frequency-Inverse Document Frequency)

TF-IDF is a numerical statistic used in information retrieval and text mining to evaluate the importance of a word in a document relative to a collection of documents (corpus). It is a combination of two metrics: Term Frequency (TF) and Inverse Document Frequency (IDF).

## Term Frequency (TF)

Term Frequency measures how frequently a term (word) appears in a document. The idea is that terms that appear more frequently in a document are more important. The simplest way to calculate TF is:

\[ \text{TF}(t, d) = \frac{\text{Number of times term } t \text{ appears in document } d}{\text{Total number of terms in document } d} \]

## Inverse Document Frequency (IDF)

Inverse Document Frequency measures the importance of a term within the entire corpus. The idea is that if a term appears in many documents, it is less significant. IDF can be calculated as:

\[ \text{IDF}(t, D) = \log \left( \frac{\text{Total number of documents in corpus } D}{\text{Number of documents in which term } t \text{ appears}} \right) \]

## TF-IDF Calculation

TF-IDF is the product of TF and IDF. It assigns a higher weight to terms that are frequent in a document but not frequent in the corpus. The formula for TF-IDF is:

\[ \text{TF-IDF}(t, d, D) = \text{TF}(t, d) \times \text{IDF}(t, D) \]

## Example

Consider a corpus with the following three documents:

1. "The cat sat on the mat."
2. "The cat sat."
3. "The dog sat on the log."

To calculate the TF-IDF for the term "cat" in Document 1:

1. Calculate TF:
   \[ \text{TF}(\text{"cat"}, \text{Document 1}) = \frac{1}{6} \approx 0.167 \]

2. Calculate IDF:
   \[ \text{IDF}(\text{"cat"}, D) = \log \left( \frac{3}{2} \right) \approx 0.176 \]

3. Calculate TF-IDF:
   \[ \text{TF-IDF}(\text{"cat"}, \text{Document 1}, D) = 0.167 \times 0.176 \approx 0.029 \]

## Applications

TF-IDF is widely used in:

- Information retrieval systems (e.g., search engines)
- Text mining and analysis
- Natural Language Processing (NLP) tasks
- Document similarity and clustering

By emphasizing unique terms in documents, TF-IDF helps in identifying the most relevant information for various applications.
