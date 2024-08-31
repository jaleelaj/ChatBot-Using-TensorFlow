
# ChatBot Using TensorFlow

## Overview
This project is a simple chatbot implementation using TensorFlow and Keras. The bot is trained on a set of predefined intents, which allows it to understand user input and respond with appropriate responses. The model is a neural network that uses word embeddings and is designed to classify the user's input into one of several intent categories.

## Features
- **Text Classification**: The bot can classify input sentences into predefined categories (intents).
- **Word Embeddings**: The model uses embeddings to convert words into numerical vectors that can be processed by the neural network.
- **Sequential Model**: The bot is built using a simple Sequential model from Keras.
- **Customizable**: You can easily update the intents and responses in the `intents.json` file.

## Project Structure
```
.
├── chat_model                    # Saved model file after training
├── intents.json                  # JSON file containing the intents, patterns, and responses
├── label_encoder.pickle          # Pickle file containing the trained label encoder
├── tokenizer.pickle              # Pickle file containing the trained tokenizer
├── chatbot.py                    # Main script to train and run the chatbot
└── README.md                     # This README file
```

## Getting Started

### Prerequisites
- Python 3.x
- TensorFlow
- Keras
- scikit-learn
- numpy
- colorama
2. **Install the required packages**:
    ```
    pip install -r requirements.txt
    ```

3. **Prepare your intents**:
    - The `intents.json` file contains the training data for the bot. You can modify it to include more intents, patterns, and responses.

### Training the Model

To train the model, simply run the `chatbot.py` script:

```bash
python chatbot.py
```

This will load the training data, preprocess it, and train a neural network model. The trained model, along with the tokenizer and label encoder, will be saved for future use.

### Using the Chatbot

After training the model, you can start a conversation with the bot by running the `chatbot.py` script:

```bash
python chatbot.py
```

The bot will continuously take user input until you type "quit" to exit the chat.

## Customization

- **Adding New Intents**: To add new intents, update the `intents.json` file with new patterns and responses. Make sure to retrain the model after making changes to this file.
  
- **Modifying the Model**: If you want to experiment with different architectures, you can modify the neural network defined in the `chatbot.py` script.

## Example Intents

Here's a snippet of what the `intents.json` file looks like:

```json
{
    "intents": [
        {
            "tag": "greeting",
            "patterns": ["Hi", "Hello", "How are you?"],
            "responses": ["Hello!", "Hi there!", "Greetings!"]
        },
        {
            "tag": "goodbye",
            "patterns": ["Bye", "See you later", "Goodbye"],
            "responses": ["Goodbye!", "See you later!", "Take care!"]
        }
        // Add more intents here
    ]
}
```

## Contributing
If you'd like to contribute to this project, feel free to fork the repository and submit a pull request. Please ensure that your code adheres to the project's coding standards and is well-documented.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements
This project was inspired by various chatbot tutorials and TensorFlow examples.
