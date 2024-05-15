# One_bit DoA estimation


[![Build Status](https://github.com/JuliaTeX/TikzPictures.jl/workflows/CI/badge.svg)](https://github.com/JuliaTeX/TikzPictures.jl/actions)
[![codecov](https://codecov.io/gh/JuliaTeX/TikzPictures.jl/branch/master/graph/badge.svg?token=nCBJc77iDE)](https://codecov.io/gh/JuliaTeX/TikzPictures.jl)

This library allows one to create Tikz pictures and save in various formats. It integrates with IJulia, outputting SVG images to the notebook.

This library will try to use the lualatex package already installed on the system. If the library cannot run lualatex, it will fall back to trying to use tectonic for the compilation. 

Lualatex may be installed through the texlive and miktex distributions. You should have dvisvgm installed. On Ubuntu, you can get the required packages, if not already present, by running `sudo apt-get install pdf2svg texlive-latex-base texlive-binaries texlive-pictures texlive-latex-extra texlive-luatex`.

Note: this package will attempt to turn off interpolation in the generated SVG, but this currently only works in Chrome.

## Example

```julia
using TikzPictures
tp = TikzPicture("\\draw (0,0) -- (10,10);\n\\draw (10,0) -- (0,10);\n\\node at (5,5) {tikz \$\\sqrt{\\pi}\$};", options="scale=0.25", preamble="")
save(PDF("test"), tp)
save(SVG("test"), tp)
save(TEX("test"), tp)
save(TIKZ("test"), tp)
```

