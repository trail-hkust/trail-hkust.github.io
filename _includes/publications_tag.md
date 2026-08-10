<h1 id="publications"></h1>

<h2 style="margin: 30px 0px -5px;">
  Publications
  <span style="font-size:15px;">[</span>
  <a href="https://scholar.google.com/citations?user=lxrXMY0AAAAJ&hl=en&oi=ao"
     target="_blank"
     style="font-size:15px;">
    Google Scholar
  </a>
  <span style="font-size:15px;">]</span>

<span style="font-size:15px;">[</span> <a href="https://www.researchgate.net/profile/Zixuan-Yuan"
  target="_blank"
  style="font-size:15px;">
ResearchGate </a> <span style="font-size:15px;">]</span>

</h2>

<br>

<!-- ===================================================== -->

<!-- SELECTED / ALL BY DATE -->

<!-- ===================================================== -->

<div style="margin-bottom: 8px; font-size: 14px;">

<a href="javascript:void(0);"
  id="selected-btn"
  onclick="setPublicationMode('selected')"
  style="margin-right: 18px;
         text-decoration: none;
         font-weight: 600;">
Selected </a>

<a href="javascript:void(0);"
  id="all-date-btn"
  onclick="setPublicationMode('all')"
  style="text-decoration: none;
         font-weight: 400;">
All by date </a>

</div>

<!-- ===================================================== -->

<!-- TOPICS -->

<!-- ===================================================== -->

<div style="margin-bottom: 25px; font-size: 14px; line-height: 2;">

  <strong style="margin-right: 8px;">
    Topics:
  </strong>

<a href="javascript:void(0);"
  onclick="showPublicationTopic('all')"
  style="margin-right: 15px;
         text-decoration: none;">
All </a>

<a href="javascript:void(0);"
  onclick="showPublicationTopic('multi-agent')"
  style="margin-right: 15px;
         text-decoration: none;">
Multi-Agent Learning & Reasoning </a>

<a href="javascript:void(0);"
  onclick="showPublicationTopic('interpretability')"
  style="margin-right: 15px;
         text-decoration: none;">
Model Interpretability, Representation & Evaluation </a>

<a href="javascript:void(0);"
  onclick="showPublicationTopic('investment')"
  style="margin-right: 15px;
         text-decoration: none;">
AI for Investment </a>

<a href="javascript:void(0);"
  onclick="showPublicationTopic('compliance')"
  style="text-decoration: none;">
AI for Regulatory Compliance </a>

</div>

<!-- ===================================================== -->

<!-- PUBLICATIONS -->

<!-- ===================================================== -->

{% for link in site.data.publications_tag.main %}

{% assign topic_id = "" %}

{% if link.tag == "Multi-Agent Learning & Reasoning" %}
{% assign topic_id = "multi-agent" %}
{% elsif link.tag == "Model Interpretation, Representation & Evaluation" %}
{% assign topic_id = "interpretability" %}
{% elsif link.tag == "AI-driven Investment" %}
{% assign topic_id = "investment" %}
{% elsif link.tag == "AI for Regulatory Compliance" %}
{% assign topic_id = "compliance" %}
{% endif %}

<div class="publication-item"
     data-topic="{{ topic_id }}"
     data-selected="{{ link.selected }}"
     style="
       display:flex;
       width:100%;
       margin-bottom:35px;
       align-items:flex-start;
       box-sizing:border-box;
     ">

  <!-- ================================================= -->

  <!-- LEFT: IMAGE 30% -->

  <!-- ================================================= -->

  <div style="
       width:30%;
       flex:0 0 30%;
       padding-right:25px;
       box-sizing:border-box;
       ">

```
{% if link.image %}

  <a href="{{ link.image }}"
     target="_blank"
     title="View full-size image"
     style="
       display:flex;
       width:100%;
       height:180px;
       align-items:center;
       justify-content:center;
       overflow:hidden;
       background:#f7f7f7;
       border:1px solid #e5e5e5;
       border-radius:4px;
       text-decoration:none;
       box-sizing:border-box;
     ">

    <img
      src="{{ link.image }}"
      alt="{{ link.title }}"
      style="
        display:block;
        max-width:100%;
        max-height:100%;
        width:auto;
        height:auto;
        object-fit:contain;
      ">

  </a>

{% endif %}
```

  </div>

  <!-- ================================================= -->

  <!-- RIGHT: INFORMATION 70% -->

  <!-- ================================================= -->

  <div style="
       width:70%;
       flex:0 0 70%;
       box-sizing:border-box;
       padding:0;
       ">

```
<!-- TITLE -->

<div class="title"
     style="
       font-size:17px;
       font-weight:600;
       line-height:1.45;
       margin-bottom:8px;
     ">

  {% if link.pdf %}

    <a href="{{ link.pdf }}"
       target="_blank"
       style="text-decoration:none;">
      {{ link.title }}
    </a>

  {% else %}

    {{ link.title }}

  {% endif %}

</div>


<!-- AUTHORS -->

<div class="author"
     style="
       margin-bottom:6px;
       line-height:1.5;
     ">

  {{ link.authors }}

</div>


<!-- CONFERENCE -->

<div class="periodical"
     style="
       margin-bottom:10px;
       line-height:1.5;
     ">

  <em>{{ link.conference }}</em>

</div>


<!-- LINKS -->

<div class="links"
     style="
       margin-top:8px;
       line-height:1.8;
     ">


  {% if link.pdf %}

    <a href="{{ link.pdf }}"
       target="_blank"
       style="
         display:inline-block;
         padding:3px 8px;
         margin-right:5px;
         border:1px solid #cccccc;
         border-radius:3px;
         font-size:12px;
         text-decoration:none;
       ">
      PDF
    </a>

  {% endif %}


  {% if link.web %}

    <a href="{{ link.web }}"
       target="_blank"
       style="
         display:inline-block;
         padding:3px 8px;
         margin-right:5px;
         border:1px solid #cccccc;
         border-radius:3px;
         font-size:12px;
         text-decoration:none;
       ">
      Website
    </a>

  {% endif %}


  {% if link.code %}

    <a href="{{ link.code }}"
       target="_blank"
       style="
         display:inline-block;
         padding:3px 8px;
         margin-right:5px;
         border:1px solid #cccccc;
         border-radius:3px;
         font-size:12px;
         text-decoration:none;
       ">
      Code
    </a>

  {% endif %}


  {% if link.bibtex %}

    <a href="{{ link.bibtex }}"
       target="_blank"
       style="
         display:inline-block;
         padding:3px 8px;
         margin-right:5px;
         border:1px solid #cccccc;
         border-radius:3px;
         font-size:12px;
         text-decoration:none;
       ">
      BibTeX
    </a>

  {% endif %}


  {% if link.notes %}

    <strong style="margin-left:5px;">
      <i style="color:#e74d3c;">
        {{ link.notes }}
      </i>
    </strong>

  {% endif %}


  {% if link.others %}

    {{ link.others }}

  {% endif %}


</div>
```

  </div>

</div>

{% endfor %}

<!-- ===================================================== -->

<!-- JAVASCRIPT -->

<!-- ===================================================== -->

<script>

function showPublicationTopic(topic) {

  var items = document.querySelectorAll(".publication-item");

  items.forEach(function(item) {

    if (topic === "all") {

      item.style.display = "flex";

    } else {

      if (item.getAttribute("data-topic") === topic) {
        item.style.display = "flex";
      } else {
        item.style.display = "none";
      }

    }

  });

}


function setPublicationMode(mode) {

  var items = document.querySelectorAll(".publication-item");

  var selectedButton =
    document.getElementById("selected-btn");

  var allDateButton =
    document.getElementById("all-date-btn");


  if (mode === "selected") {

    items.forEach(function(item) {

      if (item.getAttribute("data-selected") === "true") {

        item.style.display = "flex";

      } else {

        item.style.display = "none";

      }

    });

    selectedButton.style.fontWeight = "600";
    allDateButton.style.fontWeight = "400";

  }


  if (mode === "all") {

    items.forEach(function(item) {

      item.style.display = "flex";

    });

    selectedButton.style.fontWeight = "400";
    allDateButton.style.fontWeight = "600";

  }

}


/* Default: Selected */

setPublicationMode("selected");

</script>
