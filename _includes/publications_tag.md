<h1 id="publications"></h1>

<h2 style="margin: 30px 0px -15px;">
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

* means equal contribution.  
† means corresponding authors.

<!-- ========================================================= -->
<!-- Topics navigation -->
<!-- ========================================================= -->

<div style="
    margin: 20px 0 30px 0;
    font-size: 15px;
    line-height: 1.8;
">

  <span style="
      color: #555;
      margin-right: 8px;
  ">
    Topics:
  </span>

  <a href="#topic-ai-investment"
     style="
        color: #333 !important;
        text-decoration: none;
        margin-right: 18px;
     ">
    AI-driven investment
  </a>

  <a href="#topic-multi-agent"
     style="
        color: #333 !important;
        text-decoration: none;
        margin-right: 18px;
     ">
    Multi-Agent Learning &amp; Reasoning
  </a>

  <a href="#topic-interpretation"
     style="
        color: #333 !important;
        text-decoration: none;
        margin-right: 18px;
     ">
    Model Interpretation, Representation &amp; Evaluation
  </a>

  <a href="#topic-compliance"
     style="
        color: #333 !important;
        text-decoration: none;
        margin-right: 18px;
     ">
    AI for regulatory compliance
  </a>

</div>


<div class="publications">

<!-- ========================================================= -->
<!-- 1. AI-driven investment -->
<!-- ========================================================= -->

<div id="topic-ai-investment"
     style="scroll-margin-top: 80px;">

  <h3 style="
      margin-top: 35px;
      margin-bottom: 25px;
  ">
    AI-driven investment
  </h3>

  {% assign category_papers = site.data.publications_tag.main
     | where: "tag", "AI-driven investment" %}

  <ol class="bibliography">

  {% for link in category_papers %}

    <li>

      <div class="publication-entry">

        <!-- ================= IMAGE ================= -->

        {% if link.image %}

        <div style="
            width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 auto 10px auto;
            padding: 10px;
            box-sizing: border-box;
        ">

          <img src="{{ link.image }}"
               class="teaser img-fluid z-depth-1"
               style="
                  display: block;
                  width: auto !important;
                  height: auto !important;
                  max-width: 100% !important;
                  max-height: 400px !important;
                  object-fit: contain;
                  margin: 0 auto;
               ">

        </div>

        {% endif %}


        <!-- ================= CONFERENCE ================= -->

        {% if link.conference_short %}

        <div style="
            text-align: center;
            margin: 5px 0 12px 0;
            font-size: 14px;
            font-weight: 600;
            color: #333 !important;
            background: transparent;
        ">
          {{ link.conference_short }}
        </div>

        {% endif %}


        <!-- ================= INFORMATION ================= -->

        <div style="
            padding: 0 15px 15px 15px;
            text-align: center;
        ">

          <!-- Title -->

          <div class="title">

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

          <div class="author">
            {{ link.authors }}
          </div>


          <!-- Conference / Journal -->

          <div class="periodical">
            <em>{{ link.conference }}</em>
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

    <br>

  {% endfor %}

  </ol>

</div>


<!-- ========================================================= -->
<!-- 2. Multi-Agent Learning & Reasoning -->
<!-- ========================================================= -->

<div id="topic-multi-agent"
     style="scroll-margin-top: 80px;">

  <h3 style="
      margin-top: 35px;
      margin-bottom: 25px;
  ">
    Multi-Agent Learning &amp; Reasoning
  </h3>

  {% assign category_papers = site.data.publications_tag.main
     | where: "tag", "Multi-Agent Learning & Reasoning" %}

  <ol class="bibliography">

  {% for link in category_papers %}

    <li>

      <div class="publication-entry">

        {% if link.image %}

        <div style="
            width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 auto 10px auto;
            padding: 10px;
            box-sizing: border-box;
        ">

          <img src="{{ link.image }}"
               class="teaser img-fluid z-depth-1"
               style="
                  display: block;
                  width: auto !important;
                  height: auto !important;
                  max-width: 100% !important;
                  max-height: 400px !important;
                  object-fit: contain;
                  margin: 0 auto;
               ">

        </div>

        {% endif %}


        {% if link.conference_short %}

        <div style="
            text-align: center;
            margin: 5px 0 12px 0;
            font-size: 14px;
            font-weight: 600;
            color: #333 !important;
            background: transparent;
        ">
          {{ link.conference_short }}
        </div>

        {% endif %}


        <div style="
            padding: 0 15px 15px 15px;
            text-align: center;
        ">

          <div class="title">

            {% if link.pdf %}

            <a href="{{ link.pdf }}"
               target="_blank">
              {{ link.title }}
            </a>

            {% else %}

              {{ link.title }}

            {% endif %}

          </div>


          <div class="author">
            {{ link.authors }}
          </div>


          <div class="periodical">
            <em>{{ link.conference }}</em>
          </div>


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

    <br>

  {% endfor %}

  </ol>

</div>


<!-- ========================================================= -->
<!-- 3. Model Interpretation, Representation & Evaluation -->
<!-- ========================================================= -->

<div id="topic-interpretation"
     style="scroll-margin-top: 80px;">

  <h3 style="
      margin-top: 35px;
      margin-bottom: 25px;
  ">
    Model Interpretation, Representation &amp; Evaluation
  </h3>

  {% assign category_papers = site.data.publications_tag.main
     | where: "tag", "Model Interpretation, Representation & Evaluation" %}

  <ol class="bibliography">

  {% for link in category_papers %}

    <li>

      <div class="publication-entry">

        {% if link.image %}

        <div style="
            width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 auto 10px auto;
            padding: 10px;
            box-sizing: border-box;
        ">

          <img src="{{ link.image }}"
               class="teaser img-fluid z-depth-1"
               style="
                  display: block;
                  width: auto !important;
                  height: auto !important;
                  max-width: 100% !important;
                  max-height: 400px !important;
                  object-fit: contain;
                  margin: 0 auto;
               ">

        </div>

        {% endif %}


        {% if link.conference_short %}

        <div style="
            text-align: center;
            margin: 5px 0 12px 0;
            font-size: 14px;
            font-weight: 600;
            color: #333 !important;
            background: transparent;
        ">
          {{ link.conference_short }}
        </div>

        {% endif %}


        <div style="
            padding: 0 15px 15px 15px;
            text-align: center;
        ">

          <div class="title">

            {% if link.pdf %}

            <a href="{{ link.pdf }}"
               target="_blank">
              {{ link.title }}
            </a>

            {% else %}

              {{ link.title }}

            {% endif %}

          </div>


          <div class="author">
            {{ link.authors }}
          </div>


          <div class="periodical">
            <em>{{ link.conference }}</em>
          </div>


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

    <br>

  {% endfor %}

  </ol>

</div>


<!-- ========================================================= -->
<!-- 4. AI for regulatory compliance -->
<!-- ========================================================= -->

<div id="topic-compliance"
     style="scroll-margin-top: 80px;">

  <h3 style="
      margin-top: 35px;
      margin-bottom: 25px;
  ">
    AI for regulatory compliance
  </h3>

  {% assign category_papers = site.data.publications_tag.main
     | where: "tag", "AI for regulatory compliance" %}

  <ol class="bibliography">

  {% for link in category_papers %}

    <li>

      <div class="publication-entry">

        {% if link.image %}

        <div style="
            width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 auto 10px auto;
            padding: 10px;
            box-sizing: border-box;
        ">

          <img src="{{ link.image }}"
               class="teaser img-fluid z-depth-1"
               style="
                  display: block;
                  width: auto !important;
                  height: auto !important;
                  max-width: 100% !important;
                  max-height: 400px !important;
                  object-fit: contain;
                  margin: 0 auto;
               ">

        </div>

        {% endif %}


        {% if link.conference_short %}

        <div style="
            text-align: center;
            margin: 5px 0 12px 0;
            font-size: 14px;
            font-weight: 600;
            color: #333 !important;
            background: transparent;
        ">
          {{ link.conference_short }}
        </div>

        {% endif %}


        <div style="
            padding: 0 15px 15px 15px;
            text-align: center;
        ">

          <div class="title">

            {% if link.pdf %}

            <a href="{{ link.pdf }}"
               target="_blank">
              {{ link.title }}
            </a>

            {% else %}

              {{ link.title }}

            {% endif %}

          </div>


          <div class="author">
            {{ link.authors }}
          </div>


          <div class="periodical">
            <em>{{ link.conference }}</em>
          </div>


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

    <br>

  {% endfor %}

  </ol>

</div>

</div>
