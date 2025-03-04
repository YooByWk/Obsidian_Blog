---
tags:
  - 블로그
  - 미업로드
  - 개발
Categoría: []
title: NextJs에 Github에서 불러온 정보 집어넣기
date: 2025-03-04T22:02:00
---

# 직판장 오픈!@

~~정상 영업합니다~~

직판장의 원할한 서비스를 위한 준비를 다루는 포스팅입니다.

제발~ 잘 되면 좋겠다!
NextJS를 처음 써보는데... 생각보다 어렵네요...

### 시작하기

Vercel이 Nextjs 플젝을 만들어줬다.
헤헤 편하다

포폴도 여기서 만들면 좋겠다는 생각이 들었다.
이미 배포된 환경에 하나 서브도메인을 넣어버리거나 그런 느낌으로!

커스텀은 소중하니까

```bash
npm install
npm run dev
```

간만에 프론트 개발 들어갔는데 음 하나도 모르겠다!!!!!!!!!

아무튼 만들어봅시다.

## Octokit

Octokit은 Github REST API를 쉽게 상호작용 할 수 있도록 해준다.

우선 프로젝트에 추가하자.

```bash
npm install @octokit/rest
npm install -D @octokit/types
```

Octokit을 사용하기로 한 이유는 프론트엔드 코드에 md 파일을 포함하지 않고 `@octokit/rest`를 통해 외부 저장소에서 동적으로 마크다운 파일을 끌어오기 위함이다.

### 설정

### 코드 쓰기

### 불러보기

### env 배포 환경 설정
