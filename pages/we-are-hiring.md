---
permalink: /we-are-hiring/
layout: page-fullwidth
title: "We Are Hiring"
header: no
teaser: "Check out the available positions below!"
location:
    - name: "IZMIR IYTE TEKNOPARK"
      jobs:
        - name: "Senior Software Developer, Pythonista"
          description: "We are looking for a talented individual with strong Python coding ability. Similar experience with OOP languages also accepted. Please send your cv to us. We have senior and junior positions. Please notify junior coders too. "
        - name: "Senior UI developer, JavaScript Wizard"
          description: "OOP Javascript skills. Angular and/or Jquery knowledge is a huge plus. We have senior and junior positions. Please notify junior coders too. "
        - name: "Summer Intern"
          description: "You should have no problem to reach our office. We will handle the rest. <br>Also, you should smart enough so already started to work on fundamentals of CENG before you knock our door. Please don't attempt to apply without having proper knowledge of: <br><a href='http://belgeler.org/howto/smart-questions.html'>how to ask a smart question </a>, <a href='http://www.gnu.org/philosophy/open-source-misses-the-point.tr.html'>what is Free Software </a>, <a href='http://www.openvim.com/'>vim usage</a>, <a href='https://try.github.io/levels/1/challenges/1'>git</a> <a href='https://git-scm.com/book/en/v2'>usage</a>, <a href='http://www.ulakbus.org/wiki/git_workflow.html'>github usage</a>."
---
{% for loc in page.location limit:1000 %}
<div id="blog-index" class="row">
	<div class="small-12 columns t30">
		<h1>{{ loc.name }}</h1>
		<dl class="accordion" data-accordion>
			{% assign counter = 1 %}
			{% for job in loc.jobs limit:1000 %}
			<dd class="accordion-navigation">
			<a href="#panel{{ counter }}"><span class="iconfont"></span><strong>{{ job.name }}</strong></a>
				<div id="panel{{ counter }}" class="content">
					{% if job.description %}{{ job.description | strip_html | escape }}{% endif %}
					<a href="/iletisim/" title="Basvur"></a><br><br>
				</div>
			</dd>
			{% assign counter=counter | plus:1 %}
			{% endfor %}
		</dl>
	</div><!-- /.small-12.columns -->
</div><!-- /.row -->
{% endfor %}