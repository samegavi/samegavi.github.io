<!-- {% assign page = site.works | where:"title", include.title | first %} -->

{% assign name = include.name %}
{% assign activity = site.data.activities[name] %}
{% assign title = activity.title %}
{% assign description = activity.description %}
{% assign category = activity.category %}
{% assign summary = activity.summary %}
{% assign link = activity.link %}
{% assign thumb = activity.thumb %}


<div class="project {{category}}">
	<a href="{{link}}">
		<img src="{{thumb}}">
		<div class="overlay">
			<div class="overlay_title">
				{{title}}
			</div>
<!-- 			<div class="overlay_description">
				{{description}}
			</div> -->
			<div class="overlay_summary">
				<ul>
				{% for s in summary %}
					<li>{{ s }}</li> 
				{% endfor %}			
				</ul>
			</div>
		</div>
	</a>
</div>

