```html
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

  <temp style="font-size:15px;">[</temp>
  <a href="https://www.researchgate.net/profile/Zixuan-Yuan"
     target="_blank"
     style="font-size:15px;">
    ResearchGate
  </a>
  <temp style="font-size:15px;">]</temp>
</h2>

<br>


<!-- ========================= -->
<!-- Publication Mode -->
<!-- ========================= -->

<div style="margin-bottom: 8px;">

  <button
    id="selected-btn"
    class="publication-mode active"
    onclick="setPublicationMode('selected')">
    Selected
  </button>

  <button
    id="all-date-btn"
    class="publication-mode"
    onclick="setPublicationMode('all')">
    All by date
  </button>

</div>


<!-- ========================= -->
<!-- Topics -->
<!-- ========================= -->

<div id="topics-container"
     style="margin-bottom: 25px;">

  <strong style="font-size: 15px;">
    Topics:
  </strong>

  <button
    class="topic-btn active"
    data-topic="All"
    onclick="filterTopic('All')">
    All
  </button>

  <button
    class="topic-btn"
    data-topic="Multi-Agent Learning & Reasoning"
    onclick="filterTopic('Multi-Agent Learning & Reasoning')">
    Multi-Agent Learning & Reasoning
  </button>

  <button
    class="topic-btn"
    data-topic="Model Interpretability, Representation & Evaluation"
    onclick="filterTopic('Model Interpretability, Representation & Evaluation')">
    Model Interpretability, Representation & Evaluation
  </button>

  <button
    class="topic-btn"
    data-topic="AI for Investment"
    onclick="filterTopic('AI for Investment')">
    AI for Investment
  </button>

  <button
    class="topic-btn"
    data-topic="AI for Regulatory Compliance"
    onclick="filterTopic('AI for Regulatory Compliance')">
    AI for Regulatory Compliance
  </button>

</div>


<!-- ========================= -->
<!-- CSS -->
<!-- ========================= -->

<style>

.publication-mode {
  background: none;
  border: none;
  padding: 0;
  margin-right: 20px;

  font-size: 15px;
  cursor: pointer;

  color: #777;
}

.publication-mode:hover {
  color: #000;
}

.publication-mode.active {
  color: #000;
  font-weight: 600;
}


.topic-btn {
  background: none;
  border: none;

  padding: 0;
  margin-left: 12px;
  margin-bottom: 6px;

  font-size: 14px;

  color: #777;

  cursor: pointer;
}

.topic-btn:hover {
  color: #000;
}

.topic-btn.active {
  color: #000;
  font-weight: 600;
}


/* ========================= */
/* Publication */
/* ========================= */

.publication-item {
  margin-bottom: 40px;
}


/* Image */

.publication-image {
  width: 100%;

  display: flex;
  justify-content: center;
  align-items: center;

  margin-bottom: 15px;
}

.publication-image img {
  display: block;

  max-width: 100%;
  width: auto;
  height: auto;

  object-fit: contain;
}


/* Information */

.publication-info {
  text-align: center;

  padding: 10px 15px;
}


/* Title */

.publication-title {
  font-size: 18px;
  font-weight: 600;

  margin-bottom: 8px;
}


/* Authors */

.publication-authors {
  margin-bottom: 6px;
}


/* Conference */

.publication-conference {
  margin-bottom: 10px;
}


/* Links */

.publication-links a {
  display: inline-block;

  padding: 3px 8px;

  margin: 2px;

  border: 1px solid #aaa;
  border-radius: 3px;

  font-size: 12px;

  text-decoration: none;
}

.publication-links a:hover {
  background-color: #f5f5f5;
}

</style>


<!-- ========================= -->
<!-- Publications -->
<!-- ========================= -->

<div id="publications-list">

{% for link in site.data.publications_tag.main %}

<div
  class="publication-item"
  data-tag="{{ link.tag }}"
  data-selected="{% if link.selected == true %}true{% else %}false{% endif %}"
>


  <!-- Image -->

  {% if link.image %}

  <div class="publication-image">

    <img
      src="{{ link.image }}"
      class="img-fluid z-depth-1"
      alt="{{ link.title }}"
    >

  </div>

  {% endif %}


  <!-- Information -->

  <div class="publication-info">


    <!-- Title -->

    <div class="publication-title">

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


    <!-- Authors -->

    <div class="publication-authors">
      {{ link.authors }}
    </div>


    <!-- Conference -->

    <div class="publication-conference">

      <em>
        {{ link.conference }}
      </em>

    </div>


    <!-- Links -->

    <div class="publication-links">


      {% if link.pdf %}

      <a
        href="{{ link.pdf }}"
        target="_blank">
        PDF
      </a>

      {% endif %}


      {% if link.web %}

      <a
        href="{{ link.web }}"
        target="_blank">
        Website
      </a>

      {% endif %}


      {% if link.bibtex %}

      <a
        href="{{ link.bibtex }}"
        target="_blank">
        BibTeX
      </a>

      {% endif %}


      {% if link.code %}

      <a
        href="{{ link.code }}"
        target="_blank">
        Code
      </a>

      {% endif %}


      {% if link.page %}

      <a
        href="{{ link.page }}"
        target="_blank">
        Project Page
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

</div>

{% endfor %}

</div>


<!-- ========================= -->
<!-- JavaScript -->
<!-- ========================= -->

<script>

let currentMode = "selected";
let currentTopic = "All";


function updatePublications() {

  const papers =
    document.querySelectorAll(".publication-item");


  papers.forEach(function(paper) {

    const selected =
      paper.getAttribute("data-selected") === "true";

    const tag =
      paper.getAttribute("data-tag");


    let show = true;


    /*
     * Selected / All by date
     */

    if (currentMode === "selected") {

      if (!selected) {
        show = false;
      }

    }


    /*
     * Topic filter
     *
     * Only applies to Selected mode
     */

    if (
      currentMode === "selected" &&
      currentTopic !== "All"
    ) {

      if (tag !== currentTopic) {
        show = false;
      }

    }


    /*
     * Display
     */

    if (show) {

      paper.style.display = "";

    } else {

      paper.style.display = "none";

    }

  });

}


/* ========================= */
/* Mode */
/* ========================= */

function setPublicationMode(mode) {

  currentMode = mode;


  /*
   * Update mode buttons
   */

  document
    .getElementById("selected-btn")
    .classList.remove("active");

  document
    .getElementById("all-date-btn")
    .classList.remove("active");


  if (mode === "selected") {

    document
      .getElementById("selected-btn")
      .classList.add("active");


    /*
     * Show Topics
     */

    document
      .getElementById("topics-container")
      .style.display = "";


  } else {

    document
      .getElementById("all-date-btn")
      .classList.add("active");


    /*
     * Hide Topics
     */

    document
      .getElementById("topics-container")
      .style.display = "none";

  }


  /*
   * Reset topic when switching modes
   */

  currentTopic = "All";


  document
    .querySelectorAll(".topic-btn")
    .forEach(function(button) {

      button.classList.remove("active");

      if (button.dataset.topic === "All") {
        button.classList.add("active");
      }

    });


  updatePublications();

}


/* ========================= */
/* Topic */
/* ========================= */

function filterTopic(topic) {

  currentTopic = topic;


  document
    .querySelectorAll(".topic-btn")
    .forEach(function(button) {

      button.classList.remove("active");

      if (button.dataset.topic === topic) {

        button.classList.add("active");

      }

    });


  updatePublications();

}


/* ========================= */
/* Initial state */
/* ========================= */

document.addEventListener(
  "DOMContentLoaded",
  function() {

    setPublicationMode("selected");

  }
);

</script>
```
