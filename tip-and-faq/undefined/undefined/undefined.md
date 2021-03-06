---
description: 엔티티 작성 요령에 대해 알아봅시다.
---

# 엔티티 작성 요령

➊ **엔티티는 명사여야 합니다.**

* 활용에 따라 형태가 바뀌는 동사, 형용사는 엔티티로 구축하지 않습니다.
* 형태가 변하지 않는 부사의 경우에도 원칙적으로는 엔티티로 작성이 가능하나, 문장 확장에 큰 영향은 없습니다.

![구축된 엔티티로 센텐스 확장](<../../../.gitbook/assets/명사 엔티티.png>)

기본적으로 명사 형태의 엔티티로 구축하고 태깅한 엔티티를 중심으로 여러 형태의 센텐스를 확장하고 구축할 수 있습니다.



➋ **엔티티를 엔트리에 포함시켜야 합니다.**

* 엔티티는 엔트리 입력 후 유의어를 입력하는 방식으로 구축합니다.  ****  &#x20;
* 엔티티는 그룹명으로, 실제 사용할 단어라면 엔트리에 꼭 추가시켜야 합니다.

![엔티티 등록 예시](<../../../.gitbook/assets/image (45).png>)

위의 예시는 "신분증" 엔티티의 구축 예시입니다. 엔티티 "신분증"을 생성하기 위해서는 최소 1개의 엔트리를 등록해야하며, "신분증"이 엔트리로 포함되어야 합니다. "신분증" 이외에도 실제 신분증의 의미로 사용하는 '여권', '운전면허증', '주민등록증'을 엔트리로 추가하고, 각 엔트리와 동일한 의미로 쓰이는 유의어를 등록함으로써 사용성을 위해 하나의 엔티티를 보다 효과적으로 구축해야합니다.

{% hint style="danger" %}
**특수문자 입력 주의사항**

엔티티 및 엔트리 작성 시 특수문자 입력이 불가합니다. 단, 엔티티 상속 기능  활용 시, '@' 사용 가능**.**

허용되는 특수 문자 : @ \* / + { } ^ $ = ( ) \_ - \ · ] \[ , ! : · ' ? 『 』 「 」 " ‘ ’  &#x20;
{% endhint %}



➌ **두 단어 이상 포함이 가능합니다.**  &#x20;

* 지식의 특성에 따라 두 단어 이상 조합하여 작성할 수 있습니다.
* 엔트리는 명사형 단어와 명사와 명사가 결합된 단어 형태의 명사구로 확장이 가능합니다.

![\[수도요금\] 엔티티 예시 ](<../../../.gitbook/assets/두단어 이상 엔티티 (2).png>)

위의 예시처럼, "수도요금"은 "수도"와 "요금" 두 명사가 결합된 단어 형태의 명사구입니다.&#x20;

1번 방안은 "수도"와 "요금"을 각각 엔티티로 구축한 경우입니다. 이 경우, "수도세 문의" 등 쪼갤 수 없는 단어인 "수도세"가 포함된 센텐스는 처리가 불가능합니다.&#x20;

2번 방안은 "수도 사용한 요금 문의" 등 "수도"와 "요금"이 떨어진 센텐스의 경우 처리가 불가능합니다. 지식의 특성에 따라 이 2가지 방안 중 보다 효과적인 방안을 고려해서 엔티티를 구축하도록 합니다.                                                  &#x20;

&#x20;

➍ **사전, 사용자 대화 이력 등을 참고합니다.**

엔티티의 엔트리 구성 시, 포털사이트의 어학사전 내 유의어 및 반의어를 참고하여 구성합니다.

![참고 포털사이트 경로](<../../../.gitbook/assets/네이버 사전.png>)

&#x20;&#x20;
