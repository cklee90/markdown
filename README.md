# markdown
마크다운 설명

### 7. 하이퍼 링크
[e클래스1](https://cafe.daum.net/pcwk "e클래스의 카페입니다.")

### 6. 가로 라인
---
***
------

### 5. 코드블록
```
def index(request):
    '''question 목록'''
    #list order create_date desc
    question_list = Question.objects.order_by('-create_date')  # order_by('-필드') 마이너스 표시 붙이면 DESC, 없으면 ASC
    #question_list = Question.objects.filter(id=99)   # 없을때 잘 되는지 확인
    context = {'question_list':question_list}
    print('question_list:{}'.format(question_list))
    return render(request,'pybo/question_list.html',context)
```


### 4. 목록
1. 아이템 1  
2. 아이템 2  
  9. 1단계 하위 아이템  
    3. 2단계 하위 아이템
9. 아이템 3

- 아이템 1  
+ 아이템 2  
  - 1단계 하위 아이템  
    * 2단계 하위 아이템  

순서없는 목록  
* 목록이름
- 목록
+ 목록2

순서있는 목록  
1. 목록이름
2. 목록
3. 목록3번

### 3. 인용문
> 여기에 인용할 내용을 넣으면 됩니다.  
> 빈 줄이 없으면 자동으로 인용 상자에 포함

### 2. 헤더
# 헤더1
## 헤더2
### 헤더3
#### 헤더4
##### 헤더5
###### 헤더6

### 1. 문단 구분을 위한 계행.
문단을 작성 합니다.   (계행: 공백 두개)  
겨울이 가고 봄이 옵니다. 
