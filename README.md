# 🤖 LangGraph Agentic AI Chatbot

A comprehensive end-to-end project demonstrating agentic AI chatbots built with LangGraph, featuring both basic conversational capabilities and advanced web search integration.

## 🚀 Features

### Core Capabilities
- **Basic Chatbot**: Simple conversational AI using Groq LLM models
- **Chatbot with Web Search**: Advanced chatbot with Tavily web search integration
- **Streamlit UI**: Modern, interactive web interface
- **Modular Architecture**: Clean, maintainable code structure
- **Multiple LLM Models**: Support for various Groq models (llama3-8b-8192, llama3-70b-8192, gemma2-9b-it)

### Technical Features
- **LangGraph Integration**: Stateful conversation management
- **Tool Integration**: Web search capabilities using Tavily API
- **Error Handling**: Robust exception handling throughout the application
- **Configuration Management**: Centralized configuration system
- **Real-time Streaming**: Live response streaming in the UI

## 📁 Project Structure

```
Chatbot_with_Web/
├── app.py                          # Main application entry point
├── requirements.txt                # Python dependencies
├── README.md                       # Project documentation
└── src/
    └── langgraphagenticai/
        ├── main.py                 # Application orchestration
        ├── LLMS/
        │   └── groqllm.py         # Groq LLM integration
        ├── graph/
        │   └── graph_builder.py   # LangGraph construction
        ├── nodes/
        │   ├── basic_chatbot_node.py      # Basic chatbot logic
        │   └── chatbot_with_Tool_node.py  # Tool-enhanced chatbot
        ├── state/
        │   └── state.py           # State management
        ├── tools/
        │   └── search_tool.py     # Web search tools
        └── ui/
            ├── streamlitui/
            │   ├── loadui.py      # UI initialization
            │   └── display_result.py      # Result display
            ├── uiconfigfile.ini   # Configuration file
            └── uiconfigfile.py    # Configuration parser
```

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.8 or higher
- Groq API key (get from [console.groq.com/keys](https://console.groq.com/keys))
- Tavily API key (get from [app.tavily.com/home](https://app.tavily.com/home)) - for web search feature

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/ashoksaidoredlaumbc/Agentic_AI_Chatbot.git
   cd Chatbot_with_Web
   ```

2. **Create and activate virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   streamlit run app.py
   ```

## 🎯 Usage

### Starting the Application
1. Run `streamlit run app.py` to start the Streamlit server
2. Open your browser and navigate to the provided URL (typically `http://localhost:8501`)

### Using the Chatbot

#### Basic Chatbot
1. Select "Groq" as the LLM provider
2. Choose your preferred model (llama3-8b-8192, llama3-70b-8192, or gemma2-9b-it)
3. Enter your Groq API key
4. Select "Basic Chatbot" as the use case
5. Start chatting in the chat interface

#### Chatbot with Web Search
1. Follow steps 1-3 from Basic Chatbot
2. Select "Chatbot With Web" as the use case
3. Enter your Tavily API key
4. Ask questions that require current information or web search

### Example Conversations

**Basic Chatbot:**
- "What is artificial intelligence?"
- "Tell me a joke"
- "Explain machine learning concepts"

**Chatbot with Web Search:**
- "What are the latest developments in AI?"
- "Find information about current weather in New York"
- "What are the trending topics in technology today?"

## 🔧 Configuration

The application uses a configuration file (`src/langgraphagenticai/ui/uiconfigfile.ini`) to manage:
- Available LLM options
- Use case options
- Groq model options
- Page title

You can modify this file to add new models or use cases.

## 🏗️ Architecture Overview

### Core Components

1. **Main Application (`main.py`)**
   - Orchestrates the entire application flow
   - Handles user input and error management
   - Coordinates between UI, LLM, and graph components

2. **Graph Builder (`graph_builder.py`)**
   - Constructs LangGraph workflows
   - Supports multiple use cases with different node configurations
   - Manages state transitions and conditional edges

3. **LLM Integration (`groqllm.py`)**
   - Handles Groq API integration
   - Manages model selection and API key validation
   - Provides unified LLM interface

4. **UI Components**
   - **LoadUI**: Handles user interface initialization and input collection
   - **DisplayResult**: Manages result presentation and streaming

5. **Node Implementations**
   - **BasicChatbotNode**: Simple conversational responses
   - **ChatbotWithToolNode**: Enhanced with tool integration capabilities

6. **Tools (`search_tool.py`)**
   - Integrates Tavily search for web-based information retrieval
   - Provides tool nodes for LangGraph integration

### State Management
The application uses a typed state system (`State`) that manages conversation messages and ensures proper state transitions throughout the graph execution.

## 🔒 Security & API Keys

- **Groq API Key**: Required for LLM functionality
- **Tavily API Key**: Required for web search capabilities
- API keys are handled securely through password input fields
- No keys are stored permanently in the application

## 🐛 Troubleshooting

### Common Issues

1. **API Key Errors**
   - Ensure you have valid API keys for both Groq and Tavily
   - Check that keys are entered correctly without extra spaces

2. **Model Loading Issues**
   - Verify your Groq API key has access to the selected model
   - Check your internet connection

3. **Streamlit Issues**
   - Ensure all dependencies are installed correctly
   - Check that the virtual environment is activated

### Error Messages
- The application includes comprehensive error handling
- Error messages are displayed in the Streamlit interface
- Check the console for additional debugging information

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- Built with [LangGraph](https://github.com/langchain-ai/langgraph)
- Powered by [Groq](https://groq.com/) LLM models
- Web search powered by [Tavily](https://tavily.com/)
- UI built with [Streamlit](https://streamlit.io/)

---

