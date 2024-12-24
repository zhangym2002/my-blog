---
title: "First Deploy"
date: 2024-12-24T12:55:00-06:00
author: "Yiming"
slug:
draft: false
toc: false
---


按照[郝鸿涛大佬的教程](https://hongtaoh.com/cn/2024/03/22/personal-website-tutorial/)成功部署网站，但仍有几个细节需要注意。

1. 在首次使用`git push`到GitHub repo时，可能需要输入Github账号密码。这里密码需要使用Github Setting - Developer Setting - Personal access tokens，因为Github已不再支持只使用账号密码链接。
2. 使用**Vercel**部署确实会比GitHub pages简单很多，域名也可以在domains处修改。
3. 在**Vercel**中部署时使用的Hugo版本时0.119.0，而本地新安装的版本为0.140.1。如果直接在本地使用`hugo server -D`，会显示存在以下问题：

> ERROR deprecated: .Site.LastChange was deprecated in Hugo v0.123.0 and will be removed in Hugo 0.141.0. Use .Site.Lastmod instead.

但在Vercel中因为版本较低则不用修改，部署并不会报错。之后可能需要将`.Site.LastChange`修改为`.Site.Lastmod`。