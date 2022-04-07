# Settings

설정 혹은 구성을 선택하는 방법을 제공해야 할지도 모르는 앱들도 있지만, 대부분의 앱은 피하거나 뒤로 미룰 수 있다. 성공적인 앱은 대부분의 이용자들에게 즉시 잘 동작할 뿐 아니라, 경험을 조정할 수 있는 편한 방법들도 제공해야 한다. 사람들이 기대하는 방향의 앱을 디자인하면, 설정의 필요성이 줄어든다.

### 시스템에서 받아올 것들

사용자, 장치, 환경에 대한 정보가 필요하면, 사용자가 아니라 시스템에 요청해라. 예를 들어, 지역 옵션을 나타내기 위해 사용자의 zip code를 물어보는 대신, 현재 위치 정보 접근 허가를 요청해라. 접근이 거부되면 수동 입력으로 전환해라.

### 구성 옵션 우선 순위는 신중하게.

앱의 메인 화면은 필수적이거나 자주 바뀌는 옵션들에게 적합한 곳이다. 두 번째 화면은 가끔 바뀌는 옵션들을 두기 좋다.

### 자주 변하지 않는 구성 옵션 표기

세팅 앱은 시스템의 구성을 변화시키는 중앙적인 위치이나, 사람들은 이를 위해 앱에서 나와야 한다. 앱에서 바로 설정을 조정하면 더욱 편리하다. 변경이 거의 없는 설정을 제공해야 한다면, [Preferences and Settings Programming Guide](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/UserDefaults/Introduction/Introduction.html) 안의 [Implementing an iOS Settings Bundle](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/UserDefaults/Preferences/Preferences.html) 를 참고 해라.

### 바로가기.

“설정 > 내 앱 > 개인정보 > 위치 서비스" 와 같이 설정으로 보내는 문구를 제공할거면, 바로 갈 수 있는 버튼도 같이 제공해라. [UIApplication](https://developer.apple.com/documentation/uikit/uiapplication) 안의 [openSettingsURLString](https://developer.apple.com/documentation/uikit/uiapplication/1623042-opensettingsurlstring) 참고

---

## Reference

원본

[Settings - App Architecture - iOS - Human Interface Guidelines - Apple Developer](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/settings/)