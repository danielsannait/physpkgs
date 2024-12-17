# ```physpkgs```: LaTeX packages for physics
Collection of LaTeX packages for a document written in english or italian with LaTeX where physics/maths notation is needed. It is compatible with the ```sapthesis``` class.


## Usage
Add the ```physpkgs.sty``` file in the same folder as the main ```.tex``` file and load it with ```\usepackage{physpkgs}```.
Up to this point, it is compatible with almost every document class.


### Options for this package ```\usepackage[options]{physpkgs}```
- ```[italian]```: Translates everything in italian (default language english).
- ```[article]```:  A4 (adjusted) layout and other packages for a article/report class.
- ```[noindent]```: Removes pragraphs indentation documentwise.
- ```[sectionbarrier]``` or ```[subsectionbarrier]```: Puts a floatbarrier after each section or after each sub(sub...)section.
- ```[tikz]```: Loads tikz and useful related packages.
- ```[code]```: Loads listing for code snippets.
- ```[biblatex]```: Loads biblatex with ref.bib as bibliography file.

If the documentclass ```sapthesis``` is chosen, then every compatible package from physpkgs is loaded and the ```biblatex``` option activated.

For specific situations, certain packages may be exluded by commenting out the appropriate line inside the ```.sty``` file. Choosing ```ntheorem``` environments is one of these situations. 


## Summary of main features
I'm lazy. Inside there is a lot of stuff that when you are facing that super-specific situation just makes sense, but I don't have enough time to make a manual. Just open the ```.sty``` and have a look. However, a bland overview of the main and obvious necessities when writing such documents is the following:
- **Layout**: sensible A4 layout with 2-3 cm magins (default LaTeX ```a4paper``` is a crime agains trees), justified text, appendix and abstract environments.
- **Maths**, physics: the ```physics``` package (it's amazing, even if very badly written, they say), special characters for equations, ```\SI{}{}``` and much more.
- **References**: better references with ```\cref{}```, links are actual links with ```hyperref```, justified footnotes (footnotes are really bad otherwise).
- **Float**: multirow and multicolumn cells in tables, better captions, automatic ```\FloatBarrier```.
- **Code**: color-coded snippets for programming languages (e.g. Phyton).


## Errrors and packages incompatibilities
Every compilation error due to incompatibilities between packages has been (painstakingly) resolved. Turns out that even the loading order of packages matters.

Note that:
- ```\qty{}``` is both used in ```physics``` and ```siunix```, but in the latter ```\SI``` is its redudancy. So ```\qty``` for ```physics``` has been preserved (and what a beauty it is) for adaptive brackets.
- ```ntheorem``` is in conflict with ```amsthm``` and ```wrapfigure```, thus these latter are not loaded by default.


