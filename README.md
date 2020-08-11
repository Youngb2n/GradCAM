Grad_CAM
=========
참고 논문 : <https://arxiv.org/pdf/1610.02391v1.pdf>    

Grad-CAM
---------
>Grad-CAM은 Zhou et al. 이 제안한 Class Activation Mapping(CAM)의 general version 이다. 여기서 CAM은 image classification task에서 관심 영역을 확인 할 수 있도록 식별 가능 지역을 heatmap 형태로 보여주는 딥러닝 시스템 해석 방법 중한가지다.  

Architecture
------------
<img src="/image/1.JPG" width="80%" height="80%" title="img1" alt="img1"></img>

환경
-------
#### Cat vs Dog dataset Download Site : <https://www.kaggle.com/c/dogs-vs-cats/data>
Cat and Dog Dataset 에서 accuracy 93.83%의 학습된 Resnet Model를 기반으로 Colab 환경에서 제작.    
자세한 모델 구조는 Code 참고   

Result
-------
>HeatMap 출력결과   

<img src="/image/2.JPG" width="80%" height="80%" title="img1" alt="img1"></img>   
<img src="/image/3.JPG" width="80%" height="80%" title="img1" alt="img1"></img>   
개 고양이 이진 분류 task에서 실험 결과 대상의 얼굴 중에서도 코를 위주로 개 고양이 판별 하는것으로 보입니다.   
평탄화 과정에서 GlobalAveragePooling이 아닌 Flatten function을 사용할 경우 code를 조금 수정하여 사용하셔야 됩니다.   
자세한 내용은 Grad-CAM.ipynb file의 code를 참조 하시길 바랍니다.   
