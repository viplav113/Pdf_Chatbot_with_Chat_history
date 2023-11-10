# langchain-openai-chainlit
Chat with your documents (pdf, csv, text) using Openai model, LangChain and Chainlit.  
In these examples, we’re going to build an chatbot QA app. We’ll learn how to:

- Upload a document
- Create vector embeddings from a file
- Create a chatbot app with the ability to display sources used to generate an answer
---

### Chat with your documents 🚀
- [OpenAI model](https://platform.openai.com/docs/models) as Large Language model
- [LangChain](https://python.langchain.com/en/latest/modules/models/llms/integrations/huggingface_hub.html) as a Framework for LLM
- [Chainlit](https://docs.chainlit.io/langchain) for deploying.

## System Requirements

You must have Python 3.11 or later installed. Earlier versions of python may not compile.  


## Steps to Replicate 

1. Fork this repository and create a codespace in GitHub as I showed you in the youtube video OR Clone it locally.


2. Get OpenAI API key from this [URL](https://platform.openai.com/account/api-keys). You need to create an account in OpenAI webiste if you haven't already.
   ```
   OPENAI_API_KEY=your_openai_api_key
   ```

3. Create a virtualenv and activate it
   ```
   python3 -m venv .venv && source .venv/bin/activate
   ```

   If you have python 3.11, then the above command is fine. But, if you have python version less than 3.11. Using conda is easier. First make sure that you have conda installed. Then run the following command.
   ```
   conda create -n .venv python=3.11 -y && source activate .venv
   ```

4. Run the following command in the terminal to install necessary python packages:
   ```
   pip install -r requirements.txt
   ```

5. Run the following command in your terminal to start the chat UI:
   ```
   chainlit run pdf_qa.py -w
   chainlit run txt_qa.py -w
   chainlit run pdf_txt_qa.py -w
   chainlit run csv_qa.py -w
   ```

