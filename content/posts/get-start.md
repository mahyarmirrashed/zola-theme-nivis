+++
title = "Getting Started"
description = "getting started with nivis"
date = 1980-01-01

[taxonomies]
tags = ["start"]

[extra]
toc = false
+++

Use `git submodule` to add the theme to your site:
```bash
git submodule add -b master --depth=1 https://github.com/Resorie/zola-theme-nivis.git themes/nivis/
git submodule update --init --recursive
```

Then, change your theme config in `config.toml`:
```toml
theme = "nivis"
```

Start your site by copying the example content into your site folder:
```bash
cp -r themes/nivis/content content
```

If you want to update the nivis theme, run the following command:
```bash
git submodule update --remote --merge
```

Move on to [Configuraion](@/posts/configure.md) for configuraions. 

If you like this theme, please give it a star on [github](https://github.com/Resorie/zola-theme-nivis). :kissing_heart: