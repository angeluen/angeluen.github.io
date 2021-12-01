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

C#의 Dictionary 는 C++의 `Map`과 비슷한 구조를 가지고 있다. 

`KeyValuePair` 방식으로 `Key` 값을 이용해 `Value`를 가져오는 방식은 같다.

내부는 `HashTable` 구조로 구현되며 값을 검색하면 O(1)의 시간 복잡도로 검색 작업이 된다.


주의사항

- Dictionary는 유니크한 `Key`를 가져 야만 하여 동일한 `Key`를 `Add` 하는 경우에는 `Error`를 발생한다.
이는 배열 참조 형식으로 데이터를 넣으면 수정 할 수 있다.
또는 ContainsKey로 이미 데이터가 있는지 검사해서 넣어주면 된다.

```csharp
_dictionary[key] = value
```

참고 링크 : [**MS API 문서**][studylink]


[studylink]: https://docs.microsoft.com/ko-kr/dotnet/api/system.collections.generic.dictionary-2?view=net-6.0