# 데이터 모델링
* 살아가면서 나타날 수 있는 다양한 현상을 **표기법에 의해 규칙을 가지고 표기**하는 것을 뜻한다.

## 모델링의 특징
1. **추상화**: 현실세계를 일정한 형식에 맞춰 표현한다.
2. **단순화**: 복잡한 현실세계를 약속된 규약에 의해 제한된 표기법이나 언어로 표현한다.
3. **명확화**: 대상에 대한 애매모호함을 제거하고 정확하게 현상을 기술한다.

## 데이터 모델링의 3요소
1. 어떤 것 (Things)
2. 성격 (Attribute)
3. 관계 (Relationships)

## 좋은 데이터 모델의 요소
1. **완전성**: 업무에 필요한 모든 데이터가 데이터 모델에 정의되어 있어야 한다.
2. **중복 배제**: 하나의 데이터베이스 내에 동일한 사실은 한 번만 기록하여야 한다.
3. **업무 규칙**: 데이터 모델링 과정에서 규명되는 수많은 업무규칙을 데이터 모델에 표현하고, 모든 사용자가 공유하도록 제공한다.
4. **데이터 재사용**: 데이터는 어플리케이션에 대해 독립적으로 설계되어야 재사용성을 향상시킬 수 있다.
5. **의사소통**: 데이터 분석 과정에서 도출되는 많은 업무규칙은 엔터티, 서브타입, 속성, 관계 등의 형태로 최대한 자세히 표현한다.
6. **통합성**: 동일한 데이터는 조직의 전체에서 한 번만 정의되고 이를 다른 영역에서 참조 및 활용한다.