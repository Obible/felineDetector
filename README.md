# felineDetector
고양이과 동물을 구분해주어요

# 성경
(23.12.15 15:29)  
생각보다 트레이닝을 작은 수의 사진으로 한 것 같다.
```python
PATH = './pycatfd/training_data_dir/training_data'  
print(os.listdir(PATH))
```
```
└── training.xml
└── image_metadata_stylesheet.xsl
└── 1.jpg
└── 2.jpg
└── ...
└── 40.jpg
```

Future works (near...)
- 고양이 landmark 표시되어 있는 데이터(kaggle)로 얼마나 정확도가 높은지?
- 더 학습시켜서 몇 개 더 학습시킬 때 정확도가 더 높아지나...
- 이러한 모델을 다른 동물에 test 해보았을 때 정확도가 어떻게 되는지?
    - 이건 다른 동물들도 한 20~40개 정도 찍어서 확인해봐야 될 듯
    - 정확도 높다면 사용
    - 정확도 낮다면 모델 학습시키기...


(17:47) 할 일
- (1) 현재 모델(40개 이미지)에서 
    - (a) 고양이 annotation 얼마나 잘 detect하는지 확인  
     : Cat Dataset(from kaggle; [link](https://www.kaggle.com/datasets/crawford/cat-dataset/data))의 annotation과 얼마나 일치하는지 (9개만) 유사도 검증 : 점 간의 Euclidean distance 계산
    - (b) 다른 고양잇과 동물(호랑이, 사자, 치타, 표범)들에도 계산을 잘 하는지 확인
- (2) 고양이 사진(w/ annotations)을 더 넣으면서 모델의 정확도 판단!
    - (a) cat dataset(up)에서 턱이랑 bounding box 좌표 찍기 ([link](https://github.com/NaturalIntelligence/imglab))
    - (b) 이걸로 학습
- (3) 학습시킨 후에 혹시 야생동물들 잘 계산합니까?
- ** 시간이 남는다면? tiger model, cheetah model, ...각각 학습시켜서 performance 보기.