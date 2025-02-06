# Baseball Dice Roller

Copyright © 2025 Ken J. https://github.com/kenjij

## Components

- `dice.min.css` - CSS for the dice
- `dice_roller.min.js` - JavaScript file to roll the dice
- [Animate.css](https://animate.style/) - for dice aninimation, only using CSS; verified with v4.1.1
- Your HTML and CSS files

## Setup

### General

Link CSS and JavaScript files.

```html
<!-- Should be in the HTML <head> section -->
<link rel="stylesheet" href="src/animate.min.css">
<link rel="stylesheet" href="src/dice.min.css">
<!-- Add your own CSS as necessary -->

<!-- Should be at the bottom of the HTML <body> section -->
<script src="src/dice_roller.min.js"></script>
```

Optionally, add dice rolling sound effects audio files. Any audio type/length/name is acceptable. The only requirement is to set the class to `dsfx_dice_roll`. When multiple audio files are added, it will play one of them at random.

```html
<audio class="dsfx_dice_roll" src="audio/dice1.mp3" preload="auto"></audio>
<audio class="dsfx_dice_roll" src="audio/dice2.mp3" preload="auto"></audio>
```

### Set of Three 6-Faced Dice

Add the following HTML elements with the necessary classes and id.

```html
<div>
  <div class="d6_face d6_face_white" id="d6_face_0"><span class="d6_pip"></span></div>
  <div class="d6_face d6_face_red" id="d6_face_1"><span class="d6_pip"></span></div>
  <div class="d6_face d6_face_red" id="d6_face_2"><span class="d6_pip"></span></div>
</div>
<button id="d6es_btn_roll">Roll D6es</button>
<!-- Optionally, show history of up to last 3 rolls -->
<ul>
  <li>Current Roll: <span id="d6es_history_0"></span></li>
  <li>Last Roll: <span id="d6es_history_1"></span></li>
  <li>Previous Roll: <span id="d6es_history_2"></span></li>
</ul>
```

### 20-Faced Die

Add the following HTML elements with the necessary classes and id.

```html
<div>
  <div class="d20_face" id="d20_face">
    <div class="d20_triangle"></div>
    <div class="d20_number" id="d20_face_number">1</div>
  </div>
</div>
<button id="d20_btn_roll">Roll D20</button>
<!-- Optionally, show history of up to last 3 rolls -->
<ul>
  <li>Current Roll: <span id="d20_history_0"></span></li>
  <li>Last Roll: <span id="d20_history_1"></span></li>
  <li>Previous Roll: <span id="d20_history_2"></span></li>
</ul>
```

### Inning Outs Indicator

Add the following HTML elements with the necessary classes and id.

```html
<div>
  <div class="outs_indicator" id="outs_indicator">
    <span class="outs_lights_off" id="outs_indicator_1">1</span>
    <span class="outs_lights_off" id="outs_indicator_2">2</span>
    <span class="outs_lights_off" id="outs_indicator_3">3</span>
  </div>
</div>
<button id="outs_indicator_btn_toggle">Out!</button>
```

## Customization

Layout/design elements are all controlled by HTML and CSS. Simply adjust or overwrite to your liking.

## Usage

### Dice

Simply click the **roll** button to roll the dice. Sound effects will play if set up.

History will show the last three rolls in the format of: `A-B`, whereas `A` is the number of the first die and `B` is the sum of the last two dice.

### Outs Indicator

Simply click the **toggle** button to toggle the lights. Each click will increment the lights, in which after all lights are on, the subsequent click will reset the indicator and turn all of the lights off.

### Note

When the page is reloaded/refreshed, everything will be reset/cleared.