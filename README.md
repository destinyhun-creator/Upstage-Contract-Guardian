# Upstage-Contract-Guardian
본 프로젝트는 사회초년생 및 부동산 계약 입문자들이 겪는 '법률 정보의 비대칭' 문제를 해결하기 위해 개발되었습니다. 복잡한 특약 사항 속에 숨겨진 독소 조항을 AI가 탐지하고, 안전 리포트를 제공합니다.
🚀 주요 기능 (Key Features)

지능형 문서 분석 (Document Intelligence)
Upstage Document Parse를 사용하여 비정형 계약서 이미지(PDF)에서 표 구조와 텍스트 좌표를 완벽하게 복원합니다.

법률 RAG (Legal Grounding)
주택임대차보호법 및 표준계약서 판례 데이터를 Qdrant Vector DB에 구축하여, AI가 실제 법적 근거를 바탕으로 답변합니다.

독소 조항 자동 탐지 (Red-flag Detection)
Upstage Solar LLM이 단순 요약을 넘어 문맥을 파악합니다. (예: "담보권을 설정할 수 없다"는 안전, "이의를 제기하지 않는다"는 위험으로 분류)

자동 리포트 및 가이드 생성
분석 결과를 PDF로 변환하여 이메일로 발송하며, 임대인에게 보낼 '협상용 거절 메시지'를 자동 생성합니다.

🛠️ 기술 스택 (Tech Stack)

AI Engine: Upstage Solar-pro, Upstage Document Parse
Orchestration: n8n (Low-code Automation)
Database: Qdrant (Vector Store)
Integration: Google Drive, Gmail API, HTML-to-PDF
📂 파일 구조 및 실행 방법
workflow/가디어_최종본.json: n8n에서 Import from File을 통해 바로 불러올 수 있는 전체 워크플로우 파일입니다.
docs/: 서비스 시나리오 및 기술 설계서(PDF)가 포함되어 있습니다.

실행 순서
구글 드라이브 지정 폴더에 계약서 파일을 업로드합니다.
n8n 워크플로우가 트리거되어 분석을 시작합니다.
분석 완료 후 사용자 이메일로 PDF 리포트가 발송됩니다.

🎓 Upstage 앰배서더 지원 동기
업스테이지의 모델들은 한국어 이해도와 문서 파싱 능력에서 독보적인 성능을 보여주었습니다. 본 프로젝트를 통해 Solar 모델이 단순한 챗봇을 넘어 실생활에 적용을 해보고자 하였습니다.

🎓 Upstage 앰배서더 지원 동기

업스테이지의 모델들은 한국어 법률 문맥 이해도와 문서 파싱 능력에서 독보적인 성능을 보여주었습니다. 본 프로젝트를 통해 Solar 모델이 단순한 챗봇을 넘어 실생활의 '안전망'이 될 수 있음을 증명하고자 했습니다.
