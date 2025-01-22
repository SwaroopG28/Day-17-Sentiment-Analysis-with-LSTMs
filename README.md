# Sentiment Analysis with LSTMs

## **Overview**
This project demonstrates how to perform **sentiment analysis** on movie reviews using a **Long Short-Term Memory (LSTM)** network. The model predicts whether a movie review has a **positive** or **negative** sentiment.

## **Dataset**
### IMDB Reviews Dataset
- Contains **50,000 movie reviews**, each labeled as positive or negative.
- **Training Data**: 25,000 reviews.
- **Testing Data**: 25,000 reviews.
- Each review is pre-tokenized into sequences of word indices.

## **Project Workflow**
1. **Data Preparation**:
   - Reviews are padded or truncated to a fixed length of **200 words** for uniformity.
   - The vocabulary size is limited to the **10,000 most common words**.

2. **Model Architecture**:
   - **Embedding Layer**:
     - Converts word indices into dense vectors of size 128.
   - **Bidirectional LSTM**:
     - Processes text sequences in both forward and backward directions for better context understanding.
   - **Dropout Layers**:
     - Prevent overfitting by randomly dropping neurons during training.
   - **Dense Layers**:
     - Fully connected layers for binary classification.
   - **Output Layer**:
     - Uses a **sigmoid activation function** to predict sentiment (positive or negative).

3. **Training**:
   - Trained the model for **5 epochs** with a batch size of **64**.
   - Optimizer: **Adam**.
   - Loss Function: **Binary Cross-Entropy**.

4. **Evaluation**:
   - Achieved a test accuracy of **82.99%** on the IMDB dataset.

5. **Custom Review Testing**:
   - The model can predict the sentiment of any custom movie review.

---

## **Results**
### Model Accuracy:
- **Test Accuracy**: 82.99%

### Example Output:
- Input: `"The movie was very boring. The script could have been better"`
- Predicted Sentiment: **Negative**


