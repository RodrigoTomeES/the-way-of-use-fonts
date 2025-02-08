# The way of use fonts

## 01

Example 01 contains a website that use fonts without any optimization.

[Link](./01/index.html)

## 02

Example 02 contains a website with the best format for the fonts that is right now woff2.

You can use font-convert npm package to convert fonts to woff2 format.

```bash
# Using bun
bunx @hayes0724/web-font-converter font-convert --pathIn='./02/fonts/Roboto-Regular.ttf' --pathOut='./02/fonts/Roboto-Regular.woff2'

# Using npx
npx @hayes0724/web-font-converter font-convert --pathIn='./02/fonts/Roboto-Regular.ttf' --pathOut='./02/fonts/Roboto-Regular.woff2'

# Using pnpx
pnpx @hayes0724/web-font-converter font-convert --pathIn='./02/fonts/Roboto-Regular.ttf' --pathOut='./02/fonts/Roboto-Regular.woff2'
```

[Link](./02/index.html)

## 03

Example 02 contains a website using variable fonts instead of multilple static fonts.

Instead of using multiple static fonts, you can use a single variable font that contains all the styles.

```bash
# Using bun
bunx @hayes0724/web-font-converter font-convert --pathIn='./03/fonts/Roboto-VariableFont.ttf' --pathOut='./03/fonts/Roboto-VariableFont.woff2'

# Using npx
npx @hayes0724/web-font-converter font-convert --pathIn='./03/fonts/Roboto-VariableFont.ttf' --pathOut='./03/fonts/Roboto-VariableFont.woff2'

# Using pnpx
pnpx @hayes0724/web-font-converter font-convert --pathIn='./03/fonts/Roboto-VariableFont.ttf' --pathOut='./03/fonts/Roboto-VariableFont.woff2'
```

[Link](./03/index.html)

## 04

Example 04 contains a website using subsetting fonts.

## 05

Example 05 contains a website using a good fallback values.

## 06

Example 06 contains a website using a good font-display value.

## 07

Example 07 contains a website loading fonts asynchronously.

## 08

Example 08 contains a website preloading fonts.

## 09 - Extra

Example 09 contains a website using preconnect for external fonts (like Google Fonts).
