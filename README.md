# Noto Sans JP Extra
(c) 2024, dp.

~~NO EDITING ALLOWED..~~

**Based on Noto Sans JP**

It covers only the glyphs in [Adobe-Japan1-4](https://github.com/adobe-type-tools/Adobe-Japan1?tab=readme-ov-file#supplement-4adobe-japan1-4) and [Adobe-Japan1-5](https://github.com/adobe-type-tools/Adobe-Japan1?tab=readme-ov-file#supplement-5adobe-japan1-5).

See [Noto CJK Fonts](https://github.com/notofonts/noto-cjk).

----------------------

# hello.github.io
Help NOW! $desmos$
$$\text{Using an underscore in a file name, such as example\\_one.text}$$
The tangent of 90 degrees is **undefined**.

Here's why:

The tangent function is defined as the ratio of the sine of an angle to its cosine:
$tan(\theta) = \frac{sin(\theta)}{cos(\theta)}$

For 90 degrees:
* $sin(90^\circ) = 1$
* $cos(90^\circ) = 0$

Therefore:
$tan(90^\circ) = \frac{1}{0}$

Division by zero is undefined, so the tangent of 90 degrees is undefined.

Geometrically, if you consider the unit circle, the tangent represents the slope of the line from the origin to the point on the circle. At 90 degrees, the line is perfectly vertical, and a vertical line has an undefined slope.

You are absolutely correct\! By default, standard LaTeX 2e (using `article`, `book`, `report`, etc., classes without additional packages) has a somewhat limited set of mathematical symbols. Many commonly used and more advanced mathematical symbols are provided by the **American Mathematical Society (AMS) fonts**, which are made available through the `amsmath` and, specifically for symbols, the **`amssymb` package**.

Here's why `amssymb` is so crucial for mathematical typesetting in LaTeX:

### Why `amssymb` is Needed

1.  **Expanded Symbol Set:** `amssymb` provides a vast collection of additional mathematical symbols that are not part of the core LaTeX font set. These include:

      * **Specific Relations:** $\\lesssim$, $\\gtrsim$, $\\subsetneqq$, $\\supseteqq$, $\\nsubseteq$, $\\nsupseteq$, $\\trianglelefteq$, $\\trianglerighteq$, etc.
      * **Binary Operations:** $\\circledast$, $\\boxplus$, $\\ltimes$, $\\rtimes$, $\\rightthreetimes$, etc.
      * **Arrows:** $\\curvearrowleft$, $\\curvearrowright$, $\\Lsh$, $\\Rsh$, $\\circlearrowleft$, $\\circlearrowright$, $\\looparrowleft$, $\\looparrowright$, etc.
      * **Miscellaneous Symbols:** $\\hbar$, $\\ell$, $\\nabla$, $\\forall$, $\\exists$, $\\infty$, $\\aleph$, $\\emptyset$, $\\top$, $\\bot$, $\\angle$, $\\complement$, $\\blacksquare$, $\\checkmark$, $\\diagdown$, $\\diagup$, $\\intercal$, $\\bigstar$, $\\sphericalangle$, $\\measuredangle$, $\\measuredangle$, $\\diamondsuit$, $\\heartsuit$, $\\spadesuit$, $\\clubsuit$, etc.
      * **Blackboard Bold Characters:** The popular double-struck uppercase letters for number sets like $\\mathbb{N}$ (natural numbers), $\\mathbb{Z}$ (integers), $\\mathbb{Q}$ (rational numbers), $\\mathbb{R}$ (real numbers), $\\mathbb{C}$ (complex numbers). These are accessed via `\mathbb{N}`, `\mathbb{Z}`, etc.
      * **Fraktur Characters:** Gothic-style letters like $\\mathfrak{A}$, $\\mathfrak{B}$, etc., accessed via `\mathfrak{A}`.
      * **Script Characters:** Calligraphic letters like $\\mathcal{A}$, $\\mathcal{B}$, etc. (though `\mathcal` is part of core LaTeX, `amssymb` might enhance its rendering or provide related fonts).

2.  **AMS-Fonts (`msam` and `msbm`):** The symbols provided by `amssymb` come from the `msam` and `msbm` (Math Symbols A and B) font families, which were designed by the American Mathematical Society. These fonts integrate seamlessly with the standard Computer Modern fonts and other popular math fonts.

### How to Use `amssymb`

To use these symbols in your LaTeX document, you simply need to include the package in your preamble:

```latex
\documentclass{article}
\usepackage{amsmath} % Often used alongside amssymb for better math environments
\usepackage{amssymb} % Provides the additional symbols

\begin{document}

Here are some common symbols from \texttt{amssymb}:

\begin{itemize}
    \item Real numbers: $\mathbb{R}$
    \item Natural numbers: $\mathbb{N}$
    \item Integers: $\mathbb{Z}$
    \item Complex numbers: $\mathbb{C}$
    \item For all: $\forall$
    \item There exists: $\exists$
    \item Infinity: $\infty$
    \item Not subset: $\nsubseteq$
    \item Not equal: $\neq$ (also in core LaTeX, but good to mention context)
    \item Black square: $\blacksquare$
\end{itemize}

Here's an example using Fraktur and blackboard bold:
Let $G$ be a group, and $\mathfrak{g}$ be its Lie algebra.
Consider the set of natural numbers $\mathbb{N}$.

\end{document}
```

### Important Considerations: XeLaTeX/LuaLaTeX and `unicode-math`

While `amssymb` is essential for pdfLaTeX users, if you're using **XeLaTeX** or **LuaLaTeX** and wish to leverage modern OpenType math fonts (like Latin Modern Math, TeX Gyre Termes Math, XITS Math, Cambria Math, etc.), you will typically use the **`unicode-math` package** instead of `amsmath` and `amssymb`.

`unicode-math` provides access to an even broader range of mathematical symbols directly from Unicode math fonts, often including all the `amssymb` symbols and many more, with more consistent styling across different font faces.

```latex
% For XeLaTeX or LuaLaTeX
\documentclass{article}
\usepackage{unicode-math} % Replaces amsmath/amssymb for font loading

% Choose an OpenType Math Font
% \setmathfont{Latin Modern Math}
% \setmathfont{XITS Math}
\setmathfont{STIX Two Math} % Often a good choice

\begin{document}

Here are symbols using \texttt{unicode-math} (often includes \texttt{amssymb} symbols):

\begin{itemize}
    \item Real numbers: $\symbb{R}$ (or $\mathbb{R}$ still works if the font maps it)
    \item For all: $\forall$
    \item Infinity: $\infty$
    \item Not subset: $\nsubseteq$
    \item Black square: $\blacksquare$
    \item Fraktur $\symfrak{g}$ and Script $\symcal{A}$
\end{itemize}

\end{document}
```

In `unicode-math`, symbols like $\\mathbb{R}$ are often accessed directly, or via their Unicode math aliases (e.g. `\symbb{R}` for blackboard bold R). However, many standard LaTeX commands for these symbols are mapped correctly by `unicode-math` if the font supports them.

In conclusion, you are absolutely right: `\usepackage{amssymb}` is a fundamental package for anyone doing serious mathematical typesetting in LaTeX, especially with pdfLaTeX. For modern XeLaTeX/LuaLaTeX workflows, `unicode-math` often takes its place, providing similar and extended functionality through OpenType math fonts.

--------

HBP.md file:

#Here's a Heading

> [!WARNING]
> Do NOT do this !

HBP.md file:

#Here's a Heading

> [!WARNING]
> Do NOT do this !

# Here's a Heading

> [!IMPORTANT]
> Add spaces between the heading \# sign !

----------


----------

Cc.md file:

The example is :

> You may do ... —
>
>> And You ...... ——




----------

Without blank lines, this might not look right.
> This is a blockquote
Don't do this!

> [!WARNING]
> Do NOT do this !

----

\`Hello, World!\'

\``Hello, World!\''

 !"\#\$\%\&\'\(\)*+,-.\/0123456789\:;\<=\>?

@ABCDEFGHIJKLMNOPQRSTUVWXYZ\[\\\]\^\_

\`abcdefghijklmnopqrstuvwxyz\{\|\}\~

---

 !\"\#\$%&\'\(\)*+,-./0123456789\:;\<=\>?

@ABCDEFGHIJKLMNOPQRSTUVWXYZ\[\\\]^\_

\`abcdefghijklmnopqrstuvwxyz\{\|\}\~

----

&#xFFFF; &#x20AC; &#xFFFF; &#xFFFF; &#x2044; &#x02D9; &#x02DD; &#x02DB;

fl       &#xFFFF; &#x200B; ff       fi       &#xFFFF; ffi      ffl

&#x0131; &#x0237; &#x0060; &#x00B4; &#x02C7; &#x02D8; &#x00AF; &#x02DA;

&#x00B8; &#x00DF; &#x00E6; &#x0153; &#x00F8; &#x00C6; &#x0152; &#x00D8;

&#x0020; \!       \"       \#       \$       %        &#x0026; &#x2019;

\(       \)       \*       \+       ,        \-       \.       /

0        1        2        3        4        5        6        7

8        9        :        ;        \<       \=       \>       ?

@        A        B        C        D        E        F        G

H        I        J        K        L        M        N        O

P        Q        R        S        T        U        V        W

X        Y        Z        \[       \\       \]       &#x02C6; \_

&#x2018; a        b        c        d        e        f        g

h        i        j        k        l        m        n        o

p        q        r        s        t        u        v        w

x        y        z        \{       \|       \}       &#x02DC; &#x00A8;

&#x0141; &#x0027; &#x201A; &#x0192; &#x201E; &#x2026; &#x2020; &#x2021;

&#x02C6; &#x2030; &#x0160; &#x2039; &#x0152; &#x017D; &#x005E; &#x2212;
