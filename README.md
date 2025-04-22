# mcp-agentic-rag

## Overview

This project implements an MCP (Model Context Protocol) server and client for building agentic RAG (Retrieval-Augmented Generation) applications. The server provides a set of tools that can be used to enhance the performance of RAG systems, such as entity extraction, query refinement, and relevance checking. The client demonstrates how to connect to the server and use its tools.

## Server (server.py)

The server is implemented using the `FastMCP` class from the `mcp` library. It exposes the following tools:

*   **get_time_with_prefix:** Returns the current date and time.
*   **extract_entities_tool:** Extracts entities from a given text query using OpenAI. This tool can be used to identify key entities in a user's query, which can then be used to improve the retrieval of relevant documents.
*   **refine_query_tool:** Refines a given text query using OpenAI. This tool can be used to improve the quality of a user's query, which can then be used to improve the retrieval of relevant documents.
*   **check_relevance:** Checks the relevance of a text chunk to a given question using an LLM. This tool can be used to filter out irrelevant documents from the retrieval results.

## Client (mcp-client.py)

The client demonstrates how to connect to the MCP server and use its tools. It uses the `ClientSession` class from the `mcp` library to establish a connection with the server. The client provides examples of how to:

*   Connect to the server
*   List available tools
*   Call a specific tool with arguments
*   Process a query using OpenAI and available MCP tools

## Requirements

*   Python 3.7+
*   openai
*   mcp
*   dotenv

## Installation

1.  Clone the repository:

    ```bash
    git clone https://github.com/rukshanet/mcp-agentic-rag.git
    ```
2.  Install the dependencies:

    ```bash
    pip install -r requirements.txt
    ```
3.  Configure the environment variables:

    *   Create a `.env` file based on the `.env.sample` file.
    *   Set the `OPENAI_MODEL_NAME` environment variable to the name of the OpenAI model you want to use.

## Usage

1.  Start the MCP server:

    ```bash
    python server.py
    ```
2.  Run the MCP client:

    ```bash
    python mcp-client.py
    ```

## License

[MIT](LICENSE)
