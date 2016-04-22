---
permalink: /we-are-hiring/
layout: page-fullwidth
title: "We Are Hiring"
header:
    thumb: header_homepage_13.jpg
breadcrumbs: true
teaser: "Check out the available positions below!"
---
{% assign placecounter = 1 %}
{% for loc in site.places limit:1000 %}
<div id="blog-index" class="row">
	<div class="small-12 columns t30">
		<h2>{{ loc.name }}</h2>
		<dl class="accordion" data-accordion>
			{% assign jobcounter = 1 %}
			{% for job in loc.jobs limit:1000 %}
			<dd class="accordion-navigation">
			<a href="#panel{{ placecounter }}-{{ jobcounter }}"><span class="iconfont"></span><strong>{{ job.name }}</strong></a>
				<div id="panel{{ placecounter }}-{{ jobcounter }}" class="content">
					{% if job.description %}{{ job.description | strip_html | escape }}{% endif %}
					<br><a href="/iletisim/?place={{ placecounter }}&job={{ jobcounter }}" class="button tiny radius" style="float:right;" title="Basvur">Basvur</a><br><br>
				</div>
			</dd>
			{% assign jobcounter=jobcounter | plus:1 %}
			{% endfor %}
		</dl>
	</div><!-- /.small-12.columns -->
</div><!-- /.row -->
{% assign placecounter=placecounter | plus:1 %}
{% endfor %}