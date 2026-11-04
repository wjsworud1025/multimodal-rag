# Multimodal RAG

PDF의 텍스트와 이미지를 활용하는 멀티모달 RAG 실습 프로젝트입니다.

현재는 폴더와 파일 구조만 만든 목업입니다. 실행 기능이나 의존성은 아직 없습니다.

- `data/invest.pdf`: 빈 자리표시자입니다. 실제 PDF로 교체하세요.
- `data/figures/`: 추출 이미지 저장 위치입니다.
- `notebooks/Multi_modal_RAG.ipynb`: 실습 노트북입니다.
- `src/`: PDF 파싱, 요약 체인, 다중 벡터 검색기 구현 위치입니다.

`.venv/`는 빈 폴더입니다. 실제 가상환경이 필요하면 `python -m venv .venv`로 생성하세요.
`.env`에 실제 키를 보관하며, `.env.example`에는 키 없는 설정 템플릿만 작성하세요.
`.env`, `.venv/`, `data/figures/`는 Git에서 제외됩니다.

git clone <저장소 주소>
cd multimodal-rag

# 가상환경 생성 및 활성화
python -m venv .venv
source .venv/bin/activate          # 윈도우: .venv\Scripts\activate

# 의존성 설치
pip install --upgrade pip
pip install -r requirements.txt     # 또는 requirements.lock.txt

# 커널 등록
python -m ipykernel install --user --name multimodal-rag

# .env 작성
cp .env.example .env                # 윈도우: copy .env.example .env
# .env 파일을 열어 실제 API 키를 입력