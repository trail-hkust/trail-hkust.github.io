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

<!-- ================================================= -->
<!-- Publication Mode -->
<!-- ================================================= -->

<div style="margin-bottom: 12px;">

  <button
    id="selected-btn"
    class="publication-mode active"
    onclick="setPublicationMode('selected')"
    style="border:none;
           background:none;
           padding:0;
           margin-right:20px;
           font-size:15px;
           cursor:pointer;">
    Selected
  </button>

  <button
    id="all-date-btn"
    class="publication-mode"
    onclick="setPublicationMode('all')"
    style="border:none;
           background:none;
           padding:0;
           font-size:15px;
           cursor:pointer;">
    All by date
  </button>

</div>


<!-- ================================================= -->
<!-- Topics -->
<!-- ================================================= -->

<div style="margin-bottom: 25px;">

  <strong style="margin-right: 8px;">
    Topics:
  </strong>

  <a href="#topic-all"
     onclick="showPublicationTopic('all'); return false;"
     style="margin-right: 15px;
            text-decoration:none;">
    All
  </a>

  <a href="#topic-multi-agent"
     onclick="showPublicationTopic('multi-agent'); return false;"
     style="margin-right: 15px;
            text-decoration:none;">
    Multi-Agent Learning &amp; Reasoning
  </a>

  <a href="#topic-interpretability"
     onclick="showPublicationTopic('interpretability'); return false;"
     style="margin-right: 15px;
            text-decoration:none;">
    Model Interpretability, Representation &amp; Evaluation
  </a>

  <a href="#topic-investment"
     onclick="showPublicationTopic('investment'); return false;"
     style="margin-right: 15px;
            text-decoration:none;">
    AI for Investment
  </a>

  <a href="#topic-compliance"
     onclick="showPublicationTopic('compliance'); return false;"
     style="margin-right: 15px;
            text-decoration:none;">
    AI for Regulatory Compliance
  </a>

</div>


<!-- ================================================= -->
<!-- Publication List -->
<!-- ================================================= -->

<div id="publication-list">

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

{% assign topic_id = "" %}

{% if category == "Multi-Agent Learning & Reasoning" %}
  {% assign topic_id = "multi-agent" %}
{% elsif category == "Model Interpretability, Representation & Evaluation" %}
  {% assign topic_id = "interpretability" %}
{% elsif category == "AI-driven investment" %}
  {% assign topic_id = "investment" %}
{% elsif category == "AI for regulatory compliance" %}
  {% assign topic_id = "compliance" %}
{% endif %}


<!-- ================================================= -->
<!-- ONE PUBLICATION -->
<!-- ================================================= -->

<div class="publication-item"
     data-topic="{{ topic_id }}"
     data-selected="true"
     style="display:flex;
            width:100%;
            align-items:flex-start;
            margin-bottom:35px;
            padding-bottom:25px;
            border-bottom:1px solid #eeeeee;
            box-sizing:border-box;">


  <!-- ================================================= -->
  <!-- LEFT: IMAGE 30% -->
  <!-- ================================================= -->

  <div style="width:30%;
              flex:0 0 30%;
              padding-right:25px;
              box-sizing:border-box;">

    {% if link.image %}

    <a href="{{ link.image }}"
       target="_blank"
       style="display:block;
              width:100%;
              height:180px;
              overflow:hidden;
              border:1px solid #e5e5e5;
              border-radius:4px;
              background:#f8f8f8;
              text-decoration:none;">

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

  </div>


  <!-- ================================================= -->
  <!-- RIGHT: INFORMATION 70% -->
  <!-- ================================================= -->

  <div style="width:70%;
              flex:0 0 70%;
              box-sizing:border-box;">


    <!-- Title -->

    <div class="title"
         style="font-size:17px;
                font-weight:600;
                line-height:1.45;
                margin-bottom:8px;">

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


    <!-- Authors -->

    <div class="author"
         style="margin-bottom:6px;
                line-height:1.5;">

      {{ link.authors }}

    </div>


    <!-- Conference -->

    <div class="periodical"
         style="margin-bottom:10px;
                line-height:1.5;">

      <em>{{ link.conference }}</em>

    </div>


    <!-- ================================================= -->
    <!-- Links -->
    <!-- ================================================= -->

    <div class="links"
         style="margin-top:8px;">

      {% if link.pdf %}

      <a href="{{ link.pdf }}"
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

      <a href="{{ link.web }}"
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

      <a href="{{ link.code }}"
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

      <a href="{{ link.bibtex }}"
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

  </div>

</div>

{% endfor %}

{% endfor %}

</div>


<!-- ================================================= -->
<!-- JavaScript -->
<!-- ================================================= -->

<script>

function showPublicationTopic(topic) {

  var items = document.querySelectorAll(".publication-item");

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

  var items = document.querySelectorAll(".publication-item");

  var selectedButton = document.getElementById("selected-btn");
  var allDateButton = document.getElementById("all-date-btn");


  if (mode === "selected") {

    items.forEach(function(item) {

      if (item.getAttribute("data-selected") === "true") {

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

</script>
