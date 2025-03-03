![DataKirk Logo](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/datakirk%20logo.png)
# Gen AI for Women: Getting Started with Langflow

## About The DataKirk  
The DataKirk is committed to empowering communities with data literacy and AI skills. Through initiatives like the **Gen AI for Women** programme, we provide accessible education, hands-on training, and a pathway into AI-driven innovation.


## Introduction
Welcome to the **Gen AI for Women** programme! This guide will help you get started with **Langflow**, a powerful low-code visual framework for building AI applications. Whether you're a beginner or have some AI experience, Langflow provides an intuitive way to create, prototype, and deploy AI-powered workflows without extensive coding.

## What is a Large Language Model?
LLMs are AI systems used to model and process human language. They are called **“large”** because these types of models are normally made of hundreds of millions or even billions of parameters that define the model's behavior, which are pre-trained using a massive corpus of text data.





## But wait 🤔, What is a Parameter?😒😒
LLMs are based on models called neural networks. But let’s ignore the terminology for now and focus on a simpler example. Suppose you’re an estate agent estimating the value of a house. You’ve seen lots of houses sold recently, and have come up with a simple rule of thumb that says the price of a house is roughly £75,000 for each room in the house. You can write this in a formula that says:

<div align="center">
House price = 75000 * number of rooms
</div>

There’s one input— that’s the number of rooms. The other number — £75,000 — is a parameter. Perhaps next year, house prices will go up and you’ll update the parameter to £78,000. This formula gives you the flexibility to do that.

Your colleague has come up with a different rule. They believe that it’s not the number of rooms in the house that matters, but the number of bedrooms and the size of the garden. Their formula has two inputs and parameters:

<div align="center">
House price = 75000 * number of rooms + 100 * garden size
</div>

Both of these formulas are models for estimating house prices. When the house down the road gets sold, you could compare your model’s prediction of house price with the price that it actually sold for. You could even have a competition with your colleague where you find a list of recently sold houses in the area and see which of the two models estimates house prices that are closest to the actual value they sold for.

Having discovered that neither model is very accurate, you could come up with a longer list of inputs that impact house prices, like how far away the nearest school is and the age of the house. By adding more and more inputs & parameters to your model, and adjusting the values of the parameters, your model might get better and better house price estimates.

Suppose that you and your colleague settle on 7 inputs that you believe are the most important to house prices.




The inputs are on the left. Each blue arrow multiplies an input by a parameter, and then all are added together to give the estimated house price at the green arrow. In this diagram, there are 7 parameters, and those 7 parameters can be adjusted until you land on a good model.

So, a parameter is a number inside a model that we can adjust to make it more or less accurate. With 7 inputs we’d hope to make the model more accurate than with just 1 or 2. But we couldn’t create a model that took into account all the factors that affect house price and the random fluctuations that sometimes happen!

## Lets see some Live AI data 📊

You can view and interact with the dataset here:  
[Open Google Sheet](https://docs.google.com/spreadsheets/d/1kc262HZSMAWI6FVsh0zJwbB-ooYvzhCHaHcNUiA0_hY/edit?gid=38726112)


## What is Langflow?
Langflow is an **open-source**, Python-powered visual tool for building **multi-agent** and **Retrieval-Augmented Generation (RAG)** applications. It allows users to easily create AI workflows by connecting different components, such as language models, data sources, and prompts, through a **drag-and-drop interface**.

## Visual flow builder
Langflow is an **intuitive visual flow builder**. This drag-and-drop interface allows developers to create complex AI workflows **without writing extensive code.** You can easily connect different components, such as prompts, language models, and data sources, to build sophisticated AI applications.

![Langflow](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/langflow.png)

### **Key Features:**
- **No-Code & Low-Code AI Development** – Build AI-powered workflows without needing extensive programming skills.
- **Visual Flow Builder** – Drag and drop components to create complex AI solutions.
- **Multi-Agent Support** – Build AI applications that involve multiple interacting agents.
- **LLM & Vector Store Agnostic** – Works with different Large Language Models (LLMs) and data stores.
- **Customizable & Extensible** – Adapt workflows to specific needs with ease.

## Use Cases
Langflow can be used for a variety of AI applications, including:
- 🤖 **Chatbot Development** – Create intelligent chatbots.
- 📄 **Document Analysis** – Extract insights from documents.
- ✍️ **Content Generation** – Automate text creation.
- 🧠 **Multi-Agent Orchestration** – Build systems that integrate multiple AI agents.

---
## Installation Guide
You can install and run **Langflow** locally on your laptop. Please ensure your system meets the following **prerequisites**.

### **System Requirements**
- Python **3.10 - 3.13**
- Package managers: **uv**, **pip**, or **pipx**
- Chromium-based browser (Google Chrome, Edge, Brave, etc.)

### **Step 1: Set Up Your Environment**
It's recommended to create a virtual environment before installing Langflow. Use one of the following methods:

#### **Option 1: Install using uv (Recommended)**
```sh
uv pip install langflow
```

#### **Option 2: Install using pip**
```sh
python -m pip install langflow
```

#### **Option 3: Install using pipx**
```sh
pipx install langflow --python python3.10
```

### **Step 2: Running Langflow**
Once installed, you can start Langflow using the following command:
```sh
uv run langflow run
```
Or, if using pip:
```sh
python -m langflow run
```
After running, open your browser and go to **[http://127.0.0.1:7860](http://127.0.0.1:7860)** to access the Langflow interface.

---
## Getting Started: Building Your First AI Flow
### **Step 1: Create a New Flow**
1. Open Langflow in your browser.
2. Click **New Flow** → **Blank Flow** (or choose a pre-built template like **Basic Prompting**).
3. A blank workspace will appear, ready for building.

### **Step 2: Build a Basic Chatbot Flow**
1. **Add Chat Input:** Drag the **Chat Input** component to the canvas.
2. **Add Prompt:** Drag the **Prompt** component and connect it to the **Chat Input**.
3. **Add AI Model:** Drag the **GROQ** component, connecting it to the **Prompt**.
4. **Add Chat Output:** Drag the **Chat Output** component and connect it to the **AI Model**.

Your basic prompting flow should look like this:

![Basic Prompt](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/starter.png)

### **Step 3: Run Your Chatbot**
1. **Add GROQ API Key**: Go to **Settings > Global Variables**, create a new variable, and paste your GROQ API key.
2. **Set a Prompt**: In the **Prompt** component, add instructions like:
   ```
   Answer the user as if you were a Gen AI expert, enthusiastic about helping them get started.
   ```
3. **Click Playground** and start chatting with your AI bot!

---

## Agents overview
Agents are AI systems that use LLMs as a brain to analyze problems and select external tools.

Instead of developers having to create logical statements to direct every possible path of a program, an agent can operate with autonomy. An agent can leverage external tools and APIs to gather information and take action, demonstrate chain-of-thought reasoning, and generate tailored text for specific purposes.

---
## Simple Agent
Build a Simple Agent flow for an agentic application using the Tool-calling agent component.

An agent uses an LLM as its "brain" to select among the connected tools and complete its tasks.

In this flow, the Tool-calling agent reasons using an OpenAI LLM. The agent selects the Calculator tool for simple math problems and the URL tool to search a URL for content.

## Prerequisites
To use this flow, you need an GROQ API key.

Open Langflow and Start a New Flow
Click New Flow, and then select Simple Agent flow.
This opens a starter flow with the necessary components to run an agentic application using the Tool-calling agent.

## Simple Agent Flow Components
Tool-calling agent: Uses the connected LLM to reason through the user's input and select among the connected tools to complete its task.
URL tool: Searches a list of URLs for content.
Calculator component: Performs basic arithmetic operations.
Chat Input component: Accepts user input to the chat.
Prompt component: Combines the user input with a user-defined prompt.
Chat Output component: Prints the flow's output to the chat.
OpenAI model component: Sends the user input and prompt to the OpenAI API and receives a response.
Run the Simple Agent Flow
Add your credentials to the GROQ component.

Your sample agent flow should look like this:

![Agent](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/agent.png)

Click Playground to start a chat session.

To confirm the tools are connected, ask the agent:
"What tools are available to you?"

Now that your query has completed the journey from Chat Input to Chat Output, you have successfully built and run the Simple Agent Flow. 🎉


## Vector store RAG
Retrieval Augmented Generation, or RAG, is a pattern for training LLMs on your data and querying it.

RAG is backed by a vector store, a vector database which stores embeddings of the ingested data.

This enables vector search, a more powerful and context-aware search.


## A broad definition of RAG
One helpful way to think about RAG is to look at its individual elements backwards. **“Generation”** is what you get when working with an LLM with no tailoring or prompt engineering. You might ask it a question like **“generate an image,”** and it does just that, and the response might—or might not—be what you had hoped for. 

**“Augmentation”** is all about adding some more detailed instructions for the LLM. What are the boundaries it should adhere to? How should it or shouldn’t respond?

Then the **“retrieval”** part is about fetching information from somewhere else, like a database or other sources. When you put the three parts together, you get better, more accurate results from your prompts.  

![Embeddings](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/embeddings.png)
![Embeddings](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/embeddings2.png)
![Vector](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/vector.png)
![Vector](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/vectordb.png)
![Search](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/vectorsearch.png)
![Rag](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/rag.png)
![RAG](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/ragvec.png)


Prerequisites
An GROQ API key
An Astra DB vector database with the following:
An Astra DB application token scoped to read and write to the database
A collection created in Astra or a new collection created in the Astra DB component
Open Langflow and start a new project
From the Langflow dashboard, click New Flow.
Select Vector Store RAG.
The Vector Store RAG flow is created.
Build the vector RAG flow
The vector store RAG flow is built of two separate flows for ingestion and query.

The Load Data Flow (bottom of the screen) creates a searchable index to be queried for contextual similarity. This flow populates the vector store with data from a local file. It ingests data from a local file, splits it into chunks, indexes it in Astra DB, and computes embeddings for the chunks using the OpenAI embeddings model.

The Retriever Flow (top of the screen) embeds the user's queries into vectors, which are compared to the vector store data from the Load Data Flow for contextual similarity.

Chat Input receives user input from the Playground.
OpenAI Embeddings converts the user query into vector form.
Astra DB performs similarity search using the query vector.
Parse Data processes the retrieved chunks.
Prompt combines the user query with relevant context.
OpenAI generates the response using the prompt.
Chat Output returns the response to the Playground.



---
## Additional Resources
- 📖 **[Langflow Documentation](https://github.com/logspace-ai/langflow)**
- 💬 **[Langflow Community & Support](https://discord.com/invite/langflow)**
- 🚀 **[Langchain](https://python.langchain.com/en/latest/)** (For more advanced AI workflows)

## Conclusion
By completing this guide, you have successfully set up Langflow and built a basic AI workflow. As part of the **Gen AI for Women** program, continue experimenting with Langflow to create more advanced AI applications.

Happy building! 🚀

