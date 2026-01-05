+++
title = "Configuration"
description = "configuration guide"
date = 1980-01-01

[taxonomies]
tags = ["guide"]

[extra]
toc = true
+++

## Pinned Posts

Nivis allows you to pin special posts so that they are placed at the frontmost of the post list. To pin posts, add the following to the front matter of your `posts/_index.md`:
```toml
[extra]
pinned_posts = [
    "posts/pinned_post1.md",
    "posts/pinned_post2.md"
]
```

## Math display

Nivis theme supports Mathjax for rendering math contents. Add these contents to your `config.toml` to enable math rendering:
```toml
[extra]
math = "mathjax"
```

Due to the weirdsome escape rules of zola, some of your math content might not display correctly. I referred to [this post](https://zola.discourse.group/t/maths-support-via-mathjax/1000) for a solution. If your math content fails to display, follow the steps below:

After adding or changing your post, run `themes/nivis/scripts/wrap_math.py` to process the markdown files. After running the script, (or of course you can change them manually), your math contents should be wrapped in code blocks, e.g.:
`````markdown
This is an inline math example: `$e^{\pi i}=-1$`.

And this is a display math example:
```math-display
$$
\sum_{i=1}^n i^3=\frac{n^2(n+1)^2}{4}
$$
```
`````

When building the site, zola would warn that it fails to find a render rule for language `math-display`. Of course, we don't need these warnings. Add the following lines to your `config.toml` to get rid of these warnings:
```toml
[markdown]
extra_syntaxes_and_themes = ["themes/nivis/syntaxes/"]
```

## Special Pages

Nivis theme provides About page, Archives page, Categories page and Links page to help you fully customize your site. Move on to [Special Pages](@/posts/sp-pages.md) for more information.