---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: 首页
---
欢迎来到我的博客！
# 最新文章

<ul>
{% for post in site.posts %}
  <li>
    <span style="white-space:nowrap;">{{ post.date | date: "%Y-%m-%d" }}</span>
    &nbsp;—&nbsp;
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    {% if post.excerpt %}
      <div style="margin: .25rem 0 1rem; color:#666;">
        {{ post.excerpt | strip_html | truncate: 160 }}
      </div>
    {% endif %}
  </li>
{% endfor %}
</ul>
