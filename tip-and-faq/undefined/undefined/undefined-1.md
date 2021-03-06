---
description: 엔티티 작성 시 주의사항에 대해 알아봅시다.
---

# 엔티티 작성 시 주의사항

➊ **엔트리 중복 사용으로 인텐트 간 중복 센텐스가 발생하지 않도록 조정합니다.**

엔트리는 중복해서 사용하면 안됩니다. 엔티티 일괄 업로드 하기 전에, 엔트리 중복 체크는 필수입니다. 만약 중복 작성해서 엔티티 일괄 업로드한 경우, 상위 행에 있는 엔트리와 유의어가 등록되며 하위 행에 있는 엔트리는 등록되지 않습니다.

기본적으로 인텐트 별로 출력되는 응답메시지가 설정되어 있는데 2개 이상의 인텐트 안에 동일한 센텐스가 등록되어 챗봇이 학습한다면 학습 오류가 발생할 수 있습니다.                                               &#x20;

![인텐트간 중복 센텐스 발생 예시   ](<../../../.gitbook/assets/인텐트간 중복 센텐스 (2).png>)

위의 예시처럼, '도서관' 엔티티와 '판교도서관' 엔티티는 서로 다른 엔티티이지만 소속된 엔트리 중 '도서관' 엔트리가 동일합니다. 이 경우, \[도서관\_운영시간]과 \[판교도서관\_운영시간] 인텐트 간에 중복 센텐스가 발생하는 오류를 볼 수 있습니다.         &#x20;

&#x20;   &#x20;

➋ **같은 인텐트에 사용되는 엔티티는 서로 엔트리가 겹치지 않도록 구성합니다.**

같은 인텐트 안에서도 사용되는 엔티티 안에 소속된 엔트리가 중복되지 않도록 주의해야 합니다. 사용되는 엔트리가 같은 경우, 센텐스 내 자동 태깅시에 오류가 발생할 수 있습니다.                         &#x20;

![엔트리 중복 발생 예시   ](<../../../.gitbook/assets/엔트리 중복 발생.png>)

위의 예시처럼, 용례상 \[알림] 엔티티에 \[안내] 엔트리를 추가할 수 있지만, 다른 \[안내] 엔티티의 엔트리와 중복되는 경우, 자동태깅이 제대로 기능하지 않습니다.                          &#x20;



➌ **한 단어를 두 개 이상의 엔티티로 태깅하지 않습니다.**

엔티티를 태깅할 때는 명사형 단어와 명사와 명사가 결합된 단어 형태의 명사구인지 확인하며 태깅할 필요가 있습니다. 둘 이상의 명사가 결합(N1 + N2)되어 형성된 합성명사를, 형태소 단위로 분해(N1, N2를 각각 분리)하여 엔티티를 생성하고 각 단어에 태깅했을 경우 태깅 오류가 발생합니다.                    ****        &#x20;

![엔티티 태깅 오류 예시](<../../../.gitbook/assets/엔티티 태깅 오류 예시.png>)

위의 예시인, \[이용법]은 '이용법' 자체가 하나의 단어이므로 이용과 법으로 나눠서 태깅하게 되면 오류가 발생합니다. 한 단어인지 여부는 표준국어대사전을 참고합니다. 형태소 분석 결과는 Teana Studio 탑재 후 시뮬레이션을 돌려서 NLU 분석 결과에서 확인할 수 있습니다.&#x20;

[시뮬레이션 및 NLU 상세 자세히 알아보기 > ](../../../undefined-1/undefined-3/undefined.md#3.) &#x20;

&#x20;          &#x20;

➍ **센텐스 작성 시, 엔티티의 확장으로 같은 단어가 두 번 반복되지 않도록 조정합니다.**

![단어 반복 발생 예시   ](<../../../.gitbook/assets/image (219).png>)

엔티티나 엔트리에 사용되는 단어들이 센텐스 안에 연이어 반복되는 경우 정확도 스코어가 하락될 수 있습니다. 정확도 스코어는 지식검증을 통해 확인 가능하며 정상 센텐스 중, 정확도가 100%가 되지 않는 센텐스의 경우 이러한 사례들이 있으므로 확인이 필요합니다.     &#x20;
