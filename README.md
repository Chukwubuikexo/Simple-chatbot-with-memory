# Chatbot with Summarizing Messages and Memory

This ipynb file that demonstrates how to build a chatbot with memory capabilities using the LangChain and Google Generative AI models. The chatbot is designed to maintain a conversation history and summarize the conversation when it exceeds a certain length. This is particularly useful for long conversations where summarizing the key points can help maintain context and improve the chatbot's responses.

## Features

- **Conversation Memory**: The chatbot maintains a memory of the conversation, allowing it to reference previous messages and provide contextually relevant responses.
- **Summarization**: When the conversation exceeds a predefined length (6 messages in this example), the chatbot summarizes the conversation to maintain context.
- **Google Generative AI**: The chatbot uses Google's Gemini Pro model for generating responses.
- **LangGraph Integration**: The chatbot leverages LangGraph for managing the conversation state and conditional logic.

## Requirements

To run this notebook, you will need the following:

- Python 3.10
- Jupyter Notebook
- Google API Key
- LangChain API Key

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/chatbot-with-summarizing-memory.git
   cd chatbot-with-summarizing-memory
   ```

2. **Set Up Environment Variables**:
   - Create a `.env` file in the root directory and add your Google API Key and LangChain API Key:
     ```plaintext
     GOOGLE_API_KEY=your_google_api_key
     LANGCHAIN_API_KEY=your_langchain_api_key
     ```


## Code Overview

- **Environment Setup**: The notebook starts by setting up the environment variables and importing necessary libraries.
- **Model Initialization**: The Google Generative AI model is initialized using the `ChatGoogleGenerativeAI` class.
- **State Management**: The `State` class is used to manage the conversation state, including the messages and the summary.
- **Message Handling**: The `calling_model` function is responsible for generating responses based on the conversation history.
- **Summarization**: The `summarize_conversation` function summarizes the conversation when it exceeds the predefined length.
- **Conditional Logic**: The `should_continue` function determines whether to continue the conversation or summarize it.
- **Graph Construction**: The `StateGraph` is used to construct the conversation workflow, including nodes for message handling and summarization.
- **Memory Management**: The `MemorySaver` class is used to save the conversation state in memory.

## Example Output

The notebook includes example outputs from the chatbot, demonstrating how it maintains context and summarizes the conversation.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request if you have any improvements or suggestions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [LangChain](https://langchain.com/) for providing the tools to build conversational AI.
- [Google Generative AI](https://ai.google/) for the powerful language model used in this project.

