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
![Static Badge](https://img.shields.io/badge/Javascript-%23FFA500)
![Static Badge](https://img.shields.io/badge/CSS-%23006400)
![Static Badge](https://img.shields.io/badge/Html-%230000FF)

## 📌 웹 서비스 구조도 
![structure](https://github.com/SemiKwon/Dev_Forest/assets/76101347/d16d58a3-b150-4dd8-a065-feb6a9a72f71)

## 📌 구성
1. 로그인/로그아웃
   * 회원 정보 불러오기 → session authenticate:true 처리 → **회원 정보 DB 세션 테이블**에 저장
   * session 회원 정보 지우기 → session authenticate:false 처리 → DB의 세션 테이블에 저장

2. 검색
   * 회원 정보 불러오기 → session authenticate:true 처리 → **회원 정보 DB 세션 테이블**에 저장
   * session 회원 정보 지우기 → session authenticate:false 처리 → DB의 세션 테이블에 저장
     
