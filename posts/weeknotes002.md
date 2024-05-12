+++
date = "2024-05-11"
title = "Weeknotes 002"
var"layout-post" = nothing
tags = ["weeknotes", "personal"]
rss = ""

# Dependent variables
website_description = replace(rss, "*" => "")
rss_pubdate = Date(date)
+++

~~~
<h1><a href="{{ get_url }}">{{ markdown2html title }}</a></h1>
~~~

## What I've been learning
- Learnt about sorting and filtering results in SQL, limiting the sorted results, pagination of results, and removing duplicates. [Sort and Filter][sf]
- Learning about multiple types of join between different tables in a database, including Inner, Outer, and Cross joins, along with self joins for joining data within a single table. [Joins][joins]
- Worked through this example from freeCodeCamp website using a simple Machine Learning model on the Titanic data set using Julia. [Julia Machine Learning][titanic] 

## What I've been reading
- [A fascinating introduction into LLMs without the maths][LLMs]
- [Some initial reading about Flux, one of the machine learning libraries in Julia][FLux]

## What I've been listening to
- How to become a Data Scientist podcast. Helpful take aways from this episode were build a project, any project, give it a front end so people can see it and you can showcase it in interviews. Also interesting ways to augment your data set; if for example you have a series of reviews in English, translate them from English to French to German to Spanish and back to English and you've doubled your data set. [Link][pod]


[sf]: https://learn.microsoft.com/en-us/training/modules/sort-filter-queries/
[joins]: https://learn.microsoft.com/en-us/training/modules/query-multiple-tables-with-joins/
[titanic]: https://www.freecodecamp.org/news/machine-learning-using-julia/
[LLMs]: https://blog.miguelgrinberg.com/post/how-llms-work-explained-without-math
[FLux]: https://fluxml.ai/Flux.jl/stable/
[pod]: https://podcasts.apple.com/gb/podcast/super-data-science-ml-ai-podcast-with-jon-krohn/id1163599059?i=1000654426181