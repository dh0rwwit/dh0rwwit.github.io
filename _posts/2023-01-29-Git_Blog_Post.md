---
title: Test Article by dh0rwwit
author: dh0rwwit
date: 2023-01-29 20:18:00 +0900
categories: [Blogging, Tutorial]
tags: [writing]
render_with_liquid: false
---


D:\Git_Blog\~.github.io\_posts 안에 포스트를 작성하는데
해당 파일 제목에 띄어쓰기가 있으면 안 됨

그리고 작성하고 commit and push하기 전에 항상 
``` cmd
bundle exec jekyll serve
```
를 실행해줘야 하는 번거로움이 있다....

깃허브로 블로그 만들고 구글에 검색 활성화에 추적까지는 
[https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-4/](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-4/) 이 분 홈페이지 보고 만들었다.

댓글 기능은 https://utteranc.es/ 에서 repo 입력
Issue title contains page URL 체크
해서 생성된 스크립트를 
D:\Git_Blog\dh0rwwit.github.io\_layouts\posts
안에 추가 해줘서 만들었다.

![use-English-uploading-Photo](assets/img/favicons/utteranc_Script.png){: width="928" height="797"}

![google-analytics-data-stream](/posts/20210103/01-google-analytics-data-stream.png){: width="1086" height="542"}

## Naming and Path

글씨 진하게 : 작은 따옴표 이용
{: .filepath} 이건 뭔지 모르겠다.
링크 : [네이버](https://www.naver.com/)

## Front Matter
코드입력하기
윗 첨자(`)를 3개 입력하여 시작하고 다시 3개를 입력하여 닫는다.
``` Title
title: TITLE
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [TAG]     # TAG names should always be lowercase
```

녹색 전구 : 오른쪽 방향 '>'를 입력하면 된다.
근데 {: .prompt-tip }은 왜 있는지 모르겠다. 문미에 입력해야 하는건가
이 안에서 윗 첨자를 글을 감싸면 `이렇게` 된다.

기울임 : _아래 하이픈?_

### Timezone of Date

In order to accurately record the release date of a post, you should not only set up the `timezone` of `_config.yml`{: .filepath} but also provide the post's timezone in variable `date` of its Front Matter block. Format: `+/-TTTT`, e.g. `+0800`.

### Categories and Tags
```yaml
---
categories: [Animal, Insect]
tags: [bee]
---
```

### Author Information
'>'를 입력하고 {: .prompt-info }를 문미에 입력하면 파란색 음영박스에 느낌표나타난다.

## Table of Contents

대문자 입력은 '**'을 2개 입력하면 된다. 
**와일드카드 2개를 입력한다**

## Mermaid
큰 괄호안에 와일드 카드 2개로 글을 다시 감싸고 옆에 링크를 붙이면 
[**네이버**](https://www.naver.com/)

[https://www.**youtube**.com/watch?v=**H-B46URT4mg**](https://www.youtube.com/watch?v=H-B46URT4mg)

### Position

``` 주황색 느낌표
> 오른쪽 화살표 입력후 중괄호 안에 : .prompt-warning
{: .prompt-warning }

```


- **Normal position**
  {: .nolineno}  이게 뭔지 모르겠다.



### 영상 올리기
```
|column 1                              |column 2           | 
|--------------------------------------|-------------------|
|other language like korean doesn't fit| `value`           |

| Video URL                                                                                          | Platform  | ID            |
|----------------------------------------------------------------------------------------------------|-----------|:--------------|
| [https://www.**youtube**.com/watch?v=**H-B46URT4mg**](https://www.youtube.com/watch?v=H-B46URT4mg) | `youtube` | `H-B46URT4mg` |
| [https://www.**twitch**.tv/videos/**1634779211**](https://www.twitch.tv/videos/1634779211)         | `twitch`  | `1634779211`  |

```