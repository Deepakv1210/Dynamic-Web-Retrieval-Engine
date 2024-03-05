# Dynamic Web Retrieval Engine

# LangChain Conversational Agent

## Project Overview

This search engine is designed to handle user queries through an integrated workflow automation system. The project's architecture encompasses various functionalities, such as document retrieval, relevance grading, question transformation, web search, and document generation. With dynamic retrieval and web scraping capabilities, result relevancy has significantly enhanced effectively eliminating content hallucination.

## Project Structure

1. **Document Retrieval (`retrieve` Function):**
   - Initiates the workflow by fetching documents relevant to the user's question.
   - Retrieved documents are stored in the `documents` key of the system's state.

2. **Document Relevance Grading (`grade_documents` Function):**
   - Implements a grading system to assess the relevance of each document to the user's query.
   - Documents with positive scores are deemed relevant, triggering a decision on whether to perform a web search.

3. **Web Search (`web_search` Function):**
   - Conducts a web search using the Tavily API if the grading indicates a need for additional information.

4. **Question Transformation (`transform_query` Function):**
   - Transforms the user's question to potentially enhance retrieval or generate a more refined response.

5. **Document Generation (`generate` Function):**
   - Generates a response or summary based on the retrieved and relevant documents.

6. **Graph State and Workflow Execution:**
   - Represents the workflow as a directed acyclic graph (`StateGraph`).
   - Nodes represent different stages or functions (`retrieve`, `grade_documents`, etc.).
   - Edges define the flow between nodes based on conditional logic (`decide_to_generate`).
   - The entire workflow is compiled into an executable application (`app`), processing input data through the defined stages.


