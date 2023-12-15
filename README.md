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