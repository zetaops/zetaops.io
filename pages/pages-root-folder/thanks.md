---
title: "Mesajınız Onaylandı, Tesekkür Ederiz!"
layout: page
sitemap: false
permalink: /thanks/
header:
    image: header_typewriter.jpg
---

{{ site.data.language.if_you_are_not_redirected_automatically }} <a href="{{ page.redirect_to }}">{{ site.data.language.click_here }}</a>.
<script>
    setTimeout(function(){
        location='{{ site.url }}'
    },3000);
</script>