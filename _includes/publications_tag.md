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

<!-- Category navigation -->

<!-- ========================= -->

<div style="
    margin: 10px 0 30px 0;
    text-align: left;
">

{% assign categories = "AI-driven investment|Multi-Agent Learning & Reasoning|Model Interpretation, Representation & Evaluation|AI for regulatory compliance" | split: "|" %}

{% for category in categories %}

<a href="#{{ category | slugify }}"
style="
   display: inline-block;
   margin: 4px 6px 4px 0;
   padding: 7px 14px;
   border: 1px solid #bbb;
   border-radius: 18px;
   font-size: 13px;
   text-decoration: none;
   color: #555;
   background-color: #fff;
">
{{ category }} </a>

{% endfor %}

</div>

<!-- ========================= -->

<!-- Contribution notes -->

<!-- ========================= -->

<p>
  * means equal contribution.<br>
  † means corresponding authors.
</p>

<!-- ========================= -->

<!-- Publications -->

<!-- ========================= -->

{% assign categories = "AI-driven investment|Multi-Agent Learning & Reasoning|Model Interpretation, Representation & Evaluation|AI for regulatory compliance" | split: "|" %}

{% for category in categories %}

<!-- ========================= -->

<!-- REAL ANCHOR TARGET -->

<!-- ========================= -->

<h3 id="{{ category | slugify }}"
    style="
      margin-top: 45px;
      margin-bottom: 25px;
      padding-bottom: 8px;
      border-bottom: 2px solid #ddd;
      font-size: 21px;
      font-weight: 600;
    ">
  {{ category }}
</h3>

{% assign category_papers = site.data.publications_tag.main | where: "tag", category %}

{% for link in category_papers %}

<li style="
      margin-bottom: 45px;
      list-style-position: outside;
">

  <!-- ========================= -->

  <!-- Publication container -->

  <!-- ========================= -->

  <div style="
      width: 100%;
      max-width: 900px;
      margin: 0 auto;
  ">

```
<!-- ========================= -->
<!-- IMAGE AREA -->
<!-- ========================= -->

{% if link.image %}

<div style="
    width: 100%;
    height: 380px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    margin-bottom: 25px;
    overflow: hidden;
">

  <img src="{{ link.image }}"
       alt="{{ link.title }}"
       style="
          display: block;
          max-width: 100%;
          max-height: 100%;
          width: auto;
          height: auto;
          object-fit: contain;
          margin: 0 auto;
       ">

  {% if link.conference_short %}

  <abbr class="badge"
        style="
          position: absolute;
          top: 10px;
          left: 10px;
          z-index: 10;
        ">
    {{ link.conference_short }}
  </abbr>

  {% endif %}

</div>

{% endif %}


<!-- ========================= -->
<!-- TEXT AREA -->
<!-- ========================= -->

<div style="
    width: 100%;
    text-align: center;
    padding: 0 10px;
">


  <!-- Title -->

  <div class="title"
       style="
         margin-bottom: 8px;
         line-height: 1.4;
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

  <div class="author"
       style="
         margin-bottom: 6px;
         line-height: 1.5;
       ">
    {{ link.authors }}
  </div>


  <!-- Conference -->

  <div class="periodical"
       style="
         margin-bottom: 10px;
         line-height: 1.5;
       ">

    <em>
      {{ link.conference }}
    </em>

  </div>


  <!-- Links -->

  <div class="links">


    {% if link.pdf %}

    <a href="{{ link.pdf }}"
       class="btn btn-sm z-depth-0"
       role="button"
       target="_blank"
       style="font-size:12px;">
      PDF
    </a>

    {% endif %}


    {% if link.code %}

    <a href="{{ link.code }}"
       class="btn btn-sm z-depth-0"
       role="button"
       target="_blank"
       style="font-size:12px;">
      Code
    </a>

    {% endif %}


    {% if link.page %}

    <a href="{{ link.page }}"
       class="btn btn-sm z-depth-0"
       role="button"
       target="_blank"
       style="font-size:12px;">
      Project Page
    </a>

    {% endif %}


    {% if link.bibtex %}

    <a href="{{ link.bibtex }}"
       class="btn btn-sm z-depth-0"
       role="button"
       target="_blank"
       style="font-size:12px;">
      BibTex
    </a>

    {% endif %}


    {% if link.web %}

    <a href="{{ link.web }}"
       class="btn btn-sm z-depth-0"
       role="button"
       target="_blank"
       style="font-size:12px;">
      Website
    </a>

    {% endif %}


    {% if link.notes %}

    <strong>
      <i style="color:#e74d3c">
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

</li>

{% endfor %}

{% endfor %}
