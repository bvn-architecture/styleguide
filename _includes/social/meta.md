<!-- Twitter card markup -->
{% if site.twitter_username %}
<meta name="twitter:card"        content="summary" />
<meta name="twitter:site"        content="{% if page.twitter_username %}{{ page.twitter_username }}{% else %}{{ site.twitter_username }}{% endif %}" />
<meta name="twitter:title"       content="{% if page.title %}{{site.title}} - {{page.title}}{% else %}{{ site.title }}{% endif %}" />
<meta name="twitter:description" content="{% if page.description %}{{ page.description }}{% else %}{{ site.description }}{% endif %}" />
<meta name="twitter:image"       content="{% if page.image %}{{ page.image }}{% else %}{{ site.image }}{% endif %}" />
<meta name="twitter:creator"    content="{% if page.twitter_username %}{{ page.twitter_username }}{% else %}{{ site.twitter_username }}{% endif %}">
{% endif %}

<!-- Schema.org markup for Google+ -->
<meta itemprop="name"             content="{% if page.title %}{{site.title}} - {{page.title}}{% else %}{{ site.title }}{% endif %}"/>
<meta itemprop="description"      content="{% if page.description %}{{ page.description }}{% else %}{{ site.description }}{% endif %}"/>
<meta itemprop="image"            content="{% if page.image %}{{ page.image }}{% else %}{{ site.image }}{% endif %}"/>

<!-- Open Graph data -->
<meta property="og:title"               content="{% if page.title %}{{site.title}} - {{page.title}}{% else %}{{ site.title }}{% endif %}" />
<meta property="og:description"         content="{% if page.description %}{{ page.description }}{% else %}{{ site.description }}{% endif %}"/>
<meta property="og:type"                content="article"/>
<meta property="og:url"                 content="{{ page.url | replace:'index.html','' | prepend: site.baseurl | prepend: site.url }}"/>
<meta property="og:image"               content="{% if page.image %}{{ page.image }}{% else %}{{ site.image }}{% endif %}" />
<meta property="og:site_name"           content="{% if page.title %}{{site.title}} - {{page.title}}{% else %}{{ site.title }}{% endif %}"/>
<meta property="article:published_time" content="{% if page.time %}{{ page.time }}{% else %}{{ site.time }}{% endif %}" />
<!-- <meta property="article:modified_time"  content="2013-09-16T19:08:47+01:00"    />
<meta property="article:section"        content="Article Section" />
<meta property="article:tag"            content="Article Tag"     /> -->

<!-- <meta property="fb:admins"              content="architecturebvn"  /> TODO: understand this --><!-- 1522938594658821 -->