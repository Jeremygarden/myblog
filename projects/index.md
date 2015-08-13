---
layout: page
title: Projects
excerpt: "An archive of my projects."
image:
  feature: squirrel.jpg
---

<div id="projects">
	{% for project in site.data.projects %}
		<div class="project">
			<h1>{{ project.name }}</h1> 
			<span class="separator" style="font-size: 20px">|</span>
			<span style="font-size: 20px">{{ project.tagline }}</span>
			<div class="meta">
				<span class="time" style="font-weight: bold">{{ project.time }}</span>
				<span class="toolstack">| toolstack:</span> {{ project.tools | join: ", " }}
			</div>
			<div class="description">{{ project.description | markdownify}}
			</div>


			{% if project.url or project.github %}
				{% if project.url %}
					<a href="{{ project.url }}" class="btn" target="_blank"><i class="fa fa-link fa-fw"></i>view online</a>
				{% endif %}
				{% if project.github %}
					<a href="https://github.com/{{ project.github.url }}" class="btn" target="_blank"><i class="fa fa-github fa-fw"></i>view on GitHub</a>
				{% endif %}

			{% endif %}
		</div>
	{% endfor %}
</div>

