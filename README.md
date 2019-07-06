# 한규주 회고

## 전 뭘했냐면요
우리팀은 실시간 질문답변 서비스를 만들었고, 팀 내 개발자는 1명이라 홀로 진행했습니다.
서버는 순수 API 서버로만 작동하였고, 웹페이지 없이 React native로 앱을 만들었습니다.

**레포**
[honeypot 백엔드](https://github.com/hanqyu/honeypot)
[honeypot 클라이언트](https://github.com/hanqyu/honeypot-cli)

**스택**
```
백엔드: Django REST Framework API
프론트엔드: React Native iOS
DB: PostgresSQL
호스팅: AWS EC2 / RDS
```

## 작업한 피쳐들은?

#### 모델
* User
* Question
* Answer
* QuestionVote (Question에 like 하듯이 부스트 기능이 있었음)
* Category
* Region (구현 못함)
* District (구현 못함)


#### API
모델 별로 list를 retrieve하는 viewset은 전부 구현하였고 아래 API를 별도로 만들었습니다.
API마다 작동할 수 있는 CRUD는 다르며, 모두 따로 구현하였습니다.

* RegistrationAPI
* QuestionAPI
* LoginAPI
* UserAPI (Token Verification)
* AnswerAPI
* SelectAnswerAPI
* RecentQuestionAPI
* PopularQuestionAPI
* PreferredQuestionAPI
* VoteQuestionAPI
* AnswerInQuestionAPI


## 회고
#### 좋았던 점
**Django REST Framework에 대해 배우다**
API 서버를 직접 구축해본 경험이 가장 많이 얻을 수 있었던 점이 아닌가 싶습니다. DRF(Django REST Framework)라는 API 개발을 위한 규모가 꽤 큰 API가 있는데, 진입장벽이 높은 편에 속합니다. 제가 뭔가를 배우는 방식이 이론을 충분히 다져놓고 하는 방식이라기보단 일단 구현에 뛰어드는 방식인데 이 방식이 처음 2,3주는 헤매지만 나중에는 문서에서 하는 얘기가 뭔지 경험을 통해서 알게 되는 것 같아서 빠른 러닝커브를 가지는 것 같습니다. DRF는 controller와 model 사이의 데이터 validation을 위해 serializer 라는 개념을 사용하는데, 이 개념에 익숙해지고 나서는. 개발 속도가 빨라진 것 같습니다.

**프론트에 대해 배우다**
또한 javascript는 물론이고 react-native도 처음 도전해보았는데, 프론트 스택이 하나 늘은 것 같아 좋습니다. 프론트 시작 전에 async 개념에 대해 유튜브 강의라도 듣고 시작하시면 많은 도움이 될 것 같습니다.

redux도 좋은 경험이었습니다. DOM구조라는 react 특성상 필요했는데, 완전히 이해는 못했지만 뷰마다 user의 token값은 동일하게 사용되니까 이 토큰을 관리하기에 좋은 방법이었습니다.

react native 스터디도 매우 도움이 된 것 같습니다. 강의를 통해 얻을 수 있었던 지식이 아니라면 진행하기 어려웠을 겁니다. 다음 기수도 스터디를 진행하는걸 적극 추천합니다.


그래도 나름 3\~400시간은 투자한 것 같습니다. 투자한 시간만큼 얻을 것이 있었다고 생각합니다.

#### 안 좋았던 점
**혼자라 힘들었습니다**

사실 협업 경험을 느껴보고 싶어서 들어온 동아린데, 팀원이 없어 그게 힘들었습니다. 혼자 백부터 프론트까지 경험해본 좋은 계기긴 했지만 코드리뷰를 해줄 사람이 없어 퀄리티가 좋은 결과물을 낸 건 아닌 것 같습니다.

또한 MVP 스펙을 진짜진짜 작게 잡을 필요가 있는 것 같습니다. 넓은 개발 스펙 때문에 힘들어서가 아니고, 일단 최소스펙으로 MVP를 내보고 팀원의 의견을 받아서 기능을 추가하거나 수정하는 경험이 추가로 있었다면 더 도움이 되지 않았을까 싶습니다.


