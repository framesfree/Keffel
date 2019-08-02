# Keffel

LaTeX drawings of typical HPGe detector geometries.



## Instructions

### How to use the tex script

Simply type in your detector dimensions in the first block of code with variables, it would be like this:

```latex
\newcommand\Name{India/1904}          % Name
\newcommand\Crystal{INTRI~7218}       % Crystal number
\newcommand\HEAD{1.59}                % HEAD conc x 10^10
\newcommand\TAIL{1.60}                % TAIL conc x 10^10
\newcommand\Dia{59.0}                 % Detector diameter in mm
\newcommand\Hei{53.8}                 % Detector hight in mm
\newcommand\Gdt{5.0}                  % Groove depth
\newcommand\Bult{3.0}                 %widow bulletization
\newcommand\Cdiam{7.7}                %Contact diam 
\newcommand\Cdepth{37.7}              %Contact depth
\newcommand\GrvEx{27.0}               %Groove ext. diameter
\newcommand\GrvIn{17.0}               %Groove int. diameter
\setboolean{passivated}{true}         %passivation?[true|false]
\setboolean{thin_window}{false}       %thin window?[true|false]
```

After editing just compile the PDF file. That's all! :) 
The resulting document should look something like this:

![Example detector](https://github.com/framesfree/Keffel/blob/master/example.png)

### How to convert PDF to PNG

1. Install [ImageMagick](https://imagemagick.org/index.php)

2. In your terminal window simply type this command:

    `convert -density 120 -background white -alpha remove -alpha off gcd.pdf .\crystals\000_name_1900.png`

    Where is `gcd.pdf` is input file name and `.\crystals\000_name_1900.png` is output file name.

---

## What's inside?

- gcd.tex - Germanium Coaxial Detector (alpha)
- gfd.tex - Germanium Flat Detector (similar to BeGe from CANBERRA) (beta)
- ~~gcdx.tex - Germanium Coaxial Detector with thin entrance window~~ - redundant, replaced with gcd.tex

### In development

- gpd.tex - Germanium Planar Detector
- gwd.tex - Germanium Well-type Detector
