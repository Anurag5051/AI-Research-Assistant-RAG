<h1>AI Research Assistant with RAG</h1>

<p align="center">
  <img width="1440" alt="image" src="https://github.com/user-attachments/assets/f09fbe93-4235-4bf0-bd91-339320d1dd69" />
</p>

<h2>🧠 Overview</h2>

<p>This AI Research Assistant leverages Retrieval-Augmented Generation (RAG) to provide accurate, context-aware responses to research queries. The system combines multiple LLMs with vector search capabilities, allowing you to ask questions about uploaded documents, search academic papers, and gather information from the web.</p>

<h2>✨ Features</h2>

<ul>
  <li><strong>Multiple AI Models</strong>: Support for OpenAI GPT, Groq, and Google Gemini models</li>
  <li><strong>Document Q&A</strong>: Upload PDFs and ask questions about their content</li>
  <li><strong>Research Paper Analysis</strong>: Search and analyze academic papers from arXiv</li>
  <li><strong>Web Search Integration</strong>: Gather information from the web when needed</li>
  <li><strong>PDF Processing</strong>: Extract and process text from uploaded PDFs</li>
  <li><strong>Vector Search</strong>: Efficient document retrieval using Pinecone vector database</li>
  <li><strong>Modern UI</strong>: Clean and responsive interface built with Streamlit</li>
</ul>

<h2>🏗️ Architecture</h2>

<p>The application follows a RAG (Retrieval-Augmented Generation) architecture:</p>

<ol>
  <li><strong>Retrieval</strong>: Documents are processed, chunked, and stored in Pinecone vector database</li>
  <li><strong>Augmentation</strong>: Relevant context is retrieved based on user queries</li>
  <li><strong>Generation</strong>: LLMs (OpenAI GPT, Groq, or Gemini) generate responses using the retrieved context</li>
</ol>

<h2>📋 Requirements</h2>

<ul>
  <li>Python 3.8 or higher</li>
  <li>API keys for:
    <ul>
      <li>OpenAI (optional)</li>
      <li>Groq (optional)</li>
      <li>Google Gemini</li>
      <li>Pinecone</li>
    </ul>
  </li>
</ul>

<h2>🚀 Getting Started</h2>

<h3>Installation</h3>

<ol>
  <li>
    <p>Clone the repository:</p>
    <pre><code>git clone https://github.com/yourusername/AI-Research-Assistant-RAG.git
cd AI-Research-Assistant-RAG</code></pre>
  </li>
  <li>
    <p>Install required packages:</p>
    <pre><code>pip install -r requirements.txt</code></pre>
  </li>
  <li>
    <p>Create a <code>.env</code> file in the project root with your API keys:</p>
    <pre><code>OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key
GEMINI_API_KEY=your_gemini_api_key
PINECONE_API_KEY=your_pinecone_api_key
PINECONE_ENV=research-rag</code></pre>
  </li>
</ol>

<h3>Running the Application</h3>

<p>You can run either the original application or the enhanced version:</p>

<pre><code># Run the original app
streamlit run app.py

# Run the enhanced app with improved UI
streamlit run new_app.py</code></pre>

<h2>💻 Usage</h2>

<h3>Available Modes</h3>

<ol>
  <li><strong>Research Assistant</strong>: Ask research questions and get answers from arXiv papers and Wikipedia</li>
  <li><strong>Document Q&A</strong>: Upload PDF documents and ask questions about them</li>
  <li><strong>Web Search</strong>: Search the web for answers to your questions</li>
</ol>

<h3>Model Options</h3>

<ul>
  <li><strong>OpenAI</strong>: GPT-3.5</li>
  <li><strong>Groq</strong>: Various models including:
    <ul>
      <li>Llama 3.1/3.3</li>
      <li>Mixtral</li>
      <li>Gemma2</li>
      <li>DeepSeek</li>
    </ul>
  </li>
</ul>

<h2>📁 Project Structure</h2>

<pre><code>.
├── app.py                  # Original Streamlit application
├── bg.png                  # Background image
├── groq_chain.py           # Groq chain implementation
├── new_app.py              # Enhanced Streamlit application
├── Notebooks/              # Jupyter notebooks for development
├── Python Scripts/         # Individual implementation scripts
├── README.md               # Project documentation
├── requirements.txt        # Package dependencies
├── research_chain.py       # Research assistant implementation
├── Text Corpus examples/   # Sample PDF documents for testing
└── web_scrape_chain.py     # Web search capabilities</code></pre>

<h2>🔧 Key Components</h2>

<h3>Vector Storage</h3>

<p>The system uses Pinecone for vector storage, with different indexes for different purposes:</p>
<ul>
  <li><code>research-rag</code>: For storing document embeddings and research papers</li>
</ul>

<h3>Document Processing</h3>

<p>PDFs are processed using:</p>
<ol>
  <li>Text extraction with pdfplumber</li>
  <li>Chunking with RecursiveCharacterTextSplitter</li>
  <li>Embedding generation (using the selected model's embeddings)</li>
  <li>Vector storage in Pinecone</li>
</ol>

<h3>Web Scraping</h3>

<p>The application can scrape web content using:</p>
<ul>
  <li>Static page extraction with Requests/BeautifulSoup</li>
  <li>Dynamic page extraction with Selenium (for JavaScript-heavy pages)</li>
</ul>

<h2>🤝 Contributing</h2>

<p>Contributions are welcome! Please feel free to submit a Pull Request.</p>

<h2>📄 License</h2>

<p>This project is licensed under the Open CC - see the LICENSE file for details.</p>
