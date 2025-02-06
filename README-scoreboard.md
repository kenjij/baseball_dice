# Baseball Scoreboard

Copyright © 2025 Ken J. https://github.com/kenjij

## Components

- `scoreboard.min.css` - CSS for the scoreboard
- `scoreboard.min.js` - JavaScript file to operate the scoreboard
- Your HTML and CSS files

## Setup

### General

Link CSS and JavaScript files.

```html
<!-- Should be in the HTML <head> section -->
<link rel="stylesheet" href="src/scoreboard.min.css">
<!-- Add your own CSS as necessary -->

<!-- Should be at the bottom of the HTML <body> section -->
<script src="src/scoreboard.min.js"></script>
```

### The Scoreboard

Add the following HTML elements with the necessary classes and id.

```html
<div>
  <table class="sb_tbl_scoreboard">
    <thead>
      <th class="sb_col_team">Team</th>
      <th class="sb_col_inning_score">1</th>
      <th class="sb_col_inning_score">2</th>
      <th class="sb_col_inning_score">3</th>
      <th class="sb_col_total_score">Total</th>
    </thead>
    <tbody>
      <tr>
        <td class="sb_team_name sb_team_a">A</td>
        <td class="sb_inning_score sb_team_a"></td>
        <td class="sb_inning_score sb_team_a"></td>
        <td class="sb_inning_score sb_team_a"></td>
        <td class="sb_score_total sb_team_a" id="sb_score_total_a"></td>
      </tr>
      <tr>
        <td class="sb_team_name sb_team_b">B</td>
        <td class="sb_inning_score sb_team_b"></td>
        <td class="sb_inning_score sb_team_b"></td>
        <td class="sb_inning_score sb_team_b"></td>
        <td class="sb_score_total sb_team_b" id="sb_score_total_b"></td>
      </tr>
    </tbody>
  </table>
  <div class="scoreboard_buttons_container">
    <button class="sb_btn_score_changer" id="sb_btn_score_sub">-</button>
    <button class="sb_btn_score_changer" id="sb_btn_score_add">+</button>
    <button class="sb_btn_score_changer" id="sb_btn_score_clr">AC</button>
  </div>
</div>
```

## Customization

Layout/design elements are all controlled by HTML and CSS. Simply adjust or overwrite to your liking.

To adjust the number of innings, simply add more table columns in HTML. There is no minimum or maximum limit.

## Usage

### Set Team Names

Click on the team name cells to bring up a dialog box to set team names.

### Set the Current Inning

Click on the current inning cell to highlight it.

### Update Scores

When an inning cell is highlighted, clicking on the **sub** or **add** button will update the score.


### Data Persistence

Once team names are set, the scoreboard is saved to the web browser's local storage. This means when the page is reloaded/refreshed, scores will be preserved. If team names are not set, scores are not preserved.

To clear the scoreboard, click on the **clr** button.
