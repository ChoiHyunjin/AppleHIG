# Modality

Modality는 임시 모드에서 내용을 표시하는 디자인 테크닉이다. modal한 내용 표시는 다음과 같은 이점이 있다.

- 독립적인 일 혹은 연관된 옵션 세트에 집중할 수 있다.
- 사람들이 중요한 정보를 받을 수 있고, 필요하면 대응할 수 있다.

다양한 시스템 기반의 modal을 경험하기 위해, iOS는 alerts, activity view, share sheets, action sheet 을 제공한다.

- Automatic : 기본 스타일을 사용한다. 특히 sheet
- Fullscreen : 이전 화면을 덮고, 사라지기 위한 버튼이 필요하다.
- Popover : 수평의 일반적인 환경에선 popover, 소형 환경에서는 sheet 으로 나타난다.
- Page Sheet & Form Sheet : 이전 view의 일부분을 덮는다. ([자세히](https://developer.apple.com/design/human-interface-guidelines/ios/views/sheets/))
- Current Context : 특정 이전 뷰를 포함한다.
- Custom : 커스텀 컨테이너에 커스텀 애니메이션으로 내용을 나타낸다.

[개발자 참고](https://developer.apple.com/documentation/uikit/uimodalpresentationstyle)

## 적절히

사용자의 주의를 끌어 선택을 해야하거나, 최근의 작업과 다른 종류의 작업을 해야할 때만 사용하라. Modal은 최근 흐름에서 벗어나고 끄기 위한 액션을 필요로 하기 때문에 명백히 이익을 제공할 수 있을때만 필수적으로 사용해야 한다.

## 필수적이고 이상적으로 실행 가능한 정보 전달 경고

일반적으로, 경고는 무언가 잘못 되고 있을 때 발생한다. 경고는 현재의 작업을 침범하고 dismiss를 위해 액션을 요구하기에, 사람들이 정당한 침입이라고 느끼게 하는것이 중요하다. [Alert 참고](https://developer.apple.com/design/human-interface-guidelines/ios/views/alerts/)

## 심플, 짧은, 집중

모달 작업이 너무 복잡하면, 사람들은 모달에서 하려던 작업을 한 눈에 찾을 수 없다. 앱 안의 앱이라는 느낌을 받지 않도록 조심 해야한다. 특히, 모달 작업에서 계층적인 구조로 나타내는 것을 피해야 한다. 왜냐면 사람들이 원래 작업으로 돌아가는 방법을 까먹을 수 있기 때문이다.

모달 작업에 하위 view가 필요하면, 계층간 통과가 단순하고, 완료까지 명확한 길을 제공해야한다. 작업 완료 외에는 done 버튼 제공은 하지 마라.

## 내용이 많고나, 복잡한 작업은 전체화면으로

전체화면 모달은 집중 방해를 최소화하여 비디오, 사진, 카메라, 여러 단계 표기(문서나 카메라 편집 같은)에 효과가 좋다.

## Dismiss 버튼

버튼을 포함하면 모달은 보조 기술에 접근 가능해지고, dismiss 제스처의 대체제를 제공할 수 있다.