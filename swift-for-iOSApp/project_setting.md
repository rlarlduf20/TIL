## bundle identifier

---

웹 주소와 같다. 고유한 값을 가지며 앱 스토어에서 해당 앱을 고유하게 식별해준다.
ex) www.google.com -> com.google

최종 번들id는 회사의 회사의 식별자를 포함한다.
ex)product name - I am Rich,
organization name - www.appbrewery.co
=>co.appbrewery.I-am-Rich

이 방식은 회사의 앱이 앱스토어에서 고유하게 식별되도록 하는 매우 간단한 방법이다.

번들 id를 사용하는 다른 사람이 없다면 실제로 중요하지 않다.

## Interface SwiftUI vs Storyboard

---

앱의 흐름을 나타내며, <u>**_시각적_**</u>으로 화면을 구성하는 곳이다. 스토리보드에서 앱의 전반적인 형태와 앱의 화면 전환, 다양한 Object를 관리해준다. SwiftUI는 Storyboard의 단점을 보완해 최근에 나왔다.(최근 버젼에서만 사용가능)
(단점을 보완하는 부분은 추후 공부)

장점

- 초보자들도 쉽게 배우고 사용할 수 있게 해준다.
- 앱의 흐름을 한눈에 볼 수 있다.

단점

- 생산성, 가독성이 떨어진다.
- 협업이 어렵다.
- 재사용하기가 어렵고 번거롭다.

## LaunchScreen, Main

---

Storyboard - LaunchScreen은 앱이 첫 실행될 때 화면, Main은 실제 앱의 화면 구성

## App Icon Generator Site

---

어플의 아이콘이나 이미지의 사이즈를 다양하게 생성해준다.
