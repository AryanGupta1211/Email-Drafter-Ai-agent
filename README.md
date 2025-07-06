# Drafter AI: Your Smart CLI Email Assistant

**Drafter AI** is a powerful, command-line based AI agent that revolutionizes your email writing process. Leveraging the capabilities of LangChain and LangGraph, this tool helps you generate high-quality emails, refine them with a human-in-the-loop feedback system, and save the final version directly to your local machine. Say goodbye to writer's block and time-consuming edits!

## ✨ Features

- **🤖 AI-Powered Generation:** Quickly generate email drafts for any purpose.
- **🔄 Iterative Feedback Loop:** Not perfect on the first try? Provide feedback and let the agent refine the draft until it meets your standards.
- **💾 Local Storage:** Save your finalized emails as `.txt` files for easy access and record-keeping.
- **👨‍💻 Purely CLI:** A lightweight, fast, and efficient command-line interface that integrates seamlessly into your workflow.
- **🔧 Extensible:** Built with LangGraph, the agent's reasoning and drafting process can be easily customized and extended.

## ⚙️ How It Works

Drafter AI uses a state machine built with LangGraph to manage the email creation process. The flow is designed to be intuitive and cyclical, ensuring you have full control over the final output.


```
            +------------------+
            |      START       |
            +------------------+
                   |
                   v
      +---------------------------+
      |  User provides a prompt   |
      +---------------------------+
                   |
                   v
+-----> +---------------------------+
|       |  Agent generates/revises  |
|       |        email draft        |
|       +---------------------------+
|                    |
|                    v
|       +---------------------------+
|       |   Present draft to user   |
|       +---------------------------+
|                    |
|                    v
|       +---------------------------+
|       |  User provides feedback?  |
|       +-----------+---------------+
|                   |
+------------------(Yes)
                    |
                   (No)
                    |
                    v
      +---------------------------+
      | Save final email to .txt  |
      +---------------------------+
                   |
                   v
            +------------------+
            |       END        |
            +------------------+
```

## 🛠️ Tech Stack

- **Core Framework:** Python
- **AI Orchestration:** [LangChain](https://python.langchain.com/)
- **Agent Logic:** [LangGraph](https://python.langchain.com/docs/langgraph)
- **LLM:** Groq LangChain-compatible model

## 🚀 Getting Started

### Prerequisites

- Python 3.11+
- An API key for your chosen Large Language Model (LLM) provider (e.g., GROQ).

### Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/AryanGupta1211/Email-Drafter-Ai-agent
    cd Email-Drafter-Ai-agent
    ```

2.  **Create a virtual environment and install dependencies:**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    pip install langchain langchain-groq langgraph python-dotenv
    ```

3.  **Configure your environment:**
    Create a `.env` file in the root directory and add your LLM API key:
    ```
    GROQ_API_KEY="your-api-key-here"
    ```

### Usage

Run the agent from your terminal with a prompt for the email you want to create.

```bash
python drafter.py
```

The agent will then guide you through the drafting and feedback process.

## 🤝 Contributing

Contributions are welcome! Whether it's a bug report, a new feature, or an improvement to the documentation, please feel free to open an issue or submit a pull request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

Please make sure to update tests as appropriate.

## 🙏 Acknowledgments

- The teams behind LangChain and LangGraph for their incredible open-source tools.
