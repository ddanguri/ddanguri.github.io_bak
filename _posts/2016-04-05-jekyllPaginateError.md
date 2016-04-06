---
layout: post
title:  "Deprecation: You appear to have pagination turned on, but you haven't included the `jekyll-paginate` gem"
date:   2016-04-05 19:07:49
categories:
- error
comments: true
---

오늘 jekyll 을 빌드하니 아래와 같이 에러가 난다. -_-

``` command
$ jekyll build
Configuration file: E:/Dev/ddanguri.github.io/_config.yml
       Deprecation: You appear to have pagination turned on, but you haven't included the `jekyll-paginate` gem. Ensure you have `gems: [jekyll-paginate]` in your configuration file.
            Source: E:/Dev/ddanguri.github.io
       Destination: E:/Dev/ddanguri.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 0.618 seconds.
 Auto-regeneration: disabled. Use --watch to enable.
```

찾아보니 JeKyll3 에서 _config.yml 파일에 아래와 같이 추가해줘야 되는 항목이 있다. (https://teamtreehouse.com/community/jekyllpaginate-gem)

```
gems : [jekyll-paginate]
paginate: 5
paginate_path: "page:num"
```
