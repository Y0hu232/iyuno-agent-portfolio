# iyuno-agent-portfolio
# RAG Assistant

문서 기반 RAG(Retrieval-Augmented Generation)와 Tool Calling을 결합한
AI Assistant 데모 프로젝트입니다.

사용자의 질문과 관련된 문서를 검색하고, 검색 결과를 근거로 답변을 생성하며,
답변에 사용된 문서의 citation을 함께 제공합니다.

또한 질문의 종류에 따라 외부 Tool을 호출하여 검색, 날씨, 정책 조회 등의
API를 사용할 수 있습니다.

---

## 1. 주요 기능

### 1.1 문서 기반 RAG

다음과 같은 RAG Pipeline을 구현합니다.

```text
Document
   ↓
Document Loading
   ↓
Chunking
   ↓
Embedding
   ↓
Vector Store
   ↓
Vector Search
   ↓
Relevant Documents
   ↓
LLM
   ↓
Answer + Citation
