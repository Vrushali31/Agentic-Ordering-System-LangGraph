# 🛒 ShopBot: LangGraph-Based Shopping Assistant

ShopBot is an interactive, AI-powered virtual shopping assistant built using [LangGraph](https://www.langchain.com/langgraph), [LangChain](https://www.langchain.com/), and the Gemini API. It guides users through browsing available products, adding/removing items from the cart, and checking out with a calculated total — all via natural language.

## 🚀 Features

- 💬 Conversational interface powered by Gemini (`gemini-2.0-flash`)
- 🛍️ Real-time cart management (add, remove, view)
- 🧮 Checkout with total price calculation
- 🔧 Tool-augmented LLM using LangGraph nodes
- 🎯 Clear modular design for extending to new product categories or actions

---

## 🧠 How It Works

The system is structured as a LangGraph state machine, where:
- **Nodes** represent chatbot actions (chatbot, tools, ordering logic, human input)
- **Edges** are conditional based on tool calls or exit commands
- **Tools** enable structured function calling (e.g., `add_to_cart`, `checkout`)

Conversation flow:
1. User starts interaction → chatbot sends welcome message.
2. Based on user message, tools like `get_products` or `add_to_cart` are invoked.
3. The cart is updated and confirmed before checkout.
4. At checkout, the total is calculated and shown.
5. The conversation ends after a thank-you message.

---

## 🛠️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/Vrushali31/Agentic-Ordering-System-LangGraph
cd Agentic-Ordering-System-LangGraph
```

### 2. Create virtual environment
``` bash
python -m venv venv
source venv/bin/activate   # or `venv\Scripts\activate` on Windows
```
### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

Make sure to install:

- langgraph

- langchain

- langchain-google-genai

- IPython (for notebook support)

### 4. Set up Gemini API

``` python
import os
os.environ["GOOGLE_API_KEY"] = "your_gemini_api_key"
```
### 5. Running the App

Run the main script or execute all cells in the provided Jupyter notebook.

``` python
config = {"recursion_limit": 200}
state = graph_with_order_tools.invoke({"messages": []}, config)
```
Type natural-language queries like:

- "What products are available"

- "I want to buy a laptop"

- "Add shampoo"

- "What’s in my cart?"

- "Checkout"

## File Structure

```bash
.
├── shopbot.ipynb            # Main app file
├── requirements.txt         # Python dependencies
├── README.md                # Project documentation

```
## 📜 License

This project is open-source under the [MIT License](./LICENSE)

## 🙌 Acknowledgements
[LangChain](https://www.langchain.com/) & [LangGraph](https://www.langchain.com/langgraph)

[Building an Agent with LangGraph by Google](https://www.kaggle.com/code/markishere/day-3-building-an-agent-with-langgraph/)





