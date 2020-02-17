# DVC - Data Version Control 따라 해보기
데이터 모델링 과정 중 데이터 셋이나 모델을 관리하기 위한 도구 

git과 유사한 형태로 ML 모델이나 사용된 데이터셋을 관리할 수 있는 도구

## 설치
    '''sh
    brew install dvc
    pip install dvc
    '''
## Initialize & Add file
    '''sh
    git clone https://github.com/pko89403/DVC_Test.git
    cd DVC_Test
    
    dvc init # .dvc 디렉토리 생성
    dvc remote add -d movielens /Users/kangseokwoo/DVC/DVC_Dataset/MovieLens
    vim /Users/kangseokwoo/DVC/DVC_Test/.dvc/config
    dvc add .
    dvc push
    git add .
    git commit -m "dvc test"
    git push 
    '''
### .dvc/config
    '''sh
    ['remote "movielens"']
    url = /Users/kangseokwoo/DVC/DVC_Dataset/MovieLens
    [core]
    remote = movielens
    '''
## Clone & Pull data
    '''shell
    git clone https://github.com/pko89403/DVC_Test.git # New Environment
    dvc pull # .dvc 만 있었는데 리모트 접근해서 파일 가져옴 
    '''
## 참고

[DVC - Data version control](https://inahjeon.github.io/dvc/)

[꿈 많은 사람의 일상](https://lsjsj92.tistory.com/573)