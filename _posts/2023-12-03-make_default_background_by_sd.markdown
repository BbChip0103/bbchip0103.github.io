---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_Examples
title: Stable diffusion으로 게시물 썸네일 만들기

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
author: bbchip13
# multiple category is not supported
category: Life
# multiple tag entries are possible
tags: [
    Stable diffusion, 블로그 관리
]
# thumbnail image for post
img: ":post_pic_bg/post_pic_sample_00.png"
# disable comments on this page
#comments_disable: true

# publish date
date: 2023-12-03 12:31:00 +0900

# if not specified, date will be used.
#meta_modify_date: 2022-02-10 08:11:06 +0900
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

예전부터 블로그 글 올리면서 신경 쓰이는게 있었는데.

<img src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-17-02-47-image.png" title="" alt="" width="435">

바로 게시물의 대표 이미지.

아직 jekyll 테마 기본 이미지인지라 워터마크가 떡하니 박혀있다.

그냥 인터넷에서 아무 사진이나 가져와서 바꿀까 하다가, 그래도 나만의 이미지로 바꿔보자 싶었다.

<br>

봄, 여름, 가을, 겨울과 같은 계절 컨셉으로 4장 정도 만들까 했더니 괜찮은 체크포인트가 있더라.

<img src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-18-35-48-image.png" title="" alt="" width="554">

모델 필요하신 분은 [링크](https://civitai.com/models/5041/cheese-daddys-landscapes-mix)

시험삼아 몇 개 만들어보니 꽤 괜찮은 느낌으로 나왔음.

<img src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-18-51-49-image.png" title="" alt="" width="495">

사용한 프롬프트를 비롯한 설정은 [이 링크](https://civitai.com/images/471017) 참고.

<br>

목표하는 컨셉은 내 자캐 물고기가 저 동산에서 뛰노는 걸 하고 싶었기 때문에, 대충 포토샵에서 누끼따서 합성.

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-18-53-40-image.png" alt="" width="286">

당연히 이거 그대로 쓸 건 아니라서 누끼딴 김에 마스크도 같이 생성.

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-18-54-10-image.png" alt="" width="292">

그리고 img2img 입력으로 넣어보니

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-18-57-25-image.png" alt="" width="599">

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-18-58-32-image.png" alt="" width="415">

썩 나쁘진 않지만 그림체에서 나오는 위화감이 너무 크다...

<br>

그러다가 문득 자캐 살리는 건 포기하고 느낌만 녹여내는 식으로 하면 어떨까 싶었음.

다시 txt2img로 돌아가서 controlnet-canny 를 한 번 줘 봄.

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-01-28-image.png" alt="" width="281"> 

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-03-41-image.png" alt="" width="595">

흠 이건 아닌가... 

그러면 초반에는 자유롭게 만들고, 중간에만 잠깐 canny edge 따라 만들게 했다가 나중엔 다시 자유롭게 만들게 하면?

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-05-37-image.png" alt="" width="407">

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-07-08-image.png" alt="" width="415">

무슨 투명모드 동작한 것 같다.

애초에 controlnet의 제한 때문에 배경을 잘 못 만드는 경향이 매우 강한 듯 함.

<br>

canny가 너무 잔 선까지 그려내려고 해서 그런가 싶어 controlnet-lineart 쪽으로 변경해서 다시 시도.

<img src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-11-59-image.png" title="" alt="" width="417">

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-14-31-image.png" alt="" width="375">

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-16-15-image.png" alt="" width="368">

흠... 꽤 나쁘지 않은데...?

<br>

기세를 몰아 가을도 시도.

설정 및 프롬프트는 [링크](https://civitai.com/images/471006) 참조.

<img title="" src="../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-43-03-image.png" alt="" width="409">

이런 식으로 만들면 될 것 같다

<br>

### 결과물들

![](../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-58-21-image.png)

![](../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-58-29-image.png)

![](../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-58-37-image.png)

![](../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-58-43-image.png)

![](../assets/img/posts/2023-12-03-make_default_background_by_sd/2023-12-03-19-58-59-image.png)

<br>

아주 맘에 든다. 내가 별로 눈이 높지 않아서 그럴 지는 몰라도...

차후엔 포스트 내용에 맞춰서 이런 썸네일 이미지를 자동으로 뽑아주는 프로젝트를 해 볼 예정이다.

<br>

이 글이 누군가에게는 도움이 되었으면 좋겠다.
