#  R Avançado

[![Status de Construção](https://travis-ci.org/hadley/adv-r.svg?branch=master)](https://travis-ci.org/hadley/adv-r)

Este é o código por trás do livro [Advanced R](http://adv-r.hadley.nz)
O site é feito com [bookdown](https://bookdown.org/yihui/bookdown/).

## Diagramas

Omnigraffle:
  
* Make sure that 100% is "one postscript point": this ensures canvas
  size matches physical size. Export at 300 dpi scaled to 100%.

* Set grid to 1cm with 10 minor units. Ensure there is 2mm padding around
  all sides of each diagram.

* Convenções:
    * Texto configurado em fonte **inconsolata** 10pt, com text padding configurado em 3. 
    * Emoji configurado em "Apple Color Emoji" 8pt.
    * Tamanho escalar padrão é 6mm x 6mm.
    * Simbolos possuem 4pt de cantos arredondados e plum border.
    * Arrow heads should be set to 75%.
    * Names should be coloured in steel.

Livro:

* Inconsolata scaled (by fontspec) to match main font is 9.42pt.

* Preview at 100% matches physical size of book. Maxiumum diagram width is 11cm.

RMarkdown

* Remove dpi specification from `include_graphics()`, instead relying
  on `common.R`. Chunk should have `output.width = NULL`.

* Beware caching: after changing the size of an image you may need to
  clear the cache before it is correctly updated.

To zip files to for publisher:

```
mkdir crc
cp _book/_main.tex crc
cp -r _bookdown_files/*_files crc
cp -r diagrams crc
cp -r screenshots crc
cp -r emoji crc
cp mina.jpg crc
cp krantz.cls crc
cp book.bib crc
rm crc/diagrams/*.graffle

zip -r adv-r-source.zip crc
```

## Code of conduct

Por favor observe que **R Avançado** é disponibilizado um [Código de conduta do contribuidor](CODE_OF_CONDUCT.md).
Contribuindo com este projeto, você aceita seguir estes termos.

