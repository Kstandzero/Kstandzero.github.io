---
layout: single
title: "[LG Aimers 3기] Module 1. AI 윤리"
categories: LGAimers
tag: AI
use_math: false
---

## 1. 데이터 분석과 AI학습에서 유의할 점
<span style="color:red"> **1) 데이터의 확보, 전처리, 분석, 해석의 전 과정이 중요하다.**</span>  

<span style="font-size:95%">**데이터를 잘 해석하고 있는가?**</span>  
<span style="font-size:90%">
예를 들어, 상관관계는 인과관계와 다르다. 데이터 과학자라면 이러한 부분을 혼용하여 사용하거나 혼동하면 안 된다.</span>

<span style="font-size:95%">**데이터 전처리와 분석 방법은 적절한가?**</span>  
<span style="font-size:90%">
    - Error bar 추가하기  
    - 적합한 통계 테스트 찾기  
    - 아웃라이어 제거하기  
    - 데이터 표준화하기  
    - EDA(Exploratory Data Analysis) 충분한 시간을 보내기
</span>

<span style="font-size:95%">**학습에 쓰는 데이터가 충분한가?**</span>  
![Kstandzero]({{site.url}}/images/2023-07-10-%5BLGAimers3%EA%B8%B0%5DModule1/FittingGraphs.jpg)
<br>
<span style="font-size:90%">
**Under-fitting** : 충분하기 설명하기에는 너무 간단한 모델  
**Over-fitting** : 데이터가 조금만 달라져도 무용지물이 될 수 있는 모델
</span>

<span style="font-size:90%">
    - 데이터 학습의 결과가 적절한 수준인지에 대한 인식이 있어야 한다.  
    - 학습(training) 데이터는 테스트(testing) 데이터와 달라야 한다.
</span>  

<br>

<span style="color:red">**2) 고품질의 데이터가 입력되었을 때 학습 결과도 유의미하며, 데이터가 가지는 오차 범위와 특이점, 대표성에 대한 충분한 이해를 가지고 접근해야 한다.**</span>  

<span style="font-size:95%">**알고리즘의 설명력 문제**</span>  
<span style="font-size:90%">
    - 흔히 AI 기반 학습 알고리즘은 설명 가능하지 않고 블랙박스 형태라는 단점이 있다.  
    - 하지만 High risk 결정에서는 설명력도 정확도 만큼이나 중요해졌다.  
    - Saliency map, SHAP와 같이 post-hoc explainability(사후 설명력)를 제공하는 기술이 생겼다.  
</span>

<span style="font-size:95%">**알고리즘의 편향, 신뢰 문제**</span>  
<span style="font-size:90%">
    - 의견의 대표성 : Spiral of silence (인터넷 상의 의견이 대표성 있는 의견이 아닐 수 있음을 인지해야 한다.)  
    - 오정보의 빠른 확산으로 인한 인포데믹(infodemic) 현상 : 사실정보와 더불어 오정보의 양이 늘어 구분이 어려워지는 정보 과부화 현상
    - 예시 : Predictive Policing, Recruiting, Hate Speech
</span>

<span style="font-size:95%">**유의해야할 사항**</span>  
<span style="font-size:90%">
    - 알고리즘의 설명력, 편향, 신뢰의 문제에 주의해야 한다.   
    - 블랙박스 알고리즘이 실제 사회에 사용되기 위해서는 많은 경우 설명력 보강이 필요하며, 노이즈와 데이터 가변성에도 대처 가능한 알고리즘을 개발하도록 노력해야 한다.   
    - AI가 다양한 사회 서비스에서 인간 결정을 돕거나 대체함에 따라 윤리적 의사결정이 확보되도록 점검해야 한다.  
</span>

<br>
<br>

## 2. AI Ethics
<span style="color:red"> **인간의 창조적 활동 영역으로 들어온 인공지능**</span>  
<span style="font-size:90%">
작문, 미술, 음악 등 다양한 영역의 활동을 인공지능이 수행할 수 있게 되었다.  
이처럼 AI가 기술혁신과 창작 도구로 활용이 점차 확대됨에 따라, 인간의 개입 없이 독자적 창작과 혁신활동이 가능한 수준으로 발전할 것으로 보인다.
</span>  

<span style="color:red"> **AI 시대 지식재산, 법인격, 처벌, 그리고 윤리의 문제 부각**</span>  
<span style="font-size:90%">
세계적으로 AI에 의한 발명과 저작 등에 대한 법제 정비, 미래에 강한 AI 등장 시 법인격 부여 여부 논의, 오동작 시 처벌과 윤리 규정 마련 등이 필요하며, 이러한 논의는 다양한 계층 시민의 수요와 요구를 반영하도록 유의해야 한다.
</span>

<br>
<br>

<span style="font-size:80%">
본 글은 LG Aimers 3기에 참여하여 듣게 된 강의의 내용을 정리한 것으로, 본 글의 출처는 LG Aimers에 있습니다.
{: .notice}
</span>