---
tags:
  - 개발
  - 블로그
  - 업로드
Categoría: []
title: NextJS 404 페이지 변경
date: 2025-03-05T00:02:00
---

# 404 페이지를 바꿔보자


### NextJS 404 페이지 변경하기 

따로 잡아주는게 아님...

알고보니까 NextJS가 자동으로 404를 만들어주는 모습을 ~~(신기한 모습을)~~ 확인할 수 있는데...

그걸 어떻게 바꾸냐는 다른 문제!

따라서 

```bash
 app
  |
  |- NOT_FOUND.js(tsx,ts,jsx)
```

이렇게 만들어주면... 알아서 해당 페이지를 컴파일하고 404의 경우 불러오더라...

```tsx
export default function NotFoundPage() {
  return (
    <div className="flex flex-col items-center justify-center h-full min-h-[calc(100vh-16rem)]">
      <h1 className="text-4xl font-bold mb-4">404 Not Found!</h1>

      <hr className="w-1/3 my-4" />

      <h2 className="text-xl mb-2">이 페이지는 존재하지 않습니다</h2>
      <h3 className="text-muted-foreground">뱅어포에게 보고하기</h3>
    </div>
  );
}
```
