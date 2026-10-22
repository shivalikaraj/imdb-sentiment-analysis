# IMDb Sentiment Analysis using Hugging Face

## Project Overview
This project classifies movie reviews as positive or negative using
a fine-tuned DistilBERT model from Hugging Face Transformers.

## Technologies Used
- Python
- Google Colab
- Hugging Face Transformers
- Hugging Face Datasets
- Evaluate
- DistilBERT

## Workflow
1. Load the IMDb movie-review dataset.
2. Tokenize movie reviews using a pretrained tokenizer.
3. Fine-tune DistilBERT for binary sentiment classification.
4. Save the trained model and tokenizer.
5. Predict sentiment for new movie reviews.
6. Evaluate the model on a randomly shuffled sample
   of 1,000 held-out test reviews.

## Evaluation Results
- Accuracy: 91.4%
- Precision: 92.95%
- Recall: 89.14%
- F1 score: 91.00%

These results are from a 1,000-review test sample.
They should not be interpreted as results on the full test set.

## Example Inference
Input:
"This movie was absolutely fantastic!"

Expected type of output:
A sentiment label (POSITIVE or NEGATIVE) and a confidence score.

## Project Artifacts
- imdb_sentiment_model/: saved model and tokenizer
- evaluation_results.json: evaluation metrics
- README.md: project documentation

## How to Use
Load the saved model and tokenizer using
AutoModelForSequenceClassification and AutoTokenizer,
then create a text-classification pipeline.

## Limitations
- Evaluation was performed on a sample, not the entire test set.
- Predictions can be incorrect, even when confidence is high.
- Performance may vary on reviews unlike those in the IMDb dataset.
