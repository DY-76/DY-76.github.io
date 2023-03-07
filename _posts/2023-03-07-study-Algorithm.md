---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Study_
title: Algorithm] 피터슨 알고리즘(Peterson's algorithm) 이해하기

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
#author: ""
# multiple category is not supported
category: study
# multiple tag entries are possible
tags: [algorithm]
# thumbnail image for post
img: ":post_title/algorithm1.jpg"
# disable comments on this page
comments_disable: true

# publish date
date: 2023-03-07 09:00:00 +0900

# seo
# if not specified, date will be used.
#meta_modify_date: 2022-11-26 20:00:00 +0900
# check the meta_common_description in _data/owner/[language].yml
#meta_description: ""

# optional
# if you enabled image_viewer_posts you don't need to enable this. This is only if image_viewer_posts = false
#image_viewer_on: true
# if you enabled image_lazy_loader_posts you don't need to enable this. This is only if image_lazy_loader_posts = false
#image_lazy_loader_on: true
# exclude from on site search
#on_site_search_exclude: true
# exclude from search engines
#search_engine_exclude: true
# to disable this page, simply set published: false or delete this file
#published: false
---

<!-- outline-start -->

- **교착 상태 (Dead lock)**
  - 둘 이상의 프로세스가 다른 프로세스가 점유하고 있는 자원을 서로 기다릴 때 **무한 대기**에 빠지는 상황

  Ex) A,B = 프로세스(Process) | 노트, 연필 = 자원(공유자원, Shared Resource)

  ![Untitled](:contents/2023-03-07-study/deadLockex.png)

- **임계 영역 (Critical Section)**
  - 공유자원(Ex. 연필, 노트)에서 문제가 발생하지 않게 독점을 보장해줘야 하는 영역
    (위 예시에서는 노트필기)

  ![Untitled](:contents/2023-03-07-study/criticalSectionex.png)

- **임계 영역의 해결방안**
  - **상호 배제 :** 한 프로세스가 임계 영역에 들어갔을 때 다른 프로세스는 들어가지 마!
  - **한정 대기 :** 그렇다고 한 프로세스가 영원히 못들어가도 안되지,, 대기는 유한하게 해!
  - **진행 or 융퉁성 :** 임계 영역에 들어간 프로세스가 없는 상태에서, 들어가려고 하는 프로세스가 여러 개 있다면 어느 것이 들어갈지를 적절히 결정해주어야 하는데,,, 어쩌지?

에서 나온 아이디어들이 바로 데커 알고리즘(Dekker's algorithm), 피터슨 알고리즘(Peterson's algorithm) 등등이다.

**Then, What is Peterson’s algorithm?**

![Untitled](:contents/2023-03-07-study/PetersonRule.png)

<!-- outline-end -->


