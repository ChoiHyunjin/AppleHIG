# Notifications

노티피케이션(이하 노티)은 잠겨있거나 사용중인지에 상관 없이 시기 적절하고 중요한 정보들을 사람들에게 전해준다. 메시지가 왔을때, 이벤트가 발생했을 때, 새로운 데이터가 사용 가능할 때, 상태가 바뀌었을 때 처럼.

사람들은 그들이 관심 있는 노티 도착은 좋아하지만, 모든 방해를 좋아하진 않는다. 사용자의 모든 경험 관리를 도우려면, 어떤 노티는 보내기 전에 허가를 받아야 한다. 시스템(설정 > 알람)에서 이 결정을 바꿀 수 있고, 경고 스타일, 예고, 시리 상호작용도 조정할 수 있다. 사용자들은 또한 설정 > Focus에서 노티를 끌 수도 있다.(정부에서 보내는 경고 빼고). [UserNotifications](https://developer.apple.com/documentation/usernotifications) 참조.

## 노티 권한 요청

노티 전송 전, 권한을 받아야 한다. 시스템은 앱이 보낼 노티의 설명과 함께 표준 권한 요청 경고창을 띄운다. 사용자는 이 설명을 볼 수 있으며, 설정 > 알림 에서 결정을 수정할 수 있다.

### 설명은 간결히.

표준 경고는 앱 이름과 수락/거절 버튼 사이에 (*목적 혹은 사용 설명 문자*로 불리는) 설정한 문구를 보여준다. 문구는 직관적이고, 특수하며, 이해하기 쉽기를 목표로 해야한다. *Sentence-style capitalization*를 사용해야하고, 수동적인 표현을 피하며, 기간을 포함해야 한다.

알림 수신의 이점에 대한 추가 정보를 표기해야 하면, 시스템 경고창을 띄우기 전에 커스텀 화면을 표시해라. 다른 사용자가 노티 수신 권한을 거절한 경우에도, 이 화면을 표시할 수 있다.

## 알림 관리

iOS 15 이후, 사용자는 정해진 시간 그리고 집중 모드 유무에 따라 노티에 반응할 행동을 세세하게 정의할 수 있다. 예약 배달은 사용자가 즉시 받은 알림창이던 이미 받았던 노티들이던 상관 없이 고를 수 있게 한다. 집중 모드는 사용자가 설정한 활동(수면, 업무, 운전 같은) 간에 노티들을 필터링할 수 있게 도와준다.

사용자는 노티창을 배달하는 집중 모드를 무시할 수 있는 접촉과 앱을 식별한다. 예를 들어 업무 모드에서는, 사용자들은 회사 동료, 가족, 업무 관련 앱에서 오는 노티들만 받기를 원할 수 있다. 또한 집중 모드 동안 모든 *시간 민감* 노티들을 받기 원할 수도 있다. *시간 민감* 노티들은 사람들이 즉시 받기 원하는 필수적인 정보를 포함한다.

> 중요
집중 모드가 알림창 배달을 딜레이할 지라도, 알림 자체는 도착 즉시 사용 가능하다.
> 

커스텀 행동을 지원하기 위해서, 첫째로 앱이 보낼 수 있는 노티 종류를 식별한다. 전화, 메시지 같은 직통 대화를 지원한다면 communication 노티를 사용해라.
---

## Reference

[Notifications - System Capabilities - iOS - Human Interface Guidelines - Apple Developer](https://developer.apple.com/design/human-interface-guidelines/ios/system-capabilities/notifications/)

원본
