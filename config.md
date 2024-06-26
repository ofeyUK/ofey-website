<!-- RSS settings -->

@def website_title = "ofey"
@def website_description = "ofey - open/data/julia"
@def website_url = ""
@def generate_rss = true

+++
# Exclude everything that is not explicitly in include
_include = ["_assets/", "_css/", "_libs/", "_layout/", "index.html", "404.md", "posts/", "about/"]
_exclude = if get(ENV, "FRANKLIN_OPTIMIZE", nothing) == "true"
        # ["_libs/highlight/highlight.min.js"]
        String[]
    else
        String[]
    end
ignore = [setdiff([isfile(x) ? x : x * "/" for x in readdir()], _include); _exclude]
+++



<!-- Theme specific options -->
<!-- @def title = "Fredrik Ekre" -->
@def sitename = "ofey"
@def author.name = "mrtn"
@def author = "Martin Parkes"

<!-- Social icons -->
@def social = (
        github = "https://github.com/ofeyUK",
        twitter = "https://twitter.com",
    )

<!-- Logo -->
@def logo.mark = "\$"
@def logo.text = "cd /home/ofey"

<!-- Menu -->
@def menu = [
        #(name = "posts", url = "/posts/"),
        #(name = "research", url = "/research/"),
        (name = "about", url = "/about/"),
    ]

@def prepath = "ofey-website"

\newcommand{\codetoggle}[1]{
~~~
<div class="toggle-code-wrap" style="position:relative">
<input id="{{ unique_id new }}" type="checkbox" checked=true">
<label for="{{ unique_id }}" class="switch">
  <span class="slider round"></span>
</label>
<div class="toggle-code-new">
~~~
`````julia
!#1
`````
~~~
</div>
<div class="toggle-code-old">
~~~
`````julia-old
!#1
`````
~~~
</div>
</div>
~~~
}
