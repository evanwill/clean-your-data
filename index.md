---
layout: default
---

{% include figure.html img="open-refine-320px.png" alt="openrefine logo" width="60%" %}

# Getting Started with OpenRefine: Explore, Clean, and Transform your Data!

Before analysis comes the messy work of evaluating, cleaning, and transforming data.
This hands on workshop will introduce a free power tool to get the job done: [OpenRefine](http://openrefine.org/index.html){:target='_blank' rel='noopener'}. 
We will install Refine, create a project, and get oriented to the many features for exploring and transforming tabular data. 

Intended for students, faculty, and staff with an interest in cleaning, transforming, and working with diverse data sources. 
No experience necessary.

This site provides a basic lesson outline. See the [2017 workshop video](https://youtu.be/wGVtycv3SS0){:target='_blank' rel='noopener'} for more content.

<div class="toc" markdown="1">
## Contents:

{% for lesson in site.pages %}
{% if lesson.nav == true %}- [{{ lesson.title }}]({{ lesson.url | relative_url }}){% endif %}
{% endfor %}
</div>

Hosted by [University of Idaho Library](http://www.lib.uidaho.edu/){:target='_blank' rel='noopener'}, {{ site.pub_year }}, 2017, 2016.

> built using [Jekyll](https://jekyllrb.com/){:target='_blank' rel='noopener'} and [GitHub Pages](https://pages.github.com/){:target='_blank' rel='noopener'}
>
> content: cc-by-sa <a href="https://github.com/{{ site.github_username }}">{{ site.author }}</a> {{ site.pub_year}}. (get [source code]({{ site.repo }}))
> Last build date: {{ site.time | date: "%Y-%m-%d" }}.
>
> <a href="http://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" alt="Creative Commons License" /></a>
