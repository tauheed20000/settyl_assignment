# settyl_assignment

### Data Preprocessing:

The dataset was preprocessed to clean and format the external status descriptions and internal status labels.
The clean_text function was used to remove extra information from the external status descriptions, such as vessel names.
The Tokenizer from TensorFlow was utilized to tokenize the external status descriptions.
The internal status labels were encoded using LabelEncoder from scikit-learn.

### Model Architecture:

A sequential model was defined using TensorFlow's Sequential API.
The model architecture consisted of an Embedding layer followed by a Bidirectional LSTM layer, a dropout layer, and two dense layers.
The Embedding layer was used to convert tokenized input sequences into dense vectors of fixed size.
The Bidirectional LSTM layer allowed the model to learn from the input sequence in both forward and backward directions.
Dropout regularization was applied to prevent overfitting.
The output layer consisted of a single neuron with a sigmoid activation function, suitable for binary classification.

### Model Training:

The model was compiled with binary cross-entropy loss and the Adam optimizer.
The training data was fitted to the model using a batch size of 32 and for 10 epochs.
Validation data was used to monitor the model's performance during training.
Model Evaluation:

The model's performance was evaluated using the test data.
Predictions were obtained using the predict method, and then rounded to obtain binary predictions.
The accuracy of the model was computed using the accuracy_score function from scikit-learn.
