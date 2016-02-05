<dt class="building-components-dt-block">


<dl>

<dt id="building-components-dt-content">
</dt>
<dd id="building-components-dd-content">
<div markdown="1">
<span class="transform-to-uppercase">{{ include.title }}</span>
</div>
</dd>

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
{% include {{ include.theimage }} %}
</dd>