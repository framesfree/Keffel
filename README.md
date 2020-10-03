# Keffel

## LaTeX drawings of typical HPGe detector geometries.

---

## Instructions

### How to use the script

Simply type in your detector dimensions in the first block of code with variables, it would be like this:

```latex
\newcommand\Name{Test/0001}           % Name
\newcommand\Crystal{INTRI~5422}       % Crystal number
\newcommand\HEAD{1.59}                % HEAD conc x 10^10
\newcommand\TAIL{1.60}                % TAIL conc x 10^10
\newcommand\Dia{59.0}                 % Detector diameter in mm
\newcommand\Hei{53.8}                 % Detector hight in mm
\newcommand\Gdt{5.0}                  % Groove depth
\newcommand\Bult{3.0}                 % widow bulletization
\newcommand\Cdiam{7.7}                % Contact diam 
\newcommand\Cdepth{37.7}              % Contact depth
\newcommand\GrvEx{27.0}               % Groove ext. diameter
\newcommand\GrvIn{17.0}               % Groove int. diameter
\setboolean{passivated}{true}         % passivation?[true|false]
\setboolean{thin_window}{false}       % thin window?[true|false]
```

After editing just compile the PDF file. That's all! :) 
The resulting document should look something like this:

![Example drawing](https://github.com/framesfree/Keffel/blob/master/example.png)

### How to convert PDF to PNG?

1. Install [ImageMagick](https://imagemagick.org/script/download.php)

2. Install [GhostScript](https://www.ghostscript.com/download/gsdnld.html)

2. After compiling a PDF file with LaTeX, simply type this command in your terminal window:

    `convert -background white -alpha remove -alpha off input.pdf output.png`

    Where is `input.pdf` is input file name and `output.png` is output file name.

By default the picture size is 1200px in width, but you can change it if you want at line `\resizebox{1200px}{!}`. Exclamation mark symbol stands for relative height resizing.

---

## What's inside?

- gcd.tex - Germanium Coaxial Detector
- gfd.tex - Germanium Flat Detector (similar to BeGe from CANBERRA)

### To do next:

- gpd.tex - Germanium Planar Detector
- gwd.tex - Germanium Well-type Detector

