![DataKirk Logo](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/datakirk%20logo.png)
# Gen AI for Women: Getting Started with Langflow

# Agenda - 5 March, 2025

- **Introduction to Gen AI for Women & The DataKirk**
- **What is Langflow?**
- **Understanding Large Language Models (LLMs)**
- **Exercise**
- **Key Features of Langflow**
- **Installation & Setup**
- **Building Your First AI Flow**
- **Interactive AI Projects**
- **Q&A and Next Steps**


## About The DataKirk  
The DataKirk is committed to empowering communities with data literacy and AI skills. Through initiatives like the **Gen AI for Women** programme, we provide accessible education, hands-on training, and a pathway into AI-driven innovation.


## Introduction
Welcome to the **Gen AI for Women** programme! This guide will help you get started with **Langflow**, a powerful low-code visual framework for building AI applications. Whether you're a beginner or have some AI experience, Langflow provides an intuitive way to create, prototype, and deploy AI-powered workflows without extensive coding.

## What is a Large Language Model?
LLMs are AI systems used to model and process human language. They are called **“large”** because these types of models are normally made of hundreds of millions or even billions of parameters that define the model's behavior, which are pre-trained using a massive corpus of text data.


![llms](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/llms.png)
<div align="center">
    <strong>Source:</strong> [Information is beautiful](https://informationisbeautiful.net/visualizations/the-rise-of-generative-ai-large-language-models-llms-like-chatgpt/)
</div>

### Link to Exercise Dataset https://tinyurl.com/genaiw

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
![Parameters](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/parameters.png)

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
- **Tool-calling agent:** Uses the connected LLM to reason through the user's input and select among the connected tools to complete its task.
- **URL tool:**  Searches a list of URLs for content.
- **Calculator component:** Performs basic arithmetic operations.
- **Chat Input component:** Accepts user input to the chat.
- **Prompt component:** Combines the user input with a user-defined prompt.
- **Chat Output component:** Prints the flow's output to the chat.
- **Model component:** Sends the user input and prompt to the OpenAI API and receives a response.
- Run the Simple Agent Flow
- Add your credentials to the GROQ component.

Your sample agent flow should look like this:

![Agent](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/agent.png)

Click Playground to start a chat session.

To confirm the tools are connected, ask the agent:
"What tools are available to you?"

Now that your query has completed the journey from Chat Input to Chat Output, you have successfully built and run the Simple Agent Flow. 🎉


# AskMyDoc: Interactive Document Q&A  
**Build a chatbot that can answer questions based on a document loaded from local memory.**  


---

## 1. Create the AskMyDoc Flow  
1. From the **Langflow** dashboard, click **New Flow**.  
2. Select **Blank Flow** instead of a template.  
3. Manually add the required components (see next section).  

---

## 2. Add and Connect Components  
To build the **AskMyDoc** chatbot, add the following components and connect them as shown:  

### Required Components:  
- **Chat Input** – Takes user questions.  
- **Prompt** – Constructs the input query with document context.  
- **OpenAI** – Processes the prompt and generates responses.  
- **Chat Output** – Displays the chatbot’s response.  
- **File** – Loads a file from your local machine.  
- **Parse Data** – Converts file content into a format for the Prompt component.  

![AskMyDoc](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/askmydoc.png)


### Connection Flow:  
1. **Chat Input** → Connect to **Prompt**  
2. **File** → Connect to **Parse Data**  
3. **Parse Data** → Connect to **Prompt** as `{Document}`  
4. **Prompt** → Connect to **OpenAI**  
5. **OpenAI** → Connect to **Chat Output**  

> **How It Works:** The **Prompt component** ensures that OpenAI answers based on the document's content, giving it context it wouldn’t otherwise have.  

---

## 3. Run the AskMyDoc Flow  

### Load a Document:  
1. In the **File** component, click the **Path** field.  
2. Select a local file and click **Open**. The file name will appear in the field.  

### Start Chatting with the Document:  
1. Click the **Playground** button.  
2. Ask a question about the document’s content.  
3. The AI will generate a response based on the file’s data.  

## Congratulations!  
🎉 **You are now a Document Processing AI Expert!** 🎉

By completing the **AskMyDoc: Interactive Document Q&A** flow, you've mastered the process of creating an AI-powered chatbot capable of understanding and answering questions based on any document. You've learned how to integrate document loading, context-based responses, and real-time interactions with OpenAI. This skill will enable you to build dynamic, document-aware applications.  

Now that you've unlocked this powerful capability, keep experimenting with advanced features, and continue building more AI-driven solutions for enhanced document processing!
---

# **PostBuilder: AI-Powered Blog Generator**  
**Build a blog post using AI, by fetching content from URLs and transforming it into a fully written article.**

---

## 1. Create the PostBuilder Flow  
1. From the **Langflow** dashboard, click **New Flow**.  
2. Select **Blank Flow** instead of a template.  
3. Manually add the required components (see next section).  

---

## 2. Add and Connect Components  
To build the **PostBuilder** flow, add the following components and connect them as shown:  

### Required Components:  
- **Text Input** – Provides the instructions on what to write about.  
- **URL** – Fetches content from one or more URLs.  
- **Parse Data** – Converts the extracted content into plain text for the prompt.  
- **Prompt** – Structures the input with the extracted data and instructions.  
- **OpenAI** – Generates the blog post based on the processed input.  
- **Chat Output** – Displays the generated blog post.

### Connection Flow:  
1. **Text Input** → Connect to **Prompt**  
2. **URL** → Connect to **Parse Data**  
3. **Parse Data** → Connect to **Prompt** as `{References}`  
4. **Prompt** → Connect to **OpenAI**  
5. **OpenAI** → Connect to **Chat Output**  

> **How It Works:** The **Prompt component** combines instructions and fetched content to guide **OpenAI** in generating a coherent and relevant blog post.  

---

## 3. Run the PostBuilder Flow  

### Set Up Content:  
1. In the **URL** component, add one or more web URLs from which you want to fetch content.  
2. In the **Text Input** component, type in your instructions for the blog post (e.g., "Write a blog post about the benefits of electric cars").  

### Generate the Blog:  
1. Click the **Playground** button.  
2. Click the **Lightning Bolt** icon to run the flow.  
3. The AI will generate a blog post based on the content fetched from the URLs and your instructions.  

---

## Congratulations!  
🎉 **You are now a Blog Post AI Creator!** 🎉

By completing the **PostBuilder: AI-Powered Blog Generator** flow, you've learned how to build an AI-powered tool that can generate blog posts based on web content. You've mastered the process of extracting content from URLs, processing it with AI, and crafting detailed blog posts with ease. This skill unlocks endless possibilities for automating content creation and building sophisticated AI-powered writing tools.

Now that you've gained this ability, keep experimenting with more advanced features, and continue enhancing your AI-driven blog creation process!

---

# **Contextual Search AI: Advanced Retrieval Augmented Generation**  
Retrieval Augmented Generation, or RAG, is a powerful method for training LLMs (Large Language Models) on your own data and querying it effectively.

RAG is backed by a **vector store**, a vector database that stores embeddings of the ingested data. This enables **vector search**, a more context-aware and powerful search method for your queries.

![RAG FLOW](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/ragflow.png)

---

## A Broad Definition of RAG  
One way to understand RAG is by breaking it down into its three core components:  

**Generation**: This is what you get when working with a standard LLM without any tailored instructions or prompt engineering. For example, you might ask it, "Generate an image," and it will respond with whatever it understands, which may not always be what you expect.  

**Augmentation**: Augmentation involves adding specific instructions to guide the LLM. What are the boundaries? What should it or shouldn't it include in its responses?  

**Retrieval**: Retrieval refers to fetching relevant information from a database or another external source. This allows the LLM to incorporate real-world data into its responses, improving accuracy and relevance.  

When these three elements are combined, you get enhanced, context-aware results from your queries.

![Embeddings](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/embeddings.png)  
![Embeddings](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/embeddings2.png)  
![Vector](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/vector.png)  
![Vector](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/vectordb.png)  
![Search](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/vectorsearch.png)  
![Rag](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/rag.png)  
![RAG](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/ragvec.png)

---

## Prerequisites  
- An **GROQ** API key  
- An **Astra DB** vector database with the following:  
  - An **Astra DB application token** scoped to read and write to the database  
  - A **collection** created in Astra, or create a new collection  
- Open **Langflow** and start a new project  
- From the **Langflow** dashboard, click **New Flow**  
- Select **Contextual Search AI**  

---

## 1. Build the Contextual Search AI Flow  
This flow is divided into two separate parts: **Load Data Flow** and **Retriever Flow**.

### Load Data Flow  
This flow creates a searchable index, populated with data from a local file. It ingests data, splits it into chunks, and indexes it in **Astra DB** while computing embeddings for the chunks using the **OpenAI embeddings model**.

### Retriever Flow  
The Retriever Flow takes user queries, embeds them into vectors, and compares them with data in the **Astra DB vector store** to find contextually similar data.

![RAG STORE](https://github.com/azeemite1/GEN-AI-WOMEN/blob/main/asset/ragflow.png)

---

## 2. Connect the Components  

The **Contextual Search AI** flow is composed of the following components:

1. **Chat Input** – Receives user input in the Playground.  
2. **OpenAI Embeddings** – Converts the user query into vector form.  
3. **Astra DB** – Performs similarity search on the query vector.  
4. **Parse Data** – Processes the retrieved chunks.  
5. **Prompt** – Combines the user query with relevant context.  
6. **OpenAI** – Generates the final response using the prompt.  
7. **Chat Output** – Returns the AI-generated response.

---

## 3. Run the Contextual Search AI Flow  

### Load Your Data:  
1. In the **Load Data Flow**, provide the file from which the system should ingest data.  
2. The system will process and index the data into the vector store.  

### Start Querying:  
1. Go to the **Retriever Flow**.  
2. Enter a query in the **Chat Input** and click **Run**.  
3. The AI will retrieve relevant information based on the context of the query and the stored data, and generate a response.

---

## 4. Next Steps & Enhancements  
- **Refine Similarity Search**: Fine-tune the **Retriever Flow** to enhance contextual accuracy.  
- **Integrate More Data Sources**: Add more data sources and make the system more robust.  
- **Leverage Embeddings**: Use advanced **embeddings** for better query processing and retrieval.

---

## Congratulations!  
🎉 **You are now an Expert in Context-Aware AI Retrieval!** 🎉

By completing the **Contextual Search AI** flow, you've gained a valuable skill in building AI systems that retrieve and process data intelligently using vector-based search. You’ve learned how to use **RAG** to enhance LLM outputs by integrating context from your own data. With this foundational knowledge, you're now ready to dive deeper into **advanced retrieval strategies** and more sophisticated use cases.

Keep building and experimenting with AI-powered solutions to unlock even more potential in your projects!

Happy building! 🚀

---




