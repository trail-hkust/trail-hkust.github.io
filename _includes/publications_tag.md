<h1 id="publications"></h1>

<h2 style="margin: 30px 0px -15px;">

  Publications

  <temp style="font-size:15px;">[</temp>
  <a
    href="https://scholar.google.com/citations?user=lxrXMY0AAAAJ&hl=en&oi=ao"
    target="_blank"
    style="
      font-size:15px;
      text-decoration:none;
    ">
    Google Scholar
  </a>
  <temp style="font-size:15px;">]</temp>

  <temp style="font-size:15px;">[</temp>
  <a
    href="https://www.researchgate.net/profile/Zixuan-Yuan-4"
    target="_blank"
    style="
      font-size:15px;
      text-decoration:none;
    ">
    ResearchGate
  </a>
  <temp style="font-size:15px;">]</temp>

  <span style="
    font-size:15px;
    margin-left:15px;
    font-weight:normal;
  ">

    <a
      href="javascript:void(0);"
      id="selected-btn"
      onclick="setPublicationMode('selected')"
      style="
        text-decoration:none;
      ">
      <strong>Selected</strong>
    </a>

    <span style="margin:0 8px;">|</span>

    <a
      href="javascript:void(0);"
      id="all-date-btn"
      onclick="setPublicationMode('all')"
      style="
        text-decoration:none;
      ">
      All by date
    </a>

  </span>

</h2>

<br>

<!-- ===================================================== -->

<!-- SELECTED / ALL BY DATE                                -->

<!-- ===================================================== -->

<div
  style="
    display:flex;
    align-items:center;
    flex-wrap:wrap;
    gap:0;
    margin-bottom:12px;
  ">

<a
 href="javascript:void(0);"
 id="selected-btn"
 onclick="setPublicationMode('selected')"
 style="
   margin-right:12px;
   text-decoration:none;
   cursor:pointer;
 "> <strong>Selected</strong> </a>

<a
 href="javascript:void(0);"
 id="all-date-btn"
 onclick="setPublicationMode('all')"
 style="
   text-decoration:none;
   cursor:pointer;
 ">
All by date </a>

</div>

<!-- ===================================================== -->

<!-- TOPIC FILTERS                                         -->

<!-- ===================================================== -->

<div
  style="
    display:flex;
    align-items:center;
    flex-wrap:wrap;
    margin-bottom:25px;
    line-height:1.8;
  ">

  <span style="margin-right:12px;">
    Topics:
  </span>

  <!-- ALL -->

<a
 href="javascript:void(0);"
 class="topic-filter"
 data-topic="all"
 onclick="showPublicationTopic('all')"
 style="
   margin-right:15px;
   text-decoration:none;
   cursor:pointer;
   border-bottom:2px solid transparent;
   padding-bottom:2px;
 ">
All </a>

  <!-- MULTI-AGENT -->

<a
 href="javascript:void(0);"
 class="topic-filter"
 data-topic="multi-agent"
 onclick="showPublicationTopic('multi-agent')"
 style="
   margin-right:15px;
   text-decoration:none;
   cursor:pointer;
   border-bottom:2px solid transparent;
   padding-bottom:2px;
 ">
Multi-Agent Learning & Reasoning </a>

  <!-- INTERPRETABILITY -->

<a
 href="javascript:void(0);"
 class="topic-filter"
 data-topic="interpretability"
 onclick="showPublicationTopic('interpretability')"
 style="
   margin-right:15px;
   text-decoration:none;
   cursor:pointer;
   border-bottom:2px solid transparent;
   padding-bottom:2px;
 ">
Model Interpretability, Representation & Evaluation </a>

  <!-- INVESTMENT -->

<a
 href="javascript:void(0);"
 class="topic-filter"
 data-topic="investment"
 onclick="showPublicationTopic('investment')"
 style="
   margin-right:15px;
   text-decoration:none;
   cursor:pointer;
   border-bottom:2px solid transparent;
   padding-bottom:2px;
 ">
AI for Investment </a>

  <!-- COMPLIANCE -->

<a
 href="javascript:void(0);"
 class="topic-filter"
 data-topic="compliance"
 onclick="showPublicationTopic('compliance')"
 style="
   text-decoration:none;
   cursor:pointer;
   border-bottom:2px solid transparent;
   padding-bottom:2px;
 ">
AI for Regulatory Compliance </a>

</div>

<!-- ===================================================== -->

<!-- PUBLICATIONS                                          -->

<!-- ===================================================== -->

{% for link in site.data.publications_tag.main %}

<!-- ===================================================== -->

<!-- DETERMINE TOPIC ID                                    -->

<!-- ===================================================== -->

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

<!-- PUBLICATION ITEM                                      -->

<!-- ===================================================== -->

<div
  class="publication-item"
  data-topic="{{ topic_id }}"
  data-selected="{{ link.selected }}"
  style="
    display:flex;
    width:100%;
    margin-bottom:30px;
    box-sizing:border-box;
  ">

  <!-- =================================================== -->

  <!-- LEFT: IMAGE 30%                                     -->

  <!-- =================================================== -->

  <div
    style="
      width:30%;
      flex:0 0 30%;
      padding-right:25px;
      box-sizing:border-box;
    ">


{% if link.image %}

  <a
    href="{{ link.image }}"
    target="_blank"
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


  </div>

  <!-- =================================================== -->

  <!-- RIGHT: INFORMATION 70%                              -->

  <!-- =================================================== -->

  <div
    style="
      width:70%;
      flex:0 0 70%;
      box-sizing:border-box;
      padding:0;
    ">


<!-- ================================================= -->
<!-- TITLE                                             -->
<!-- ================================================= -->

<div
  class="title"
  style="
    font-size:17px;
    font-weight:600;
    line-height:1.45;
    margin-bottom:8px;
  ">

  {% if link.pdf %}

    <a
      href="{{ link.pdf }}"
      target="_blank"
      style="
        text-decoration:none;
      ">
      {{ link.title }}
    </a>

  {% else %}

    {{ link.title }}

  {% endif %}

</div>


<!-- ================================================= -->
<!-- AUTHORS                                           -->
<!-- ================================================= -->

<div
  class="author"
  style="
    margin-bottom:6px;
    line-height:1.5;
  ">

  {{ link.authors }}

</div>


<!-- ================================================= -->
<!-- YEAR + TOPIC                                      -->
<!-- ================================================= -->

<div
  style="
    margin-bottom:6px;
    line-height:1.5;
  ">


  {% if link.year %}

    <em>
      {{ link.year }}
    </em>

  {% endif %}


  {% if topic_id != "" %}

    <span style="margin-left:10px;">

      <a
        href="javascript:void(0);"
        class="publication-topic"
        data-topic="{{ topic_id }}"
        onclick="showPublicationTopic('{{ topic_id }}')"
        style="
          text-decoration:none;
          cursor:pointer;
        ">
        {{ link.tag }}
      </a>

    </span>

  {% endif %}

</div>


<!-- ================================================= -->
<!-- CONFERENCE SHORT + LINKS                          -->
<!-- ================================================= -->

<div
  class="periodical"
  style="
    margin-bottom:10px;
    line-height:1.5;
  ">


  {% if link.conference_short %}

    <strong>
      {{ link.conference_short }}
    </strong>

  {% endif %}


  <!-- PDF -->

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
      PDF
    </a>

  {% endif %}


  <!-- WEBSITE -->

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
      Website
    </a>

  {% endif %}


  <!-- CODE -->

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
      Code
    </a>

  {% endif %}


  <!-- BIBTEX -->

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
      BibTeX
    </a>

  {% endif %}


  <!-- OTHERS -->

  {% if link.others %}

    <span style="margin-left:8px;">
      {{ link.others }}
    </span>

  {% endif %}

</div>


<!-- ================================================= -->
<!-- NOTES                                             -->
<!-- ================================================= -->


  </div>

</div>

{% endfor %}

<!-- ===================================================== -->

<!-- JAVASCRIPT                                            -->

<!-- ===================================================== -->

<script>

/* =========================================================
   TOPIC FILTER
   ========================================================= */

function showPublicationTopic(topic) {

  var items = document.querySelectorAll(".publication-item");

  var topicButtons = document.querySelectorAll(".topic-filter");


  /* -------------------------------------------------------
     Filter publications
     ------------------------------------------------------- */

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


  /* -------------------------------------------------------
     Update selected topic appearance
     ------------------------------------------------------- */

  topicButtons.forEach(function(button) {

    if (button.getAttribute("data-topic") === topic) {

      button.style.fontWeight = "600";

      button.style.borderBottom = "2px solid currentColor";

    } else {

      button.style.fontWeight = "400";

      button.style.borderBottom = "2px solid transparent";

    }

  });

}


/* =========================================================
   SELECTED / ALL BY DATE
   ========================================================= */

function setPublicationMode(mode) {

  var items = document.querySelectorAll(".publication-item");

  var selectedButton =
    document.getElementById("selected-btn");

  var allDateButton =
    document.getElementById("all-date-btn");


  /* -------------------------------------------------------
     SELECTED
     ------------------------------------------------------- */

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


  /* -------------------------------------------------------
     ALL BY DATE
     ------------------------------------------------------- */

  if (mode === "all") {

    items.forEach(function(item) {

      item.style.display = "flex";

    });


    selectedButton.style.fontWeight = "400";

    allDateButton.style.fontWeight = "600";

  }

}


/* =========================================================
   DEFAULT STATE
   ========================================================= */

document.addEventListener(
  "DOMContentLoaded",
  function() {

    /*
     * Default:
     * Selected publications
     * All topics
     */

    setPublicationMode("selected");

    showPublicationTopic("all");

  }
);

</script>
