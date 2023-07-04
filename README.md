# *개발자의 숲 / Dev_Forest*
개발자 커뮤니티, **개발자의 숲** 서비스

프로그래밍 코드와 오류 및 해결방안을 제시하는 소통 공간

## 📌 다른 서비스와의 차별점
* Stack Overflow : 영어 기반 서비스기에 초보 한국인 개발자들이 접근하기 비교적 어려움.
* OKKY : 한국어 기반 개발자 커뮤니티지만, 이직과 같은 개발자 관련 정보 공유나 개발의 전반적인 질문(예: 어느 언어를 먼저 배우는 게 좋을까요?) 등에 특화됨.

제작하고자 하는 개발자 커뮤니티들은**한국어 기반 서비스**로, 초보 개발자들이 부담 없이 사용할 수 있는, **코딩 중 발생한 오류에 대한 질문**만을 대상으로 하는 서비스

## 📌 서비스 기능
* 한국어 기반 서비스 : 한국인 개발자들과 한국어로 편하게 소통 가능
* 명예의 전당 : 지식인처럼 답변을 달고 해당 답변이 채택될 경우 포인트를 합산하여, 개인 순위/소속에 대한 순위를 제공 → 동기와 성취감을 얻을 수 있음.
* 정보 공유 : 답변이 달린 게시글은 삭제되지 않고 모든 사용자들이 볼 수 있음.

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
   - 채택 있는 경우 : 해당 질문 답변 중 채택된 내역 검색 → 채택 내역이 '있는 경우' 채택 불가
   - 채택 없는 경우 : 유저는 해당 답변에 대해 채택 포인트 입력 → 서버에서 해당 포인트 전달받아 DB에 전송 → answerTable의 포인트를 UPDATE

**4. 즐겨찾기**
   - 질문글의 즐겨찾기 클릭 → 서버는 DB scrapTable에서 게시글 즐겨찾기 데이터가 있는지 조회 → 있는 경우는 DELETE, 없는 경우는 INSERT
