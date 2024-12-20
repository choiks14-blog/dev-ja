---
title: 함수형 언어란 무엇이며 종류는 어떤것이 있는가?
author: alpa28980
date: Mon, 25 Nov 2024 04:37:17 GMT
categories: undefined
tags: undefined
comment: true
---
서론
--

함수형 프로그래밍은 순수 함수를 기반으로 하는 프로그래밍 패러다임입니다. 순수 함수는 외부 상태에 의존하지 않고 동일한 입력에 대해 항상 같은 출력을 내는 함수를 말합니다. 함수형 프로그래밍에서는 변수 값의 변경이 불가능한 불변성(Immutability)을 따르며, 함수 자체를 변수로 취급하고 다른 함수의 인자로 전달할 수 있는 고차 함수(Higher-order Function)를 활용합니다.

절차지향/객체지향 프로그래밍과 비교했을 때, 함수형 프로그래밍은 추상화 수준이 높아 코드 리딩이 어렵지만, 기존 자료구조를 크게 변경할 필요가 없습니다. 또한 함수형 언어는 대중성이 낮은 편입니다. 하지만 함수형 프로그래밍은 불변성으로 인해 병렬 처리와 테스트/디버깅이 용이한 장점이 있습니다.

함수형 프로그래밍은 순수 함수, 불변성, 고차 함수 등의 핵심 개념을 통해 병렬 처리와 디버깅 측면에서 강점이 있지만, 상대적으로 낮은 대중성과 높은 추상화 수준은 단점으로 지적됩니다.

불변성
---

함수형 프로그래밍에서 불변성(Immutability)은 핵심 개념입니다. 불변성이란 한번 정의된 값은 변경할 수 없다는 것을 의미합니다. 기존 값을 변경하는 대신, 새로운 값을 생성해야 합니다. 이를 위해 destructive update 대신 persistent data structure를 사용합니다.

불변성은 다음과 같은 장점이 있습니다:

1. 병렬 처리가 용이합니다. 데이터가 변경되지 않으므로 스레드 안전성이 보장되어 병렬 처리가 쉽습니다.
2. 참조 투명성이 보장됩니다. 함수의 결과가 외부 상태에 영향을 받지 않습니다.
3. 디버깅이 용이합니다. 데이터 변경이 없으므로 상태 추적이 쉽습니다.

불변 데이터 구조의 예시로는 Linked List, Vector, HashMap 등이 있습니다. 일반적으로 새로운 노드나 배열을 생성하여 기존 데이터를 유지하면서 변경 사항을 반영합니다.

순수 함수
-----

순수 함수(Pure Function)는 함수형 프로그래밍의 핵심 개념으로, 외부 상태에 의존하지 않고 입력이 같으면 항상 같은 출력을 내는 함수입니다. 순수 함수는 부작용(Side Effect)이 없어 프로그램의 상태를 변경하지 않습니다. 이로 인해 병렬 프로그래밍이 용이해지는데, 동시에 여러 스레드에서 순수 함수를 호출해도 안전하기 때문입니다.

또한 순수 함수는 입력이 같으면 출력이 항상 같아 메모이제이션(Memoization)이 가능합니다. 이전 계산 결과를 저장해두고 재활용함으로써 성능을 높일 수 있습니다. 반면에 부작용이 있는 함수는 외부 상태에 따라 출력이 달라지므로 메모이제이션이 어렵습니다. 4 예를 들어 피보나치 수열을 계산하는 재귀 함수에 메모이제이션을 적용하면 시간 복잡도가 지수 시간에서 선형 시간으로 개선됩니다.

순수 함수의 또 다른 장점은 테스트와 디버깅이 용이하다는 점입니다. 외부 상태에 영향을 받지 않기 때문에 함수의 동작을 격리하여 검증할 수 있습니다. 따라서 버그를 찾고 수정하기가 쉬워집니다. 반면 부작용이 있는 함수는 외부 상태에 의존하므로 테스트하기 어려워집니다. 이처럼 순수 함수는 병렬 프로그래밍, 성능 최적화, 테스트 등 다양한 측면에서 이점을 제공합니다.

함수 합성
-----

함수 합성(Function Composition)은 두 개 이상의 함수를 조합하여 새로운 함수를 만드는 것을 의미합니다. 이를 위해서는 고차 함수(Higher-Order Function)가 활용됩니다. 고차 함수란 함수를 인자로 받거나 반환하는 함수를 말합니다.

함수 합성을 통해 복잡한 작업을 작은 단위의 함수로 나누어 해결할 수 있습니다. 또한 불변성과 순수 함수의 특성으로 인해 합성된 함수의 동작을 예측하기 쉽고, 테스트와 디버깅도 용이해집니다.  마지막으로 함수 합성은 코드의 모듈성과 재사용성을 높여 생산성 향상에도 기여합니다.

함수형 프로그래밍에서 함수 합성은 매우 중요한 개념입니다. 작은 단위의 함수를 조합하여 복잡한 문제를 해결할 수 있으며, 코드의 가독성과 테스트 용이성 등 다양한 장점을 제공합니다. 따라서 함수 합성은 함수형 프로그래밍의 핵심 원리 중 하나라고 볼 수 있습니다.

주요 함수형 언어
---------

주요 함수형 프로그래밍 언어로는 Lisp, Haskell, Erlang, Scala 등이 있습니다.

Lisp는 1958년 개발된 가장 오래된 함수형 언어로, 기호 데이터 처리에 적합합니다. 인공지능, 컴파일러 등의 분야에서 많이 활용되고 있습니다.

Haskell은 1990년대 말 개발된 순수 함수형 언어로, 정적 타입 시스템과 타입 추론 기능이 있습니다. 강력한 타입 시스템과 병렬 프로그래밍 지원 등의 특징이 있으며, 금융, 과학 분야에서 활용되고 있습니다.

Erlang은 1986년 에릭슨 전화교환기 개발을 위해 만들어진 언어로, 분산 시스템과 병렬 프로그래밍에 특화되어 있습니다. 높은 내결함성과 핫스왑 기능으로 유명하며, 통신, 금융 시스템 등에 활용됩니다.

Scala는 2000년대 초반 개발된 멀티 패러다임 언어로, 함수형과 객체지향 프로그래밍을 모두 지원합니다. JVM 기반으로 자바와의 상호운용성이 뛰어나며, 빅데이터 처리, 웹 개발 등 다양한 분야에서 사용됩니다.

결론
--

함수형 프로그래밍은 불변성과 순수 함수를 기반으로 병렬/동시성 프로그래밍과 디버깅, 유닛 테스트에 유리합니다. 고차 함수와 함수 합성을 통해 간결하고 재사용 가능한 코드를 작성할 수 있으며, 메모이제이션, 지연 평가 등 다양한 최적화 기법을 활용할 수 있습니다. 하지만 높은 추상화 수준으로 인해 배우기 어렵고 생산성이 낮을 수 있으며, 기존 자료구조를 persistent data structure로 변경해야 하는 부담이 있습니다. 또한 순수 함수형 언어의 대중성이 낮아 활용 분야가 제한적이며, 값 변경 시 새 메모리 할당으로 인한 성능 저하와 가비지 컬렉션 오버헤드가 발생할 수 있습니다. 그러나 멀티코어 CPU와 분산 시스템 환경에서 함수형 프로그래밍의 장점이 부각될 것으로 보이며, 빅데이터, 머신러닝, 웹 개발 등 다양한 분야에서 활용도가 높아질 전망입니다. 비록 완전한 주류 패러다임으로 자리잡기에는 어려움이 있지만, 기존 언어에 점차 함수형 기능이 도입되고 있습니다.
---
---

<iframe src="https://ads-partners.coupang.com/widgets.html?id=807239&template=carousel&trackingCode=AF3190673&subId=&width=680&height=140&tsource=" width="680" height="140" frameborder="0" scrolling="no" referrerpolicy="unsafe-url" browsingtopics></iframe>
해당 링크를 통해 제품 구매가 이루어진 경우 쿠팡 파트너스 활동 일환으로 인해 일정 수수료가 블로거에게 제공되고 있습니다

