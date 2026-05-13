# Week 7: RAG Security Knowledge Assistant — Evaluation Report

## 1. Setup Summary
- **LLM:** llama3-8b-8192 via Groq
- **Embeddings:** sentence-transformers/all-MiniLM-L6-v2 via HuggingFace
- **Vector Store:** In-Memory Vector Store
- **Documents Loaded:**
  - mitre-initial-access.txt
  - mitre-credential-access.txt
  - mitre-lateral-movement.txt
---

## 2. Test Results
| # | Question | Used Documents? | Quality | Notes |
|---|---|---|---|---|
| 1 | What are common techniques for credential access according to MITRE? | Yes | Good | Response referenced credential dumping, keylogging, Mimikatz, and password hash dumping from uploaded MITRE documents.|
| 2 | How does phishing relate to initial access in the ATT&CK framework? | Yes | Good | Correctly identified phishing as an Initial Access technique in the MITRE ATT&CK framework and explained how attackers use it.|
| 3 | What is lateral movement and what techniques do attackers use? | Yes | Good | Response included remote services, valid accounts, pass-the-hash, and exploitation of remote services from uploaded documents.|
| 4 | What is the difference between spearphishing attachment and spearphishing link? | Yes | Good | Correctly explained the difference between malicious attachments and malicious links used in phishing campaigns.|
| 5 | What does the NIST framework recommend for the Detect function? | No | Partial | The uploaded documents did not contain NIST Detect framework information. The chatbot correctly stated that the information was not present instead of generating a false answer.|
---

## 3. Edge Case Observations
- **Unrelated question:** When asked unrelated cybersecurity and non-cybersecurity questions, the chatbot generally stated that the information was not present in the uploaded documents rather than inventing a detailed answer.
- **Topic not in documents:** The chatbot correctly acknowledged when NIST framework information was missing from the uploaded MITRE ATT&CK documents. This demonstrated that the RAG system constrained the language model to the retrieved document context instead of fully hallucinating responses.
---

## 4. Settings Experiments (if completed)
- **Temperature change:** Not completed.
- **Chunk size change:** Not completed.
- **Top K change:** Not completed.
---

## 5. Reflection
One surprising aspect of RAG systems was how strongly the quality of the uploaded documents affected the chatbot’s responses. The chatbot performed significantly better when the documents contained detailed MITRE ATT&CK descriptions and examples. The lab also demonstrated how embeddings and vector retrieval allow a language model to answer questions using external knowledge instead of relying entirely on pretrained model memory.
For real-world use, the chatbot could be improved with additional cybersecurity frameworks, persistent vector databases, and more structured document sources. RAG systems like this could also be useful in a capstone project for threat intelligence analysis, security operations support, or cybersecurity training assistants.

## Chatbox Share Link
https://cloud.flowiseai.com/chatbot/f514187a-c0e2-4098-88d3-28e32faf81c9
