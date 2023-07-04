# *개발자의 숲 / Dev_Forest*
개발자 커뮤니티, **개발자의 숲** 서비스

프로그래밍 코드와 오류 및 해결방안을 제시하는 소통 공간

## 📌 다른 서비스와의 차별점
* Stack Overflow : 영어 기반 서비스기에 초보 한국인 개발자들이 접근하기 비교적 어려움.
* OKKY : 한국어 기반 개발자 커뮤니티지만, 이직과 같은 개발자 관련 정보 공유나 개발의 전반적인 질문(예: 어느 언어를 먼저 배우는 게 좋을까요?) 등에 특화됨.

제작하고자 하는 개발자 커뮤니티들은 **한국어 기반 서비스**로, 초보 개발자들이 부담 없이 사용할 수 있는, **코딩 중 발생한 오류에 대한 질문**만을 대상으로 하는 서비스

## 📌 서비스 기능
* **한국어 기반 서비스** : 한국인 개발자들과 한국어로 편하게 소통 가능
* **명예의 전당** : 지식인처럼 답변을 달고 해당 답변이 채택될 경우 포인트를 합산하여, 개인 순위/소속에 대한 순위를 제공 → 동기와 성취감을 얻을 수 있음.
* **정보 공유** : 답변이 달린 게시글은 삭제되지 않고 모든 사용자들이 볼 수 있음.

## 📌 웹 서비스 구현 요소
![Static Badge](https://img.shields.io/badge/Node.js-%23FF0000)
![Static Badge](https://img.shields.io/badge/MySQL-%23FFA500)


![Static Badge](https://img.shields.io/badge/Javascript-%23006400)
![Static Badge](https://img.shields.io/badge/CSS-%230000FF)
![Static Badge](https://img.shields.io/badge/Html-%234B0082)

## 📌 웹 서비스 구조도 
![structure](https://github.com/SemiKwon/Dev_Forest/assets/76101347/d16d58a3-b150-4dd8-a065-feb6a9a72f71)

## 📌 구성
**1. 로그인/로그아웃**
   - 회원 정보 불러오기 → session authenticate:true 처리 → **회원 정보 DB 세션 테이블**에 저장
   - session 회원 정보 지우기 → session authenticate:false 처리 → DB의 세션 테이블에 저장

**2. 검색**
- 사용자 검색 → trim() 함수를 활용하여 검색어 공백 제거 → DB 질문 테이블의 title, content에서 해당 검색어가 포함된 게시글 정보 제공

**3. 답변글 채택**
- 채택 있는 경우 : 해당 질문 답변 중 채택된 내역 검색 → 채택 불가
- 채택 없는 경우 : 유저는 해당 답변에 대해 채택 포인트 입력 → 서버에서 해당 포인트 전달받아 DB에 전송 → answerTable의 포인트를 UPDATE

**4. 즐겨찾기**
- 질문글의 즐겨찾기 클릭 → 서버는 DB scrapTable에서 게시글 즐겨찾기 데이터가 있는지 조회 → 있는 경우는 DELETE, 없는 경우는 INSERT

## 📌 어려웠던 점과 해결 방법
- **답변글, 즐겨찾기 한 글, 좋아요 한 답변글 정보는 세 개 이상의 테이블을 조인해야 해서 쿼리문이 복잡했음.** : Ajax 통신을 이용하여 페이지의 갱신 없이 요청을 보낸 뒤 응답과 상관없이 동작하는 비동기 방식을 통해 서버와의 통신을 가능케 함.
- **GitHub로 협업을 하는 과정에서 브랜치 하나를 삭제함.** : main 브랜치를 놔두고 그 전에 임시 브랜치에서 구동이 잘 되면 commit하는 방식을 취했기에, 다행스럽게 main 브랜치의 내용들이 삭제되거나 날아가지 않았음.

## 📌 [팀] 담당 부분
* 회원 가입
* 회원 가입 페이지 Html, CSS

## 📌 개인적으로 아쉬웠던 점
데이터베이스 개론은 들은 적이 있었고, MySQL까지는 문제가 없었는데, 이를 node.js와 연동시키다 보니 생각지도 못한 곳에서 오류가 났습니다. 나는 하느라고 열심히 했지만, 생각만큼 잘 따라오지 않았다. 아무래도 서버에 대한 이해가 조금 모자랐던 것 같습니다. 그리고 브랜치 하나를 통으로 폭파시킨 것도 아쉬웠습니다. 내가 오래 전에 commit 했던 파일이 있었는데, 그 부분이 그대로 브랜치에 들어와서 당황스러웠습니다. 다음에 이런 프로젝트를 구동할 때에는 이런 부분들을 좀 더 세밀하게 생각해서 준비해야겠습니다.
