+++
title = "From Jekyll to Zola"

[taxonomies]
tags = ["jekyll", "rust", "zola"]
+++

## Motivation
The blog has been migrated from [Jekyll](https://jekyllrb.com/) to [Zola](https://www.getzola.org/) for fun and profit.
- Setting up Jekyll was surprisingly fiddly on Windows - I had to install ruby & msys, then troubleshoot live reloading. On the other hand, Zola is a single executable that _just works_
- My next job is going to involve a lot of [Rust](https://www.rust-lang.org/) - I thought I'd get used to things like [TOML](https://github.com/toml-lang/toml)!
- It's something new and hence - wonderful{{ aside(text="There is a book by Soviet-era poet Daniil Kharms titled 'Я думал о том, как прекрасно всё первое!' - 'I thought about how wonderful is everything [first/new]!'") }}

## Migration
After creating a brand new site with  `zola init myblog`, I have added [Slim](https://www.getzola.org/themes/slim/) theme as a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules), copied over my posts, converted variables from [YAML](https://en.wikipedia.org/wiki/YAML) to TOML and... that's mostly it.

### Automatic deployment
I make use of [Github Actions](https://github.com/features/actions) just like in the [docs](https://www.getzola.org/documentation/deployment/github-pages/), except that checkout needs `submodules: true` due to how the theme is added as a git submodule. 

### Blog structure
Dividing posts by year and making each year section transparent so that everything is aggregated in the parent `blog` section is super neat! The only problem I had was with [javascript playthings](@/javascript-playthings/index.md) page. To make it _not_ appear in the list of regular posts, I had to add `sort_by = "date"` to the root `_index.md`, then delete the date field from the javascript `index.md`. Oh, well!
{{ image(url="structure.png", alt="Content folder structure", title="All posts are divided by year and make use of asset colocation") }}

### Marginal notes
Lifted pretty much verbatim from [here](https://kennethfriedman.org/thoughts/2019/marginal-notes/). I love them!

### Theme tweaks
- Mobile-friendly list of posts - I have discovered it doesn't look so good with long titles/many tags by default
- Modified template for post header to allow `null` date in pages
- Removed circles under emphasized text 

The second one was the most cumbersome, as I had to modify a macro that is responsible for post headers. It was done in 2 steps:
1. First, create `templates/custom_macros.html` with a modified version of `post_header` macro from `themes/slim/templates/macros.html`
2. Second, create `templates/page.html` that extends `themes/slim/templates/page.html`, to import `custom_macros.html` and use its version of the `post_header` inside `{% block content %}` 

The rest was just copying `slim.css` from `themes/slim/sass/` to `sass/` and changing what I needed.

## What's next?
I have been toying with an idea of adding a comment section. Something suitable for a static website while being less intrusive than [Disqus](https://disqus.com/). Perhaps [Isso](https://posativ.org/isso/)? Seems like fiddling with a blog is at least just as fun as writing it.