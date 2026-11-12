# ship-maintenance-ai
# 선박 정비이력 질의응답 AI 실습

- 이름: 송문석
- 학번: 20230299

## 1. DuckDB 적용
제공된 MAI SMA 학생 패키지에서 Ollama의 qwen3:1.7b를
연결하고, 학생용 DuckDB를 대상으로 질의와 평가를 수행했다.

제공 DB는 재배포 제한으로 포함하지 않았다.
PC 실험을 재현하려면 수업 제공 패키지가 별도로 필요하다.

## 2. Colab GPU 실습
- GPU: Tesla T4
- 모델: Qwen/Qwen3-1.7B
- 내용: 선박 정비 질문 5개의 SQL 생성 및 생성 시간 시각화
- 방식: 추가 학습 없이 GPU 추론
- 코드: ship_maintenance_gpu.ipynb
- 결과: ship_sql_results.csv
- 그래프: generation_time.png

### 실행 방법
노트북을 Colab에서 열고 GPU 런타임을 선택한 뒤
첫 셀부터 순서대로 실행한다.

### 결과와 한계
GPU에서 SQL 생성과 시간 측정을 완료했다.
Codex 검토에서 생성 SQL의 의미 오류가 확인됐다.
Colab에서는 실제 DB 실행과 정답률 평가를 수행하지 않았다.

## 3. Codex 활용
실습 코드와 결과를 검토하고 SQL 오류 분석,
수정 후보 및 생성 시간 해석을 받았다.
수정 후보는 실제 DB에서 검증하지 않았다.

## 4. 증빙
- screenshots/duckdb: DuckDB 실행
- screenshots/colab: Colab 증빙 5장
- screenshots/codex: Codex 증빙 5장
