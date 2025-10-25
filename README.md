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

&#x0142; &#x2018; &#x2019; &#x201C; &#x201D; &#x2022; --       ---

&#x02DC; &#x2122; &#x0161; &#x203A; &#x0153; &#x017E; &#x007E; &#x0178;

&#x00A0; &#x00A1; &#x00A2; &#x00A3; &#x00A4; &#x00A5; &#x00A6; &#x00A7;

&#x00A8; &#x00A9; &#x00AA; &#x00AB; &#x00AC; &#x00AD; &#x00AE; &#x00AF;

&#x00B0; &#x00B1; &#x00B2; &#x00B3; &#x00B4; &#x00B5; &#x00B6; &#x00B7;

&#x00B8; &#x00B9; &#x00BA; &#x00BB; &#x00BC; &#x00BD; &#x00BE; &#x00BF;

&#x00C0; &#x00C1; &#x00C2; &#x00C3; &#x00C4; &#x00C5; &#x00C6; &#x00C7;

&#x00C8; &#x00C9; &#x00CA; &#x00CB; &#x00CC; &#x00CD; &#x00CE; &#x00CF;

&#x00D0; &#x00D1; &#x00D2; &#x00D3; &#x00D4; &#x00D5; &#x00D6; &#x00D7;

&#x00D8; &#x00D9; &#x00DA; &#x00DB; &#x00DC; &#x00DD; &#x00DE; &#x00DF;

&#x00E0; &#x00E1; &#x00E2; &#x00E3; &#x00E4; &#x00E5; &#x00E6; &#x00E7;

&#x00E8; &#x00E9; &#x00EA; &#x00EB; &#x00EC; &#x00ED; &#x00EE; &#x00EF;

&#x00F0; &#x00F1; &#x00F2; &#x00F3; &#x00F4; &#x00F5; &#x00F6; &#x00F7;

&#x00F8; &#x00F9; &#x00FA; &#x00FB; &#x00FC; &#x00FD; &#x00FE; &#x00FF;

> [!IMPORTANT]
> **THIS SITE IS NOT OPEN SOURCE -- DO NOT EDIT**
> 
> WE CAN MAKE CHANGES IF WE WANT TO. OTHER FILES ARE OPEN SOURCE.

You're diving into an advanced and very relevant topic for web typography and mathematical display\! Combining SF Pro Rounded for general text and STIX Two Math for equations **via MathJax and MathML embedding** is absolutely possible and often a desired setup for modern web applications.

Let's break down the "how" and the "embed in the web font" aspect.

### The Challenge of Web Fonts for Math

The core challenge when displaying math on the web, even with MathML, is that browsers need to know not just *what* characters to display, but *how* to lay them out. This "how" information (metrics for superscripts, subscripts, fraction bar thickness, operator stretching, etc.) is contained in the **OpenType `MATH` table** within a font file. Few fonts have this table, and even fewer browsers fully leverage it natively.

This is where **MathJax** comes in.

### Using SF Pro Rounded for General Text

SF Pro Rounded is available as a web font, though its licensing from Apple is typically tied to Apple's platforms. If you have the appropriate licensing or are developing for an Apple-centric web environment, you can embed it like any other web font using `@font-face` in your CSS:

```css
@font-face {
  font-family: 'SF Pro Rounded';
  src: url('path/to/SF-Pro-Rounded-Regular.woff2') format('woff2');
  font-weight: normal;
  font-style: normal;
  /* Add other weights/styles as needed */
}

body {
  font-family: 'SF Pro Rounded', sans-serif;
}
```

**Important Note on Licensing:** Be very careful about the licensing of SF Pro Rounded outside of Apple's ecosystem. Using it on a public website might violate Apple's EULA unless explicitly permitted.

### Using STIX Two Math for Math Display via MathJax

This is where the magic happens. MathJax is designed to handle the complex rendering of mathematical expressions on the web.

1.  **MathJax's Role:** MathJax renders mathematical content (from LaTeX, MathML, or AsciiMath) into HTML/CSS, SVG, or Native MathML (if the browser supports it well). For the HTML/CSS and SVG output, MathJax needs its *own* font data because browsers don't expose the OpenType `MATH` table information to JavaScript directly. This is why you can't just tell MathJax to use *any* font with a `MATH` table; MathJax needs pre-processed font metrics.

2.  **STIX Two Math in MathJax v3:**

      * **MathJax v2** had built-in support for STIX General (the predecessor to STIX Two).
      * **MathJax v3** has a redesigned font architecture. Initially, it primarily supported the "MathJax TeX" font. However, support for **STIX Two Math** (and other OpenType math fonts) is a major goal and has been implemented or is actively being integrated into MathJax v3 (check the latest MathJax documentation, as font support continues to evolve).
      * When MathJax v3 uses STIX Two Math, it will download its own highly optimized **web font files** (e.g., in WOFF/WOFF2 format) that it ships with or can access from a CDN. These web fonts are accompanied by the necessary font metric data that MathJax pre-generates.

3.  **Configuring MathJax for STIX Two Math:**
    You would configure MathJax in your HTML to use STIX Two Math. The exact configuration depends on your MathJax version and desired output.

    For example, with MathJax v3, for SVG output, you might have something like (check official docs for the most current configuration):

    ```html
    <script>
      MathJax = {
        tex: {
          inlineMath: [['$', '$'], ['\\(', '\\)']]
        },
        // For SVG output, where MathJax controls font rendering
        svg: {
          fontCache: 'global', // 'global' or 'none'
          font: 'STIXTwoMath' // Or whatever the official MathJax name for STIX Two Math is
        },
        // For CommonHTML output, which also relies on MathJax's fonts
        chtml: {
          fontURL: 'https://cdn.jsdelivr.net/npm/mathjax@3/es5/output/chtml/fonts/woff-v2' // Example URL for MathJax's fonts
        },
        options: {
          renderActions: {
            add: [
              // You might need custom rules if you want SF Pro Rounded within certain MathML elements
              // This gets complex, usually you let MathJax handle its own math fonts.
            ]
          }
        }
      };
    </script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-svg.js"></script>
    ```

    **Crucial Point:** When MathJax renders math (especially in HTML/CSS or SVG output), it typically takes full control of the fonts for the mathematical characters. It won't try to use your `SF Pro Rounded` for math variables or operators because `SF Pro Rounded` doesn't have the `MATH` table data MathJax needs for correct layout. MathJax will use its bundled STIX Two Math web fonts.

### MathML and Web Fonts

You specifically mentioned "MathML." There are two main ways MathJax interacts with MathML:

1.  **MathML as Input:** MathJax can process MathML code directly and then *render it* using its own output processors (HTML/CSS, SVG). In this case, MathJax's font configuration (e.g., to use STIX Two Math) takes precedence for the rendered math.
2.  **Native MathML Output:** Some browsers (Firefox, Safari) have native MathML rendering capabilities. If MathJax is configured for `NativeMML` output, or if you serve raw MathML without MathJax, then the browser's native MathML engine is responsible for rendering.
      * For native MathML, you *can* try to control the math font using CSS `font-family` on `<math>` elements.
      * **Example for Native MathML:**
        ```css
        @font-face {
          font-family: 'STIX Two Math';
          src: url('path/to/STIXTwoMath-Regular.woff2') format('woff2');
          /* Note: You need a web-font version of STIX Two Math here */
        }
        math {
          font-family: 'STIX Two Math', serif; /* Or other fallback math fonts */
        }
        ```
      * **Challenges with Native MathML and Custom Fonts:**
          * **Browser Consistency:** Native MathML rendering varies significantly across browsers (Chrome has limited native support).
          * **Font Support:** Browsers need fonts with a proper `MATH` table to render MathML correctly. STIX Two Math is one of the best for this.
          * **Web Font Embedding:** You would need to ensure the STIX Two Math font (and its various forms, including italics for variables) is correctly embedded as a web font.

### Embedding Fonts in the Web

To address "Embed in the Web Font ??":

Yes, both SF Pro Rounded (for text) and STIX Two Math (for MathJax's rendering or native MathML) need to be available as **web fonts** (typically `.woff` or `.woff2` formats) and referenced via `@font-face` rules in your CSS.

  * **SF Pro Rounded:** You'd link to its `woff2` files for your general `font-family` property.
  * **STIX Two Math:**
      * **For MathJax (recommended):** MathJax handles its own font delivery. It has pre-packaged web fonts for STIX Two Math (or its predecessors) that it downloads as needed from a CDN. You just configure MathJax to use them.
      * **For Native MathML:** You would explicitly `@font-face` the `STIX Two Math` web font files (e.g., from the official STIX Two GitHub or a CDN that hosts them) and then apply `font-family: 'STIX Two Math';` to your `<math>` elements.

**In summary:**

Using **SF Pro Rounded for general text** and **STIX Two Math for math display via MathJax** is a highly effective and robust strategy for web content. MathJax's built-in font handling for STIX Two Math means it intelligently manages the complex mathematical layout. For the general text, you embed SF Pro Rounded as a regular web font. If you decide to rely on native MathML, you'd be more responsible for directly embedding STIX Two Math as a web font and configuring CSS for `<math>` elements, but this approach comes with more cross-browser compatibility challenges than using MathJax.

Now this site is OPEN SOURCE! YOU CAN—
