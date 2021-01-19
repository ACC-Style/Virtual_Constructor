---
title:  "Twitter Tag"
date:   2021-01-15 10:14:44 -0500
categories: icons
---
<div class="ul_none grid template-x_20 gap-y_5 gap-x_4 font_1">
{% for twitter in site.data.TwitterList %}
<div>
{{ twitter.name}}
<a data-sf-ec-immutable="" href="https://twitter.com/{{twitter.tag}}" class="link block">@{{twitter.tag}}</a></div>
{% endfor %}
</div>
