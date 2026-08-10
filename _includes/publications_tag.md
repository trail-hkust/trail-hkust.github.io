
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
    flex-wrap:wrap;
    gap:10px;
    margin-bottom:30px;
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
<!-- CONVERT TOPIC NAME TO TOPIC ID                        -->
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
<!-- ONE PUBLICATION ITEM                                  -->
<!-- ===================================================== -->

<div
  class="publication-item"
  data-topics="{{ topic_ids | strip }}"
  data-year="{{ link.year }}"
  style="
    margin-bottom:30px;
  "
>


  <!-- ================================================= -->
  <!-- IMAGE                                             -->
  <!-- ================================================= -->

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
  <!-- YEAR + TOPICS                                     -->
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

{% endfor %}



<!-- ===================================================== -->
<!-- JAVASCRIPT                                            -->
<!-- ===================================================== -->

<script>

document.addEventListener("DOMContentLoaded", function () {


  /* =====================================================
   * GET ELEMENTS
   * ===================================================== */

  const searchInput =
    document.getElementById("publication-search");

  const yearSelect =
    document.getElementById("publication-year");

  const publications =
    document.querySelectorAll(".publication-item");

  const topicFilters =
    document.querySelectorAll(".topic-filter");


  /* =====================================================
   * CURRENT TOPIC
   *
   * Topic is completely independent from Search.
   * ===================================================== */

  let currentTopic = "all";


  /* =====================================================
   * TOPIC FILTER
   *
   * This function ONLY handles Topic.
   *
   * Search is NOT involved here.
   * Year is NOT involved here.
   * ===================================================== */

  window.showPublicationTopic = function (topic) {


    currentTopic = topic;


    publications.forEach(function (item) {


      const topics =
        (item.dataset.topics || "")
          .trim()
          .split(/\s+/)
          .filter(Boolean);


      if (topic === "all") {

        item.style.display = "";

      }

      else if (topics.includes(topic)) {

        item.style.display = "";

      }

      else {

        item.style.display = "none";

      }

    });


    /* =================================================
     * UPDATE TOPIC VISUAL STATE
     * ================================================= */

    topicFilters.forEach(function (filter) {


      const filterTopic =
        filter.dataset.topic;


      if (filterTopic === topic) {

        filter.style.borderBottom =
          "2px solid currentColor";

      }

      else {

        filter.style.borderBottom =
          "2px solid transparent";

      }

    });

  };


  /* =====================================================
   * SEARCH + YEAR
   *
   * IMPORTANT:
   *
   * This function completely ignores currentTopic.
   *
   * It ALWAYS searches through ALL publications.
   * ===================================================== */

  function searchPublications() {


    const query =
      searchInput.value
        .toLowerCase()
        .trim();


    const selectedYear =
      yearSelect.value;


    /* =================================================
     * SEARCH ALL PUBLICATIONS
     * ================================================= */

    publications.forEach(function (item) {


      /*
       * Get the complete text of this publication.
       *
       * This includes:
       * title
       * authors
       * year
       * topics
       * conference
       * etc.
       */

      const text =
        item.textContent
          .toLowerCase();


      const year =
        item.dataset.year || "";


      /* ===============================================
       * SEARCH CONDITION
       * =============================================== */

      const matchesSearch =
        query === "" ||
        text.includes(query);


      /* ===============================================
       * YEAR CONDITION
       * =============================================== */

      const matchesYear =
        selectedYear === "all" ||
        year === selectedYear;


      /* ===============================================
       * DISPLAY
       *
       * NO currentTopic here.
       * =============================================== */

      if (
        matchesSearch &&
        matchesYear
      ) {

        item.style.display = "";

      }

      else {

        item.style.display = "none";

      }

    });


    /*
     * Search has now switched the display back to
     * the ALL-publications search space.
     *
     * Therefore visually activate "All".
     */

    topicFilters.forEach(function (filter) {


      if (
        filter.dataset.topic === "all"
      ) {

        filter.style.borderBottom =
          "2px solid currentColor";

      }

      else {

        filter.style.borderBottom =
          "2px solid transparent";

      }

    });


    /*
     * Do NOT change currentTopic here.
     *
     * The variable is intentionally left untouched.
     *
     * Search and Topic are logically independent.
     */

  };


  /* =====================================================
   * SEARCH INPUT
   * ===================================================== */

  if (searchInput) {

    searchInput.addEventListener(
      "input",
      searchPublications
    );

  }


  /* =====================================================
   * YEAR SELECT
   *
   * Year follows the same logic as Search:
   * it searches ALL publications.
   * ===================================================== */

  if (yearSelect) {

    yearSelect.addEventListener(
      "change",
      searchPublications
    );

  }


  /* =====================================================
   * INITIAL STATE
   *
   * Start with ALL publications.
   * ===================================================== */

  window.showPublicationTopic("all");


});

</script>
