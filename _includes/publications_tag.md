<h1 id="publications"></h1>

<h2 style="margin: 30px 0px 5px;"> Publications

</h2>

<!-- ===================================================== -->

<!-- TOPIC FILTERS                                         -->

<!-- ===================================================== -->

<div
  style="
    display:flex;
    align-items:baseline;
    flex-wrap:wrap;
    margin-bottom:20px;
    padding-left:10px;
    line-height:1.8;
  ">

  <span style="margin-right:12px;">
    <strong>Topics:</strong>
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

</div>


<!-- ===================================================== -->
<!-- PUBLICATION SEARCH                                   -->
<!-- ===================================================== -->

<div
  style="
    display:flex;
    align-items:center;
    gap:12px;
    margin-left:20px;
    margin-bottom:25px;
  ">

  <input
    type="text"
    id="publication-search"
    placeholder="Search publications..."
    oninput="searchPublications()"
    style="
      width:300px;
      padding:7px 10px;
      font-size:14px;
      border:1px solid #cccccc;
      border-radius:4px;
      box-sizing:border-box;
    ">

  <select
    id="publication-year"
    onchange="searchPublications()"
    style="
      padding:7px 10px;
      font-size:14px;
      border:1px solid #cccccc;
      border-radius:4px;
      background:white;
      cursor:pointer;
    ">

    <option value="all">Year: All</option>
    <option value="2026">2026</option>
    <option value="2025">2025</option>
    <option value="2024">2024</option>
    <option value="2023">2023</option>
    <option value="2022">2022</option>
    <option value="2021">2021</option>
    <option value="2020">2020</option>

  </select>

</div>


<!-- ===================================================== -->
<!-- PUBLICATIONS                                          -->
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
<!-- ONE PUBLICATION ITEM                                  -->
<!-- ===================================================== -->

<div
  class="publication-item"
  data-title="{{ link.title | escape | downcase }}"
  data-year="{{ link.year }}"
  data-topic="{{ topic_id }}"
  style="
    display:flex;
    width:100%;
    margin-bottom:30px;
    box-sizing:border-box;
  ">


  <!-- =================================================== -->
  <!-- LEFT: IMAGE                                          -->
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
  <!-- RIGHT: INFORMATION                                   -->
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

        {{ link.year }}

      {% endif %}


      {% if topic_id != "" %}

        <span style="margin-left:6px; margin-right:6px;">
          ·
        </span>

        <a
          href="javascript:void(0);"
          class="publication-topic"
          data-topic="{{ topic_id }}"
          onclick="showPublicationTopic('{{ topic_id }}')"
          style="
            text-decoration:none;
            cursor:pointer;
            color:inherit;
          ">
          {{ link.tag }}
        </a>

      {% endif %}

    </div>


    <!-- ================================================= -->
    <!-- CONFERENCE + LINKS                                -->
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


      {% if link.others %}

        <span style="margin-left:8px;">
          {{ link.others }}
        </span>

      {% endif %}

    </div>

  </div>

</div>

{% endfor %}

<!-- ===================================================== -->

<!-- JAVASCRIPT                                            -->

<!-- ===================================================== -->

<script>

function showPublicationTopic(topic) {

  var items = document.querySelectorAll(".publication-item");
  var topicButtons = document.querySelectorAll(".topic-filter");


  /* =======================================================
     FILTER PUBLICATIONS
     ======================================================= */

  items.forEach(function(item) {

    if (topic === "all") {

      item.style.display = "flex";

    } else if (item.getAttribute("data-topic") === topic) {

      item.style.display = "flex";

    } else {

      item.style.display = "none";

    }

  });


  /* =======================================================
     UPDATE TOPIC APPEARANCE
     ======================================================= */

  topicButtons.forEach(function(button) {

    if (button.getAttribute("data-topic") === topic) {

      button.style.fontWeight = "600";
      button.style.borderBottom = "2px solid currentColor";
      button.style.paddingBottom = "2px";

    } else {

      button.style.fontWeight = "400";
      button.style.borderBottom = "2px solid transparent";
      button.style.paddingBottom = "2px";

    }

  });

}


/* =========================================================
   INITIAL STATE
   ========================================================= */

document.addEventListener("DOMContentLoaded", function() {

  var items = document.querySelectorAll(".publication-item");
  var topicButtons = document.querySelectorAll(".topic-filter");


  /* -----------------------------------------
     Hide ALL publications initially
     ----------------------------------------- */

  items.forEach(function(item) {

    item.style.display = "none";

  });


  /* -----------------------------------------
     No topic selected initially
     ----------------------------------------- */

  topicButtons.forEach(function(button) {

    button.style.fontWeight = "400";
    button.style.borderBottom = "2px solid transparent";
    button.style.paddingBottom = "2px";

  });

});

</script>
