<h2 id="publications">
  Publications
  <span style="font-size:15px;">
    [
    <a href="https://scholar.google.com/citations?user=lxrXMY0AAAAJ&hl=en&oi=ao"
       target="_blank">
      Google Scholar
    </a>
    ]
    [
    <a href="https://www.researchgate.net/profile/Zixuan-Yuan"
       target="_blank">
      ResearchGate
    </a>
    ]
  </span>
</h2>

<br>

<p>
  * means equal contribution.
  † means corresponding authors.
</p>


<!-- ===================================================== -->
<!-- TAG NAVIGATION                                        -->
<!-- ===================================================== -->

<div style="
    margin: 20px 0 35px 0;
    text-align: left;
">

  <a href="#tag-ai-investment"
     style="
       display: inline-block;
       margin: 4px 6px 4px 0;
       padding: 7px 14px;
       border: 1px solid #bbb;
       border-radius: 18px;
       font-size: 13px;
       text-decoration: none;
       color: inherit;
     ">
    AI-driven investment
  </a>

  <a href="#tag-multi-agent"
     style="
       display: inline-block;
       margin: 4px 6px 4px 0;
       padding: 7px 14px;
       border: 1px solid #bbb;
       border-radius: 18px;
       font-size: 13px;
       text-decoration: none;
       color: inherit;
     ">
    Multi-Agent Learning & Reasoning
  </a>

  <a href="#tag-model-interpretation"
     style="
       display: inline-block;
       margin: 4px 6px 4px 0;
       padding: 7px 14px;
       border: 1px solid #bbb;
       border-radius: 18px;
       font-size: 13px;
       text-decoration: none;
       color: inherit;
     ">
    Model Interpretation, Representation & Evaluation
  </a>

  <a href="#tag-regulatory"
     style="
       display: inline-block;
       margin: 4px 6px 4px 0;
       padding: 7px 14px;
       border: 1px solid #bbb;
       border-radius: 18px;
       font-size: 13px;
       text-decoration: none;
       color: inherit;
     ">
    AI for regulatory compliance
  </a>

</div>


<!-- ===================================================== -->
<!-- CATEGORY 1: AI-DRIVEN INVESTMENT                     -->
<!-- ===================================================== -->

<div id="tag-ai-investment"
     style="
       margin-top: 50px;
       margin-bottom: 30px;
       padding-bottom: 8px;
       border-bottom: 2px solid #ddd;
     ">

  <h3 style="margin: 0;">
    AI-driven investment
  </h3>

</div>


{% assign category = "AI-driven investment" %}

{% assign category_papers = site.data.publications_tag.main
     | where: "tag", category %}


<div class="publications">

<ol>

{% for link in category_papers %}

<li style="
    margin-bottom: 55px;
    padding-bottom: 20px;
">


  <!-- ================= IMAGE ================= -->

  {% if link.image %}

  <div style="
      width: 100%;
      max-width: 900px;
      margin: 0 auto 25px auto;
      text-align: center;
      line-height: 0;
  ">

    <img src="{{ link.image }}"
         alt="{{ link.title }}"
         style="
           display: inline-block;
           width: auto;
           height: auto;
           max-width: 100%;
           max-height: 500px;
           object-fit: contain;
         ">

  </div>

  {% endif %}


  <!-- ================= PAPER INFORMATION ================= -->

  <div style="
      width: 100%;
      text-align: center;
      padding: 0 15px;
      box-sizing: border-box;
  ">


    <!-- Conference -->

    {% if link.conference_short %}

    <div style="margin-bottom: 10px;">

      <abbr class="badge">
        {{ link.conference_short }}
      </abbr>

    </div>

    {% endif %}


    <!-- Title -->

    <div class="title"
         style="margin-bottom: 8px;">

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
         style="margin-bottom: 8px;">

      {{ link.authors }}

    </div>


    <!-- Conference -->

    {% if link.conference %}

    <div class="periodical"
         style="margin-bottom: 10px;">

      <em>
        {{ link.conference }}
      </em>

    </div>

    {% endif %}


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
        <i style="
          color:#e74d3c;
          margin-left:8px;
        ">
          {{ link.notes }}
        </i>
      </strong>

      {% endif %}


      {% if link.others %}

        {{ link.others }}

      {% endif %}

    </div>

  </div>

</li>

{% endfor %}

</ol>

</div>



<!-- ===================================================== -->
<!-- CATEGORY 2: MULTI-AGENT LEARNING & REASONING        -->
<!-- ===================================================== -->

<div id="tag-multi-agent"
     style="
       margin-top: 60px;
       margin-bottom: 30px;
       padding-bottom: 8px;
       border-bottom: 2px solid #ddd;
     ">

  <h3 style="margin: 0;">
    Multi-Agent Learning & Reasoning
  </h3>

</div>


{% assign category = "Multi-Agent Learning & Reasoning" %}

{% assign category_papers = site.data.publications_tag.main
     | where: "tag", category %}


<div class="publications">

<ol>

{% for link in category_papers %}

<li style="
    margin-bottom: 55px;
    padding-bottom: 20px;
">


  {% if link.image %}

  <div style="
      width: 100%;
      max-width: 900px;
      margin: 0 auto 25px auto;
      text-align: center;
      line-height: 0;
  ">

    <img src="{{ link.image }}"
         alt="{{ link.title }}"
         style="
           display: inline-block;
           width: auto;
           height: auto;
           max-width: 100%;
           max-height: 500px;
           object-fit: contain;
         ">

  </div>

  {% endif %}


  <div style="
      width: 100%;
      text-align: center;
      padding: 0 15px;
      box-sizing: border-box;
  ">

    {% if link.conference_short %}

    <div style="margin-bottom: 10px;">
      <abbr class="badge">
        {{ link.conference_short }}
      </abbr>
    </div>

    {% endif %}


    <div class="title" style="margin-bottom: 8px;">

      {% if link.pdf %}

      <a href="{{ link.pdf }}" target="_blank">
        {{ link.title }}
      </a>

      {% else %}

        {{ link.title }}

      {% endif %}

    </div>


    <div class="author" style="margin-bottom: 8px;">
      {{ link.authors }}
    </div>


    {% if link.conference %}

    <div class="periodical" style="margin-bottom: 10px;">
      <em>{{ link.conference }}</em>
    </div>

    {% endif %}


    <div class="links">

      {% if link.pdf %}
      <a href="{{ link.pdf }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        PDF
      </a>
      {% endif %}

      {% if link.code %}
      <a href="{{ link.code }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        Code
      </a>
      {% endif %}

      {% if link.page %}
      <a href="{{ link.page }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        Project Page
      </a>
      {% endif %}

      {% if link.bibtex %}
      <a href="{{ link.bibtex }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        BibTex
      </a>
      {% endif %}

      {% if link.web %}
      <a href="{{ link.web }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        Website
      </a>
      {% endif %}

      {% if link.notes %}
      <strong>
        <i style="color:#e74d3c; margin-left:8px;">
          {{ link.notes }}
        </i>
      </strong>
      {% endif %}

    </div>

  </div>

</li>

{% endfor %}

</ol>

</div>



<!-- ===================================================== -->
<!-- CATEGORY 3: MODEL INTERPRETATION                      -->
<!-- ===================================================== -->

<div id="tag-model-interpretation"
     style="
       margin-top: 60px;
       margin-bottom: 30px;
       padding-bottom: 8px;
       border-bottom: 2px solid #ddd;
     ">

  <h3 style="margin: 0;">
    Model Interpretation, Representation & Evaluation
  </h3>

</div>


{% assign category = "Model Interpretation, Representation & Evaluation" %}

{% assign category_papers = site.data.publications_tag.main
     | where: "tag", category %}


<div class="publications">

<ol>

{% for link in category_papers %}

<li style="
    margin-bottom: 55px;
    padding-bottom: 20px;
">


  {% if link.image %}

  <div style="
      width: 100%;
      max-width: 900px;
      margin: 0 auto 25px auto;
      text-align: center;
      line-height: 0;
  ">

    <img src="{{ link.image }}"
         alt="{{ link.title }}"
         style="
           display: inline-block;
           width: auto;
           height: auto;
           max-width: 100%;
           max-height: 500px;
           object-fit: contain;
         ">

  </div>

  {% endif %}


  <div style="
      width: 100%;
      text-align: center;
      padding: 0 15px;
      box-sizing: border-box;
  ">

    {% if link.conference_short %}

    <div style="margin-bottom: 10px;">
      <abbr class="badge">
        {{ link.conference_short }}
      </abbr>
    </div>

    {% endif %}


    <div class="title" style="margin-bottom: 8px;">

      {% if link.pdf %}

      <a href="{{ link.pdf }}" target="_blank">
        {{ link.title }}
      </a>

      {% else %}

        {{ link.title }}

      {% endif %}

    </div>


    <div class="author" style="margin-bottom: 8px;">
      {{ link.authors }}
    </div>


    {% if link.conference %}

    <div class="periodical" style="margin-bottom: 10px;">
      <em>{{ link.conference }}</em>
    </div>

    {% endif %}


    <div class="links">

      {% if link.pdf %}
      <a href="{{ link.pdf }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        PDF
      </a>
      {% endif %}

      {% if link.code %}
      <a href="{{ link.code }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        Code
      </a>
      {% endif %}

      {% if link.page %}
      <a href="{{ link.page }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        Project Page
      </a>
      {% endif %}

      {% if link.bibtex %}
      <a href="{{ link.bibtex }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        BibTex
      </a>
      {% endif %}

      {% if link.web %}
      <a href="{{ link.web }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        Website
      </a>
      {% endif %}

      {% if link.notes %}
      <strong>
        <i style="color:#e74d3c; margin-left:8px;">
          {{ link.notes }}
        </i>
      </strong>
      {% endif %}

    </div>

  </div>

</li>

{% endfor %}

</ol>

</div>



<!-- ===================================================== -->
<!-- CATEGORY 4: AI FOR REGULATORY COMPLIANCE             -->
<!-- ===================================================== -->

<div id="tag-regulatory"
     style="
       margin-top: 60px;
       margin-bottom: 30px;
       padding-bottom: 8px;
       border-bottom: 2px solid #ddd;
     ">

  <h3 style="margin: 0;">
    AI for regulatory compliance
  </h3>

</div>


{% assign category = "AI for regulatory compliance" %}

{% assign category_papers = site.data.publications_tag.main
     | where: "tag", category %}


<div class="publications">

<ol>

{% for link in category_papers %}

<li style="
    margin-bottom: 55px;
    padding-bottom: 20px;
">


  {% if link.image %}

  <div style="
      width: 100%;
      max-width: 900px;
      margin: 0 auto 25px auto;
      text-align: center;
      line-height: 0;
  ">

    <img src="{{ link.image }}"
         alt="{{ link.title }}"
         style="
           display: inline-block;
           width: auto;
           height: auto;
           max-width: 100%;
           max-height: 500px;
           object-fit: contain;
         ">

  </div>

  {% endif %}


  <div style="
      width: 100%;
      text-align: center;
      padding: 0 15px;
      box-sizing: border-box;
  ">

    {% if link.conference_short %}

    <div style="margin-bottom: 10px;">
      <abbr class="badge">
        {{ link.conference_short }}
      </abbr>
    </div>

    {% endif %}


    <div class="title" style="margin-bottom: 8px;">

      {% if link.pdf %}

      <a href="{{ link.pdf }}" target="_blank">
        {{ link.title }}
      </a>

      {% else %}

        {{ link.title }}

      {% endif %}

    </div>


    <div class="author" style="margin-bottom: 8px;">
      {{ link.authors }}
    </div>


    {% if link.conference %}

    <div class="periodical" style="margin-bottom: 10px;">
      <em>{{ link.conference }}</em>
    </div>

    {% endif %}


    <div class="links">

      {% if link.pdf %}
      <a href="{{ link.pdf }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        PDF
      </a>
      {% endif %}

      {% if link.code %}
      <a href="{{ link.code }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        Code
      </a>
      {% endif %}

      {% if link.page %}
      <a href="{{ link.page }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        Project Page
      </a>
      {% endif %}

      {% if link.bibtex %}
      <a href="{{ link.bibtex }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        BibTex
      </a>
      {% endif %}

      {% if link.web %}
      <a href="{{ link.web }}"
         class="btn btn-sm z-depth-0"
         target="_blank"
         style="font-size:12px;">
        Website
      </a>
      {% endif %}

      {% if link.notes %}
      <strong>
        <i style="color:#e74d3c; margin-left:8px;">
          {{ link.notes }}
        </i>
      </strong>
      {% endif %}

    </div>

  </div>

</li>

{% endfor %}

</ol>

</div>
