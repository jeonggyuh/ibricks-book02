---
description: 지식 구축의 기본 개념인 인텐트에 대해 알아봅니다.
---

# 인텐트

## 1. 인텐트 정의&#x20;

인텐트(Intent)란 사용자의 발화 의도로 대화(질의·응답)의 단위입니다. Teana Studio에서 인텐트는 1개의 의도를 가지며 챗플로우(Chatflow, 대화 흐름)를 구성하는 요소 중 하나로 활용됩니다. 하나의 인텐트는 보통 유사한 의도를 가진 다수의 질의와 1개의 응답으로 구성됩니다. (분기 시나리오 제외)           &#x20;

## 2. 인텐트 구조

하나의 인텐트 안에는 해당 인텐트에 맞춰 작성된 학습 문장들인 센텐스로 구성되어 있고 각각의 센텐스는 연관된 엔티티와 파라미터들이 포함되어 있습니다. 챗봇을 잘 설계하기 위해서는 이 인텐트의 구성이 매우 중요합니다. 인텐트를 생성하고 관리하는 방법에 대한 상세 내용은 **챗봇만들기 > 대화 생성 방법 >** [**인텐트 생성하기**](../undefined-1/undefined-1/undefined/#2.)에서 확인할 수 있습니다.                                          &#x20;

인텐트의 구조를 시각화하면 다음과 같습니다.

![인텐트의 구조](<../.gitbook/assets/인텐트 구조 (3).png>)

### 2-1. 인텐트 예시

다음은 \[시설\_도서관위치] 인텐트에 대한 예시입니다.&#x20;

| 인텐트명      | 응답 메시지                                                    | 센텐스                                                                                                                                        | 엔티티                                                             |
| --------- | --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------- |
| 시설\_도서관위치 | <p>아이브릭스 도서관은 2층입니다.</p><p>엘레베이터를 타고 이동하시면 됩니다.      </p> | <p>아이브릭스 도서관 위치</p><p>아이브릭스 도서관 어디있어</p><p>도서관 위치 안내</p><p>도서관 위치 알려줘</p><p>도서관 위치 궁금해</p><p>도서관 위치 정보</p><p>도서관 몇층에 있어               </p> | <p>아이브릭스                   도서관</p><p>위치</p><p>안내</p><p>정보  </p> |

&#x20;

&#x20;          &#x20;