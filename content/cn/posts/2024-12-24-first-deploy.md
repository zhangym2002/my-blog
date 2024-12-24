---
title: "First Deploy"
date: 2024-12-24
author: "Yiming"
slug:
draft: false
toc: false
---

按照[郝鸿涛大佬的教程](https://hongtaoh.com/cn/2024/03/22/personal-website-tutorial/)成功部署网站，但仍有几个细节需要注意。

1. 在首次使用`git push`到GitHub repo时，可能需要输入Github账号密码。这里密码需要使用Github Setting - Developer Setting - Personal access tokens，因为Github已不再支持只使用账号密码链接。
2. 使用**Vercel**部署确实会比GitHub pages简单很多，域名也可以在domains处修改。
3. 在**Vercel**中部署和在本地`hugo server -D`时，会常见以下版本相关问题：

> ERROR deprecated: .Site.LastChange was deprecated in Hugo v0.123.0 and will be removed in Hugo 0.141.0. Use .Site.Lastmod instead.

解决方法是：在`vercel.json`文件中设定为较低版本（如0.119.0）和Vercel Settings- Environment variables指定`HUGO_VERSION`为较低版本（如0.119.0）。这样本地和部署都没问题。