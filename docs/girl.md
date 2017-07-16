---
layout: page
title: 能力表
permalink: /docs/girl/
---

能力表是能力制作的基准。
如果程序中的表现与本文档的描述出现任何出入，
那就说明程序有问题， 可作为bug发馈到贴吧。
如果程序中出现有关本文档中未提及的细节的问题，
或文档本身出现与原作不符的描述， 可作为能力提案反馈。
反馈时不要忘了参考[规范](/feedback/)，从而获得「榴莲汁」。

以下正文中带（\*）的能力尚未实现，旨在提前放出制作计划以供讨论。

## 目录

<ul>
{% for girl in site.data.girls %}
  <li><a href="#{{ girl.id }}">{{ girl.name }}</a></li>
{% endfor %}
</ul>

<br />

## 正片
----
{% for girl in site.data.girls %}
<h3><a name="{{ girl.id }}"></a>{{ girl.name }}</h3>
{% for skill in girl.skills %}
<h4> {{ skill.name }} </h4>
<ul>
{% for desc in skill.descs %}
<li>{{ desc.content }}
{% if desc.subdescs %}
<ul>
{% for subdesc in desc.subdescs %}
<li>{{ subdesc }}</li>
{% endfor %}
</ul></li>
{% else %}
</li>
{% endif %}
{% endfor %}
</ul>
{% endfor %}
----
{% endfor %}

