# The way of use fonts

## Demo

### 01

Example 01 contains a website that use fonts without any optimization.

[Link](./01/index.html)

### 02

Example 02 contains a website with the best format for the fonts that is right now woff2.

We will use [fonttools](https://github.com/fonttools/fonttools) to convert fonts to woff2 format.

```bash
# Installing fonttools
pip install fonttools # or brew install fonttools

# Installing brotli
pip install brotli # or brew install brotli

# Compresing using brotli a TTF font to WOFF2
fonttools ttLib ./01/fonts/Roboto-Regular.ttf --flavor woff2 -o ./01/fonts/Roboto-Regular.woff2
```

[Link](./02/index.html)

## 03

Example 02 contains a website using variable fonts instead of multilple static fonts.

Instead of using multiple static fonts, you can use a single variable font that contains all the styles.

```bash
# Compresing using brotli a TTF font to WOFF2
fonttools ttLib ./03/fonts/Roboto-VariableFont.ttf --flavor woff2 -o ./03/fonts/Roboto-VariableFont.woff2
```

[Link](./03/index.html)

### 04

Example 04 contains a website using subsetting fonts.

```bash
# Removing unused axis
fonttools varLib.instancer ./04/fonts/Roboto-VariableFont.woff2 wdth=100 wght=100:900

# Subsetting the font using fonttools with Latin charset and removing all layout features
pyftsubset ./04/fonts/Roboto-VariableFont-partial.woff2 --unicodes="U+000-5FF" --layout-features="" --flavor="woff2"

# Or you can subset the font using a specific file
pyftsubset ./04/fonts/Roboto-VariableFont-partial.woff2 --text-file="./04/index.html" --layout-features="" --flavor="woff2"
```

[Link](./04/index.html)

### 05

Example 05 contains a website using a good fallback values.

We will use [fontpie](https://github.com/pixel-point/fontpie) to generate the fallback values.

```bash
# Using bunx
bunx fontpie ./05/fonts/RobotoCondensed-Black.woff2 --name RobotoCondensed --weight 900

# Using npx
npx fontpie ./05/fonts/RobotoCondensed-Black.woff2 --name RobotoCondensed --weight 900

# Using pnpx
pnpx fontpie ./05/fonts/RobotoCondensed-Black.woff2 --name RobotoCondensed --weight 900
```

[Link](./05/index.html)

### 06

Example 06 contains a website using a good [font-display](https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face/font-display) value.

[Link](./06/index.html)

### 07

Example 07 contains a website loading [fonts asynchronously](https://www.filamentgroup.com/lab/load-css-simpler/).

[Link](./07/index.html)

### 08

Example 08 contains a website [preload](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/preload) in fonts.

[Link](./08/index.html)

### 09 - Extra

Example 09 contains a website using [preconnect](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/preconnect) for external fonts (like Google Fonts).

## Resources

- [csswizardry.com: Speed Up Google Fonts](https://csswizardry.com/2020/05/the-fastest-google-fonts/)
- [web.dev: Prevent layout shifting and flashes of invisible text (FOIT) by preloading optional fonts](https://web.dev/articles/preload-optional-fonts)
- [web.dev: Preload web fonts to improve loading speed](https://web.dev/articles/codelab-preload-web-fonts)
- [web.dev: Optimize WebFont loading and rendering](https://web.dev/articles/optimize-webfont-loading)
- [web.dev: Optimize web fonts](https://web.dev/learn/performance/optimize-web-fonts)
- [web.dev: Reduce web font size](https://web.dev/articles/reduce-webfont-size)
- [Roboto Font](https://fonts.google.com/specimen/Roboto)
- [Roboto Condensed Font](https://fonts.google.com/specimen/Roboto+Condensed)