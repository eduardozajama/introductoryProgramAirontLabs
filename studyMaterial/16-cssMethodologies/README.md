# 16. CSS Methodologies.
## OOCSS, SMACSS, BEM
CSS is notoriously difficult to manage in large, complex, rapidly-iterated systems. One reason is CSS lacks a built-in scoping mechanism. Everything in CSS is global.

That means any change you make has the potential to cascade and alter the presentation of unrelated bits of the UI. Extended CSS languages, a.k.a. CSS preprocessors, such as Sass, Less and Stylus make things a little easier by offering up features that make writing CSS easier.

But even these extended CSS languages, in my opinion, don’t truly fix the scalability issue. Until CSS gets its own native scoping mechanism, we need to devise our own system for locking down styles to specific sections of an HTML document. CSS methodologies are the solution.

## Why should we use them?
It is important to have a standardised approach to CSS architecture and naming conventions when developing CSS at scale. Conventions can benefit the team to produce higher quality, consistent code that can be ported between projects. This also gives teams clear guidance on syntax and style preference.

1. OOCSS (Object orientated CSS)
>[OOCSS Explained](https://www.hongkiat.com/blog/basics-of-object-oriented-css/)

2. BEM (Block element modifier)
>[BEM](https://en.bem.info/)

3. SMACSS - Scalable Modular architecture
>[SMACSS](http://smacss.com/)

## More Resources
>[OOCSS](https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/)

>[Css Methodologies](https://www.valoremreply.com/post/5_css_methodologies/)