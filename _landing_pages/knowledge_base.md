---
title: Knowledge Base
permalink: /knowledge_base/
---

When I'm working on projects, I'll often run into problems which I don't know
how to solve.

[![https://docs.google.com/file/d/0B0Jfms0twG8EclYtSnJEdEV1dzA/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EclYtSnJEdEV1dzA)](https://docs.google.com/file/d/0B0Jfms0twG8EclYtSnJEdEV1dzA/edit?usp=drive_web)

Ever had a moment like this during a project? Me too.

Often, I am able to find good tutorials on the subject. In other cases,
however, the resources I need are scattered about the web, the tutorials
available are not very good, or I simply can't find anything. In these cases, I
end up having to figure out things for myself. To help others (and myself!)
avoid struggling with these topics in the future, I'll be posting tutorials for
future reference.


{% for article in site.knowledge_base %}
    {% assign article_url_parts = article.url | split: '/' %}
    {% assign article_url_parts_size = article_url_parts | size %}
    {% if article_url_parts_size == 3 or article.path contains 'index' %}
# [{{ article.title }}]({{ article.url }})
[![{{ article.title }}]({{ article.image_path }}){:height="200px"}]({{ article.url }})
    {% endif %}
{% endfor %}
