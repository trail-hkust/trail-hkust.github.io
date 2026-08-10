<h1 id="publications"></h1>

<h2 style="margin: 30px 0px -15px;">
  Publications
  <temp style="font-size:15px;">[</temp>
  <a href="https://scholar.google.com/citations?user=lxrXMY0AAAAJ&hl=en&oi=ao"
     target="_blank"
     style="font-size:15px;">
    Google Scholar
  </a>
  <temp style="font-size:15px;">]</temp>

<temp style="font-size:15px;">[</temp> <a href="https://www.researchgate.net/profile/Zixuan-Yuan"
  target="_blank"
  style="font-size:15px;">
ResearchGate </a> <temp style="font-size:15px;">]</temp>

</h2>

<br>

<!-- ================================================= -->

<!-- SELECTED / ALL BY DATE -->

<!-- ================================================= -->

<div style="margin-bottom: 15px;">

<button
 id="selected-btn"
 class="publication-mode active"
 onclick="setPublicationMode('selected')"
 style="background:none;
        border:none;
        padding:5px 12px;
        margin-right:10px;
        font-size:14px;
        cursor:pointer;">
Selected </button>

<button
 id="all-date-btn"
 class="publication-mode"
 onclick="setPublicationMode('all')"
 style="background:none;
        border:none;
        padding:5px 12px;
        margin-right:10px;
        font-size:14px;
        cursor:pointer;">
All by date </button>

</div>

<!-- ================================================= -->

<!-- TOPICS -->

<!-- ================================================= -->

<div id="publication-topics"
     style="margin-bottom:25px;">

  <strong style="margin-right:10px;">
    Topics:
  </strong>

<a href="#topic-all"
  class="topic-link active"
  onclick="showTopic('all'); return false;"
  style="margin-right:15px;
         text-decoration:none;">
All </a>

<a href="#topic-multi-agent"
  class="topic-link"
  onclick="showTopic('multi-agent'); return false;"
  style="margin-right:15px;
         text-decoration:none;">
Multi-Agent Learning & Reasoning </a>

<a href="#topic-model"
  class="topic-link"
  onclick="showTopic('model'); return false;"
  style="margin-right:15px;
         text-decoration:none;">
Model Interpretability, Representation & Evaluation </a>

<a href="#topic-investment"
  class="topic-link"
  onclick="showTopic('investment'); return false;"
  style="margin-right:15px;
         text-decoration:none;">
AI for Investment </a>

<a href="#topic-compliance"
  class="topic-link"
  onclick="showTopic('compliance'); return false;"
  style="text-decoration:none;">
AI for Regulatory Compliance </a>

</div>

<!-- ================================================= -->

<!-- NOTES -->

<!-- ================================================= -->

<div style="margin-bottom:20px;">
  * means equal contribution.
  † means corresponding authors.
</div>

<!-- ================================================= -->

<!-- PUBLICATIONS -->

<!-- ================================================= -->

<div class="publications">

{% assign categories = "Multi-Agent Learning & Reasoning|Model Interpretability, Representation & Evaluation|AI-driven investment|AI for regulatory compliance" | split: "|" %}

{% for category in categories %}

{% assign category_papers = site.data.publications_tag.main | where: "tag", category %}

{% for link in category_papers %}

<!-- ================================================= -->

<!-- ONE PUBLICATION -->

<!-- ================================================= -->

<div
  class="publication-item"
  data-tag="{{ link.tag }}"
  data-mode="selected"
  style="display:flex;
         width:100%;
         align-items:flex-start;
         margin-bottom:35px;
         padding-bottom:25px;
         border-bottom:1px solid #eeeeee;
         box-sizing:border-box;">

  <!-- ================================================= -->

  <!-- IMAGE: 30% -->

  <!-- ================================================= -->

  <div
    style="width:30%;
           flex:0 0 30%;
           padding-right:25px;
           box-sizing:border-box;">

```
{% if link.image %}

<a
  href="{{ link.image }}"
  target="_blank"
  style="display:block;
         width:100%;
         height:180px;
         overflow:hidden;
         border:1px solid #eeeeee;
         border-radius:4px;
         background:#f5f5f5;
         box-sizing:border-box;">

  <img
    src="{{ link.image }}"
    alt="{{ link.title }}"
    style="display:block;
           width:100%;
           height:100%;
           object-fit:cover;
           object-position:center;">

</a>

{% endif %}
```

  </div>

  <!-- ================================================= -->

  <!-- INFORMATION: 70% -->

  <!-- ================================================= -->

  <div
    style="width:70%;
           flex:0 0 70%;
           box-sizing:border-box;">

```
<!-- TITLE -->

<div
  class="title"
  style="font-size:17px;
         font-weight:600;
         line-height:1.45;
         margin-bottom:8px;">

  {% if link.pdf %}

  <a
    href="{{ link.pdf }}"
    target="_blank">
    {{ link.title }}
  </a>

  {% else %}

  {{ link.title }}

  {% endif %}

</div>


<!-- AUTHORS -->

<div
  class="author"
  style="line-height:1.5;
         margin-bottom:6px;">

  {{ link.authors }}

</div>


<!-- CONFERENCE -->

<div
  class="periodical"
  style="line-height:1.5;
         margin-bottom:10px;">

  <em>
    {{ link.conference }}
  </em>

</div>


<!-- LINKS -->

<div
  class="links"
  style="margin-top:8px;">


  {% if link.pdf %}

  <a
    href="{{ link.pdf }}"
    target="_blank"
    style="display:inline-block;
           padding:3px 8px;
           margin-right:5px;
           border:1px solid #cccccc;
           border-radius:3px;
           font-size:12px;
           text-decoration:none;">
    PDF
  </a>

  {% endif %}


  {% if link.web %}

  <a
    href="{{ link.web }}"
    target="_blank"
    style="display:inline-block;
           padding:3px 8px;
           margin-right:5px;
           border:1px solid #cccccc;
           border-radius:3px;
           font-size:12px;
           text-decoration:none;">
    Website
  </a>

  {% endif %}


  {% if link.code %}

  <a
    href="{{ link.code }}"
    target="_blank"
    style="display:inline-block;
           padding:3px 8px;
           margin-right:5px;
           border:1px solid #cccccc;
           border-radius:3px;
           font-size:12px;
           text-decoration:none;">
    Code
  </a>

  {% endif %}


  {% if link.bibtex %}

  <a
    href="{{ link.bibtex }}"
    target="_blank"
    style="display:inline-block;
           padding:3px 8px;
           margin-right:5px;
           border:1px solid #cccccc;
           border-radius:3px;
           font-size:12px;
           text-decoration:none;">
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

{% endfor %}

</div>

<!-- ================================================= -->

<!-- CSS -->

<!-- ================================================= -->

<style>

.publication-mode.active {
  font-weight:600 !important;
  border-bottom:2px solid #000 !important;
}

.topic-link {
  color:#777;
}

.topic-link:hover {
  color:#000;
}

.topic-link.active {
  color:#000;
  font-weight:600;
}


/* ================================================= */
/* MOBILE */
/* ================================================= */

@media (max-width:768px) {

  .publication-item {
    display:block !important;
  }

  .publication-item > div:first-child {
    width:100% !important;
    padding-right:0 !important;
    margin-bottom:15px;
  }

  .publication-item > div:last-child {
    width:100% !important;
  }

}

</style>

<!-- ================================================= -->

<!-- JAVASCRIPT -->

<!-- ================================================= -->

<script>

function showTopic(topic) {

  var items =
    document.querySelectorAll(".publication-item");

  var links =
    document.querySelectorAll(".topic-link");


  /* Remove active state */

  links.forEach(function(link) {
    link.classList.remove("active");
  });


  /* Set active topic */

  if (topic === "all") {
    links[0].classList.add("active");
  }

  if (topic === "multi-agent") {
    links[1].classList.add("active");
  }

  if (topic === "model") {
    links[2].classList.add("active");
  }

  if (topic === "investment") {
    links[3].classList.add("active");
  }

  if (topic === "compliance") {
    links[4].classList.add("active");
  }


  /* Filter publications */

  items.forEach(function(item) {

    var tag =
      item.getAttribute("data-tag");


    if (topic === "all") {

      item.style.display = "flex";

    }

    else if (
      topic === "multi-agent" &&
      tag === "Multi-Agent Learning & Reasoning"
    ) {

      item.style.display = "flex";

    }

    else if (
      topic === "model" &&
      tag === "Model Interpretability, Representation & Evaluation"
    ) {

      item.style.display = "flex";

    }

    else if (
      topic === "investment" &&
      tag === "AI-driven investment"
    ) {

      item.style.display = "flex";

    }

    else if (
      topic === "compliance" &&
      tag === "AI for regulatory compliance"
    ) {

      item.style.display = "flex";

    }

    else {

      item.style.display = "none";

    }

  });

}


/* ================================================= */
/* SELECTED / ALL BY DATE */
/* ================================================= */

function setPublicationMode(mode) {

  var selectedBtn =
    document.getElementById("selected-btn");

  var allBtn =
    document.getElementById("all-date-btn");


  if (mode === "selected") {

    selectedBtn.classList.add("active");
    allBtn.classList.remove("active");

  }

  else {

    selectedBtn.classList.remove("active");
    allBtn.classList.add("active");

  }

}


/* ================================================= */
/* INITIAL */
/* ================================================= */

document.addEventListener(
  "DOMContentLoaded",
  function() {

    showTopic("all");

  }
);

</script>
