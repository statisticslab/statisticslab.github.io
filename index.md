---
layout: default
title: Ma Lab
categories:
 - home
---
{% include JB/setup %}
{% for page in site.categories.misc %}
{% if page.homepage %}
	{% assign homepage = page %}
{% endif %}
{% endfor %}

<div class="container">
	<div class="col-md-12">
		<div class="bigtitle logobox">
			Ma Lab of Statistical Genomics 
		</div>
	</div>	
</div> 


The Ma Lab at [Fred Hutchinson Cancer Center](https://www.fredhutch.org/en/faculty-lab-directory/ma-jing.html) specializes in statistical and computational methods for genomic data, in particular microbiome data. We employ a variety of statistical learning methods, ranging from dimensionality reduction, graphical models, and high-dimensional inference, to address the analytical challenges faced with interpreting omics data. The long-term goals of our research are to enhance biomarker discoveries through powerful and robust statistical inference, and to translate these findings to advance clinical research.

**Keywords**: network analysis, high-dimensional inference, data integration

<!--
Our lab collaborates with Dr. [Daniel Promislow](http://www.promislowlab.org/) on the [Dog Aging Project](https://dogagingproject.org/), supported by U19 grant AG057377 from the National Institute of Aging, a part of the National Institutes of Health. 

For a complete list of publications, see my [Google Scholar](http://scholar.google.com/citations?user=TClZmdkAAAAJ). For more details about my background, read my [CV](/assets/pdfs/team/jingma-cv.pdf). The best way to contact me is through [email](/team/jingma). 

Our current research focuses on integrative analysis of microbiome multi-omics data with applications to cancer biology and aging. 
-->


<hr/>

<div class="row">
	<div class="col-md-12">
		<div class="head">
			{{ homepage.content }}
		</div>
	</div>				
</div>

<div class="row">
	
	<div class="col-md-4">
		<div class="head">
			<a class="off" href="/news/">News</a>
		</div>
		<div class="bigspacer"></div>
		<div class="feedbox pad-left">
			{% for news in site.categories.news limit:5 %}
			
				{% for member in site.categories.team %}
					{% if member.handle == news.author_handle %}
						{% assign author = member %}
					{% endif %}
				{% endfor %}		
				
				<div class="note-title">
					<i class="fa fa-bullhorn"></i>
					<a class="off" href="{{ news.url }}">
					{{ news.title }}
					</a>
				</div>
				<div class="note">
					{{ news.content }}
				</div>
				<div class="smallspacer"></div>
				<div class="smallnote">
					Posted
					{{ news.date | date_to_string }}
					{% if author %}
					by <a class="off" href="{{ author.url }}">{{ author.handle }}</a>
					{% endif %}						
				</div>
				<div class="spacer"></div>	
				<div class="spacer"></div>				
			{% endfor %}
		</div>
		<div class="bigspacer"></div>		
	</div>
	
	
	<div class="col-md-4">
		<div class="head">
			<a class="off" href="/papers/">Recent Papers
			</a>
		</div>
		<div class="bigspacer"></div>
		<div class="feedbox pad-left">		
			{% for paper in site.categories.papers limit:5 %}
				<div class="note-title">
					<i class="fa fa-file-text-o fa-fw"></i>
					<a class="off" href="{{ paper.url }}">
					{{ paper.title }}
					</a>
					<br/>
					<div class='shortref note'>
					{{ paper.shortref }}
					</div>
				</div>
				<div class="smallspacer"></div>
				<div class="smallnote">
					Published
					{{ paper.date | date_to_string }}
				</div>
				<div class="spacer"></div>	
				<div class="spacer"></div>				
			{% endfor %}
		</div>
		<div class="bigspacer"></div>		
	</div>
	

	<div class="col-md-4">
		<div class="head">
			<a class="off" href="/blog/">Blogs</a>
		</div>
		<div class="bigspacer"></div>
		<div class="feedbox pad-left">
			{% for blog in site.categories.blog limit:5 %}
				<div class="note-title">
					<i class="fa fa-comment-o fa-fw"></i>
					<a class="off" href="{{ blog.url }}">
					{{ blog.title }}
					</a>
					<br/>
					<div class='shortref note'>
					{{ blog.description }}
					</div>
				</div>
				
				<div class="smallspacer"></div>
				<div class="smallnote">
					Posted
					{{ blog.date | date_to_string }}
					{% if author %}
					by <a class="off" href="{{ author.url }}">{{ author.handle }}</a>
					{% endif %}						
				</div>
				<div class="spacer"></div>	
				<div class="spacer"></div>
				
				<div class="smallspacer"></div>
				<div class="spacer"></div>
				<div class="spacer"></div>
			{% endfor %}
		</div>
		<div class="bigspacer"></div>
	</div>
	
	<!-- <div class="col-md-4">
		<div class="head">
			<a class="off" href="/projects/">Projects</a>
		</div>
		<div class="bigspacer"></div>
		<div class="feedbox pad-left">
			{% for project in site.categories.project limit:4 %}
				<div class="note-title">
					<i class="fa fa-terminal"></i>
					<a class="off" href="{{ project.url }}">
					{{ project.title }}
					</a>
					<br/>
					<div class='shortref note'>
					{{ project.tags }}
					</div>
				</div>
				<div class="smallspacer"></div>
				<div class="spacer"></div>
				<div class="spacer"></div>
			{% endfor %}
		</div>
		<div class="bigspacer"></div>
	</div> -->


</div>

<div class="bigspacer"></div>

