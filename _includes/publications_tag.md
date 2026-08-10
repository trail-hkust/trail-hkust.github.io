<h1 id="publications"></h1>

<h2 style="margin: 30px 0px 10px;">
  Publications

  <temp style="font-size:15px; margin-left:15px;">[</temp>
  <a href="https://scholar.google.com/citations?user=lxrXMY0AAAAJ&hl=en&oi=ao"
     target="_blank"
     style="font-size:15px;">
    Google Scholar
  </a>
  <temp style="font-size:15px;">]</temp>

  <temp style="font-size:15px;">[</temp>
  <a href="https://www.researchgate.net/profile/Zixuan-Yuan"
     target="_blank"
     style="font-size:15px;">
    ResearchGate
  </a>
  <temp style="font-size:15px;">]</temp>

  <!-- Selected / All by date -->
  <span style="font-size:15px; margin-left:25px; font-weight:normal;">

    <a href="javascript:void(0);"
       id="selected-btn"
       onclick="setPublicationMode('selected')"
       style="margin-right:12px; text-decoration:none;">
      <strong>Selected</strong>
    </a>

    <a href="javascript:void(0);"
       id="all-date-btn"
       onclick="setPublicationMode('all')"
       style="text-decoration:none;">
      All by date
    </a>

  </span>

</h2>

<br>


<!-- ===================================================== -->

<!-- TOPICS -->

<!-- ===================================================== -->

<div style="
     margin-bottom:25px;
     font-size:14px;
     line-height:2;
     ">

  <strong style="margin-right:8px;">
    Topics:
  </strong>

<a href="javascript:void(0);"
  onclick="showPublicationTopic('all')"
  style="
    margin-right:15px;
    text-decoration:none;
  ">
All </a>

<a href="javascript:void(0);"
  onclick="showPublicationTopic('multi-agent')"
  style="
    margin-right:15px;
    text-decoration:none;
  ">
Multi-Agent Learning & Reasoning </a>

<a href="javascript:void(0);"
  onclick="showPublicationTopic('interpretability')"
  style="
    margin-right:15px;
    text-decoration:none;
  ">
Model Interpretability, Representation & Evaluation </a>

<a href="javascript:void(0);"
  onclick="showPublicationTopic('investment')"
  style="
    margin-right:15px;
    text-decoration:none;
  ">
AI for Investment </a>

<a href="javascript:void(0);"
  onclick="showPublicationTopic('compliance')"
  style="text-decoration:none;">
AI for Regulatory Compliance </a>

</div>

<!-- ===================================================== -->

<!-- PUBLICATIONS -->

<!-- ===================================================== -->

{% for link in site.data.publications_tag.main %}

{% assign topic_id = "" %}

{% if link.tag == "Multi-Agent Learning & Reasoning" %}
{% assign topic_id = "multi-agent" %}
{% elsif link.tag == "Model Interpretability, Representation & Evaluation" %}
{% assign topic_id = "interpretability" %}
{% elsif link.tag == "AI-driven Investment" %}
{% assign topic_id = "investment" %}
{% elsif link.tag == "AI for Regulatory Compliance" %}
{% assign topic_id = "compliance" %}
{% endif %}

<!-- ===================================================== -->

<!-- ONE PUBLICATION -->

<!-- ===================================================== -->

<div class="publication-item"
     data-topic="{{ topic_id }}"
     data-selected="{{ link.selected }}"
     style="
       display:flex;
       width:100%;
       align-items:flex-start;
       margin-bottom:35px;
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
       box-sizing:border-box;
       text-decoration:none;
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


  </div>

  <!-- ================================================= -->

  <!-- RIGHT: INFORMATION 70% -->

  <!-- ================================================= -->

  <div style="
       width:70%;
       flex:0 0 70%;
       box-sizing:border-box;
       ">


<!-- ================================================= -->
<!-- TITLE -->
<!-- ================================================= -->

<div class="title"
     style="
       font-size:17px;
       font-weight:600;
       line-height:1.45;
       margin-bottom:7px;
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


<!-- ================================================= -->
<!-- AUTHORS -->
<!-- ================================================= -->

<div class="author"
     style="
       margin-bottom:5px;
       line-height:1.5;
     ">

  {{ link.authors }}

</div>


<!-- ================================================= -->
<!-- YEAR + TOPIC -->
<!-- ================================================= -->

<div style="
     margin-bottom:7px;
     line-height:1.5;
     font-size:14px;
     ">
  
  {% if link.year %}
  
  <em>{{ link.year }}</em>
  
  {% endif %}
  
  {% if topic_id != "" %}
  
    <span style="margin-left:10px;">
  
  ```
  <a href="javascript:void(0);"
     onclick="showPublicationTopic('{{ topic_id }}')"
     style="
       text-decoration:none;
     ">
    {{ link.tag }}
  </a>
  ```
  
    </span>
  
  {% endif %}
  

</div>


<!-- ================================================= -->
<!-- CONFERENCE SHORT + LINKS -->
<!-- ================================================= -->

<div style="
     line-height:1.8;
     font-size:13px;
     ">

  {% if link.conference_short %}
  
    <strong>
      {{ link.conference_short }}
    </strong>
  
  {% endif %}
  
  {% if link.pdf %}
  
    <span style="margin-left:8px;">
      /
    </span>
  
  <a
   href="{{ link.pdf }}"
   target="_blank"
   style="
     margin-left:5px;
     text-decoration:none;
   ">
  PDF </a>
  
  {% endif %}
  
  {% if link.web %}
  
    <span style="margin-left:5px;">
      /
    </span>
  
  <a
   href="{{ link.web }}"
   target="_blank"
   style="
     margin-left:5px;
     text-decoration:none;
   ">
  Website </a>
  
  {% endif %}
  
  {% if link.code %}
  
    <span style="margin-left:5px;">
      /
    </span>
  
  <a
   href="{{ link.code }}"
   target="_blank"
   style="
     margin-left:5px;
     text-decoration:none;
   ">
  Code </a>
  
  {% endif %}
  
  {% if link.bibtex %}
  
    <span style="margin-left:5px;">
      /
    </span>
  
  <a
   href="{{ link.bibtex }}"
   target="_blank"
   style="
     margin-left:5px;
     text-decoration:none;
   ">
  BibTeX </a>
  
  {% endif %}
  
  {% if link.others %}
  
  {{ link.others }}
  
  {% endif %}
  
  {% endfor %}


<!-- ===================================================== -->

<!-- JAVASCRIPT -->

<!-- ===================================================== -->

<script>

function showPublicationTopic(topic) {

  var items =
    document.querySelectorAll(".publication-item");

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

  var items =
    document.querySelectorAll(".publication-item");

  var selectedButton =
    document.getElementById("selected-btn");

  var allDateButton =
    document.getElementById("all-date-btn");


  if (mode === "selected") {

    items.forEach(function(item) {

      if (
        item.getAttribute("data-selected") === "true"
      ) {

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


/* ===================================================== */
/* DEFAULT MODE */
/* ===================================================== */

setPublicationMode("selected");

</script>
