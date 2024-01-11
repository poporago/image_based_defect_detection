# 이미지 기반 제품 결함 탐지
- `이어드림스쿨 3기` 과정 중, 경진 대회 플랫폼 AI Connet에서 주최한 이미지 분류 문제에 참여했던 소스코드 입니다. 
- 대회 기간 : `2023.09.27` ~ `2023.10.06`
![image](https://github.com/poporago/image_based_defect_detection/assets/131949171/17b86afb-8dd0-401e-b369-f13bb11167db)

## Description
정상 이미지 (6820), 결함 이미지(30), Segmentation Mask(30)가 데이터로 주어집니다.
<br>`Macro F1-Score`를 통해 정상 이미지와 결함 이미지를 모두 잘 예측해야하는 Task입니다.

## Metrics 
<!-- 첫 번째 이미지 -->
<img src="https://github.com/poporago/image_based_defect_detection/assets/131949171/c32bb131-fcdc-499a-9945-2f510dae7813" alt="First Image" width="532" height="94">
<br>
<!-- 두 번째 이미지 -->
<img src="https://github.com/poporago/image_based_defect_detection/assets/131949171/7e21193a-7a9a-4765-a155-96a6d8ab4417" alt="Second Image" width="540" height="101">

## Details
주어진 task는 정상 이미지와 결함 이미지의 `이진 분류` 문제로 두가지 접근 방법을 사용하였습니다.<br>
<br>
(1)Image Classification model <br>
\- CNN기반 아키텍쳐인 efficientNet (train/efficientnet_15th.ipynb)
<br>

(2)Anomaly detection 방식의 접근 <br>
\- fastlfow사용 (train/fastflow_anomalib.ipynb) <br> 

최종적인 산출물은 effcientNetb5모델을 적용하였습니다.

## Results
- Private LB Score
  - Macro F1-score : 0.9611
  - Rank : 6/64 (9%)
