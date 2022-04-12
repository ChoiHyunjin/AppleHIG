# Accounts

앱의 핵심 기능에 필요하면, 이용자에게 계정 생성을 요청해라. 반면에, 계정 없이도 앱을 즐길 수 있어야 한다. 앱에서 계정이 필요하면, [Sign in with Apple](https://developer.apple.com/design/human-interface-guidelines/sign-in-with-apple/overview/)을 사용해서 일관된 로그인 유지 경험을 줘라. 이는 사람들이 여러 계정과 비밀번호를 기억할 필요가 없어 신뢰도와 편리함을 준다.

### 계정 생성의 이점과 방법 설명

계정이 필요한 앱이면, 계정 필요의 이유에 대한 친절한 설명과 이점을 로그인 화면에서 브리핑 해라.

### 최대한 늦게.

이용자가 유용한 어떤 것을 하기 전에 로그인을 강요하면, 앱을 떠나는 경향이 있다. 이런 상황을 피하려면, 사람들이 앱을 감상한 후에 약속을 요구해야한다(asking them to make a commitment to it). 예를 들어, 쇼핑 앱은 사람들이 원하는 것을 충분히 탐색할 수 있어야 하고, 구매가 준비되었을 때만 로그인을 요청해야한다.

### 자동 입력.

비밀번호 자동 입력은 비밀번호와 보안코드를 자동 생성, 입력하는 기능이다. 그래서 사람들이 인증 화면에서의 시간을 줄일 수 있다. [Password AutoFill](https://developer.apple.com/documentation/security/password_autofill/) 참조

### “암호" 회피

이용자들은 Apple 서비스를 위해 기기나 인증을 해제할 비밀번호를 만든다. 그래서 당신이 앱에서 재사용하려고 요청한다고 생각할 수도 있다. ‘암호', ‘PIN’, ‘코드', ‘키', ‘접근 코드' 등 과 같은 단어는 피해라.

# 계정 삭제

이용자들이 계정을 만들었다면, 단순 정지 뿐 아니라 삭제 또한 가능해야 한다. 아래의 가이드라인을 따르는 것 이외에도, 계정 삭제와 잊혀질 권리에 대한 해당 지역의 법적 요청을 이해하고 준수해야 한다.

> 법적 요구사항이 계정이나 정보를 유지하도록 강요하거나 - 건강 기록과 같이 - 특별한 계정 삭제 절차를 따라야 한다면, 이용자에게 유지해야 하는 정보나 계정 정보와 따라야 하는 과정에 대해 이해할 수 있도록 설명해야한다.
> 

### 명확한 삭제 방법

앱 내에서 삭제를 할 수 없으면, 이를 할 수 있는 웹페이지 링크를 제공해야 한다. 그리고 찾기 쉬워야 한다. 개인 정보 정책 혹은 서비스 용어 설명 화면에 숨겨두지 않도록.

### 웹이던, 앱이던.

둘 중 하나가 더 길거나 복잡하게 하지말고 동일한 플로우를 유지해야한다.

### 삭제 예약.

이용자들은 계정 삭제 전에 남은 서비스를 이용하거나, 구독이 자동으로 갱신될 때 까지 기다리기를 바란다. 계정 삭제 예약 기능을 제공할 거면, 즉시 삭제 옵션도 제공해라.

### 삭제 예정과 완료 알림

계정 삭제에 시간이 필요할 때가 있기 때문에, 삭제 과정의 상태를 알려 주는 것은 필수이다.

### 인앱 구매시 청구과 취소는?

다음과 같은 경우 당신은 사람들을 이해시킬 필요가 있을 수 있다.

- 자동 갱신 구독의 비용 청구는 사용자의 취소 신청 전까지 애플을 통해 계정 삭제 여부와 상관없이 계속 된다.
- 계정 삭제 후, 구독 취소나 환불을 요청한다.

이 경우 이해시키는 것 외에도 어떻게 취소되는지, 어떻게 구매가 관리되는지를 설명해야한다. [Helping People Manage Their Subscriptions](https://developer.apple.com/design/human-interface-guidelines/in-app-purchase/overview/auto-renewable-subscriptions/#helping-people-manage-their-subscriptions)와 [Providing Help with In-App Purchases](https://developer.apple.com/design/human-interface-guidelines/in-app-purchase/overview/introduction/#providing-help-with-in-app-purchases) 참조

# Face Id & Touch ID

이 둘은 사람들이 신뢰하는 안전하고 친숙한 인증 방법이다. 생체 인증이 가능해지면서 어떻게 동작하는지 이해하고, 편리함을 좋아하며, 가능하면 사용하기를 선호할 것이다. 사람들이 생체 인식을 끌 수도 있기 때문에, 이를 대비해야 된다.

[Local Authentication](https://developer.apple.com/documentation/localauthentication) 참조

### 심플하게

첫 시도가 실패하면, 아이디와 비밀번호를 묻는 것 처럼 대체 옵션을 제공해도 된다.

### 사용자가 요청할 때만

버튼 클릭 같은 명확한 액션은 사용자가 인증을 원한다는 걸 보장한다. Face ID는 사용자가 카메라를 응시할 가능성을 높인다.

### 명확하게

무엇을 요청할지를 식별할 수 있어야 한다. Face ID로 로그인 하기 위한 버튼을 표시할 거면, 제목은 “Face ID로 로그인”이어야 한다. “로그인하기” 가 아니라.

### 가능한 것만

현재 문맥에서 가능한 것만 참조해라. Face ID가 가능한 기기에서 Touch ID 참조하는 것과 그 반대 모두 옳지 않다. 기기를 확인하고 적절한 것을 사용해라. [LABiometryType](https://developer.apple.com/documentation/localauthentication/labiometrytype) 참조.

### 설정은 설정에서.

앱 내에서 생체 인증을 선택하기 위한 설정을 제공하지 마라. 사람들은 시스템 레벨에서 생체 인증을 활성화하기 때문에, 인앱에서 설정을 표시하는건 불필요하고 헷갈리게 만들 수 있다.

---

## Reference

원본

[Accounts - User Interaction - iOS - Human Interface Guidelines - Apple Developer](https://developer.apple.com/design/human-interface-guidelines/ios/user-interaction/accounts/)