<!-- ==================== Publications ==================== -->

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


<!-- ==================== Tag Navigation ==================== -->

<div style="
    margin: 20px 0 35px 0;
    text-align: left;
">

  <a href="#investment"
     style="
       display: inline-block;
       margin: 5px 6px 5px 0;
       padding: 7px 14px;
       border: 1px solid #ccc;
       border-radius: 16px;
       font-size: 13px;
       text-decoration: none;
     ">
    AI-driven investment
  </a>

  <a href="#multi-agent"
     style="
       display: inline-block;
       margin: 5px 6px 5px 0;
       padding: 7px 14px;
       border: 1px solid #ccc;
       border-radius: 16px;
       font-size: 13px;
       text-decoration: none;
     ">
    Multi-Agent Learning &amp; Reasoning
  </a>

  <a href="#representation"
     style="
       display: inline-block;
       margin: 5px 6px 5px 0;
       padding: 7px 14px;
       border: 1px solid #ccc;
       border-radius: 16px;
       font-size: 13px;
       text-decoration: none;
     ">
    Model Interpretation, Representation &amp; Evaluation
  </a>

  <a href="#compliance"
     style="
       display: inline-block;
       margin: 5px 6px 5px 0;
       padding: 7px 14px;
       border: 1px solid #ccc;
       border-radius: 16px;
       font-size: 13px;
       text-decoration: none;
     ">
    AI for regulatory compliance
  </a>

</div>


<!-- ==================== Notes ==================== -->

<div style="margin-bottom: 20px;">
  * means equal contribution.
  † means corresponding authors.
</div>


<!-- ========================================================= -->
<!-- AI-driven investment -->
<!-- ========================================================= -->

<h3 id="investment"
    style="
      margin-top: 40px;
      margin-bottom: 25px;
      padding-bottom: 8px;
      border-bottom: 2px solid #eaeaea;
    ">
  AI-driven investment
</h3>


{% assign category_papers = site.data.publications_tag.main
   | where: "tag", "AI-driven investment" %}

{% for link in category_papers %}

<li style="margin-bottom: 45px;">

  <div class="publication-entry">

    <!-- ================= IMAGE ================= -->

    {% if link.image %}

    <div style="
        width: 100%;
        height: 360px;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        margin: 0 auto 20px auto;
    ">

      <img src="{{ link.image }}"
           alt="{{ link.title }}"
           style="
             display: block;
             max-width: 100%;
             max-height: 340px;
             width: auto;
             height: auto;
             object-fit: contain;
           ">

    </div>

    {% endif %}


    <!-- ================= TEXT ================= -->

    <div style="
        width: 100%;
        text-align: center;
        padding: 0 15px;
    ">

      <!-- Conference -->
      {% if link.conference_short %}
      <div style="
          margin-bottom: 8px;
          font-size: 13px;
          font-weight: 600;
      ">
        {{ link.conference_short }}
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
           style="margin-bottom: 6px;">
        {{ link.authors }}
      </div>


      <!-- Conference / Journal -->
      <div class="periodical"
           style="margin-bottom: 10px;">
        <em>{{ link.conference }}</em>
      </div>


      <!-- Links -->
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
          <i style="color:#e74d3c;">
            {{ link.notes }}
          </i>
        </strong>
        {% endif %}

      </div>

    </div>

  </div>

</li>

{% endfor %}



<!-- ========================================================= -->
<!-- Multi-Agent Learning & Reasoning -->
<!-- ========================================================= -->

<h3 id="multi-agent"
    style="
      margin-top: 50px;
      margin-bottom: 25px;
      padding-bottom: 8px;
      border-bottom: 2px solid #eaeaea;
    ">
  Multi-Agent Learning &amp; Reasoning
</h3>


{% assign category_papers = site.data.publications_tag.main
   | where: "tag", "Multi-Agent Learning & Reasoning" %}

{% for link in category_papers %}

<li style="margin-bottom: 45px;">

  <div class="publication-entry">

    {% if link.image %}

    <div style="
        width: 100%;
        height: 360px;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        margin: 0 auto 20px auto;
    ">

      <img src="{{ link.image }}"
           alt="{{ link.title }}"
           style="
             display: block;
             max-width: 100%;
             max-height: 340px;
             width: auto;
             height: auto;
             object-fit: contain;
           ">

    </div>

    {% endif %}


    <div style="
        width: 100%;
        text-align: center;
        padding: 0 15px;
    ">

      {% if link.conference_short %}
      <div style="
          margin-bottom: 8px;
          font-size: 13px;
          font-weight: 600;
      ">
        {{ link.conference_short }}
      </div>
      {% endif %}


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


      <div class="author"
           style="margin-bottom: 6px;">
        {{ link.authors }}
      </div>


      <div class="periodical"
           style="margin-bottom: 10px;">
        <em>{{ link.conference }}</em>
      </div>


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
          <i style="color:#e74d3c;">
            {{ link.notes }}
          </i>
        </strong>
        {% endif %}

      </div>

    </div>

  </div>

</li>

{% endfor %}



<!-- ========================================================= -->
<!-- Model Interpretation, Representation & Evaluation -->
<!-- ========================================================= -->

<h3 id="representation"
    style="
      margin-top: 50px;
      margin-bottom: 25px;
      padding-bottom: 8px;
      border-bottom: 2px solid #eaeaea;
    ">
  Model Interpretation, Representation &amp; Evaluation
</h3>


{% assign category_papers = site.data.publications_tag.main
   | where: "tag", "Model Interpretation, Representation & Evaluation" %}

{% for link in category_papers %}

<li style="margin-bottom: 45px;">

  <div class="publication-entry">

    {% if link.image %}

    <div style="
        width: 100%;
        height: 360px;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        margin: 0 auto 20px auto;
    ">

      <img src="{{ link.image }}"
           alt="{{ link.title }}"
           style="
             display: block;
             max-width: 100%;
             max-height: 340px;
             width: auto;
             height: auto;
             object-fit: contain;
           ">

    </div>

    {% endif %}


    <div style="
        width: 100%;
        text-align: center;
        padding: 0 15px;
    ">

      {% if link.conference_short %}
      <div style="
          margin-bottom: 8px;
          font-size: 13px;
          font-weight: 600;
      ">
        {{ link.conference_short }}
      </div>
      {% endif %}


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


      <div class="author"
           style="margin-bottom: 6px;">
        {{ link.authors }}
      </div>


      <div class="periodical"
           style="margin-bottom: 10px;">
        <em>{{ link.conference }}</em>
      </div>


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
          <i style="color:#e74d3c;">
            {{ link.notes }}
          </i>
        </strong>
        {% endif %}

      </div>

    </div>

  </div>

</li>

{% endfor %}



<!-- ========================================================= -->
<!-- AI for regulatory compliance -->
<!-- ========================================================= -->

<h3 id="compliance"
    style="
      margin-top: 50px;
      margin-bottom: 25px;
      padding-bottom: 8px;
      border-bottom: 2px solid #eaeaea;
    ">
  AI for regulatory compliance
</h3>


{% assign category_papers = site.data.publications_tag.main
   | where: "tag", "AI for regulatory compliance" %}

{% for link in category_papers %}

<li style="margin-bottom: 45px;">

  <div class="publication-entry">

    {% if link.image %}

    <div style="
        width: 100%;
        height: 360px;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        margin: 0 auto 20px auto;
    ">

      <img src="{{ link.image }}"
           alt="{{ link.title }}"
           style="
             display: block;
             max-width: 100%;
             max-height: 340px;
             width: auto;
             height: auto;
             object-fit: contain;
           ">

    </div>

    {% endif %}


    <div style="
        width: 100%;
        text-align: center;
        padding: 0 15px;
    ">

      {% if link.conference_short %}
      <div style="
          margin-bottom: 8px;
          font-size: 13px;
          font-weight: 600;
      ">
        {{ link.conference_short }}
      </div>
      {% endif %}


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


      <div class="author"
           style="margin-bottom: 6px;">
        {{ link.authors }}
      </div>


      <div class="periodical"
           style="margin-bottom: 10px;">
        <em>{{ link.conference }}</em>
      </div>


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
          <i style="color:#e74d3c;">
            {{ link.notes }}
          </i>
        </strong>
        {% endif %}

      </div>

    </div>

  </div>

</li>

{% endfor %}
