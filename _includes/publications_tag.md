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

  <input
    type="text"
    id="publication-search"
    placeholder="Search publications..."
    style="
      width:350px;
      padding:7px 10px;
      font-size:14px;
      border:1px solid #cccccc;
      border-radius:4px;
      box-sizing:border-box;
    "
  >


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


<!-- ===================================================== -->
<!-- CONVERT TAGS TO TOPIC IDS                             -->
<!-- ===================================================== -->

{% assign topic_ids = "" %}

{% for tag in link.tag %}

  {% if tag == "Multi-Agent Learning & Reasoning" %}

    {% assign topic_ids = topic_ids | append: "multi-agent " %}

  {% elsif tag == "Model Interpretability, Representation & Evaluation" %}

    {% assign topic_ids = topic_ids | append: "interpretability " %}

  {% elsif tag == "AI for Investment" %}

    {% assign topic_ids = topic_ids | append: "investment " %}

  {% elsif tag == "AI for Regulatory Compliance" %}

    {% assign topic_ids = topic_ids | append: "compliance " %}

  {% endif %}

{% endfor %}



<!-- ===================================================== -->
<!-- ONE PUBLICATION                                       -->
<!-- ===================================================== -->

<div
  class="publication-item"
  data-title="{{ link.title | escape | downcase }}"
  data-year="{{ link.year }}"
  data-topics="{{ topic_ids | strip }}"
  style="
    display:none !important;
    width:100%;
    margin-bottom:30px;
    box-sizing:border-box;
  "
>


  <!-- =================================================== -->
  <!-- IMAGE                                                -->
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
          height:160px;
          align-items:center;
          justify-content:center;
          overflow:hidden;
          background:#f7f7f7;
          border:1px solid #e5e5e5;
          border-radius:8px;
          text-decoration:none;
          box-sizing:border-box;
        "
      >

        <img
          src="{{ link.image }}"
          alt="{{ link.title }}"
          style="
            display:block;
            width:100%;
            height:100%;
            object-fit:cover;
            object-position:center;
          "
        >

      </a>

    {% endif %}

  </div>



  <!-- =================================================== -->
  <!-- INFORMATION                                         -->
  <!-- =================================================== -->

  <div
    style="
      width:70%;
      flex:0 0 70%;
      box-sizing:border-box;
      padding:0;
    "
  >


    <!-- TITLE -->

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
          style="text-decoration:none;"
        >
          {{ link.title }}
        </a>

      {% else %}

        {{ link.title }}

      {% endif %}

    </div>



    <!-- AUTHORS -->

    <div
      class="author"
      style="
        margin-bottom:6px;
        line-height:1.5;
      "
    >
      {{ link.authors }}
    </div>



    <!-- YEAR + TOPICS -->

    <div
      style="
        margin-bottom:6px;
        line-height:1.5;
      "
    >

      {% if link.year %}
        {{ link.year }}
      {% endif %}


      {% if link.tag %}

        <span
          style="
            margin-left:6px;
            margin-right:6px;
          "
        >
          ·
        </span>


        {% for tag in link.tag %}

          {% assign tag_id = "" %}


          {% if tag == "Multi-Agent Learning & Reasoning" %}

            {% assign tag_id = "multi-agent" %}

          {% elsif tag == "Model Interpretability, Representation & Evaluation" %}

            {% assign tag_id = "interpretability" %}

          {% elsif tag == "AI for Investment" %}

            {% assign tag_id = "investment" %}

          {% elsif tag == "AI for Regulatory Compliance" %}

            {% assign tag_id = "compliance" %}

          {% endif %}


          {% if tag_id != "" %}

            <a
              href="javascript:void(0);"
              class="publication-topic"
              data-topic="{{ tag_id }}"
              onclick="showPublicationTopic('{{ tag_id }}')"
              style="
                text-decoration:none;
                cursor:pointer;
                color:inherit;
              "
            >
              {{ tag }}
            </a>

          {% else %}

            <span>
              {{ tag }}
            </span>

          {% endif %}


          {% unless forloop.last %}

            <span
              style="
                margin-left:6px;
                margin-right:6px;
              "
            >
              ·
            </span>

          {% endunless %}

        {% endfor %}

      {% endif %}

    </div>



    <!-- CONFERENCE + LINKS -->

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

  /*
   * null means:
   *
   * NO TOPIC HAS BEEN SELECTED.
   *
   * Therefore the initial page shows
   * ZERO publications.
   */

  var currentPublicationTopic = null;



  /* =====================================================
     APPLY FILTERS
     ===================================================== */
  
  function applyPublicationFilters() {
  
    var searchInput =
      document.getElementById("publication-search");
  
    var yearSelect =
      document.getElementById("publication-year");
  
  
    if (!searchInput || !yearSelect) {
      return;
    }
  
  
    var keyword =
      searchInput.value
        .toLowerCase()
        .trim();
  
  
    var selectedYear =
      yearSelect.value;
  
  
    var items =
      document.querySelectorAll(
        ".publication-item"
      );
  
  
  
    /* ===================================================
       CHECK EVERY PUBLICATION
       =================================================== */
  
    items.forEach(function (item) {
  
  
      /* ===============================================
         GET DATA
         =============================================== */
  
      var title =
        (
          item.getAttribute("data-title") || ""
        ).toLowerCase();
  
  
      var year =
        (
          item.getAttribute("data-year") || ""
        ).toLowerCase();
  
  
      var topicString =
        (
          item.getAttribute("data-topics") || ""
        ).toLowerCase().trim();
  
  
      var topics =
        topicString === ""
          ? []
          : topicString.split(/\s+/);
  
  
      var fullText =
        (
          item.textContent || ""
        ).toLowerCase();
  
  
  
      /* ===============================================
         SEARCH
         =============================================== */
  
      var matchesSearch =
        keyword === "" ||
        title.indexOf(keyword) !== -1 ||
        fullText.indexOf(keyword) !== -1;
  
  
  
      /* ===============================================
         YEAR
         =============================================== */
  
      var matchesYear =
        selectedYear === "all" ||
        year === selectedYear;
  
  
  
      /* ===============================================
         IMPORTANT:
         SEARCH MODE IS INDEPENDENT FROM TOPIC
         =============================================== */
  
      /*
       * If the user is typing something into the
       * search box, Search + Year are used.
       *
       * The current Topic is completely ignored.
       *
       * Therefore:
       *
       * Topic = Multi-Agent
       * Search = investment
       *
       * will search "investment" across ALL papers.
       */
  
      if (keyword !== "") {
  
        if (
          matchesSearch &&
          matchesYear
        ) {
  
          item.style.setProperty(
            "display",
            "flex",
            "important"
          );
  
        } else {
  
          item.style.setProperty(
            "display",
            "none",
            "important"
          );
  
        }
  
        return;
      }
  
  
  
      /* ===============================================
         NO SEARCH KEYWORD
         =============================================== */
  
      /*
       * When Search is empty, Topic works normally.
       *
       * Therefore:
       *
       * Search = empty
       * Topic = Multi-Agent
       *
       * → only Multi-Agent papers are shown.
       */
  
      if (currentPublicationTopic === null) {
  
        item.style.setProperty(
          "display",
          "none",
          "important"
        );
  
        return;
  
      }
  
  
      var matchesTopic =
        currentPublicationTopic === "all" ||
        topics.indexOf(
          currentPublicationTopic
        ) !== -1;
  
  
  
      /* ===============================================
         SHOW / HIDE
         =============================================== */
  
      if (
        matchesYear &&
        matchesTopic
      ) {
  
        item.style.setProperty(
          "display",
          "flex",
          "important"
        );
  
      } else {
  
        item.style.setProperty(
          "display",
          "none",
          "important"
        );
  
      }
  
    });
  
  }


  /* =====================================================
     TOPIC BUTTON
     ===================================================== */

  window.showPublicationTopic =
    function (topic) {


      /*
       * DIRECT REPLACEMENT.
       *
       * Clicking Investment after Multi-Agent
       * does NOT combine the two.
       *
       * It simply changes:
       *
       * multi-agent
       *
       * into:
       *
       * investment
       */

      currentPublicationTopic = topic;



      /* ===============================================
         UPDATE BUTTON STYLE
         =============================================== */

      var topicButtons =
        document.querySelectorAll(
          ".topic-filter"
        );


      topicButtons.forEach(function (button) {

        var buttonTopic =
          button.getAttribute(
            "data-topic"
          );


        if (buttonTopic === topic) {

          button.style.fontWeight = "600";

          button.style.borderBottom =
            "2px solid currentColor";

        } else {

          button.style.fontWeight = "400";

          button.style.borderBottom =
            "2px solid transparent";

        }

      });



      /* ===============================================
         APPLY FILTER
         =============================================== */

      applyPublicationFilters();

    };



  /* =====================================================
     INITIALIZATION
     ===================================================== */

  function initializePublicationFilters() {


    /*
     * Make absolutely sure that every publication
     * starts hidden.
     */

    var items =
      document.querySelectorAll(
        ".publication-item"
      );


    items.forEach(function (item) {

      item.style.setProperty(
        "display",
        "none",
        "important"
      );

    });



    /* ===============================================
       SEARCH
       =============================================== */

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



    /* ===============================================
       YEAR
       =============================================== */

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



    /*
     * DO NOT call applyPublicationFilters()
     * here with topic = all.
     *
     * currentPublicationTopic is null,
     * so the page stays empty.
     */

  }



  /* =====================================================
     START
     ===================================================== */

  initializePublicationFilters();


})();

</script>
