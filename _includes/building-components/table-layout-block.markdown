<dt class="building-components-dt-block">

{% if 2 >= 5 %}

<span class="transform-to-uppercase" markdown="1">{{ include.title }}</span>

{% endif %}

<span class="transform-to-uppercase" markdown="1">**Describe** Finishes</span>

<div markdown="1">

<dl>
<dt id="building-components-dt-content">
<div markdown="1">
{{ include.letter }}
</div>
</dt>
<dd id="building-components-dd-content">
<div markdown="1">
{% include {{ include.key }} %}
</div>
</dd>

<dt id="building-components-dt-content">
<div markdown="1">
-
</div>
</dt>
<dd id="building-components-dd-content">
<div markdown="1">
{% include {{ include.value }} %}
</div>
</dd>
</dl>

</div>
</dt>
<dd class=".building-components-dd-block">

</dd>