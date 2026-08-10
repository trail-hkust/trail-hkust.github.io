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


<!-- ========================================================= -->
<!-- Contribution Notes -->
<!-- ========================================================= -->

<div style="margin-bottom: 15px;">
  * means equal contribution.<br>
  † means corresponding authors.
</div>


<!-- ========================================================= -->
<!-- Topics Navigation -->
<!-- ========================================================= -->

<div style="
    margin: 20px 0 35px 0;
    font-size: 15px;
    line-height: 1.8;
">

  <strong style="font-weight: 600;">Topics:</strong>

  {% assign categories =
    "AI-driven Investment|Multi-Agent Learning & Reasoning|Model Interpretation, Representation & Evaluation|AI for Regulatory Compliance"
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
      <span style="color:#aaa;"> | </span>
    {% endunless %}

  {% endfor %}

</div>


<!-- ========================================================= -->
<!-- Category List -->
<!-- ========================================================= -->

{% assign categories =
  "AI-driven Investment|Multi-Agent Learning & Reasoning|Model Interpretation, Representation & Evaluation|AI for Regulatory Compliance"
  | split: "|"
%}


{% for category in categories %}

  <!-- ======================================================= -->
  <!-- Category Title -->
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
  <!-- Publications under this category -->
  <!-- ======================================================= -->

  {% assign category_papers =
    site.data.publications_tag.main
    | where: "tag", category
  %}


  <ol class="bibliography">


  {% for link in category_papers %}

    <li style="
          margin-bottom: 50px;
          list-style-position: outside;
        ">


      <div class="publication-entry"
           style="
             width: 100%;
             overflow: hidden;
           ">


        <!-- ================================================= -->
        <!-- Image -->
        <!-- ================================================= -->

        {% if link.image %}

        <div style="
            width: 100%;
            min-height: 300px;
            max-height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            margin: 0 auto 25px auto;
        ">

          <img src="{{ link.image }}"
               class="teaser img-fluid z-depth-1"
               style="
                 display: block;
                 max-width: 100%;
                 max-height: 400px;
                 width: auto;
                 height: auto;
                 object-fit: contain;
                 margin: 0 auto;
               ">

        </div>

        {% endif %}


        <!-- ================================================= -->
        <!-- Publication Information -->
        <!-- ================================================= -->

        <div style="
            width: 100%;
            padding: 0 10px;
            text-align: center;
        ">


          <!-- =============================================== -->
          <!-- Title -->
          <!-- =============================================== -->

          <div class="title"
               style="
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


          <!-- =============================================== -->
          <!-- Authors -->
          <!-- =============================================== -->

          <div class="author"
               style="
                 margin-bottom: 7px;
                 line-height: 1.5;
               ">

            {{ link.authors }}

          </div>


          <!-- =============================================== -->
          <!-- Conference -->
          <!-- =============================================== -->

          {% if link.conference %}

          <div class="periodical"
               style="
                 margin-bottom: 10px;
                 line-height: 1.5;
               ">

            <em>{{ link.conference }}</em>

          </div>

          {% endif %}


          <!-- =============================================== -->
          <!-- Publication Links -->
          <!-- =============================================== -->

          <div class="links"
               style="
                 margin-top: 10px;
                 line-height: 2;
               ">


            <!-- PDF -->

            {% if link.pdf %}

            <a href="{{ link.pdf }}"
               target="_blank"
               style="
                 display: inline-block;
                 padding: 3px 9px;
                 margin: 2px 3px;
                 border: 1px solid #bbb;
                 border-radius: 3px;
                 font-size: 12px;
                 text-decoration: none;
                 color: #555;
                 background: #fff;
               ">
              PDF
            </a>

            {% endif %}


            <!-- Website -->

            {% if link.web %}

            <a href="{{ link.web }}"
               target="_blank"
               style="
                 display: inline-block;
                 padding: 3px 9px;
                 margin: 2px 3px;
                 border: 1px solid #bbb;
                 border-radius: 3px;
                 font-size: 12px;
                 text-decoration: none;
                 color: #555;
                 background: #fff;
               ">
              Website
            </a>

            {% endif %}


            <!-- Code -->

            {% if link.code %}

            <a href="{{ link.code }}"
               target="_blank"
               style="
                 display: inline-block;
                 padding: 3px 9px;
                 margin: 2px 3px;
                 border: 1px solid #bbb;
                 border-radius: 3px;
                 font-size: 12px;
                 text-decoration: none;
                 color: #555;
                 background: #fff;
               ">
              Code
            </a>

            {% endif %}


            <!-- Project Page -->

            {% if link.page %}

            <a href="{{ link.page }}"
               target="_blank"
               style="
                 display: inline-block;
                 padding: 3px 9px;
                 margin: 2px 3px;
                 border: 1px solid #bbb;
                 border-radius: 3px;
                 font-size: 12px;
                 text-decoration: none;
                 color: #555;
                 background: #fff;
               ">
              Project Page
            </a>

            {% endif %}


            <!-- BibTex -->

            {% if link.bibtex %}

            <a href="{{ link.bibtex }}"
               target="_blank"
               style="
                 display: inline-block;
                 padding: 3px 9px;
                 margin: 2px 3px;
                 border: 1px solid #bbb;
                 border-radius: 3px;
                 font-size: 12px;
                 text-decoration: none;
                 color: #555;
                 background: #fff;
               ">
              BibTex
            </a>

            {% endif %}


            <!-- Notes -->

            {% if link.notes %}

            <strong style="
                margin-left: 5px;
              ">

              <i style="
                  color:#e74d3c;
                ">
                {{ link.notes }}
              </i>

            </strong>

            {% endif %}


            <!-- Other Links -->

            {% if link.others %}

              {{ link.others }}

            {% endif %}


          </div>


        </div>

      </div>

    </li>

  {% endfor %}

  </ol>

{% endfor %}
