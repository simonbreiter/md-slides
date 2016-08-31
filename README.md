# md-slides
dead simple way to create semantic, nice to look at slides

  * forget about styling, only think about content
    * write markdown (using [remarkable](https://github.com/jonschlinkert/remarkable))
    * code samples are syntactically highlighted (uses [highlightjs](https://highlightjs.org))
    * generates nice slides in the browser (uses [slidy.js](http://www.w3.org/Talks/Tools/Slidy2/))
      * use arrow keys to navigate
      * use the generated 'table of contents' for quick navigation
      * supports printing to pdf (see [presentation.pdf](https://github.com/munen/p_slides/raw/master/build/presentation.pdf))
      * every slide has a unique url for easy sharing
      * supports having a timer in the presentation (see meta[name="duration"] element in presentation.html
        * use an empty first slide if you don't want the timer to start
          automatically

---
# usage

* edit presentation.html to create your content
  * use [markdown syntax](http://commonmark.org)
  * create page breaks using '---'
* open presentation.html in your favourite browser
  * tested in current versions of chrome/safari/ff
* if need be, print the document to pdf
 * slides will automatically get separated into pages

---
# syntax highlighting

* write your code in three backticks
* optional: annotate the given language

## example code

<pre>
```c
static int foo;
void bar(void) {
    foo = 0;
    while (foo != 255) ; }
```
</pre>


---
# LaTeX support

* LaTeX is supported through [Katex](https://github.com/Khan/KaTeX)
* simply put your equations between two single dollar-sign delimiter

## example equations

<pre>
$\frac{2}{3}$
$\frac{n!}{k!(n-k)!} = {n \choose k}$
$x^2 + y^2 = z^2$
</pre>


---

# Tables

Tables are possible

## example table

<pre>
| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |
</pre>
