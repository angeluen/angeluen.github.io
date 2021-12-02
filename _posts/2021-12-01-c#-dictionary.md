---
title: C#-01 Dictionary
author: EnRU
date: 2021-12-01 09:33:00 +0800
categories: [C#, Dictionary]
tags: [C#]
math: true
mermaid: true

---

## 01. Dictionary 

`KeyValuePair` 방식으로 `Key` 값을 이용해 `Value`를 가져오는 방식이다.

내부는 `HashTable` 구조로 구현되며 값을 검색하면 O(1)의 시간 복잡도로 검색 작업이 된다.

주어진 키를 `HashCode`(정수)로 바꾸고, 이를 적당한 알고리즘을 통해 `HashKey`로 바꾼다. 

Dictionary는 충돌을 해결하기 위해 `Chaining`(각 HashTable bucket에 항목 목록을 유지함)에 의존한다.

Dictionary는 HashTable과는 다르게 자료형이 선언되어 있어 `boxing` 문제가 없다. 다만 자료형이 선언 되어 있는 문제때문에 모든 타입을 담을 수 없다.

단점
---
- 항목이 저장되는 순서가 항목을 추가하는 순서와는 다름.
- 정렬되지 않음. 정렬을 원하면 SortedDictionary(RB Tree)를 사용.




주의사항

- Dictionary는 유니크한 `Key`를 가져 야만 하여 동일한 `Key`를 `Add` 하는 경우에는 `Error`를 발생한다.
이는 배열 참조 형식으로 데이터를 넣으면 수정 할 수 있다.
또는 ContainsKey로 이미 데이터가 있는지 검사해서 넣어주면 된다.

```csharp
_dictionary[key] = value
```

참고 링크 : [**MS API 문서**][studylink]


[studylink]: https://docs.microsoft.com/ko-kr/dotnet/api/system.collections.generic.dictionary-2?view=net-6.0