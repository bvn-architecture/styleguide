

<!-- Twitter card markup -->
{% if site.twitter_username %}
<meta name="twitter:card"        content="summary" />
<meta name="twitter:site"        content="{{site.twitter_username}}" />
<meta name="twitter:title"       content="{{site.title}} - {{page.title}}" />
<meta name="twitter:description" content="{{page.description}}" />
<meta name="twitter:image"       content="{% if page.image %}{{ page.image }}{% else %}{{ site.image }}{% endif %}" />
<meta name="twitter:creator" content="{{site.twitter_username}}">
{% endif %}

<!-- Schema.org markup for Google+ -->
<meta itemprop="name"             content="{{site.title}}">
<meta itemprop="description"      content="{{page.description}}">
<meta itemprop="image"            content="http://bvn-architecture.github.io/styleguide/assets/bvn-logo-meta.jpeg">

<!-- Open Graph data -->
<meta property="og:title"               content="{{site.title}}"/>
<meta property="og:description"         content="{{page.description}}"/>
<meta property="og:type"                content="article"/>
<meta property="og:url"                 content="{{ page.url | replace:'index.html','' | prepend: site.baseurl | prepend: site.url }}"/>
<meta property="og:image"               content="{% if page.image %}{{ page.image }}{% else %}{{ site.image }}{% endif %}" />
<meta property="og:site_name"           content="{{site.title}}" />
<meta property="article:published_time" content="{{page.date}}"    />
<!-- <meta property="article:modified_time"  content="2013-09-16T19:08:47+01:00"    />
<meta property="article:section"        content="Article Section" />
<meta property="article:tag"            content="Article Tag"     /> -->

<!-- <meta property="fb:admins"              content="architecturebvn"  /> TODO: understand this --><!-- 1522938594658821 -->