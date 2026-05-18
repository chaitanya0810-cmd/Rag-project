<img width="940" height="724" alt="Screenshot 2026-05-18 154109" src="https://github.com/user-attachments/assets/ef442885-5f19-46e0-9748-02b8b2272e9d" />
<img width="940" height="724" alt="Screenshot 2026-05-18 154109" src="https://github.com/user-attachments/assets/210febed-cffe-4daf-a588-42d8469c4ae1" />
Deliverable 1: HLD (High Level Design)

Sections:
1. Problem Statement
Customer support teams overloaded.
Need AI assistant for common queries.

2. Scope
Read company PDF
Answer FAQs
Escalate complex issues

3. Components
Component	                    Use
UI	                          Streamlit
Loader	                      PyPDF
Embeddings	                  sentence-transformers
Vector DB	                    ChromaDB
LLM	                          GPT / Gemini
Workflow	                    LangGraph
HITL	                        Manual escalation

4. Scalability
Multiple PDFs
Faster search
Cache embeddings


Deliverable 2: LLD (Low Level Design)
Modules:

PDF Module:
load_pdf()
extract_text()

Chunk Module:
split_text(chunk_size=500)

Embedding Module:
create_embeddings()

Retrieval Module:
similarity_search(query)

Graph Module:
Nodes:
input_node
process_node
output_node
human_node

LangGraph Workflow Example:-

START
 ↓
Check Intent
 ↓
[Simple] → Retrieve → Generate → End

[Complex] → Human Support → End


Deliverable 3: Technical Documentation
Introduction:
RAG solves hallucination problem by grounding LLM responses in documents.

Why ChromaDB?
Free
Easy setup
Fast vector search

Why LangGraph?
Visual workflow
Conditional routing
Better than linear chain

Why HITL?
Prevent wrong answers
Better trust
Real-world customer support needs escalation

Sample Queries
User Query	                                Output
What is refund policy?	                    AI answers
Order missing after 7 days	                AI answers
Legal complaint regarding payment fraud	    Escalate human
