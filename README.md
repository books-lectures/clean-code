# clean-code
[clean code] 책 내용을 정리하는 레포지토리 입니다

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
