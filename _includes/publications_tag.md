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

<!-- ===================================================== -->

<!-- Publication Mode -->

<!-- ===================================================== -->

<div style="margin-bottom: 12px;">

<button
 id="selected-btn"
 class="publication-mode active"
 onclick="setPublicationMode('selected')">
Selected </button>

<button
 id="all-date-btn"
 class="publication-mode"
 onclick="setPublicationMode('all')">
All by date </button>

</div>

<!-- ===================================================== -->

<!-- Topics -->

<!-- ===================================================== -->

<div id="publication-topics"
     style="margin-bottom: 25px;">

<strong style="margin-right: 8px;">Topics:</strong>

<a href="#topic-all"
  class="topic-link active"
  onclick="showTopic('all'); return false;">
All </a>

<a href="#topic-multi-agent"
  class="topic-link"
  onclick="showTopic('multi-agent'); return false;">
Multi-Agent Learning & Reasoning </a>

<a href="#topic-model"
  class="topic-link"
  onclick="showTopic('model'); return false;">
Model Interpretability, Representation & Evaluation </a>

<a href="#topic-investment"
  class="topic-link"
  onclick="showTopic('investment'); return false;">
AI for Investment </a>

<a href="#topic-compliance"
  class="topic-link"
  onclick="showTopic('compliance'); return false;">
AI for Regulatory Compliance </a>

</div>

<!-- ===================================================== -->

<!-- Notes -->

<!-- ===================================================== -->

<div style="margin-bottom: 20px;">
  * means equal contribution.
  † means corresponding authors.
</div>

<!-- ===================================================== -->

<!-- Publication List -->

<!-- ===================================================== -->

<div class="publications">

{% assign categories =
"Multi-Agent Learning & Reasoning|
Model Interpretability, Representation & Evaluation|
AI-driven investment|
AI for regulatory compliance"
| split: "|" %}

{% for category in categories %}

{% assign category_papers =
site.data.publications_tag.main
| where: "tag", category %}

{% for link in category_papers %}

  <div
    class="publication-item"
    data-tag="{{ link.tag }}"
    data-mode="selected"
    style="display: flex;
           width: 100%;
           margin-bottom: 35px;
           padding-bottom: 25px;
           border-bottom: 1px solid #eeeeee;
           align-items: flex-start;">

```
<!-- ================================================= -->
<!-- LEFT: IMAGE 30% -->
<!-- ================================================= -->

<div
  style="width: 30%;
         flex: 0 0 30%;
         padding-right: 25px;
         box-sizing: border-box;">

  {% if link.image %}

  <a href="{{ link.image }}"
     target="_blank"
     style="display: block;
            width: 100%;
            height: 180px;
            overflow: hidden;
            border-radius: 4px;
            background: #f5f5f5;
            border: 1px solid #eeeeee;
            text-decoration: none;">

    <img
      src="{{ link.image }}"
      alt="{{ link.title }}"
      style="display: block;
             width: 100%;
             height: 100%;
             object-fit: cover;
             object-position: center;">

  </a>

  {% endif %}

</div>


<!-- ================================================= -->
<!-- RIGHT: INFORMATION 70% -->
<!-- ================================================= -->

<div
  style="width: 70%;
         flex: 0 0 70%;
         padding-left: 0;
         box-sizing: border-box;">


  <!-- Title -->

  <div
    class="title"
    style="font-size: 17px;
           font-weight: 600;
           line-height: 1.45;
           margin-bottom: 8px;">

    {% if link.pdf %}

      <a href="{{ link.pdf }}"
         target="_blank">
        {{ link.title }}
      </a>

    {% else %}

      {{ link.title }}

    {% endif %}

  </div>


  <!-- Authors -->

  <div
    class="author"
    style="margin-bottom: 6px;
           line-height: 1.5;">

    {{ link.authors }}

  </div>


  <!-- Conference -->

  <div
    class="periodical"
    style="margin-bottom: 10px;
           line-height: 1.5;">

    <em>{{ link.conference }}</em>

  </div>


  <!-- ================================================= -->
  <!-- Links -->
  <!-- ================================================= -->

  <div class="links"
       style="margin-top: 8px;">


    {% if link.pdf %}

    <a href="{{ link.pdf }}"
       target="_blank"
       style="display: inline-block;
              padding: 3px 8px;
              margin-right: 5px;
              border: 1px solid #cccccc;
              border-radius: 3px;
              font-size: 12px;
              text-decoration: none;">
      PDF
    </a>

    {% endif %}


    {% if link.web %}

    <a href="{{ link.web }}"
       target="_blank"
       style="display: inline-block;
              padding: 3px 8px;
              margin-right: 5px;
              border: 1px solid #cccccc;
              border-radius: 3px;
              font-size: 12px;
              text-decoration: none;">
      Website
    </a>

    {% endif %}


    {% if link.code %}

    <a href="{{ link.code }}"
       target="_blank"
       style="display: inline-block;
              padding: 3px 8px;
              margin-right: 5px;
              border: 1px solid #cccccc;
              border-radius: 3px;
              font-size: 12px;
              text-decoration: none;">
      Code
    </a>

    {% endif %}


    {% if link.bibtex %}

    <a href="{{ link.bibtex }}"
       target="_blank"
       style="display: inline-block;
              padding: 3px 8px;
              margin-right: 5px;
              border: 1px solid #cccccc;
              border-radius: 3px;
              font-size: 12px;
              text-decoration: none;">
      BibTeX
    </a>

    {% endif %}


    {% if link.notes %}

    <strong style="margin-left: 5px;">
      <i style="color:#e74d3c;">
        {{ link.notes }}
      </i>
    </strong>

    {% endif %}


    {% if link.others %}

      {{ link.others }}

    {% endif %}

  </div>

</div>
```

  </div>

{% endfor %}

{% endfor %}

</div>

<!-- ===================================================== -->

<!-- CSS -->

<!-- ===================================================== -->

<style>

.publication-mode {
  background: none;
  border: none;
  padding: 5px 12px;
  margin-right: 10px;
  font-size: 14px;
  cursor: pointer;
  color: #777;
}

.publication-mode.active {
  color: #000;
  font-weight: 600;
  border-bottom: 2px solid #000;
}


.topic-link {
  margin-right: 14px;
  text-decoration: none;
  color: #777;
  font-size: 14px;
}

.topic-link:hover {
  color: #000;
}

.topic-link.active {
  color: #000;
  font-weight: 600;
}


/* ========================================= */
/* Mobile */
/* ========================================= */

@media (max-width: 768px) {

  .publication-item {
    display: block !important;
  }

  .publication-item > div:first-child {
    width: 100% !important;
    padding-right: 0 !important;
    margin-bottom: 15px;
  }

  .publication-item > div:last-child {
    width: 100% !important;
  }

  .publication-item img {
    height: auto !important;
    max-height: 250px;
    object-fit: contain !important;
  }

}

</style>

<!-- ===================================================== -->

<!-- JavaScript -->

<!-- ===================================================== -->

<script>

function showTopic(topic) {

  var items = document.querySelectorAll(".publication-item");

  var links = document.querySelectorAll(".topic-link");

  /*
   * Reset topic link appearance
   */

  links.forEach(function(link) {
    link.classList.remove("active");
  });


  /*
   * Activate selected topic
   */

  if (topic === "all") {

    links[0].classList.add("active");

  }

  else if (topic === "multi-agent") {

    links[1].classList.add("active");

  }

  else if (topic === "model") {

    links[2].classList.add("active");

  }

  else if (topic === "investment") {

    links[3].classList.add("active");

  }

  else if (topic === "compliance") {

    links[4].classList.add("active");

  }


  /*
   * Show / hide publications
   */

  items.forEach(function(item) {

    var tag = item.getAttribute("data-tag");

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
      tag === "Model Interpretation, Representation & Evaluation"
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


/* ========================================= */
/* Selected / All by date */
/* ========================================= */

function setPublicationMode(mode) {

  var selectedButton =
    document.getElementById("selected-btn");

  var allButton =
    document.getElementById("all-date-btn");

  if (mode === "selected") {

    selectedButton.classList.add("active");
    allButton.classList.remove("active");

    document
      .querySelectorAll(".publication-item")
      .forEach(function(item) {

        item.setAttribute("data-mode", "selected");

        item.style.display = "flex";

      });

    /*
     * Re-apply current topic
     */

    var activeTopic =
      document.querySelector(".topic-link.active");

    if (activeTopic) {

      if (activeTopic.textContent.trim() === "All") {
        showTopic("all");
      }

      else if (
        activeTopic.textContent.indexOf("Multi-Agent") !== -1
      ) {
        showTopic("multi-agent");
      }

      else if (
        activeTopic.textContent.indexOf("Model Interpretation") !== -1
      ) {
        showTopic("model");
      }

      else if (
        activeTopic.textContent.indexOf("AI-driven") !== -1
      ) {
        showTopic("investment");
      }

      else if (
        activeTopic.textContent.indexOf("Regulatory") !== -1
      ) {
        showTopic("compliance");
      }

    }

  }

  else {

    selectedButton.classList.remove("active");
    allButton.classList.add("active");

    /*
     * Show every publication.
     *
     * Because publications_tag.yml contains
     * all publications, All by date simply
     * displays them in YAML order.
     */

    document
      .querySelectorAll(".publication-item")
      .forEach(function(item) {

        item.setAttribute("data-mode", "all");

        item.style.display = "flex";

      });

    /*
     * Keep current topic filter
     */

    var activeTopic =
      document.querySelector(".topic-link.active");

    if (activeTopic) {

      if (activeTopic.textContent.trim() === "All") {
        showTopic("all");
      }

      else if (
        activeTopic.textContent.indexOf("Multi-Agent") !== -1
      ) {
        showTopic("multi-agent");
      }

      else if (
        activeTopic.textContent.indexOf("Model Interpretation") !== -1
      ) {
        showTopic("model");
      }

      else if (
        activeTopic.textContent.indexOf("AI-driven") !== -1
      ) {
        showTopic("investment");
      }

      else if (
        activeTopic.textContent.indexOf("Regulatory") !== -1
      ) {
        showTopic("compliance");
      }

    }

  }

}


/* ========================================= */
/* Initial state */
/* ========================================= */

document.addEventListener("DOMContentLoaded", function() {

  showTopic("all");

});

</script>
