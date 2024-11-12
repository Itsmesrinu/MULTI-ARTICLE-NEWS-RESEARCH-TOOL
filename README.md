
# Multi-Article News Research Tool

A user-friendly tool designed to streamline the retrieval of insights from multiple news articles. This application allows users to input article URLs and ask targeted questions, receiving relevant information from the stock market and financial domain. Built with Gen AI, LangChain, OpenAI embeddings, and FAISS, this tool efficiently processes and indexes article content for quick and accurate responses.

## Project Overview

Multi-Article News Research Tool is designed for users interested in financial markets, allowing them to analyze content from multiple sources with ease. By utilizing Retrieval-Augmented Generation (RAG) and a combination of advanced AI technologies, the tool offers reliable and rapid responses, giving users valuable insights from various articles in a single interface.

## Features

- **URL Loading**: Load multiple URLs or text files containing URLs to fetch article content.
- **Content Processing**: Uses LangChain’s UnstructuredURL Loader for consistent data structuring and processing.
- **Embedding Vector Construction**: Generates embeddings using OpenAI’s API, converting articles into vectorized representations for similarity searches.
- **Efficient Retrieval**: Leverages FAISS to quickly search and retrieve relevant content based on user queries.
- **LLM Interaction**: Allows users to ask questions in natural language and get responses powered by ChatGPT, including links to source articles.
- **Persistent Indexing**: Stores embeddings using FAISS and saves indexes locally for fast, future use.
- **User-Friendly Interface**: Built with Streamlit, allowing easy access to input URLs, process data, and interact with retrieved insights.

## Technologies Used

- **LangChain**: For consistent content loading and processing.
- **OpenAI Embeddings**: To create vector embeddings of article content, representing context and meaning in numerical form.
- **FAISS (Facebook AI Similarity Search)**: For indexing and retrieving similar content based on embeddings.
- **Streamlit**: Provides an interactive, user-friendly web interface.
- **ChromaDB**: For advanced vector database management.
- **MySQL**: Optional database for handling structured data like user queries and saved article URLs.
- **Google PaLM 2**: Used for testing alternative open-source models.

## Technical Overview

The tool relies on a Retrieval-Augmented Generation (RAG) architecture, a popular method in AI applications. By combining external data sources with generative AI, RAG enables the tool to provide well-informed responses to user queries.

### Technical Architecture

- **Framework**: LangChain
- **Vector Database**: FAISS
- **UI Framework**: Streamlit
- **Embedding Model**: OpenAI embeddings

## Project Structure

- `main.py`: Main application script for the Streamlit interface.
- `requirements.txt`: Lists required Python packages for installation.
- `faiss_store_openai.pkl`: Pickle file for storing the FAISS index of embeddings.
- `.env`: Stores the OpenAI API key configuration.

## Setup and Installation

1. **Clone the repository**:

    ```bash
    git clone https://github.com/Itsmesrinu/MULTI-ARTICLE-NEWS-RESEARCH-TOOL.git
    ```

2. **Navigate to the project directory**:

    ```bash
    cd multi-article-news-research-tool
    ```

3. **Install dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

4. **Set up your OpenAI API key**:

    Create a `.env` file in the project root and add your OpenAI API key:

    ```plaintext
    OPENAI_API_KEY=your_api_key_here
    ```

## Usage

1. **Run the Streamlit application**:

    ```bash
    streamlit run main.py
    ```

2. **Interact with the web app**:
   - The app will open in your browser.
   - On the sidebar, input URLs or upload a text file with URLs.
   - Click **Process URLs** to load, split, and embed content.
   - Ask questions in the input field and receive answers based on the content of loaded articles.

## Example Workflow

- Load articles from URLs on the sidebar.
- The system will split the text, create embedding vectors, and index them using FAISS.
- The FAISS index is saved locally, allowing future retrieval without reprocessing.
- Users can ask questions based on the content of the indexed articles, and the tool will return relevant answers along with article URLs for context.

## Example Articles Used

- [^1]: [Tata Motors Gains Certificates for Production-Linked Payouts](https://www.moneycontrol.com/news/business/tata-motors-mahindra-gain-certificates-for-production-linked-payouts-11281691.html)
- [^2]:[Tata Motors Launches Punch ICNG](https://www.moneycontrol.com/news/business/tata-motors-launches-punch-icng-price-starts-at-rs-7-1-lakh-11098751.html)
- [^3]:[Buy Tata Motors: Target of Rs 743](https://www.moneycontrol.com/news/business/stocks/buy-tata-motors-target-of-rs-743-kr-choksey-11080811.html)



## Key Insights and Challenges

- **Retrieval-Augmented Generation (RAG)**: By combining external content with generative AI, RAG enhances the quality of responses.
- **Text Splitting**: Managing varied article lengths and formats required custom text-splitting methods for consistent embeddings.
- **Efficient Indexing**: FAISS enabled fast, scalable retrieval of information, even with increasing data size.
- **Handling Multiple Sources**: The tool processes each URL independently, ensuring a reliable response for a range of topics within finance.

## Real-World Applications

This tool showcases how Gen AI can support real-world research tasks, with practical applications in:

- **Finance**: Retrieving insights from market reports for analysts.
- **Retail**: Researching and analyzing industry news for strategic planning.
- **Education**: Providing answers to complex queries using FAQ content.

## Learning Resources

This project is also available as an open-source educational tool with a video tutorial.
