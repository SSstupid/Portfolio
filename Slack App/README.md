![Slack 공유 프린터 drawio](https://github.com/SSstupid/Portfolio/assets/90036120/b6a2f891-de03-4a42-a7f7-b5de5c80b6c6)

## Slack App
Slack에서 주고 받는 메시지를 프린터 할 수 있는 앱입니다. 프린터 식별 번호, Server를 통해 원격으로 프린터가 가능합니다. 즉 모바일, 데스크탑 등 기기에서 물리적인 연결 없이 프린터가 가능하며, 프린터를 공유하여 사용 할 수 있습니다. Slack은 Block kit 객체를 제공하여 UI 구성 및 데이터를 전달합니다. 이 Json 형식의 데이터를 파싱하여 C# 객체로 전환하여 사용하였습니다.

코드 줄 개수를 61 => 21개로 줄여 가독성을 65% 향상시켰습니다. if, foreach문을 중첩으로 사용하여 특정 Item을 가져오는 코드를 dynamic을 활용하여 개선 했습니다.

* 변경 전
  
<img src="https://github.com/SSstupid/Portfolio/assets/90036120/abb2acb0-db7e-43a5-be1f-73cbb3fb5a1f" width="500" height="500"/>

* 변경 후

<img src="https://github.com/SSstupid/Portfolio/assets/90036120/bcfa8636-3c63-45d5-9265-941486d9241b" width="450" height="350"/>
