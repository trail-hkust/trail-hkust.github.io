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
<!-- Topics -->
<!-- ========================================================= -->

<div style="
    margin: 10px 0 30px 0;
    font-size: 15px;
    line-height: 1.8;
">

  <strong style="font-weight: 600;">Topics:</strong>

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
      <span style="color:#aaa;"> | </span>
    {% endunless %}

  {% endfor %}

</div>


- means equal contribution.
† means corresponding authors.


<!-- ========================================================= -->
<!-- Publications by Topic -->
<!-- ========================================================= -->

{% assign categories =
  "AI-driven investment|Multi-Agent Learning & Reasoning|Model Interpretation, Representation & Evaluation|AI for regulatory compliance"
  | split: "|"
%}


{% for category in categories %}

  <!-- ======================================================= -->
  <!-- Topic Header -->
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
  <!-- Get papers belonging to this topic -->
  <!-- ======================================================= -->

  {% assign category_papers =
    site.data.publications_tag.main
    | where: "tag", category
  %}


  <ol class="bibliography">

  {% for link in category_papers %}

    <li style="margin-bottom: 45px;">

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
            height: 360px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            margin-bottom: 20px;
        ">

          <img src="{{ link.image }}"
               class="teaser img-fluid z-depth-1"
               style="
                 display: block;
                 max-width: 100%;
                 max-height: 360px;
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
                 margin-bottom: 6px;
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
          <!-- Links -->
          <!-- =============================================== -->

          <div class="links"
               style="
                 margin-top: 8px;
                 line-height: 2;
               ">


            {% if link.pdf %}

            <a href="{{ link.pdf }}"
               class="btn btn-sm z-depth-0"
               role="button"
               target="_blank"
               style="font-size:12px;">
              PDF
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


            {% if link.notes %}

            <strong style="margin-left: 5px;">
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

    </li>

  {% endfor %}

  </ol>

{% endfor %}
