# Sass autoResize function using clamp

Use this function with sizes params on scss
<br>
for example:
```scss
font-size
line-height
width
margin
padding

```
Function `autoResize` return `clamp`
## Usage
### Step 1: Copy file <i>autoResize.scss</i> to your project
The file is located at path <i>/src/styles/autoresize.scss</i>
<br>
Copy it to your project

### Step 2: Import file to your scss file
```scss
@import "./styles/autoResize";
```

### Step 3: Use function autoResize

```scss
.className {
  // autoResize($minSize, $maxSize, $minWidthPx, $maxWidthPx, $pixelsPerRem)
  // result: clamp(0.625rem, calc(-1.78571rem + 10.71429vw), 6.25rem)
  
  font-size: autoResize(10px, 100px, 360px, 1200px, 16px);
  width: autoResize(120, 360, 500, 960);
  padding: autoResize(120, 360);
  margin: autoResize(120)
  
}
```
## Parameters
```scss
 autoResize($minSize, $maxSize, $minWidthPx, $maxWidthPx, $pixelsPerRem)
 ```

| Header              | Required | Default value       | Description             |
| ------------------- | -------- | ------------------- | ----------------------- |
| `$minSize`          |  `true`  | | Minimum font size |
| `$maxSize`          |  `false` | `$minSize`          | Maximum font size       |
| `$minWidthPx`       |  `false` | `360px`             | Maximum font size       |
| `$maxWidthPx`       |  `false` | `960px`             | Minimum viewport width  |
| `$pixelsPerRem`     |  `false` | `16pp`              | Maximum viewport width  |

Unit `px` is optional
<br>
You can use 
<br>
`autoResize(10px, 100px, 360px, 1200px);`
<br> - or - <br> 
`autoResize(10, 100, 360, 1200)`



#.
