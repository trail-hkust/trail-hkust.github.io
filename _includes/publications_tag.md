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

* means equal contribution.<br>
† means corresponding authors.

<div class="publications">

{% assign categories = "AI-driven investment|Multi-Agent Learning & Reasoning|Model Interpretation, Representation & Evaluation|AI for regulatory compliance" | split: "|" %}

{% for category in categories %}

  <!-- Category title -->
  <h3 class="publication-category">
    {{ category }}
  </h3>

  <!-- Get publications belonging to this category -->
  {% assign category_papers = site.data.publications_tag.main | where: "tag", category %}

  <ol class="bibliography">

  {% for link in category_papers %}

    <li>
      <div class="publication-entry">

        <!-- Image -->
        <div class="col-sm-12 abbr"
             style="position: relative; text-align: center; padding: 15px;">

          {% if link.image %}
          <img src="{{ link.image }}"
               class="teaser img-fluid z-depth-1"
               style="display: block;
                      max-width: 90%;
                      max-height: 320px;
                      width: auto;
                      height: auto;
                      object-fit: contain;
                      margin: 0 auto 20px auto;">
          {% endif %}

          <!-- Conference badge -->
          {% if link.conference_short %}
          <abbr class="badge"
                style="position: absolute;
                       top: 10px;
                       left: 10px;">
            {{ link.conference_short }}
          </abbr>
          {% endif %}

        </div>


        <!-- Publication information -->
        <div class="col-sm-12"
             style="padding: 15px;
                    text-align: center;
                    margin-top: 15px;">

          <!-- Title -->
          <div class="title">
            {% if link.pdf %}
              <a href="{{ link.pdf }}">
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

      </div>
    </li>

    <br>

  {% endfor %}

  </ol>

{% endfor %}

</div>
