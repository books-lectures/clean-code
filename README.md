# clean-code
[clean code] 책 내용을 정리하는 레포지토리 입니다

## 1장: 깨끗한 코드
### - 코드는 사라지지 않는다  
  어느 수준에 이르면 코드없이 요구사항을 상세히 표현할 수 없다
### - 장기적으로 봤을 때 나쁜 코드는 회사를 망하게 할 수도 있다  
  기능 고도화를 해야하는데 엉킨 덩굴과 숨겨진 함정들에 빠지게 된다  
  팀생산성을 0에 수렴하게 만든다 -> 새로 만드는 시도를 하지만 기존기능을 다 구현하며 깨끗한 코드를 만드는것은 상당한 비용이 든다. 성공 여부도 불확실하다
### - 나중은 오지 않는다  
  안돌아가는 프로그램보다 돌아가는 쓰레기가 좋다고 위안하며 나중에 정리하겠다고 다짐하지만 나중은 오지 않는다
### - 나쁜코드의 위험성을 이해하지 못하는 관리자를 그대로 따르는것은 전문가적이지 못하다  
  환자가 바쁘다며 안씻은 손으로 수술을 요구하는것과 같다
### - 깨끗한 코드는 명확하며, 한가지에 집중한다  
  너무 많은 일을 하려하면 의도가 뒤섞이고, 목적이 흐려진다  
  코드를 보며 놀랄 일이 없어야 한다
### - 깨끗한 코드는 다른사람이 고치기 쉽다  
  읽고 수정하기 때문에 가독성이 중요하다  
### - 중복을 피하라, 한기능만 수행하라, 명확히 표현하라, 작게 추상화하라  
### - 보이스카웃 원칙  
  캠프장에 처음 왔을때보다 더 깨끗하게 해놓고 떠나라  
  적극적인 수정을 위해서는 테스트케이스가 필요하다  
  깨끗한 코드는 모든테스트를 통과한다  
  




## 2장: 의미 있는 이름
- 의도가 분명하게 이름을 지어라  
  좋은 이름을 지으려면 시간이 걸리지만 좋은 이름으로 절약하는 시간이 훨씬 더 많다
```java
// BAD
ind d;

// GOOD
int elapsedTimeInDays;
int daysSinceCreation;
int daysSinceModification;
int fileAgeIndays;
```
> 변수명이 길더라도 명확하게 정의하자

- 발음하기 쉬운 이름을 사용해라  
  토론하기 어렵다
```java
// BAD
private Date genymdhms(generate date, year, month, day, hour, minute, second)

// GOOD
private Date generationTimestamp;
```

- 검색하기 쉽게 해라
```java
// BAD
taskDays / 5

// GOOD
const int WORK_DAYS_PER_WEEK = 5;
taskDays / WORK_DAYS_PER_WEEK
```

- 메서드 이름은 동사가 적합하다

- 한 개념에 한 단어를 사용하라  
  fetch, retrieve, get을 혼용하면 혼란스럽다
