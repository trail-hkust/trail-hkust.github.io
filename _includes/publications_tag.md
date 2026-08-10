```html
<h1 id="publications"></h1>

<h2 style="margin: 30px 0px 20px;">
  Publications
</h2>


<!-- ===================================================== -->
<!-- TOPIC FILTERS                                         -->
<!-- ===================================================== -->

<div
  style="
    display:flex;
    align-items:baseline;
    flex-wrap:wrap;
    margin-bottom:25px;
    padding-left:15px;
    line-height:1.8;
  "
>

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
    "
  >
    All
  </a>


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
    "
  >
    Multi-Agent Learning &amp; Reasoning
  </a>


  <!-- COMPLIANCE -->

  <a
    href="javascript:void(0);"
    class="topic-filter"
    data-topic="compliance"
    onclick="showPublicationTopic('compliance')"
    style="
      margin-right:15px;
      text-decoration:none;
      cursor:pointer;
      border-bottom:2px solid transparent;
      padding-bottom:2px;
    "
  >
    AI for Regulatory Compliance
  </a>


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
    "
  >
    Model Interpretability, Representation &amp; Evaluation
  </a>


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
    "
  >
    AI for Investment
  </a>

</div>



<!-- ===================================================== -->
<!-- SEARCH + YEAR                                         -->
<!-- ===================================================== -->

<div
  style="
    display:flex;
    align-items:center;
    gap:12px;
    margin-left:20px;
    margin-bottom:25px;
    flex-wrap:wrap;
  "
>

  <!-- SEARCH -->

  <input
    type="text"
    id="publication-search"
    placeholder="Search publications..."
    style="
      width:300px;
      padding:7px 10px;
      font-size:14px;
      border:1px solid #cccccc;
      border-radius:4px;
      box-sizing:border-box;
    "
  >


  <!-- YEAR -->

  <select
    id="publication-year"
    style="
      padding:7px 10px;
      font-size:14px;
      border:1px solid #cccccc;
      border-radius:4px;
      background:white;
      cursor:pointer;
    "
  >

    <option value="all">
      Year: All
    </option>

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
  "
>


  <!-- =================================================== -->
  <!-- LEFT: IMAGE                                          -->
  <!-- =================================================== -->

  <div
    style="
      width:30%;
      flex:0 0 30%;
      padding-right:25px;
      box-sizing:border-box;
    "
  >

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
        "
      >

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
          "
        >

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
    "
  >


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
      "
    >

      {% if link.pdf %}

        <a
          href="{{ link.pdf }}"
          target="_blank"
          style="
            text-decoration:none;
          "
        >
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
      "
    >

      {{ link.authors }}

    </div>



    <!-- ================================================= -->
    <!-- YEAR + TOPIC                                      -->
    <!-- ================================================= -->

    <div
      style="
        margin-bottom:6px;
        line-height:1.5;
      "
    >

      {% if link.year %}

        {{ link.year }}

      {% endif %}


      {% if topic_id != "" %}

        <span
          style="
            margin-left:6px;
            margin-right:6px;
          "
        >
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
          "
        >
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
      "
    >

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
          "
        >
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
          "
        >
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
          "
        >
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
          "
        >
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

(function () {

  /* =======================================================
     CURRENT TOPIC
     ======================================================= */

  var currentPublicationTopic = "all";


  /* =======================================================
     APPLY ALL FILTERS
     ======================================================= */

  function applyPublicationFilters() {

    var searchInput =
      document.getElementById("publication-search");

    var yearSelect =
      document.getElementById("publication-year");


    if (!searchInput || !yearSelect) {

      console.log(
        "Publication search elements not found."
      );

      return;

    }


    /* -----------------------------------------------------
       Search keyword
       ----------------------------------------------------- */

    var keyword =
      searchInput.value
        .toLowerCase()
        .trim();


    /* -----------------------------------------------------
       Selected year
       ----------------------------------------------------- */

    var selectedYear =
      yearSelect.value;


    /* -----------------------------------------------------
       Publications
       ----------------------------------------------------- */

    var items =
      document.querySelectorAll(
        ".publication-item"
      );


    /* -----------------------------------------------------
       Filter every publication
       ----------------------------------------------------- */

    items.forEach(function (item) {


      /* ===================================================
         TITLE
         =================================================== */

      var title =
        (
          item.getAttribute(
            "data-title"
          ) || ""
        ).toLowerCase();



      /* ===================================================
         YEAR
         =================================================== */

      var year =
        (
          item.getAttribute(
            "data-year"
          ) || ""
        ).toLowerCase();



      /* ===================================================
         TOPIC
         =================================================== */

      var topic =
        (
          item.getAttribute(
            "data-topic"
          ) || ""
        ).toLowerCase();



      /* ===================================================
         FULL TEXT
         =================================================== */

      /*
       * Search the complete publication text.
       *
       * This includes:
       *
       * - title
       * - authors
       * - year
       * - topic
       * - conference
       * - other displayed information
       */

      var fullText =
        (
          item.textContent || ""
        ).toLowerCase();



      /* ===================================================
         SEARCH MATCH
         =================================================== */

      var matchesSearch =
        keyword === "" ||
        title.indexOf(keyword) !== -1 ||
        fullText.indexOf(keyword) !== -1;



      /* ===================================================
         YEAR MATCH
         =================================================== */

      var matchesYear =
        selectedYear === "all" ||
        year === selectedYear;



      /* ===================================================
         TOPIC MATCH
         =================================================== */

      var matchesTopic =
        currentPublicationTopic === "all" ||
        topic === currentPublicationTopic;



      /* ===================================================
         FINAL MATCH
         =================================================== */

      if (
        matchesSearch &&
        matchesYear &&
        matchesTopic
      ) {

        item.style.display = "flex";

      } else {

        item.style.display = "none";

      }

    });

  }



  /* =======================================================
     TOPIC FILTER
     ======================================================= */

  window.showPublicationTopic =
    function (topic) {


      /* ---------------------------------------------------
         Save selected topic
         --------------------------------------------------- */

      currentPublicationTopic =
        topic;


      /* ---------------------------------------------------
         Update topic buttons
         --------------------------------------------------- */

      var topicButtons =
        document.querySelectorAll(
          ".topic-filter"
        );


      topicButtons.forEach(
        function (button) {


          if (
            button.getAttribute(
              "data-topic"
            ) === topic
          ) {


            /* Selected */

            button.style.fontWeight =
              "600";

            button.style.borderBottom =
              "2px solid currentColor";

            button.style.paddingBottom =
              "2px";


          } else {


            /* Not selected */

            button.style.fontWeight =
              "400";

            button.style.borderBottom =
              "2px solid transparent";

            button.style.paddingBottom =
              "2px";

          }

        }
      );


      /* ---------------------------------------------------
         Apply all filters again
         --------------------------------------------------- */

      applyPublicationFilters();

    };



  /* =======================================================
     SEARCH FUNCTION
     ======================================================= */

  window.searchPublications =
    function () {

      applyPublicationFilters();

    };



  /* =======================================================
     INITIALIZATION
     ======================================================= */

  function initializePublicationFilters() {


    console.log(
      "Publication filter initialized."
    );


    /* -----------------------------------------------------
       Search input
       ----------------------------------------------------- */

    var searchInput =
      document.getElementById(
        "publication-search"
      );


    if (searchInput) {

      searchInput.addEventListener(
        "input",
        function () {

          applyPublicationFilters();

        }
      );

    }



    /* -----------------------------------------------------
       Year selector
       ----------------------------------------------------- */

    var yearSelect =
      document.getElementById(
        "publication-year"
      );


    if (yearSelect) {

      yearSelect.addEventListener(
        "change",
        function () {

          applyPublicationFilters();

        }
      );

    }



    /* -----------------------------------------------------
       Initial topic button state
       ----------------------------------------------------- */

    var topicButtons =
      document.querySelectorAll(
        ".topic-filter"
      );


    topicButtons.forEach(
      function (button) {

        button.style.fontWeight =
          "400";

        button.style.borderBottom =
          "2px solid transparent";

        button.style.paddingBottom =
          "2px";

      }
    );



    /* -----------------------------------------------------
       Initially show all publications
       ----------------------------------------------------- */

    var items =
      document.querySelectorAll(
        ".publication-item"
      );


    items.forEach(
      function (item) {

        item.style.display =
          "flex";

      }
    );

  }



  /* =======================================================
     START
     ======================================================= */

  /*
   * The script is located AFTER the publications,
   * so the DOM already exists.
   */

  initializePublicationFilters();


})();

</script>
```
