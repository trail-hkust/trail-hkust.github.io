```liquid
<h1 id="publications"></h1>

<h2 style="margin: 30px 0px -15px;">
  Publications
  <span style="font-size:15px;">
    [
    <a href="https://scholar.google.com/citations?user=lxrXMY0AAAAJ&hl=en&oi=ao"
       target="_blank"
       style="font-size:15px;">
      Google Scholar
    </a>
    ]
  </span>

  <span style="font-size:15px;">
    [
    <a href="https://www.researchgate.net/profile/Zixuan-Yuan"
       target="_blank"
       style="font-size:15px;">
      ResearchGate
    </a>
    ]
  </span>
</h2>

<br>


<!-- ========================================================= -->
<!-- Topics navigation -->
<!-- ========================================================= -->

<div style="
    margin: 10px 0 30px 0;
    font-size: 15px;
    line-height: 1.8;
">

  <strong>Topics:</strong>

  {% assign categories =
    "AI-driven investment|Multi-Agent Learning & Reasoning|Model Interpretation, Representation & Evaluation|AI for regulatory compliance"
    | split: "|"
  %}

  {% for category in categories %}

    <a href="#topic-{{ category | slugify }}"
       style="
         margin-left: 12px;
         text-decoration: none;
         color: #555;
       ">
      {{ category }}
    </a>

    {% unless forloop.last %}
      <span style="color:#aaa;">|</span>
    {% endunless %}

  {% endfor %}

</div>


<!-- ========================================================= -->
<!-- Notes -->
<!-- ========================================================= -->

<div style="
    margin-bottom: 25px;
    font-size: 14px;
">

  * means equal contribution.
  † means corresponding authors.

</div>


<!-- ========================================================= -->
<!-- Publications -->
<!-- ========================================================= -->

{% for category in categories %}

  {% assign category_papers =
      site.data.publications_tag.main
      | where: "tag", category
  %}


  <!-- ======================================================= -->
  <!-- Topic heading -->
  <!-- ======================================================= -->

  <h3 id="topic-{{ category | slugify }}"
      style="
        margin-top: 45px;
        margin-bottom: 25px;
        padding-bottom: 8px;
        border-bottom: 1px solid #ddd;
        font-weight: 600;
      ">

    {{ category }}

  </h3>


  <!-- ======================================================= -->
  <!-- Papers under this topic -->
  <!-- ======================================================= -->

  {% for link in category_papers %}

  <li style="
      list-style: none;
      margin-bottom: 55px;
  ">

    <div class="publication-entry"
         style="
           width: 100%;
           overflow: visible;
         ">


      <!-- =================================================== -->
      <!-- IMAGE -->
      <!-- =================================================== -->

      {% if link.image %}

      <div style="
          width: 100%;
          text-align: center;
          margin: 0 auto 18px auto;
          overflow: visible;
      ">

        <img src="{{ link.image }}"
             alt="{{ link.title }}"
             style="
               display: block;
               width: auto;
               height: auto;
               max-width: 100%;
               max-height: 500px;
               object-fit: contain;
               margin: 0 auto;
             ">

      </div>

      {% endif %}


      <!-- =================================================== -->
      <!-- CONFERENCE + LINKS -->
      <!-- =================================================== -->

      <div style="
          text-align: center;
          margin: 5px 0 12px 0;
          font-size: 13px;
          line-height: 1.6;
      ">


        <!-- Conference short -->

        {% if link.conference_short %}

        <span style="
            color: #666;
            margin-right: 12px;
            font-weight: 500;
        ">
          {{ link.conference_short }}
        </span>

        {% endif %}


        <!-- PDF -->

        {% if link.pdf %}

        <a href="{{ link.pdf }}"
           target="_blank"
           style="
             margin-right: 10px;
             text-decoration: none;
           ">
          PDF
        </a>

        {% endif %}


        <!-- Website -->

        {% if link.web %}

        <a href="{{ link.web }}"
           target="_blank"
           style="
             margin-right: 10px;
             text-decoration: none;
           ">
          Website
        </a>

        {% endif %}


        <!-- Code -->

        {% if link.code %}

        <a href="{{ link.code }}"
           target="_blank"
           style="
             margin-right: 10px;
             text-decoration: none;
           ">
          Code
        </a>

        {% endif %}


        <!-- Project Page -->

        {% if link.page %}

        <a href="{{ link.page }}"
           target="_blank"
           style="
             margin-right: 10px;
             text-decoration: none;
           ">
          Project Page
        </a>

        {% endif %}


        <!-- BibTeX -->

        {% if link.bibtex %}

        <a href="{{ link.bibtex }}"
           target="_blank"
           style="
             margin-right: 10px;
             text-decoration: none;
           ">
          BibTeX
        </a>

        {% endif %}


        <!-- Notes -->

        {% if link.notes %}

        <span style="
            color: #e74d3c;
            margin-left: 3px;
        ">
          {{ link.notes }}
        </span>

        {% endif %}


        <!-- Others -->

        {% if link.others %}

          {{ link.others }}

        {% endif %}


      </div>


      <!-- =================================================== -->
      <!-- PUBLICATION INFORMATION -->
      <!-- =================================================== -->

      <div style="
          width: 100%;
          text-align: center;
          padding: 0 15px;
          box-sizing: border-box;
      ">


        <!-- Title -->

        <div class="title"
             style="
               margin-top: 5px;
               margin-bottom: 8px;
               line-height: 1.5;
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
               margin-bottom: 7px;
               line-height: 1.5;
             ">

          {{ link.authors }}

        </div>


        <!-- Conference / Journal -->

        <div class="periodical"
             style="
               margin-bottom: 10px;
               line-height: 1.5;
             ">

          <em>
            {{ link.conference }}
          </em>

        </div>


      </div>

    </div>

  </li>

  {% endfor %}

{% endfor %}
```
