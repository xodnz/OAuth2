# 헥사고날 아키텍처 도입

<p>
  <img src="https://github.com/i-Dear/sync-d-backend/blob/main/docs/HexagonalArchitecture.png">
</p>
<br/>

## 소개

저희는 스프링 백엔드 프로젝트에 헥사고날 아키텍처(Ports and Adapters Architecture)를 도입하기로 결정했습니다. 이 아키텍처 패턴은 핵심 비즈니스 로직을 데이터베이스, UI 프레임워크, 서드 파티 서비스 등 외부 시스템과 분리하는 것을 강조합니다. 아래에서는 헥사고날 아키텍처를 선택한 이유와 이 아키텍처의 장단점을 설명합니다.
<br/>
<br/>

## 헥사고날 아키텍처 도입 이유

1. **관심사의 분리**: 헥사고날 아키텍처는 핵심 비즈니스 로직과 외부 요소들을 분리합니다. 이를 통해 외부 시스템의 변경이 핵심 비즈니스 로직에 직접적인 영향을 미치지 않도록 합니다.

2. **테스트 용이성**: 비즈니스 로직을 외부 종속성에서 분리함으로써, 외부 시스템을 모킹(mock)하거나 스터빙(stub)하지 않고도 핵심 로직에 대한 단위 테스트를 쉽게 작성할 수 있습니다.

3. **유지보수성**: 이 아키텍처는 코드 구조를 명확하게 하여 유지보수를 쉽게 합니다. 특정 기능이 변경되더라도 해당 기능에만 집중하여 수정할 수 있습니다.

4. **확장성**: 새로운 기능 추가나 변경 요구사항이 발생했을 때, 핵심 로직을 건드리지 않고도 외부 어댑터만 수정하거나 추가하여 쉽게 확장할 수 있습니다.

<br/>

## 헥사고날 아키텍처의 장점

1. **독립성**: 비즈니스 로직이 외부 시스템에 의존하지 않기 때문에, 비즈니스 로직의 독립성을 유지할 수 있습니다.
2. **유연성**: 새로운 기술이나 외부 시스템을 도입할 때, 기존 비즈니스 로직을 변경하지 않고 어댑터만 추가하거나 교체할 수 있습니다.
3. **높은 테스트 커버리지**: 외부 시스템의 영향을 받지 않고 핵심 로직에 대한 테스트를 작성할 수 있어 높은 테스트 커버리지를 유지할 수 있습니다.

<br/>

## 헥사고날 아키텍처의 단점

1. **초기 복잡성**: 초기에 구조를 설정하고 이해하는 데 시간이 걸릴 수 있습니다. 특히 작은 프로젝트에서는 오버헤드가 될 수 있습니다.
2. **추가적인 추상화 레이어**: 포트와 어댑터를 정의하고 구현해야 하므로 코드베이스가 복잡해질 수 있습니다.
3. **일관성 유지**: 여러 어댑터와 포트를 관리하면서 일관성을 유지하는 것이 어려울 수 있습니다. 이는 팀 내에서의 명확한 규칙과 표준이 필요합니다.

<br/>

## 결론

헥사고날 아키텍처는 우리의 스프링 백엔드 프로젝트에서 핵심 비즈니스 로직의 독립성을 유지하고, 테스트 용이성을 높이며, 유지보수성을 향상시키기 위해 도입되었습니다. 이를 통해 변화하는 요구사항에 유연하게 대응할 수 있는 탄탄한 구조를 갖추게 되었습니다.

저희 프로젝트에서 헥사고날 아키텍처의 도입이 성공적으로 이루어지기를 기대하며, 지속적인 개선과 학습을 통해 더 나은 소프트웨어를 만들어 나가겠습니다.

