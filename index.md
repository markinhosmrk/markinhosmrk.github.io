---
layout: default
title: Marcos Marchesini
---

<style>
.post-card {
	background: #ffffff;
	padding: 20px;
	margin-bottom: 30px;
	border-radius: 8px;
	box-shadow: 0 4px 10px rgba(0,0,0,0.08);
	transition: transform 0.15s ease, box-shadow 0.15s ease;
}

.post-card:hover {
	transform: translateY(-4px);
	box-shadow: 0 6px 18px rgba(0,0,0,0.12);
}

.post-date {
	color: #777;
	font-size: 0.9em;
}

.read-more {
	display: inline-block;
	margin-top: 10px;
	padding: 6px 14px;
	background-color: #2c3e50;
	color: #ffffff;
	text-decoration: none;
	border-radius: 4px;
	font-size: 0.9em;
}

.read-more:hover {
	background-color: #1a252f;
}

</style>

{% for post in site.posts %}
	<div class="post-card">
		<h2>
			<a href="{{ post.url }}">{{ post.title }}</a>
		</h2>

		<div class="post-date">
			{{ post.date | date: "%d/%m/%Y" }}
		</div>

		<p>
			{{ post.excerpt }}
		</p>

		<a class="read-more" href="{{ post.url }}">
			Ler mais
		</a>
	</div>
{% endfor %}
