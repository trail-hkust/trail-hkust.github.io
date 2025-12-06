<h1 id="publications"></h1>

<h2 style="margin: 30px 0px -15px;">Publications <temp style="font-size:15px;">[</temp><a href="https://scholar.google.com/citations?user=lxrXMY0AAAAJ&hl=en&oi=ao" target="_blank" style="font-size:15px;">Google Scholar</a><temp style="font-size:15px;">]</temp><temp style="font-size:15px;">[</temp><a href="https://www.researchgate.net/profile/Zixuan-Yuan" target="_blank" style="font-size:15px;">ResearchGate</a><temp style="font-size:15px;">]</temp></h2><br>

 \* means equal contribution.<br>
 † means corresponding authors.

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main19 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 290px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}


{% for link in site.data.publications.main18 %}
{% if forloop.counter == 3 %}
        {% break %}
    {% endif %}
<li>
<div class="publication-entry" style="margin-bottom: 30px;">
  <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;">
      <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 50%; max-width: 700px; height: auto; object-fit: contain; margin-bottom: 20px;">
      <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
      <div class="links">
        {% if link.pdf %} 
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
        {% endif %}
        {% if link.code %} 
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
        {% endif %}
        {% if link.page %} 
        <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
        {% endif %}
        {% if link.bibtex %} 
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
        {% endif %}
        {% if link.web %} 
        <a href="{{ link.web }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
        {% endif %}
        {% if link.notes %} 
        <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
        {% endif %}
        {% if link.others %} 
        {{ link.others }}
        {% endif %}
      </div>
  </div>
</div>

</li>
{% endfor %}


{% for link in site.data.publications.main17 %}
{% if forloop.counter == 3 %}
        {% break %}
    {% endif %}
<li>
<div class="publication-entry" style="margin-bottom: 30px;">
  <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;">
      <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 60%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
      <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
      <div class="links">
        {% if link.pdf %} 
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
        {% endif %}
        {% if link.code %} 
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
        {% endif %}
        {% if link.page %} 
        <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
        {% endif %}
        {% if link.bibtex %} 
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
        {% endif %}
        {% if link.web %} 
        <a href="{{ link.web }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
        {% endif %}
        {% if link.notes %} 
        <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
        {% endif %}
        {% if link.others %} 
        {{ link.others }}
        {% endif %}
      </div>
  </div>
</div>

</li>
{% endfor %}

{% for link in site.data.publications.main0_added %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 100px; padding-bottom: 0px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 510px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px; margin-left: 70px">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}


{% for link in site.data.publications.main %}
{% if forloop.counter == 3 %}
        {% break %}
    {% endif %}
<li>
<div class="publication-entry" style="margin-bottom: 30px;">
  <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;">
      <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
      <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
      <div class="links">
        {% if link.pdf %} 
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
        {% endif %}
        {% if link.code %} 
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
        {% endif %}
        {% if link.page %} 
        <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
        {% endif %}
        {% if link.bibtex %} 
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
        {% endif %}
        {% if link.web %} 
        <a href="{{ link.web }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
        {% endif %}
        {% if link.notes %} 
        <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
        {% endif %}
        {% if link.others %} 
        {{ link.others }}
        {% endif %}
      </div>
  </div>
</div>

</li>
{% endfor %}

{% for link in site.data.publications.main3 %}
<li>
    <div class="publication-entry" style="margin-bottom: 30px;">
      <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 290px;">
          <img src="{{ link.image1 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 450px; height: auto; object-fit: contain; margin-bottom: 20px;">
          <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px; margin-left: 90px">{{ link.conference_short1 }}</abbr>
      </div>
      <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
          <div class="title"><a href="{{ link.pdf1 }}">{{ link.title1 }}</a></div>
          <div class="author">{{ link.authors1 }}</div>
          <div class="periodical"><em>{{ link.conference1 }}</em></div>
          <div class="links">
            {% if link.pdf1 %} 
            <a href="{{ link.pdf1 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
            {% endif %}
            {% if link.code1 %} 
            <a href="{{ link.code1 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
            {% endif %}
            {% if link.page1 %} 
            <a href="{{ link.page1 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
            {% endif %}
            {% if link.bibtex1 %} 
            <a href="{{ link.bibtex1 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
            {% endif %}
            {% if link.web1 %} 
            <a href="{{ link.web1 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
            {% endif %}
            {% if link.notes1 %} 
            <strong> <i style="color:#e74d3c">{{ link.notes1 }}</i></strong>
            {% endif %}
            {% if link.others1 %} 
            {{ link.others1 }}
            {% endif %}
          </div>
      </div>
    </div>
</li>
{% endfor %}

{% for link in site.data.publications.main4 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main5 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 290px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main6 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 185px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 480px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px; margin-left: 90px">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main7 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 270px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main8 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main9 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 170px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main10 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 175px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main11 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 205px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}


{% for link in site.data.publications.main12 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 340px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 440px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px; margin-left: 70px">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main13 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 175px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 800px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px;">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main14 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 302px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 560px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px; margin-left: 50px">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main15 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 200px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 550px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px; margin-left: 40px">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

{% for link in site.data.publications.main16 %}
<li>
        <div class="publication-entry" style="margin-bottom: 30px;">
          <div class="col-sm-12 abbr" style="position: relative; text-align: center; padding: 15px;height: 330px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 520px; height: auto; object-fit: contain; margin-bottom: 20px;">
              <abbr class="badge" style="position: absolute; top: 10px; left: 10px; background: #002D72; color: white; padding: 5px; margin-left: 70px">{{ link.conference_short2 }}</abbr>
          </div>
          <div class="col-sm-12" style="padding: 15px; text-align: center; margin-top: 15px;">
              <div class="title"><a href="{{ link.pdf2 }}">{{ link.title2 }}</a></div>
              <div class="author">{{ link.authors2 }}</div>
              <div class="periodical"><em>{{ link.conference2 }}</em></div>
              <div class="links">
                {% if link.pdf2 %} 
                <a href="{{ link.pdf2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
                {% endif %}
                {% if link.code2 %} 
                <a href="{{ link.code2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
                {% endif %}
                {% if link.page2 %} 
                <a href="{{ link.page2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
                {% endif %}
                {% if link.bibtex2 %} 
                <a href="{{ link.bibtex2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
                {% endif %}
                {% if link.web2 %} 
                <a href="{{ link.web2 }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
                {% endif %}
                {% if link.notes2 %} 
                <strong> <i style="color:#e74d3c">{{ link.notes2 }}</i></strong>
                {% endif %}
                {% if link.others2 %} 
                {{ link.others2 }}
                {% endif %}
              </div>
          </div>
        </div>
        
</li>
{% endfor %}

<br>

</ol>
</div>
