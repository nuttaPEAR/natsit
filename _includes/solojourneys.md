<h2 id="solojourneys" style="margin: 20px 0px 20px;">My Travels in Europe</h2>

<div class="solojourneys">
  <ol class="bibliography">

  {% for link in site.data.solojourneys.main %}

  <li>
    <div class="journey-row row"> <!-- Added unique row wrapper for Bootstrap grid -->
      <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px; padding-left: 15px;">
        {% if link.image %}
        <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 40%; height: auto;"> <!-- Ensures the image fits properly -->
        {% if link.conference_short %}
        <abbr class="badge">{{ link.conference_short }}</abbr>
        {% endif %}
        {% endif %}
      </div>

      <div class="col-sm-9" style="position: relative; padding-right: 15px; padding-left: 20px;">
        <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
        <div class="author">{{ link.authors }}</div>
        <div class="periodical"><em>{{ link.conference }}</em></div>
        <div class="links">
          {% if link.pdf %}
          <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
          {% endif %}
          
          <!-- Removed code handling since it's not in the YAML anymore -->
          
          {% if link.page %}
          <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
          {% endif %}

          <!-- Removed bibtex handling since it's not in the YAML anymore -->

          <!-- Removed notes handling since it's not in the YAML anymore -->

          {% if link.others %}
          {{ link.others }}
          {% endif %}
        </div>
      </div>
    </div>
  </li>

  {% endfor %}

  </ol>
</div>

