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

  <!-- ============================= -->
  <!-- Category -->
  <!-- ============================= -->

  <h3 class="publication-category">
    {{ category }}
  </h3>

  {% assign category_papers = site.data.publications.main | where: "tag", category %}

  {% if category_papers.size > 0 %}

  <ol class="bibliography">

    {% for link in category_papers %}

    <li>

      <div class="publication-entry">

        <!-- ============================= -->
        <!-- Image -->
        <!-- ============================= -->

        <div class="col-sm-12 abbr"
             style="position: relative; text-align: center; padding: 15px;">

          {% if link.image %}
            <img src="{{ link.image }}"
                 class="teaser img-fluid z-depth-1"
                 style="width: 100%;
                        max-width: 800px;
                        height: auto;
                        object-fit: contain;
                        margin-bottom: 20px;">

          {% elsif link.image1 %}
            <img src="{{ link.image1 }}"
                 class="teaser img-fluid z-depth-1"
                 style="width: 100%;
                        max-width: 800px;
                        height: auto;
                        object-fit: contain;
                        margin-bottom: 20px;">

          {% elsif link.image2 %}
            <img src="{{ link.image2 }}"
                 class="teaser img-fluid z-depth-1"
                 style="width: 100%;
                        max-width: 800px;
                        height: auto;
                        object-fit: contain;
                        margin-bottom: 20px;">
          {% endif %}

          <!-- Conference badge -->

          {% if link.conference_short %}
            <abbr class="badge"
                  style="position: absolute; top: 10px; left: 10px;">
              {{ link.conference_short }}
            </abbr>

          {% elsif link.conference_short1 %}
            <abbr class="badge"
                  style="position: absolute; top: 10px; left: 10px;">
              {{ link.conference_short1 }}
            </abbr>

          {% elsif link.conference_short2 %}
            <abbr class="badge"
                  style="position: absolute; top: 10px; left: 10px;">
              {{ link.conference_short2 }}
            </abbr>
          {% endif %}

        </div>


        <!-- ============================= -->
        <!-- Information -->
        <!-- ============================= -->

        <div class="col-sm-12"
             style="padding: 15px;
                    text-align: center;
                    margin-top: 15px;">

          <!-- Title -->

          <div class="title">

            {% if link.title %}

              {% if link.pdf %}
                <a href="{{ link.pdf }}">{{ link.title }}</a>
              {% else %}
                {{ link.title }}
              {% endif %}

            {% elsif link.title1 %}

              {% if link.pdf1 %}
                <a href="{{ link.pdf1 }}">{{ link.title1 }}</a>
              {% else %}
                {{ link.title1 }}
              {% endif %}

            {% elsif link.title2 %}

              {% if link.pdf2 %}
                <a href="{{ link.pdf2 }}">{{ link.title2 }}</a>
              {% else %}
                {{ link.title2 }}
              {% endif %}

            {% endif %}

          </div>


          <!-- Authors -->

          <div class="author">

            {% if link.authors %}
              {{ link.authors }}

            {% elsif link.authors1 %}
              {{ link.authors1 }}

            {% elsif link.authors2 %}
              {{ link.authors2 }}
            {% endif %}

          </div>


          <!-- Conference -->

          <div class="periodical">
            <em>

              {% if link.conference %}
                {{ link.conference }}

              {% elsif link.conference1 %}
                {{ link.conference1 }}

              {% elsif link.conference2 %}
                {{ link.conference2 }}
              {% endif %}

            </em>
          </div>


          <!-- ============================= -->
          <!-- Links -->
          <!-- ============================= -->

          <div class="links">

            <!-- PDF -->

            {% if link.pdf %}

              <a href="{{ link.pdf }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                PDF
              </a>

            {% elsif link.pdf1 %}

              <a href="{{ link.pdf1 }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                PDF
              </a>

            {% elsif link.pdf2 %}

              <a href="{{ link.pdf2 }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                PDF
              </a>

            {% endif %}


            <!-- Code -->

            {% if link.code %}
              <a href="{{ link.code }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                Code
              </a>
            {% endif %}


            <!-- Project Page -->

            {% if link.page %}
              <a href="{{ link.page }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                Project Page
              </a>
            {% endif %}


            <!-- BibTex -->

            {% if link.bibtex %}

              <a href="{{ link.bibtex }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                BibTex
              </a>

            {% elsif link.bibtex1 %}

              <a href="{{ link.bibtex1 }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                BibTex
              </a>

            {% elsif link.bibtex2 %}

              <a href="{{ link.bibtex2 }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                BibTex
              </a>

            {% endif %}


            <!-- Website -->

            {% if link.web %}

              <a href="{{ link.web }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                Website
              </a>

            {% elsif link.web1 %}

              <a href="{{ link.web1 }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                Website
              </a>

            {% elsif link.web2 %}

              <a href="{{ link.web2 }}"
                 class="btn btn-sm z-depth-0"
                 role="button"
                 target="_blank"
                 style="font-size:12px;">
                Website
              </a>

            {% endif %}


            <!-- Notes -->

            {% if link.notes %}

              <strong>
                <i style="color:#e74d3c">
                  {{ link.notes }}
                </i>
              </strong>

            {% elsif link.notes1 %}

              <strong>
                <i style="color:#e74d3c">
                  {{ link.notes1 }}
                </i>
              </strong>

            {% elsif link.notes2 %}

              <strong>
                <i style="color:#e74d3c">
                  {{ link.notes2 }}
                </i>
              </strong>

            {% endif %}


            <!-- Others -->

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

  {% else %}

    <p style="color: #999;">
      No publications in this category.
    </p>

  {% endif %}

{% endfor %}

</div>
