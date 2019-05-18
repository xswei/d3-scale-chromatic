# d3-scale-chromatic

这个模块提供了用来表示序列、发散以及分类的颜色方案，它的设计是用来和 [d3-scale](https://github.com/d3/d3-scale) 的 [d3.scaleOrdinal](https://github.com/d3/d3-scale#ordinal-scales) 和 [d3.scaleSequential](https://github.com/d3/d3-scale#sequential-scales) 结合使用。大多数的颜色方案都来自于 `Cynthia A. Brewer` 的 [ColorBrewer](http://colorbrewer2.org)。由于 `ColorBrewer` 只发布了离散的配色方案, 顺序和发散的颜色是通过 [uniform B-splines](https://bl.ocks.org/mbostock/048d21cf747371b11884f75ad896e5a5) 插值得到的。

例如，要使用 [Accent](#schemeAccent) 颜色方案创建分类颜色比例尺：

```js
var accent = d3.scaleOrdinal(d3.schemeAccent);
```

使用 [Blues](#schemeBlues) 颜色方案创建 9 色刻度尺：

```js
var blues = d3.scaleOrdinal(d3.schemeBlues[9]);
```

使用 [PiYG](#interpolatePiYG) 颜色方案撞见发散的、连续的颜色比例尺：

```js
var piyg = d3.scaleSequential(d3.interpolatePiYG);
```

## Installing

使用 `NPM` 安装： `npm install d3-scale-chromatic`. 此外还可以下载 [latest release](https://github.com/d3/d3-scale-chromatic/releases/latest) 或直接从 [d3js.org](https://d3js.org) 以 [standalone library](https://d3js.org/d3-scale-chromatic.v1.min.js) 的方式引入. 支持 `AMD`, `CommonJS`,  和基本的标签使用方式，如果使用标签引用，则会暴露全局 `d3` 变量：

```html
<script src="https://d3js.org/d3-color.v1.min.js"></script>
<script src="https://d3js.org/d3-interpolate.v1.min.js"></script>
<script src="https://d3js.org/d3-scale-chromatic.v1.min.js"></script>
<script>

var yellow = d3.interpolateYlGn(0), // "rgb(255, 255, 229)"
    yellowGreen = d3.interpolateYlGn(0.5), // "rgb(120, 197, 120)"
    green = d3.interpolateYlGn(1); // "rgb(0, 69, 41)"

</script>
```

或者作为 [D3 default bundle](https://github.com/d3/d3) 的一部分:

```html
<script src="https://d3js.org/d3.v5.min.js"></script>
<script>

var yellow = d3.interpolateYlGn(0), // "rgb(255, 255, 229)"
    yellowGreen = d3.interpolateYlGn(0.5), // "rgb(120, 197, 120)"
    green = d3.interpolateYlGn(1); // "rgb(0, 69, 41)"

</script>
```

[在浏览器中测试 d3-scale-chromatic.](https://tonicdev.com/npm/d3-scale-chromatic)

## API Reference

### Categorical

<a name="schemeCategory10" href="#schemeCategory10">#</a> d3.<b>schemeCategory10</b> [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/categorical/category10.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/category10.png" width="100%" height="40" alt="category10">

十个分类颜色的数组，表示为 `RGB` 十六进制字符串。

<a href="#schemeAccent" name="schemeAccent">#</a> d3.<b>schemeAccent</b> [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/categorical/Accent.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Accent.png" width="100%" height="40" alt="Accent">

八个分类颜色的数组，表示为 `RGB` 十六进制字符串。

<a href="#schemeDark2" name="schemeDark2">#</a> d3.<b>schemeDark2</b> [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/categorical/Dark2.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Dark2.png" width="100%" height="40" alt="Dark2">

八个分类颜色的数组，表示为 `RGB` 十六进制字符串。

<a href="#schemePaired" name="schemePaired">#</a> d3.<b>schemePaired</b> [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/categorical/Paired.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Paired.png" width="100%" height="40" alt="Paired">

十二种分类颜色的数组，表示为 `RGB` 十六进制字符串。

<a href="#schemePastel1" name="schemePastel1">#</a> d3.<b>schemePastel1</b> [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/categorical/Pastel1.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Pastel1.png" width="100%" height="40" alt="Pastel1">

十二种分类颜色的数组，表示为 `RGB` 十六进制字符串。

<a href="#schemePastel2" name="schemePastel2">#</a> d3.<b>schemePastel2</b> [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/categorical/Pastel2.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Pastel2.png" width="100%" height="40" alt="Pastel2">

八个分类颜色的数组，表示为 `RGB` 十六进制字符串。

<a href="#schemeSet1" name="schemeSet1">#</a> d3.<b>schemeSet1</b> [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/categorical/Set1.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Set1.png" width="100%" height="40" alt="Set1">

九个分类颜色的数组，表示为 `RGB` 十六进制字符串。

<a href="#schemeSet2" name="schemeSet2">#</a> d3.<b>schemeSet2</b> [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/categorical/Set2.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Set2.png" width="100%" height="40" alt="Set2">

八个分类颜色的数组，表示为 `RGB` 十六进制字符串。

<a href="#schemeSet3" name="schemeSet3">#</a> d3.<b>schemeSet3</b> [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/categorical/Set3.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Set3.png" width="100%" height="40" alt="Set3">

十二种分类颜色的数组，表示为 `RGB` 十六进制字符串。

### Diverging

发散的颜色方案可以用作连续型插值器（通常与[d3.scaleSequential](https://github.com/d3/d3-scale/blob/master/README.md#sequential-scales)一起使用）和离散方案（通常与 [d3.scaleOrdinal](https://github.com/d3/d3-scale/blob/master/README.md#ordinal-scales) 一起使用）。每一个离散方案，比如 [d3.schemeBrBG](#schemeBrBG), 被表示为十六进制颜色字符串数组的数组。数组的第 *k* 个元素表示包含大小为 *k* 的颜色方案; 例如 `d3.schemeBrBG[9]` 包含了 9 个字符串表示的颜色，表示从 `brown` 到 `blue` 到 `green` 的颜色方案。离散颜色方案支持的 *k* 大小为从 3 到 11.

<a href="#interpolateBrBG" name="interpolateBrBG">#</a> d3.<b>interpolateBrBG</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/diverging/BrBG.js "Source")
<br><a href="#schemeBrBG" name="schemeBrBG">#</a> d3.<b>schemeBrBG</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/BrBG.png" width="100%" height="40" alt="BrBG">

给定一个范围在 [0,1] 的值 *t*，返回一个经过 “BrBG” 颜色方案插值后对应的值，以 `RGB` 字符串表示。

<a href="#interpolatePRGn" name="interpolatePRGn">#</a> d3.<b>interpolatePRGn</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/diverging/PRGn.js "Source")
<br><a href="#schemePRGn" name="schemePRGn">#</a> d3.<b>schemePRGn</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/PRGn.png" width="100%" height="40" alt="PRGn">

给定一个范围在 [0,1] 的值 *t*，返回一个经过 “PRGn” 颜色方案插值后对应的值，以 `RGB` 字符串表示。

<a href="#interpolatePiYG" name="interpolatePiYG">#</a> d3.<b>interpolatePiYG</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/diverging/PiYG.js "Source")
<br><a href="#schemePiYG" name="schemePiYG">#</a> d3.<b>schemePiYG</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/PiYG.png" width="100%" height="40" alt="PiYG">

给定一个范围在 [0,1] 的值 *t*，返回一个经过 “PiYG” 颜色方案插值后对应的值，以 `RGB` 字符串表示。

<a href="#interpolatePuOr" name="interpolatePuOr">#</a> d3.<b>interpolatePuOr</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/diverging/PuOr.js "Source")
<br><a href="#schemePuOr" name="schemePuOr">#</a> d3.<b>schemePuOr</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/PuOr.png" width="100%" height="40" alt="PuOr">

给定一个范围在 [0,1] 的值 *t*，返回一个经过 “PuOr” 颜色方案插值后对应的值，以 `RGB` 字符串表示。

<a href="#interpolateRdBu" name="interpolateRdBu">#</a> d3.<b>interpolateRdBu</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/diverging/RdBu.js "Source")
<br><a href="#schemeRdBu" name="schemeRdBu">#</a> d3.<b>schemeRdBu</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/RdBu.png" width="100%" height="40" alt="RdBu">

给定一个范围在 [0,1] 的值 *t*，返回一个经过 “RdBu” 颜色方案插值后对应的值，以 `RGB` 字符串表示。

<a href="#interpolateRdGy" name="interpolateRdGy">#</a> d3.<b>interpolateRdGy</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/diverging/RdGy.js "Source")
<br><a href="#schemeRdGy" name="schemeRdGy">#</a> d3.<b>schemeRdGy</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/RdGy.png" width="100%" height="40" alt="RdGy">

给定一个范围在 [0,1] 的值 *t*，返回一个经过 “RdGy” 颜色方案插值后对应的值，以 `RGB` 字符串表示。

<a href="#interpolateRdYlBu" name="interpolateRdYlBu">#</a> d3.<b>interpolateRdYlBu</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/diverging/RdYlBu.js "Source")
<br><a href="#schemeRdYlBu" name="schemeRdYlBu">#</a> d3.<b>schemeRdYlBu</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/RdYlBu.png" width="100%" height="40" alt="RdYlBu">

给定一个范围在 [0,1] 的值 *t*，返回一个经过 “RdYlBu” 颜色方案插值后对应的值，以 `RGB` 字符串表示。

<a href="#interpolateRdYlGn" name="interpolateRdYlGn">#</a> d3.<b>interpolateRdYlGn</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/diverging/RdYlGn.js "Source")
<br><a href="#schemeRdYlGn" name="schemeRdYlGn">#</a> d3.<b>schemeRdYlGn</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/RdYlGn.png" width="100%" height="40" alt="RdYlGn">

给定一个范围在 [0,1] 的值 *t*，返回一个经过 “RdYlGn” 颜色方案插值后对应的值，以 `RGB` 字符串表示。

<a href="#interpolateSpectral" name="interpolateSpectral">#</a> d3.<b>interpolateSpectral</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/diverging/Spectral.js "Source")
<br><a href="#schemeSpectral" name="schemeSpectral">#</a> d3.<b>schemeSpectral</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Spectral.png" width="100%" height="40" alt="Spectral">

给定一个范围在 [0,1] 的值 *t*，返回一个经过 “Spectral” 颜色方案插值后对应的值，以 `RGB` 字符串表示。

### Sequential (Single Hue)

顺序，单色调的颜色方案适合作为连续型插值（通常与 [d3.scaleSequential](https://github.com/d3/d3-scale/blob/master/README.md#sequential-scales)结合使用）和离散方案 (通常与 [d3.scaleOrdinal](https://github.com/d3/d3-scale/blob/master/README.md#ordinal-scales) 结合使用)。每一个离散方案，比如 [d3.schemeBlues](#schemeBlues)，被表示为十六进制颜色字符串数组的数组。数组的第 *k* 个元素表示包含大小为 *k* 的颜色方案; 例如 `d3.schemeBlues[9]` 包含了 9 个字符串表示的 `blue` 系列颜色。顺序的多个色调的颜色方案支持的 *k* 值为从 3 到 9.

<a href="#interpolateBlues" name="interpolateBlues">#</a> d3.<b>interpolateBlues</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-single/Blues.js "Source")
<br><a href="#schemeBlues" name="schemeBlues">#</a> d3.<b>schemeBlues</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Blues.png" width="100%" height="40" alt="Blues">

根据给定的位于 [0, 1] 的值 *t*，返回 “Blues” 色调对应的插值颜色，以 `RGB` 字符串表示。

<a href="#interpolateGreens" name="interpolateGreens">#</a> d3.<b>interpolateGreens</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-single/Greens.js "Source")
<br><a href="#schemeGreens" name="schemeGreens">#</a> d3.<b>schemeGreens</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Greens.png" width="100%" height="40" alt="Greens">

根据给定的位于 [0, 1] 的值 *t*，返回 “Greens” 色调对应的插值颜色，以 `RGB` 字符串表示。

<a href="#interpolateGreys" name="interpolateGreys">#</a> d3.<b>interpolateGreys</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-single/Greys.js "Source")
<br><a href="#schemeGreys" name="schemeGreys">#</a> d3.<b>schemeGreys</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Greys.png" width="100%" height="40" alt="Greys">

根据给定的位于 [0, 1] 的值 *t*，返回 “Greys” 色调对应的插值颜色，以 `RGB` 字符串表示。

<a href="#interpolateOranges" name="interpolateOranges">#</a> d3.<b>interpolateOranges</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-single/Oranges.js "Source")
<br><a href="#schemeOranges" name="schemeOranges">#</a> d3.<b>schemeOranges</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Oranges.png" width="100%" height="40" alt="Oranges">

根据给定的位于 [0, 1] 的值 *t*，返回 “Oranges” 色调对应的插值颜色，以 `RGB` 字符串表示。

<a href="#interpolatePurples" name="interpolatePurples">#</a> d3.<b>interpolatePurples</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-single/Purples.js "Source")
<br><a href="#schemePurples" name="schemePurples">#</a> d3.<b>schemePurples</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Purples.png" width="100%" height="40" alt="Purples">

根据给定的位于 [0, 1] 的值 *t*，返回 “Purples” 色调对应的插值颜色，以 `RGB` 字符串表示。

<a href="#interpolateReds" name="interpolateReds">#</a> d3.<b>interpolateReds</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-single/Reds.js "Source")
<br><a href="#schemeReds" name="schemeReds">#</a> d3.<b>schemeReds</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/Reds.png" width="100%" height="40" alt="Reds">

根据给定的位于 [0, 1] 的值 *t*，返回 “Reds” 色调对应的插值颜色，以 `RGB` 字符串表示。

### Sequential (Multi-Hue)

顺序，多色调的颜色方案适合作为连续型插值（通常与 [d3.scaleSequential](https://github.com/d3/d3-scale/blob/master/README.md#sequential-scales)结合使用）和离散方案 (通常与 [d3.scaleOrdinal](https://github.com/d3/d3-scale/blob/master/README.md#ordinal-scales) 结合使用)。每一个离散方案，比如 [d3.schemeBuGn](#schemeBuGn)，被表示为十六进制颜色字符串数组的数组。数组的第 *k* 个元素表示包含大小为 *k* 的颜色方案; 例如 `d3.schemeBuGn[9]` 包含了 9 个字符串表示的 `blue` 到 `green` 色调的颜色方案。顺序，多个色调的颜色方案支持的 *k* 值为从 3 到 9.

<a name="interpolateViridis" href="#interpolateViridis">#</a> d3.<b>interpolateViridis</b>(<i>t</i>) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/viridis.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/viridis.png" width="100%" height="40" alt="viridis">

根据给定的位于 [0, 1] 之间的值 *t*，返回一个经 [van der Walt, Smith and Firing](https://bids.github.io/colormap/) 为 `matplotlib` 设计的 “viridis” 颜色方案插值后的颜色值，表示为 `RGB` 字符串。

<a name="interpolateInferno" href="#interpolateInferno">#</a> d3.<b>interpolateInferno</b>(<i>t</i>) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/viridis.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/inferno.png" width="100%" height="40" alt="inferno">

根据给定的位于 [0, 1] 之间的值 *t*，返回一个经 [van der Walt, Smith and Firing](https://bids.github.io/colormap/) 为 `matplotlib` 设计的 “inferno” 颜色方案插值后的颜色值，表示为 `RGB` 字符串。

<a name="interpolateMagma" href="#interpolateMagma">#</a> d3.<b>interpolateMagma</b>(<i>t</i>) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/viridis.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/magma.png" width="100%" height="40" alt="magma">

根据给定的位于 [0, 1] 之间的值 *t*，返回一个经 [van der Walt, Smith and Firing](https://bids.github.io/colormap/) 为 `matplotlib` 设计的 “magma” 颜色方案插值后的颜色值，表示为 `RGB` 字符串。

<a name="interpolatePlasma" href="#interpolatePlasma">#</a> d3.<b>interpolatePlasma</b>(<i>t</i>) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/viridis.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/plasma.png" width="100%" height="40" alt="plasma">

根据给定的位于 [0, 1] 之间的值 *t*，返回一个经 [van der Walt, Smith and Firing](https://bids.github.io/colormap/) 为 `matplotlib` 设计的 “plasma” 颜色方案插值后的颜色值，表示为 `RGB` 字符串。

<a name="interpolateWarm" href="#interpolateWarm">#</a> d3.<b>interpolateWarm</b>(<i>t</i>) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/rainbow.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/warm.png" width="100%" height="40" alt="warm">

根据给定的位于 [0, 1] 之间的值 *t*，返回经过 [Niccoli’s perceptual rainbow](https://mycarta.wordpress.com/2013/02/21/perceptual-rainbow-palette-the-method/) 旋转 180 度后的颜色值，表示为 `RGB` 字符串。

<a name="interpolateCool" href="#interpolateCool">#</a> d3.<b>interpolateCool</b>(<i>t</i>) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/rainbow.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/cool.png" width="100%" height="40" alt="cool">

根据给定的位于 [0, 1] 之间的值 *t*，返回 [Niccoli’s perceptual rainbow](https://mycarta.wordpress.com/2013/02/21/perceptual-rainbow-palette-the-method/) 颜色值，表示为 `RGB` 字符串。

<a name="interpolateCubehelixDefault" href="#interpolateCubehelixDefault">#</a> d3.<b>interpolateCubehelixDefault</b>(<i>t</i>) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/cubehelix.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/cubehelix.png" width="100%" height="40" alt="cubehelix">

根据给定的位于 [0, 1] 之间的值 *t*，返回 [Green’s default Cubehelix](https://www.mrao.cam.ac.uk/~dag/CUBEHELIX/)  颜色值，表示为 `RGB` 字符串。

<a href="#interpolateBuGn" name="interpolateBuGn">#</a> d3.<b>interpolateBuGn</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/BuGn.js "Source")
<br><a href="#schemeBuGn" name="schemeBuGn">#</a> d3.<b>schemeBuGn</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/BuGn.png" width="100%" height="40" alt="BuGn">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “BuGn” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolateBuPu" name="interpolateBuPu">#</a> d3.<b>interpolateBuPu</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/BuPu.js "Source")
<br><a href="#schemeBuPu" name="schemeBuPu">#</a> d3.<b>schemeBuPu</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/BuPu.png" width="100%" height="40" alt="BuPu">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “BuPu” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolateGnBu" name="interpolateGnBu">#</a> d3.<b>interpolateGnBu</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/GnBu.js "Source")
<br><a href="#schemeGnBu" name="schemeGnBu">#</a> d3.<b>schemeGnBu</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/GnBu.png" width="100%" height="40" alt="GnBu">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “GnBu” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolateOrRd" name="interpolateOrRd">#</a> d3.<b>interpolateOrRd</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/OrRd.js "Source")
<br><a href="#schemeOrRd" name="schemeOrRd">#</a> d3.<b>schemeOrRd</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/OrRd.png" width="100%" height="40" alt="OrRd">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “OrRd” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolatePuBuGn" name="interpolatePuBuGn">#</a> d3.<b>interpolatePuBuGn</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/PuBuGn.js "Source")
<br><a href="#schemePuBuGn" name="schemePuBuGn">#</a> d3.<b>schemePuBuGn</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/PuBuGn.png" width="100%" height="40" alt="PuBuGn">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “PuBuGn” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolatePuBu" name="interpolatePuBu">#</a> d3.<b>interpolatePuBu</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/PuBu.js "Source")
<br><a href="#schemePuBu" name="schemePuBu">#</a> d3.<b>schemePuBu</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/PuBu.png" width="100%" height="40" alt="PuBu">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “PuBu” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolatePuRd" name="interpolatePuRd">#</a> d3.<b>interpolatePuRd</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/PuRd.js "Source")
<br><a href="#schemePuRd" name="schemePuRd">#</a> d3.<b>schemePuRd</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/PuRd.png" width="100%" height="40" alt="PuRd">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “PuRd” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolateRdPu" name="interpolateRdPu">#</a> d3.<b>interpolateRdPu</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/RdPu.js "Source")
<br><a href="#schemeRdPu" name="schemeRdPu">#</a> d3.<b>schemeRdPu</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/RdPu.png" width="100%" height="40" alt="RdPu">


根据给定的位于 [0, 1] 之间的值 *t*，返回 “RdPu” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolateYlGnBu" name="interpolateYlGnBu">#</a> d3.<b>interpolateYlGnBu</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/YlGnBu.js "Source")
<br><a href="#schemeYlGnBu" name="schemeYlGnBu">#</a> d3.<b>schemeYlGnBu</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/YlGnBu.png" width="100%" height="40" alt="YlGnBu">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “YlGnBu” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolateYlGn" name="interpolateYlGn">#</a> d3.<b>interpolateYlGn</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/YlGn.js "Source")
<br><a href="#schemeYlGn" name="schemeYlGn">#</a> d3.<b>schemeYlGn</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/YlGn.png" width="100%" height="40" alt="YlGn">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “YlGn” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolateYlOrBr" name="interpolateYlOrBr">#</a> d3.<b>interpolateYlOrBr</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/YlOrBr.js "Source")
<br><a href="#schemeYlOrBr" name="schemeYlOrBr">#</a> d3.<b>schemeYlOrBr</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/YlOrBr.png" width="100%" height="40" alt="YlOrBr">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “YlOrBr” 颜色方案值，表示为 `RGB` 字符串。

<a href="#interpolateYlOrRd" name="interpolateYlOrRd">#</a> d3.<b>interpolateYlOrRd</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/YlOrRd.js "Source")
<br><a href="#schemeYlOrRd" name="schemeYlOrRd">#</a> d3.<b>schemeYlOrRd</b>[*k*]

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/YlOrRd.png" width="100%" height="40" alt="YlOrRd">

根据给定的位于 [0, 1] 之间的值 *t*，返回 “YlOrRd” 颜色方案值，表示为 `RGB` 字符串。

### Cyclical

<a name="interpolateRainbow" href="#interpolateRainbow">#</a> d3.<b>interpolateRainbow</b>(<i>t</i>) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/rainbow.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/rainbow.png" width="100%" height="40" alt="rainbow">

根据给定的位于 [0, 1] 之间的值 *t*，返回插值范围在 [0.0, 0.5] 的 [d3.interpolateWarm](#interpolateWarm) 和 插值范围在 [0.5, 1.0] 的 [d3.interpolateCool](#interpolateCool) 组成的颜色方案插值后的颜色值。

<a name="interpolateSinebow" href="#interpolateSinebow">#</a> d3.<b>interpolateSinebow</b>(<i>t</i>) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/sinebow.js "Source")

<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/sinebow.png" width="100%" height="40" alt="sinebow">

根据给定的位于 [0, 1] 之间的值 *t*，返回由 [Jim Bumgardner](https://krazydad.com/tutorials/makecolors.php) 和 [Charlie Loyd](http://basecase.org/env/on-rainbows) 组成的 “sinebow” 颜色方案对应的颜色值。