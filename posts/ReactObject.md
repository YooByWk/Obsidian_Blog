---
tags:
  - 개발
  - 블로그
  - 업로드
Categoría:
  - "[[컬렉션 - Blog 포스팅 리스트]]"
title: React에서 Object.entries() 사용하기
date: 2025-03-05T01:02:00
---

# 아. 외 않됌? 

정말 간만에 만드는 프론트 페이지? 라서 그런지, 어떻게 돌려야 이쁠까 고민하던 중 아 Map 돌리자! 라는 간단한 마음으로 시작헀지만 안되는 모습을 보아하니... 나는 너무 슬퍼졌다.

하나하나 하드코딩하기엔 뭔가 자존심이 팍팍 상하는 기분이 너무 들어서 한번 부딪혀보기로 했다. ~~평소에 공부좀 할걸~~

## 문제상황 

**이건 안된다!!!!**

```ts
  const techStacks = {
    frontend: ["Next.js", "TypeScript", "Nuxt.js", "React.js", "Vue.js"],
    backend: ["Node.js", "Nest.js", "SpringBoot", "Django"],
    else: ["GitHub API", "Obsidian", "PostgreSQL", "prismaORM",]
  };
```
이런 예시로 만든 요소를 

```tsx
techStacks.map((tech)=> (
<div>
	{tech}
</div>))
```

이런 느낌은 안되더라구요?

그래서 조금 돌아서 해결하기로 했습니다. 

## 해결
```tsx
{Object.entries(techStacks).map(([category, stacks]) => stacks.length > 0
  ? (
	<div className="mb-4" key={category}>
	  <h2 className="text-xl font-semibold space-y-4 my-5">
		  {category.toUpperCase()}
	  </h2>
	  <div className="grid gird-cols-2 md:grid-cols-4 gap-4">
		{stacks.map((tech) => (
		  <Card className="p-4 text-center retro-shadow">
			{tech}
		  </Card>
		))}
	  </div>
	</div>
  )
  : null
)}
```

뭔가 간단하게 해결된 느낌.

2번 순회해야하지만

```ts
Object.entries([key, value]) 
// return 값

```

를 사용해보자.

`Object.keys(obj)` 돌린것과, `Object.values(obj)`의 결과물을 `[key,value]` 로 묶어서 반환한다고 보면 되겟다


미리 알아둬야 하는 것

- 객체가 정의된 방법과 관련없는 정렬 순서로 나온다! 만약 정렬된 결과를 원한다면   
    `Object.entries(obj).sort((a, b) => b[0].localeCompare(a[0]));`를 사용하자   

<hr>

## 참고문헌

https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Object/entries