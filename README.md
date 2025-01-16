# Smart Assistant

## Description
Smart Assistant is a Python application that simulates a digital assistant. Users can interact with the assistant using text-based queries and receive responses. The program can learn new answers to unknown questions and save this knowledge for future interactions.

## Features
- **Greetings:** The assistant provides friendly greetings upon start.
- **Basic Responses:** It can provide the current time and date.
- **Learning Capability:** Learns from user interactions and stores learned responses in a knowledge base.
- **Question Matching:** Uses TF-IDF and cosine similarity to find similar questions in the knowledge base.
- **Knowledge Base:** Stores responses in a `knowledge.json` file.
- **Sentiment Analysis:** Analyzes user sentiment in responses and adjusts knowledge based on feedback.

## How to Use
1. Run the script with the following command:
   ```
   python filename.py
   ```
2. The assistant will greet you and prompt you to ask a question.
3. Type your query. If the assistant doesn’t know the answer, it will offer to learn a new response.
4. To end the interaction, type `exit`.

## Program Structure

### `SmartAssistant` Class
- **`__init__`:** Initializes the assistant's name, greetings, knowledge base, and conversation history.
- **`load_knowledge`:** Loads saved knowledge from `knowledge.json`.
- **`save_knowledge`:** Saves the current knowledge to a file.
- **`learn_from_interaction`:** Learns a new response based on user feedback.
- **`analyze_sentiment`:** Performs a simple sentiment analysis to gauge the tone of user responses.
- **`find_similar_question`:** Finds a similar question in the knowledge base using TF-IDF and cosine similarity.
- **`get_best_response`:** Selects the best response based on its rating and usage count.
- **`process_query`:** Generates a response to the user’s query.
- **`get_time`:** Returns the current time.
- **`get_date`:** Returns today’s date.

### `main` Function
- Initializes the assistant.
- Facilitates user interaction through the console.
- Offers the option to teach the assistant a new response if it doesn’t know the answer.
- Uses sentiment analysis to improve response quality.

## Dependencies
- Python 3.7 or newer
- Libraries: `random`, `datetime`, `json`, `collections`, `numpy`, `sklearn`

## Knowledge Base Format
The knowledge base is stored in `knowledge.json` in the following format:
```json
{
  "query": [
    {
      "response": "response",
      "score": 1,
      "uses": 1
    }
  ]
}
```

## Planned Improvements
- Expand the knowledge base with diverse topics.
- Enhance natural language processing capabilities.
- Add export and import functionality for the knowledge base.

## Author
This program was developed by Lukáš Drštička. It is freely available for further development and improvement.

