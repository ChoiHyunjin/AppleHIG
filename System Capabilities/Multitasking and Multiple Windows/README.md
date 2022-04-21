# Multitasking and Multiple Windows

멀티태스킹은 사용자가 앱 전환기로 다른 앱으로 빨리 스위치하게 하고, 다른 기기에서 추가적인 경험을 가능케 한다. 아이폰을 예로 들면, 멀티태스킹은 다른 앱을 사용하면서, 페이스타임을 하거나 동영상을 볼 수 있다.

![스크린샷 2022-04-07 오후 6.58.07.png](images/스크린샷_2022-04-07_오후_6.58.07.png)

아이패드에서 멀티태스킹은 사용자가 동시에 몇 가지 다른 앱 윈도우를 보고 반응한다. 또한 멀티 윈도우가 된다. 한번에 하나 이상의 앱을 보고 반응할 수 있다.

iPadOS는 다양한 구성으로 멀티 윈도우를 나타낼 수 있고, 여러 워크플로우를 지원한다. 또한 시스템은 구성을 스위칭할 수 있는 멀티태크싱 제어 기능과앱의 모든 열려있는 윈도우에 접근하게 하는 앱 쉘프를 제공한다. 

![스크린샷 2022-04-08 오전 10.20.47.png](images/스크린샷_2022-04-08_오전_10.20.47.png)

아이패드에서 멀티태스킹 창을 열려면 하단의 구성중 하나를 따르면 된다.

- Slide Over : 기존 창은 전체 화면으로 두고 두 번째 창을 그 위에 띄워서 여는 방법. 사용자는 Slide Over된 창의 위치를 옮기거나 숨겼다가 되돌릴 수 있다. 또한 스택 형태로 여러 창을 열 수도 있다.
    - 예시
        
        ![스크린샷 2022-04-08 오전 10.22.56.png](Multitasking%20and%20Multiple%20Windows%20aa2759f6f04044e8b5a0c5cf7b689582/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-04-08_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.22.56.png)
        
- Split View : 두 화면을 나란히 표시하는 방식으로, 창의 상대적인 크기를 양 쪽으로 조절할 수 있다. 이 방식으로 보는 동안, Slide Over 로 다른 창을 띄우는 것도 가능하다.
    - 예시
        
        ![스크린샷 2022-04-08 오전 10.27.32.png](Multitasking%20and%20Multiple%20Windows%20aa2759f6f04044e8b5a0c5cf7b689582/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-04-08_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.27.32.png)
        
- Picture in Picture : 본 화면 위로 옮길 수 있고, 크기 조절 가능한 창에서 비디오를 띄우는 방식.
    - 예시
        
        ![스크린샷 2022-04-08 오전 10.27.48.png](Multitasking%20and%20Multiple%20Windows%20aa2759f6f04044e8b5a0c5cf7b689582/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-04-08_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.27.48.png)
        

> 앱은 이러한 구성을 제어하거나 사용자 선택에 따른 어떤 정보도 받지 못한다.
> 

사용자는 멀티 태스킹을 원하고, 앱이 지원하지 않으면 뭔가 잘못 됐다고 생각할 수 있다. 아주 드문 예외들(전체화면만 지원하는 아이패드 앱들 같은 경우) 외에는 모든 앱들이 멀티태스킹이 되어야 한다. [Supporting Multitasking](https://developer.apple.com/design/human-interface-guidelines/ios/system-capabilities/multitasking/#supporting-multitasking) 참조

Split View나 Slide Over로 열 때 적절히 반응하게 하려면, [화면 사이즈에 적절히 반응하게](https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/adaptivity-and-layout/) 해야한다. 가이드는 [Multitasking on iPad](https://developer.apple.com/documentation/uikit/app_and_environment/multitasking_on_ipad) 참조. 어떻게 사람들이 아이패드 멀티태스킹을 사용하는지 궁금하다면 [Use Multitasking on your iPad](https://support.apple.com/en-us/HT207582)를 확인해라.

멀티태스킹이 잘 작동하게 하는 것 외에도, 멀티 창을 지원하도록 추가 구현해야한다. [Enabling Multiple Windows on iPad](https://developer.apple.com/design/human-interface-guidelines/ios/system-capabilities/multitasking/#enabling-multiple-windows-on-ipad) 참조.

> 아이패드 앱의 맥 버전에서 멀티 창을 가능케 하려면, 아이패드에서 멀티 창을 구현해야한다.
> 

# Supporting Multitasking

멀티태스킹 환경을 활성화하기 위해선, 기기의 다른 앱들과 조화롭게 공존할 필요가 있다. CPU, 메모리, 화면 공간 그리고 기타 자원 사용량 최소화 같은 방법으로. 멀티태스킹 앱은 다른 앱으로 부터의갑작스런 인터럽트와 오디오에 잘 반응 해야하고, 백그라운드로의 전환이 빠르고 부드러워야 하며, 백그라운드에서의 작업이 정확해야한다.

### 인터럽트와 재개

인터럽트는 언제든 발생할 수 있다. 인터럽트가 발생하면, 앱은 최신 상태를 빠르고 즉시 저장하여 사용자가 다시 돌아왔을 때, 떠난 지점에서 빈틈 없이 계속할 수 있어야 한다. [Responding to the Launch of Your App](https://developer.apple.com/documentation/uikit/app_and_environment/responding_to_the_launch_of_your_app) 참조.

### 중요한 작업은 잠시.

게임이나 미디어 재생 앱 같은 경우, 사람들이 앱 전환 간에 어떤 것도 놓쳐서는 안된다. 전환해서 다시 돌아오면, 사용자가 떠나간적 없는 것 처럼 플레이되어야 한다.

### 적절한 반응.

앱의 오디오는 다른 앱이나 시스템의 오디오에 의해 인터럽트 받을 수 있다. 예를 들면 전화나 Siri에 의한 음악 리스트는 앱의 오디오를 방해할 수 있다. 이런 경우, 사람들은 다음처럼 반응할거라 생각한다.

- 음악, 팟캐스트, 오디오북 재생과 같은 주요 오디오 인터럽트를 위해 즉시 정지한다.
- GPS 방향 안내 같은 짧은 인터럽트 동안은 볼륨을 줄이거나 잠시 멈췄다가, 끝나면 다시 볼륨을 복귀하거나 재생한다.

[Audio](https://developer.apple.com/design/human-interface-guidelines/ios/user-interaction/audio/) 참조.

### 마무리까지.

사용자는 작업을 시작하면, 앱에서 스위치해서 나갔음에도 작업이 완성되기를 바란다. 만약 앱이 추가적인 입력이 필요하지 않은 작업을 실행 중이라면, 앱이 종료되기 전에 백그라운드에서 완료해라.

### 알림은 신중히.

앱이 종료됐든, 백그라운드에서 실행 중이든, 실행되지 않았든 앱은 정해진 시점에 알림을 보내도록 설정 할 수 있다. 일반적으로 백그라운드에서 작업을 종료했을 땐 알림 전송을 피한다. 대신에, 앱으로 돌아가서 작업을 확인하게 한다. 자세한 사항은 [Notifications](https://developer.apple.com/design/human-interface-guidelines/ios/features/notifications/) 참조.

# Enabling ****Multiple Windows on iPad****

컨셉적으로, 아이패드는 내용 전달을 위해 두 타입의 창을 사용하는 경향이 있다.

- Primary Window : 앱의 전체 계층을 나타내는 방법. 전체 앱의 오브젝트와 그와 관련된 액션으로 접근을 제공한다. 예를 들면 메일 앱은 모든 메일함과 메시지 리스트를 나타낼 때 primay Window를 사용한다.
- Auxiliary Window : 앱의 특별한 작업이나 공간을 표시한다. 종종 Modal 방식으로 나타내기도 한다. 하나에 집중하기 위해서, 이 방식의 창은 다른 앱 공간으로 이동할 수 없고, 작업 종료 후 닫는데 사용되는 버튼을 포함한다. 예를 들면, 이메일에서는 단일 메시지를 표시할 때 이 방식을 사용한다.

iPadOS 15 이후, 앱에서 각 창이 처음 등장하는 방식을 지정할 수 있다. 사람들이 창이 열린 후 위치를 옮길지라도, 지정한 등장 스타일은 창의 작업이나 내용의 특성을 비주얼적으로 강화할 것이다. 다음과 같은 방식이 있다.

- Prominent : 창이 떠있는 Modal 방식. 주변 영역은 어두워지고 주변과 소통을 예방한다.
- Standard : 나란히 표시되는 방식. 다른 창과 소통이 가능하며 각 창은 기능적으로 제한되지 않는다.
- Automatic : 앱이 창을 요청하는 상황에 다라 시스템이 골라주는 방식.

> 사용자가 단순히 파일을 보게 하려면, 새 창 생성 없이 표시할 수 있지만, 멀티 창을 지원해야한다. [QLPreviewSceneActivationConfiguration](https://developer.apple.com/documentation/quicklook/qlpreviewsceneactivationconfiguration/) 참조.
> 

### 자체적인 작업이라면? Prominent 스타일

Prominent 스타일은 문서 수정이나 파일 탐색 작업에 좋다. 이 스타일은 그 자체로 유용하도록 해야한다. 다른 작업을 나타내기 위해서 사용하거나, 보조적인 액션 혹은 메인 작업에 영향을 주는 아이템 선택에 사용하지 않도록 해라.

### 같은 작업이나 내용의 여러 버전이면? Standard 스타일

사파리의 경우, 사람들에게 두 브라우징 창을 동시에 보여주고 소통하는 방법으로 standard 스타일을 사용한다.

### 새 창은 사용자의 요청이 있을 때만.

사용자는 앱 쉘프나 앱 Expose에서 ( + ) 버튼을 누르 거나 메뉴 아이템을 선택할 수 있다. 사용자가 요청하지 않았는데 새 창을 생성해서 놀래키지 않도록 하자.

### 앱 창에서 사용하도록 설정한 모든 작업을 지원하는지 확인해라.

멀티 창은 편리함과 효과적인 워크 플로우를 제공하지만, 사용자는 항상 단일 창으로 모든 앱 구성에 접근할 수 있어야 한다.

### 각 창의 상태 보존.

사용자는 창으로 돌아왔을 때, 떠날 때와 같은 상태일 것이라 생각한다. [Restoring Your App’s State](https://developer.apple.com/documentation/uikit/uiscenedelegate/restoring_your_app_s_state) 참조.

### 새 창으로의 제스처.

사용자는 새 창에서 노트를 확대할 때 pinch 제스처를 사용한다. 제스처 사용 전환은 prominent 스타일을 사용하여, 결과 모달 창이 아이템이나 작업이 확장된 자연스러운 결과물처럼 느끼게 한다. [collectionView(_:sceneActivationConfigurationForItemAt:point:)](https://developer.apple.com/documentation/uikit/uicollectionviewdelegate/3752185-collectionview) (콜렉션 뷰 아이템에서 전환) 혹은 [UIWindowScene.ActivationInteraction](https://developer.apple.com/documentation/uikit/uiwindowscene/activationinteraction) (다른 뷰의 아이템에서 전환) 참조

### “새 창에서 열기” 메뉴.

이 동작을 활성화 하면, 앱이 맥 카탈리스트를 사용하는 아이패드나 맥에서 구동 될 때는 메뉴는 “새 창에서 열기”를 나타내지만 아이폰에서는 나타나지 않는다. 가능하다면, 아이폰에서 구동할 때 “자세히 보기...” 와 같이 대체 메뉴를 제공해라. “새 창에서 열기"를 상황에 맞는 메뉴 혹은 버튼과 Bar 버튼을 메뉴에 붙일 수도 있다.

### 새 창에서 열 때는 일반적인 UI 로.

사람들이 사용하는 멀티태스킹 구성을 모르기 때문에, “스플릿 뷰로 열기" 혹은 “앞으로 열기" 같은 메뉴를 피해라.

### “윈도우" 용어 사용

시스템은 종류에 상관 없이 앱 윈도우를 “윈도우"라 부른다. ‘scene’(윈도우 구현을 참조하는)과 같은 용어는 사람들에게 혼란을 준다.

---

## Reference

원본

[Multitasking and Multiple Windows - System Capabilities - iOS - Human Interface Guidelines - Apple Developer](https://developer.apple.com/design/human-interface-guidelines/ios/system-capabilities/multitasking/)
