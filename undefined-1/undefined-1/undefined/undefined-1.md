---
description: Teana Studio에서 엔티티 태깅하는 방법에 대해서 알아봅니다.
---

# 엔티티 태깅하기

> 엔티티(Entity)는 챗봇이 센텐스의 의미를 이해하기 위하여 작성된 체계적인 집합입니다. 엔티티에 대한 상세한 정보는 아래의 자세히 알아보기 버튼을 눌러주시기 바랍니다.
>
> [엔티티 자세히 알아보기 >](../../../undefined/undefined-2.md#1.)  &#x20;

## 1. 엔티티 태깅 개념

센텐스에 포함된 여러 단어 중, 특정 단어를 엔티티로서 지정하는 것을 엔티티 태깅이라고 합니다. 등록된 센텐스 안의 특정 단어를 태깅함으로써, 챗봇은 이 태깅된 부분을 통해 해당 발화문의 의도를 파악하기 위한 중요한 정보로 인식할 수 있습니다. 그래서 센텐스 내 모든 명사에 엔티티를 태깅하는 것이 응답 매칭률을 높이는 데 효율적입니다.

예시) '도서관 위치 알려줘' 라는 센텐스 내에서 \[도서관], \[위치]를 엔티티로 태깅하면 \[도서관], \[위치]가 포함된 '도서관 위치 궁금해' 와 같은 다른 센텐스들의 응답 매칭률이 높아집니다.&#x20;

## 2. 엔티티 태깅 방법

자동 태깅이 ON인 경우, 인텐트에 어떤 엔티티가 종속되는지 설정해주면 자동으로 태깅됩니다. 센텐스를 추가하거나 이미 등록된 센텐스에서도 엔티티를 태깅하거나 태깅된 엔티티를 수정할 수 있습니다.

수동으로 엔티티를 태깅할 때는 형태소 단위와 음절 단위로 태깅할 수 있습니다. 다음은 엔티티 태깅을 할 때 필요한 주요 기능에 대한 설명입니다.

![엔티티 태깅 모드  ](<../../../.gitbook/assets/1.엔티티 태깅 모드.png>)

➊ **태깅모드**

센텐스 입력 창의 좌측에 위치한 <img src="../../../.gitbook/assets/image (405).png" alt="" data-size="line">버튼 클릭시 태깅모드로 전환해서 태깅할 단어를 지정하거나 수정할 수 있습니다.



➋ **형태소 단위 (기본값)** &#x20;

태깅모드로 전환되면 해당 센텐스에서 형태소 단위로 단어를 선택해서 태깅할 수 있습니다. <img src="../../../.gitbook/assets/image (251).png" alt="" data-size="line">은 기본값으로 설정되기 때문에 바로 지정할 단어에 더블 클릭하면 형태소 단위로 태깅됩니다.



➌ **음절 단위**

태깅모드로 전환된 센텐스에서 음절 단위로 단어를 선택해서 태깅할 수 있습니다. **** <img src="../../../.gitbook/assets/image (138).png" alt="" data-size="line">버튼을 클릭하고 지정할 단어의 첫 음절과 끝 음절을 클릭하면 해당 단어가 태깅됩니다.



센텐스에서 태깅할 부분을 마우스 클릭하면 **엔티티 태깅 설정창**이 열립니다. 엔티티 설정창에서는 엔티티를 새로 생성하거나 검색하는 것이 가능합니다. 엔티티 태깅모드 시 나타나는 설정 화면은 아래와 같습니다.&#x20;

![엔티티 설정창](<../../../.gitbook/assets/2.엔티티 태깅 설정.png>)

➊ **취소 버튼**

엔티티 태깅 설정 창을 닫는 버튼입니다.

&#x20;  &#x20;

➋ **저장 버튼**

엔티티 태깅 설정 후에 반드시 저장 버튼을 눌러야 수정 사항이 적용됩니다.       ****   &#x20;

****

➌ **엔티티 검색**&#x20;

기존에 생성된 엔티티들 중에서 찾으려는 엔티티명을 입력 후, 엔터 또는 ![](<../../../.gitbook/assets/image (126).png>) 아이콘을 클릭하면 검색 결과가 나옵니다.            &#x20;



➍ **연결 엔티티 목록**

센텐스에 종속될 엔티티를 미리 지정한 연결 엔티티 목록입니다. 목록에 있는 엔티티들은 따로 등록하지 않아도 자동으로 태깅됩니다. 연결 엔티티에 대한 상세한 정보는 아래의 자세히 알아보기 버튼을 눌러주시 바랍니다.&#x20;

<mark style="color:blue;"></mark>[<mark style="color:blue;">연결 엔티티 자세히 알아보기 ></mark> ](undefined-2.md)   <mark style="color:blue;"></mark>  &#x20;

<mark style="color:blue;"></mark>

➎ **엔티티 추가**&#x20;

기존의 연결 엔티티에서 태깅하고 싶은 엔티티가 없다면 신규 엔티티를 연결 엔티티로 바로 추가해서 등록할 수 있는 기능입니다. 엔티티 명을 창에 입력한 후에 ![](<../../../.gitbook/assets/image (409).png>)아이콘 클릭하거나 엔터를 누르면 연결 엔티티 목록에 추가됩니다.



### 2-1. 엔티티 태깅 예시

![엔티티 태깅 예시 ](<../../../.gitbook/assets/엔티티 태깅 예시.gif>)

위 예시는 '도서관 위치 정보' 센텐스에서 \[정보]를 태깅하는 방법입니다.

➊ 센텐스 입력 창에 센텐스를 등록하고 태깅모드로 전환하기 위해 <img src="../../../.gitbook/assets/image (405).png" alt="" data-size="line">버튼을 누르고 태깅할 단어인 \[정보]를 더블 클릭합니다.    &#x20;

➋ 태깅모드가 전환되면 엔티티 태깅 설정창이 나타납니다. 기존 연결 엔티티 목록에 \[정보]가 없으므로, 엔티티 추가 창에 \[정보]를 입력한 후에 ![](<../../../.gitbook/assets/image (409).png>) 아이콘을 클릭해서 해당 엔티티를 추가합니다.&#x20;

➌ 연결 엔티티 목록에 추가된 \[정보]를 클릭하고 설정 버튼을 누르면 태깅이 설정됩니다.      &#x20;

➍ 마지막으로, 반드시 <img src="../../../.gitbook/assets/image (343).png" alt="" data-size="line"> 버튼을 클릭해야지 수정된 태깅이 적용됩니다.



{% hint style="danger" %}
**엔티티 태깅 시 주의사항**

센텐스에 태깅되는 단어는 엔트리여야 하고 유의어는 불가능합니다.          &#x20;
{% endhint %}

