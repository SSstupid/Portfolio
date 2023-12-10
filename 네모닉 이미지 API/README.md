## 프로젝트 구조

<img width="302" alt="image" src="https://github.com/SSstupid/Portfolio/assets/90036120/bdad6107-967b-4073-b840-e0375531a590">

![Nemonic API drawio](https://github.com/SSstupid/Portfolio/assets/90036120/e88ed2a2-4722-419b-9825-dd6d18212c93)

* 이미지 생성 시퀀스 다이어그램 방안 1 => 이미지를 생성하고 서버에서 `Image`로 요청

<img width="1000" height="700" alt="네모닉 시퀀스 다이어그램 방안1" src="https://github.com/SSstupid/Portfolio/assets/90036120/00b682f3-9e7d-4ec9-80f8-5b0aed4339a0">

* 이미지 생성 시퀀스 다이어그램 방안 2 => 서버에서 `string Text`로 요청하고 `Drawing 프로젝트`에서 이미지 생성
<img width="1500" alt="네모닉 시퀀스 다이어그램 방안2" src="https://github.com/SSstupid/Portfolio/assets/90036120/c663c9f8-9fa2-4cd6-b4aa-84310a6cd43f">


## 네모닉 이미지 API

메모지 프린터인 Nemonic에 전달 할 이미지 생성 및 명령어로 변환하는 기능입니다.
해당 라이브러리는 Server에 추가되어 윈도우, 모바일 등 다양한 기기와 앱에서 사용 할 수 있습니다. 이미지 생성 라이브러리를 사용해 이미지 사이즈를 용지에 맞게 크기를 설정하고, 분절, 회전 등의 기능을 제공합니다.  Given-When-Then Pattern을 활용한 Unit Test 코드를 작성했습니다.

API 테스트를 Unit Test 코드 변경하여 시간, 용지 절약하기
이미지가 알맞은 각도로 회전 되었냐의 문제는 사람이 판단 가능한 문제라 생각하였고, API 변경 사항이 있을 때마다 디버그하여 Docker, Swager를 활용해 실제로 인쇄하는 방식으로 진행했습니다.

이 과정이 시간이 오래 걸리며, 용지가 낭비가 되고 변경사항이 있을 때 기존 API가 작동할까?라는 문제가 있었습니다. 이미지 크기는 실제 크기를 측정하거나 이미지 객체에 포함된 정보를 조회하는 방법으로 측정 할 수 있었고, 회전 유무는 이미지에 점 하나를 찍고 회전하여 점의 위치를 특정하는 방식으로 Test 코드를 작성했습니다.
