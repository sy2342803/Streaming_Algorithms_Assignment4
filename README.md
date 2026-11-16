# Streaming Algorithms Assignment 4

## 1. 과제 개요

본 프로젝트는 빅데이터 스트리밍 환경에서 활용되는 알고리즘 2종을 Python으로 직접 구현하고, 정확도·메모리 사용량·처리 시간 측면에서 성능을 비교 및 분석하는 과제입니다.

## 2. 개발 환경

- Language: Python
- Environment: Google Colab
- Python Version: 3.13.18
- Dataset: MovieLens 1M

## 3. 사용 데이터셋

- Dataset: MovieLens 1M
- File: `ratings.dat`
- Number of Records: 1,000,209
- 주요 데이터: 사용자 ID, 영화 ID, 평점, 타임스탬프
- 데이터 출처: [GroupLens MovieLens 1M](https://files.grouplens.org/datasets/movielens/ml-1m.zip)

데이터는 파일을 한 줄씩 읽는 방식으로 처리하여 전체 데이터를 한 번에 메모리에 적재하지 않도록 구성했습니다.

## 4. 구현 알고리즘

### 4.1 Bloom Filter
- 데이터의 원소 포함 여부를 근사적으로 판정하는 확률적 자료구조
- False Positive Rate(FPR)를 측정하여 정확도 평가
- 비트 배열 크기와 해시 함수 개수에 따른 성능 비교

### 4.2 Count-Min Sketch
- 스트림 데이터의 항목별 빈도를 근사적으로 추정하는 자료구조
- Ground Truth와 비교하여 MAE 및 평균 상대 오차 측정
- Width 변경에 따른 정확도와 메모리 사용량 비교

## 5. 성능 평가 항목

- 정확도: False Positive Rate, MAE, 평균 상대 오차
- 메모리: 주요 자료구조의 메모리 사용량
- 처리 시간: 전체 스트림 처리 시간
- 처리량: 초당 처리 레코드 수

## 6. 실험 목적

두 알고리즘의 특성과 정확도·메모리 사이의 Trade-off를 분석하고, 실제 서비스 로그 분석 환경에 적합한 알고리즘을 검토합니다.

## 7. 파일 구성

- `Streaming_Algorithms_Assignment4.ipynb`: 알고리즘 구현 및 실험 결과가 포함된 Google Colab 노트북
- `README.md`: 프로젝트 설명 및 실험 개요
