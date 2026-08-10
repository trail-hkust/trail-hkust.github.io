---

layout: page
title: Publications
permalink: /publications/
-------------------------

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

<!-- ========================= -->

<!-- Publication Mode -->

<!-- ========================= -->

<div style="margin-bottom: 10px;">

<button
 id="selected-btn"
 class="publication-mode active"
 onclick="setPublicationMode('selected')"
 style="
   border: none;
   background: none;
   padding: 0;
   margin-right: 20px;
   font-size: 15px;
   font-weight: 600;
   cursor: pointer;
   color: #222;
 ">
Selected </button>

<button
 id="all-date-btn"
 class="publication-mode"
 onclick="setPublicationMode('all')"
 style="
   border: none;
   background: none;
   padding: 0;
   font-size: 15px;
   cursor: pointer;
   color: #888;
 ">
All by date </button>

</div>

<!-- ========================= -->

<!-- Selected Publications -->

<!-- ========================= -->

<div id="selected-publications">

  <div style="margin: 12px 0 25px 0; font-size: 14px;">

```
<strong>Topics:</strong>

<a href="#multi-agent-learning-reasoning"
   style="
     margin-left: 10px;
     margin-right: 14px;
     text-decoration: none;
   ">
  Multi-Agent Learning &amp; Reasoning
</a>

<a href="#model-interpretability-representation-evaluation"
   style="
     margin-right: 14px;
     text-decoration: none;
   ">
  Model Interpretability, Representation &amp; Evaluation
</a>

<a href="#ai-for-investment"
   style="
     margin-right: 14px;
     text-decoration: none;
   ">
  AI for Investment
</a>

<a href="#ai-for-regulatory-compliance"
   style="
     text-decoration: none;
   ">
  AI for Regulatory Compliance
</a>
```

  </div>

{% assign categories = "Multi-Agent Learning & Reasoning|Model Interpretation, Representation & Evaluation|AI-driven investment|AI for regulatory compliance" | split: "|" %}

{% for category in categories %}

```
{% assign category_id = category | slugify %}

<h3 id="{{ category_id }}"
    style="
      margin-top: 35px;
      margin-bottom: 20px;
      padding-bottom: 8px;
      border-bottom: 1px solid #ddd;
      font-size: 20px;
    ">
  {{ category }}
</h3>


{% assign category_papers = site.data.publications_tag.main | where: "tag", category %}

<ol class="bibliography">

  {% for link in category_papers %}

  <li style="margin-bottom: 35px;">

    <div
      class="publication-entry"
      style="
        display: flex;
        align-items: flex-start;
        width: 100%;
        margin-bottom: 20px;
      ">


      <!-- ========================= -->
      <!-- Image: 30% -->
      <!-- ========================= -->

      <div
        style="
          width: 30%;
          flex: 0 0 30%;
          padding-right: 20px;
        ">

        {% if link.image %}

        <a href="{{ link.image }}"
           target="_blank"
           title="Click to view full-size image"
           style="
             display: block;
             width: 100%;
             height: 210px;
             overflow: hidden;
             border: 1px solid #e5e5e5;
             background: #fafafa;
             text-align: center;
           ">

          <img
            src="{{ link.image }}"
            alt="{{ link.title }}"
            style="
              width: 100%;
              height: 100%;
              object-fit: contain;
              display: block;
            ">

        </a>

        {% endif %}

      </div>


      <!-- ========================= -->
      <!-- Publication Info: 70% -->
      <!-- ========================= -->

      <div
        style="
          width: 70%;
          flex: 0 0 70%;
          padding-left: 5px;
        ">


        <!-- Title -->

        <div
          class="title"
          style="
            font-size: 17px;
            font-weight: 600;
            line-height: 1.45;
            margin-bottom: 8px;
          ">

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
          style="
            font-size: 14px;
            line-height: 1.5;
            margin-bottom: 6px;
          ">
          {{ link.authors }}
        </div>


        <!-- Conference -->

        <div
          class="periodical"
          style="
            font-size: 14px;
            line-height: 1.5;
            margin-bottom: 12px;
          ">

          <em>{{ link.conference }}</em>

        </div>


        <!-- ========================= -->
        <!-- Links -->
        <!-- ========================= -->

        <div class="links"
             style="
               margin-top: 8px;
               display: flex;
               flex-wrap: wrap;
               align-items: center;
               gap: 6px;
             ">


          {% if link.pdf %}

          <a href="{{ link.pdf }}"
             target="_blank"
             style="
               display: inline-block;
               padding: 3px 9px;
               border: 1px solid #ccc;
               border-radius: 3px;
               font-size: 12px;
               text-decoration: none;
               color: #555;
               background: #fff;
             ">
            PDF
          </a>

          {% endif %}


          {% if link.web %}

          <a href="{{ link.web }}"
             target="_blank"
             style="
               display: inline-block;
               padding: 3px 9px;
               border: 1px solid #ccc;
               border-radius: 3px;
               font-size: 12px;
               text-decoration: none;
               color: #555;
               background: #fff;
             ">
            Website
          </a>

          {% endif %}


          {% if link.code %}

          <a href="{{ link.code }}"
             target="_blank"
             style="
               display: inline-block;
               padding: 3px 9px;
               border: 1px solid #ccc;
               border-radius: 3px;
               font-size: 12px;
               text-decoration: none;
               color: #555;
               background: #fff;
             ">
            Code
          </a>

          {% endif %}


          {% if link.bibtex %}

          <a href="{{ link.bibtex }}"
             target="_blank"
             style="
               display: inline-block;
               padding: 3px 9px;
               border: 1px solid #ccc;
               border-radius: 3px;
               font-size: 12px;
               text-decoration: none;
               color: #555;
               background: #fff;
             ">
            BibTeX
          </a>

          {% endif %}


          {% if link.page %}

          <a href="{{ link.page }}"
             target="_blank"
             style="
               display: inline-block;
               padding: 3px 9px;
               border: 1px solid #ccc;
               border-radius: 3px;
               font-size: 12px;
               text-decoration: none;
               color: #555;
               background: #fff;
             ">
            Project Page
          </a>

          {% endif %}


          {% if link.notes %}

          <span
            style="
              font-size: 12px;
              color: #e74d3c;
              margin-left: 3px;
            ">
            {{ link.notes }}
          </span>

          {% endif %}


          {% if link.others %}

            {{ link.others }}

          {% endif %}


        </div>

      </div>

    </div>

  </li>

  {% endfor %}

</ol>
```

{% endfor %}

</div>

<!-- ========================= -->

<!-- All Publications -->

<!-- ========================= -->

<div
  id="all-publications"
  style="display: none;">

  <ol class="bibliography">

```
{% for link in site.data.publications_tag.main %}

<li style="margin-bottom: 35px;">

  <div
    class="publication-entry"
    style="
      display: flex;
      align-items: flex-start;
      width: 100%;
      margin-bottom: 20px;
    ">


    <!-- Image -->

    <div
      style="
        width: 30%;
        flex: 0 0 30%;
        padding-right: 20px;
      ">

      {% if link.image %}

      <a href="{{ link.image }}"
         target="_blank"
         title="Click to view full-size image"
         style="
           display: block;
           width: 100%;
           height: 210px;
           overflow: hidden;
           border: 1px solid #e5e5e5;
           background: #fafafa;
           text-align: center;
         ">

        <img
          src="{{ link.image }}"
          alt="{{ link.title }}"
          style="
            width: 100%;
            height: 100%;
            object-fit: contain;
            display: block;
          ">

      </a>

      {% endif %}

    </div>


    <!-- Publication Info -->

    <div
      style="
        width: 70%;
        flex: 0 0 70%;
        padding-left: 5px;
      ">


      <!-- Title -->

      <div
        class="title"
        style="
          font-size: 17px;
          font-weight: 600;
          line-height: 1.45;
          margin-bottom: 8px;
        ">

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
        style="
          font-size: 14px;
          line-height: 1.5;
          margin-bottom: 6px;
        ">
        {{ link.authors }}
      </div>


      <!-- Conference -->

      <div
        class="periodical"
        style="
          font-size: 14px;
          line-height: 1.5;
          margin-bottom: 12px;
        ">
        <em>{{ link.conference }}</em>
      </div>


      <!-- Links -->

      <div
        class="links"
        style="
          margin-top: 8px;
          display: flex;
          flex-wrap: wrap;
          align-items: center;
          gap: 6px;
        ">


        {% if link.pdf %}

        <a href="{{ link.pdf }}"
           target="_blank"
           style="
             display: inline-block;
             padding: 3px 9px;
             border: 1px solid #ccc;
             border-radius: 3px;
             font-size: 12px;
             text-decoration: none;
             color: #555;
             background: #fff;
           ">
          PDF
        </a>

        {% endif %}


        {% if link.web %}

        <a href="{{ link.web }}"
           target="_blank"
           style="
             display: inline-block;
             padding: 3px 9px;
             border: 1px solid #ccc;
             border-radius: 3px;
             font-size: 12px;
             text-decoration: none;
             color: #555;
             background: #fff;
           ">
          Website
        </a>

        {% endif %}


        {% if link.code %}

        <a href="{{ link.code }}"
           target="_blank"
           style="
             display: inline-block;
             padding: 3px 9px;
             border: 1px solid #ccc;
             border-radius: 3px;
             font-size: 12px;
             text-decoration: none;
             color: #555;
             background: #fff;
           ">
          Code
        </a>

        {% endif %}


        {% if link.bibtex %}

        <a href="{{ link.bibtex }}"
           target="_blank"
           style="
             display: inline-block;
             padding: 3px 9px;
             border: 1px solid #ccc;
             border-radius: 3px;
             font-size: 12px;
             text-decoration: none;
             color: #555;
             background: #fff;
           ">
          BibTeX
        </a>

        {% endif %}


        {% if link.page %}

        <a href="{{ link.page }}"
           target="_blank"
           style="
             display: inline-block;
             padding: 3px 9px;
             border: 1px solid #ccc;
             border-radius: 3px;
             font-size: 12px;
             text-decoration: none;
             color: #555;
             background: #fff;
           ">
          Project Page
        </a>

        {% endif %}


        {% if link.notes %}

        <span
          style="
            font-size: 12px;
            color: #e74d3c;
            margin-left: 3px;
          ">
          {{ link.notes }}
        </span>

        {% endif %}


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

<!-- ========================= -->

<!-- JavaScript -->

<!-- ========================= -->

<script>

function setPublicationMode(mode) {

  var selectedPublications =
    document.getElementById("selected-publications");

  var allPublications =
    document.getElementById("all-publications");

  var selectedButton =
    document.getElementById("selected-btn");

  var allDateButton =
    document.getElementById("all-date-btn");


  if (mode === "selected") {

    selectedPublications.style.display = "block";
    allPublications.style.display = "none";

    selectedButton.style.color = "#222";
    selectedButton.style.fontWeight = "600";

    allDateButton.style.color = "#888";
    allDateButton.style.fontWeight = "400";

  }


  if (mode === "all") {

    selectedPublications.style.display = "none";
    allPublications.style.display = "block";

    selectedButton.style.color = "#888";
    selectedButton.style.fontWeight = "400";

    allDateButton.style.color = "#222";
    allDateButton.style.fontWeight = "600";

  }

}

</script>
