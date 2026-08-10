<h1 id="publications"></h1>

<h2 style="margin: 30px 0px -5px;">
  Publications

  <span style="font-size:15px; font-weight:normal; margin-left:10px;">
    [
    <a href="https://scholar.google.com/citations?user=lxrXMY0AAAAJ&hl=en&oi=ao"
       target="_blank">
      Google Scholar
    </a>
    ]

```
[

<a href="https://www.researchgate.net/profile/Zixuan-Yuan"
   target="_blank">
  ResearchGate
</a>
]
```

  </span>
</h2>

<!-- =========================================================
     PUBLICATION FILTERS
     ========================================================= -->

<div style="
    margin: 20px 0 25px 0;
    font-size: 14px;
    line-height: 2;
">

  <!-- Selected / All by date -->

  <div style="margin-bottom: 5px;">

```
<strong style="margin-right: 15px;">
  Publications
</strong>

<a href="javascript:void(0);"
   onclick="showPublicationMode('selected')"
   id="selected-tab"
   style="
     margin-right: 15px;
     text-decoration: none;
     cursor: pointer;
   ">
  Selected
</a>

<a href="javascript:void(0);"
   onclick="showPublicationMode('all')"
   id="all-date-tab"
   style="
     text-decoration: none;
     cursor: pointer;
   ">
  All by date
</a>
```

  </div>

  <!-- Topics -->

  <div id="topic-filters"
       style="
         margin-top: 5px;
         display: none;
       ">

```
<strong style="margin-right: 12px;">
  Topics:
</strong>


<!-- All -->

<a href="javascript:void(0);"
   onclick="filterPublications('all')"
   class="topic-link active-topic"
   data-topic="all">
  All
</a>


<span style="margin: 0 7px;">
  |
</span>


<!-- Multi-Agent -->

<a href="javascript:void(0);"
   onclick="filterPublications('Multi-Agent Learning & Reasoning')"
   class="topic-link"
   data-topic="Multi-Agent Learning & Reasoning">
  Multi-Agent Learning &amp; Reasoning
</a>


<span style="margin: 0 7px;">
  |
</span>


<!-- Model Interpretation -->

<a href="javascript:void(0);"
   onclick="filterPublications('Model Interpretation, Representation & Evaluation')"
   class="topic-link"
   data-topic="Model Interpretation, Representation & Evaluation">
  Model Interpretation, Representation &amp; Evaluation
</a>


<span style="margin: 0 7px;">
  |
</span>


<!-- AI Investment -->

<a href="javascript:void(0);"
   onclick="filterPublications('AI-driven investment')"
   class="topic-link"
   data-topic="AI-driven investment">
  AI for Investment
</a>


<span style="margin: 0 7px;">
  |
</span>


<!-- Regulatory Compliance -->

<a href="javascript:void(0);"
   onclick="filterPublications('AI for regulatory compliance')"
   class="topic-link"
   data-topic="AI for Regulatory Compliance">
  AI for Regulatory Compliance
</a>
```

  </div>

</div>

<!-- =========================================================
     CSS
     ========================================================= -->

<style>

/* =========================================================
   Publication layout
   ========================================================= */

.publication-item {
    margin-bottom: 38px;
}


.publication-entry {

    display: flex;

    align-items: flex-start;

    width: 100%;

}


/* =========================================================
   LEFT: IMAGE
   30%
   ========================================================= */

.publication-image {

    width: 30%;

    flex: 0 0 30%;

    padding-right: 25px;

    box-sizing: border-box;

}


/* =========================================================
   RIGHT: INFORMATION
   70%
   ========================================================= */

.publication-info {

    width: 70%;

    flex: 0 0 70%;

    box-sizing: border-box;

}


/* =========================================================
   IMAGE PREVIEW BOX
   ========================================================= */

.publication-image-container {

    width: 100%;

    height: 190px;

    display: flex;

    align-items: center;

    justify-content: center;

    overflow: hidden;

    background: #f7f7f7;

    border: 1px solid #dddddd;

    border-radius: 4px;

    cursor: pointer;

    box-sizing: border-box;

}


/*
 * The image fills the preview box.
 *
 * object-fit: cover
 *
 * means different aspect ratios are cropped
 * instead of changing the box size.
 */

.publication-image-container img {

    width: 100% !important;

    height: 100% !important;

    object-fit: cover;

    display: block;

    transition: transform 0.2s ease;

}


/* Slight zoom on hover */

.publication-image-container:hover img {

    transform: scale(1.03);

}


/* =========================================================
   FULL-SIZE IMAGE LIGHTBOX
   ========================================================= */

.image-lightbox {

    display: none;

    position: fixed;

    z-index: 99999;

    left: 0;

    top: 0;

    width: 100%;

    height: 100%;

    background: rgba(0, 0, 0, 0.88);

    align-items: center;

    justify-content: center;

    padding: 30px;

    box-sizing: border-box;

    cursor: zoom-out;

}


.image-lightbox img {

    max-width: 95vw;

    max-height: 95vh;

    width: auto;

    height: auto;

    object-fit: contain;

    display: block;

    cursor: default;

}


.image-lightbox-close {

    position: fixed;

    top: 20px;

    right: 30px;

    color: white;

    font-size: 34px;

    font-weight: normal;

    cursor: pointer;

    z-index: 100000;

    line-height: 1;

}


.image-lightbox-close:hover {

    opacity: 0.7;

}


/* =========================================================
   TITLE
   ========================================================= */

.publication-title {

    font-size: 17px;

    line-height: 1.45;

    margin-bottom: 8px;

}


.publication-title a {

    text-decoration: none;

}


/* =========================================================
   AUTHORS
   ========================================================= */

.publication-authors {

    font-size: 14px;

    line-height: 1.5;

    margin-bottom: 7px;

}


/* =========================================================
   CONFERENCE
   ========================================================= */

.publication-conference {

    font-size: 14px;

    line-height: 1.5;

    margin-bottom: 10px;

}


/* =========================================================
   BUTTONS
   ========================================================= */

.publication-links {

    margin-top: 8px;

}


.publication-button {

    display: inline-block;

    padding: 2px 8px;

    margin-right: 5px;

    margin-bottom: 5px;

    border: 1px solid #aaa;

    border-radius: 3px;

    font-size: 12px;

    line-height: 1.5;

    text-decoration: none !important;

    background: transparent;

}


.publication-button:hover {

    background: #f5f5f5;

}


/* =========================================================
   PUBLISHED
   ========================================================= */

.publication-status {

    font-size: 12px;

    margin-left: 5px;

    color: #e74d3c;

}


/* =========================================================
   TOPICS
   ========================================================= */

.topic-link {

    text-decoration: none;

    cursor: pointer;

}


.topic-link:hover {

    text-decoration: underline;

}


.active-topic {

    font-weight: bold;

}


/* =========================================================
   MOBILE
   ========================================================= */

@media (max-width: 700px) {


    .publication-entry {

        display: block;

    }


    .publication-image {

        width: 100%;

        padding-right: 0;

        margin-bottom: 15px;

    }


    .publication-info {

        width: 100%;

    }


    .publication-image-container {

        height: 220px;

    }

}

</style>

<!-- =========================================================
     PUBLICATIONS
     ========================================================= -->

<div class="publications">

  <ol class="bibliography"
      style="
        padding-left: 0;
        list-style: none;
      ">

```
{% for link in site.data.publications_tag.main %}


<li class="publication-item"
    data-topic="{{ link.tag }}">


  <div class="publication-entry">


    <!-- =================================================
         LEFT IMAGE
         ================================================= -->

    <div class="publication-image">


      {% if link.image %}


      <div class="publication-image-container"
           onclick="openImageLightbox('{{ link.image }}')">


        <img src="{{ link.image }}"
             class="teaser img-fluid z-depth-1"
             alt="{{ link.title }}">


      </div>


      {% endif %}


    </div>



    <!-- =================================================
         RIGHT INFORMATION
         ================================================= -->

    <div class="publication-info">


      <!-- TITLE -->

      <div class="publication-title">


        {% if link.pdf %}


        <a href="{{ link.pdf }}"
           target="_blank">

          {{ link.title }}

        </a>


        {% else %}


        {{ link.title }}


        {% endif %}


      </div>



      <!-- AUTHORS -->

      <div class="publication-authors">

        {{ link.authors }}

      </div>



      <!-- CONFERENCE -->

      <div class="publication-conference">

        <em>
          {{ link.conference }}
        </em>

      </div>



      <!-- LINKS -->

      <div class="publication-links">


        <!-- PDF -->

        {% if link.pdf %}

        <a href="{{ link.pdf }}"
           class="publication-button"
           target="_blank">

          PDF

        </a>

        {% endif %}



        <!-- WEBSITE -->

        {% if link.web %}

        <a href="{{ link.web }}"
           class="publication-button"
           target="_blank">

          Website

        </a>

        {% endif %}



        <!-- CODE -->

        {% if link.code %}

        <a href="{{ link.code }}"
           class="publication-button"
           target="_blank">

          Code

        </a>

        {% endif %}



        <!-- BIBTEX -->

        {% if link.bibtex %}

        <a href="{{ link.bibtex }}"
           class="publication-button"
           target="_blank">

          BibTex

        </a>

        {% endif %}



        <!-- PROJECT PAGE -->

        {% if link.page %}

        <a href="{{ link.page }}"
           class="publication-button"
           target="_blank">

          Project Page

        </a>

        {% endif %}



        <!-- NOTES -->

        {% if link.notes %}

        <span class="publication-status">

          {{ link.notes }}

        </span>

        {% endif %}



        <!-- OTHERS -->

        {% if link.others %}

          {{ link.others }}

        {% endif %}


      </div>


    </div>


  </div>


</li>


{% endfor %}
```

  </ol>

</div>

<!-- =========================================================
     IMAGE LIGHTBOX
     ========================================================= -->

<div id="imageLightbox"
     class="image-lightbox"
     onclick="closeImageLightbox(event)">

<span class="image-lightbox-close"
     onclick="closeImageLightbox(event)">

```
&times;
```

  </span>

<img id="lightboxImage"
    src=""
    alt="Full-size publication image"
    onclick="event.stopPropagation();">

</div>

<!-- =========================================================
     JAVASCRIPT
     ========================================================= -->

<script>


/* =========================================================
   Current filter state
   ========================================================= */

var currentMode = "selected";

var currentTopic = "all";



/* =========================================================
   SELECTED / ALL BY DATE
   ========================================================= */

function showPublicationMode(mode) {


    currentMode = mode;


    var topicFilters =
        document.getElementById("topic-filters");


    var selectedTab =
        document.getElementById("selected-tab");


    var allDateTab =
        document.getElementById("all-date-tab");



    if (mode === "selected") {


        /* Show Topics */

        topicFilters.style.display = "block";


        /* Highlight Selected */

        selectedTab.style.fontWeight = "bold";

        allDateTab.style.fontWeight = "normal";


        /* Apply current topic */

        filterPublications(currentTopic);


    }


    else {


        /* Hide Topics */

        topicFilters.style.display = "none";


        /* Highlight All by date */

        selectedTab.style.fontWeight = "normal";

        allDateTab.style.fontWeight = "bold";


        /* Show all publications */

        var papers =
            document.querySelectorAll(".publication-item");


        papers.forEach(function(paper) {

            paper.style.display = "";

        });


    }

}



/* =========================================================
   TOPIC FILTER
   ========================================================= */

function filterPublications(topic) {


    currentTopic = topic;


    currentMode = "selected";


    var papers =
        document.querySelectorAll(".publication-item");


    papers.forEach(function(paper) {


        var paperTopic =
            paper.getAttribute("data-topic");


        if (
            topic === "all" ||
            paperTopic === topic
        ) {


            paper.style.display = "";


        }


        else {


            paper.style.display = "none";


        }


    });



    /* Update active topic */

    var topicLinks =
        document.querySelectorAll(".topic-link");


    topicLinks.forEach(function(link) {


        var linkTopic =
            link.getAttribute("data-topic");


        if (linkTopic === topic) {


            link.classList.add("active-topic");


        }


        else {


            link.classList.remove("active-topic");


        }


    });



    /* Make sure Selected is active */

    document.getElementById(
        "selected-tab"
    ).style.fontWeight = "bold";


    document.getElementById(
        "all-date-tab"
    ).style.fontWeight = "normal";


    document.getElementById(
        "topic-filters"
    ).style.display = "block";

}



/* =========================================================
   IMAGE LIGHTBOX
   ========================================================= */

function openImageLightbox(imageSrc) {


    var lightbox =
        document.getElementById("imageLightbox");


    var image =
        document.getElementById("lightboxImage");


    image.src = imageSrc;


    lightbox.style.display = "flex";


    /* Prevent background scrolling */

    document.body.style.overflow = "hidden";

}



/* =========================================================
   CLOSE LIGHTBOX
   ========================================================= */

function closeImageLightbox(event) {


    var lightbox =
        document.getElementById("imageLightbox");


    /*
     * Close if:
     *
     * 1. background is clicked
     * 2. × is clicked
     */

    if (
        event.target.id === "imageLightbox" ||
        event.target.classList.contains(
            "image-lightbox-close"
        )
    ) {


        lightbox.style.display = "none";


        document.getElementById(
            "lightboxImage"
        ).src = "";


        document.body.style.overflow = "";

    }

}



/* =========================================================
   ESC KEY
   ========================================================= */

document.addEventListener(
    "keydown",
    function(event) {


        if (event.key === "Escape") {


            var lightbox =
                document.getElementById(
                    "imageLightbox"
                );


            if (
                lightbox.style.display === "flex"
            ) {


                lightbox.style.display = "none";


                document.getElementById(
                    "lightboxImage"
                ).src = "";


                document.body.style.overflow = "";

            }

        }

    }
);



/* =========================================================
   INITIAL STATE
   ========================================================= */

document.addEventListener(
    "DOMContentLoaded",
    function() {

        showPublicationMode("selected");

    }
);

</script>
