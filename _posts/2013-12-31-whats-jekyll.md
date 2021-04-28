---
layout: post
title: npm run build 시 os environment 관련 오류
# date element overrides date in title format.
date: 2021-01-25
tag:
  - common_tag
  - other_tag
---

### 원인 : 패키지와 설치된 node-sass 사이의 버전이 맞지 않아 발생

### Solution : node-sass를 재설치 해주면 된다.

``` shell
npm rebuild node-sass
```

위의 명령어로 재설치를 하는데, 내 환경의 경우 재설치 시에도 오류가 발생했다. node 자체의 버전이 패키지와 맞지 않아서였다. 이를 위해 npm 명령어를 통해 다른 노드 버전을 설치하고 기존 버전을 삭제했다.

````shell
sudo npm install -g n
n 5.6.0
<기존 버전 삭제 후>
npm rebuild node-sass
````

