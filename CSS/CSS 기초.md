# TIL: CSS 기초

CSS는 Cascading Style Sheets의 약자로 디자인 요소를 시각화하는 스타일 시트 언어이다.

## 목차

[1. CSS 문법 구성](#1-css-문법-구성)

  - [1.1. Tag Selector](#11-tag-selector)
  - [1.2. Id Selector](#12-id-selector)
  - [1.3. Class Selector](#13-class-selector)

[2. CSS 적용 방법](#2-css-적용-방법)

  - [2.1. 인라인 스타일](#21-인라인-스타일)
  - [2.2. 내부 스타일 시트](#22-내부-스타일-시트)
  - [2.3. 외부 스타일 시트](#23-외부-스타일-시트)

[3. 캐스케이딩(Cascading)](#3-캐스케이딩cascading)

## 1. CSS 문법 구성

![cssSelector](../img/cssSelector.png)

셀렉터는 태그 이름이나 id 또는 class를 선택한다.<br>
셀렉터로 특정 요소를 선택했다면 중괄호 안에서 이 요소에 적용할 내용을 작성한다.<br>
속성과 속성값의 끝에는 세미콜론(;)을 붙여 속성끼리 구분한다.

### 1.1. Tag Selector

CSS를 body, div, button 등 특정 태그에만 적용하기 위해서는 Tag Selector를 사용한다.

### 1.2. Id Selector

id는 문서 내에 단 하나의 요소에만 적용할 수 있는 유일한 이름으로 CSS를 특정 요소에 적용하기 위해서는 Id Selector를 사용한다.

사용 방법은 Selector 앞에 '#'을 붙인다.

### 1.3. Class Selector

동일한 기능을 하는 CSS를 여러 요소에 적용하기 위해서는 Class Selector를 사용한다.

사용 방법은 Selector 앞에 '.'을 붙인다.

## 2. CSS 적용 방법

HTML 문서에 CSS를 적용하는 방법에는 인라인 스타일, 내부 스타일 시트, 외부 스타일 시트가 존재한다.

### 2.1. 인라인 스타일

인라인 스타일은 HTML 요소 내부에 style 속성을 사용하여 CSS를 적용하는 방법이다.

```
<div style="color: red; background-color: yellow;">인라인 스타일</div>
```

### 2.2. 내부 스타일 시트

내부 스타일 시트는 HTML 문서의 head 태그 내부에 style 태그를 사용하여 CSS를 적용하는 방법이다.

```
<head>
  <style>
    div {
      color: red;
      background-color: yellow;
    }
  </style>
</head>
```

### 2.3. 외부 스타일 시트

외부 스타일 시트는 외부에 작성된 CSS 파일을 head 태그 내부에 link 태그를 사용하여 CSS를 적용하는 방법이다.

```
<head>
  <link rel="stylesheet" href="CSS_file_path">
</head>
```

## 3. 캐스케이딩(Cascading)

CSS에서 사용되는 캐스케이딩의 의미는 어떤 스타일을 적용 받을지에 대한 우선순위를 뜻한다.

우선순위는 아래와 같으며 코드 순서는 늦게 선언된 스타일이 우선 적용 된다.

1. 인라인 스타일 시트
2. 내부 스타일 시트
3. 외부 스타일 시트
4. 웹 브라우저 기본 스타일