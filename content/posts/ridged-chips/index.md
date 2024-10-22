---
title: "Ridged Chips "
date: 2024-10-22T02:39:31.419Z
---
{{< youtube MsXGgZJN-IM >}}

Made[ this webpage](https://bweew.github.io/site2/10/ridged-chips.html) to help Tim figure out what food to bring. Uses switch statements to help make sense of the conditional logic. Uses  AJAX to auto refresh the UI in realtime as items are selected. 

[Mermaid Flowchart Diagram](https://mermaid.live/view#pako:eNptk29T2kAQxr_Kzr0GBjCJmhedKaSoVUTFaacevliTBa5e7jKXixQYv3s3Ke2Yal4ls7999t-TvUhtRiIWS2036Rqdh_tkYYCfz3JibQazwitrykfodj_BSJ45pTWMHPoSujBFk6G3bvt4yGmosTy3OeWYETwor95yHcir0oP_LyORI6fMCn7YysFsY6Ap3T0UR32Akwb-Iu-dKjR1l05RBjdqt0NIbLVat7CJnDi7IwNTQv-EWpeH8KQJn8nv6HKoClCMqNTZDb5QCzn_h6CHeqRD9G3nF3Lm1-RgbI136qlqlvW-84sG_iq_0Yo8PmnirjJN21b4Uo6drTwBL85TK3QlB70QvIUhFLYyWQl2CSON6TOvyhGv9BzzVsZUJuqn5dF43-gymBeOMPtggmuZUFkSX_5d19cNMJNn5HI0MF7b1GrkBsf4TC3mRl7SFq5UTnwPAgSNMGVnwUb5NVyknMLl8w_K38q54TE-2NltE79jM3nW4iM70iw796rGG-Epsm3QYStjLue1jZqCwMaDmWFZSFTxJ-lOZSv2zXititoSoiPyej6V8W-wr4UWgk-a00LE_Jqhe16IhXllDitv51uTiti7ijrC1aYT8RJ1yV9VwR6nROHKYf4XKdCIeC9-iTiIelH_6Hg4iAYnUTg8CoKO2Ip4MDztDYJgcBqGYRQF_Wj42hE7a1mh3zs5CY760WkUHvf7YRA2cg9NrFZ__Q3H_CV0)

[Slideshow](https://bweew.github.io/site2/10/revealjs/index.html) using RevealJS

The Source:

```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ridged Chips</title>
    <style>
      body {
        font-family: "Arial", sans-serif;
        background-color: #121212;
        color: #ffffff;
        margin: 0;
        padding: 20px;
      }

      h1 {
        text-align: center;
        color: #00b894;
      }

      .container {
        max-width: 600px;
        margin: 0 auto;
        padding: 10px;
      }

      .options {
        margin-bottom: 20px;
      }

      .options label {
        display: block;
        margin-bottom: 10px;
      }

      .result {
        margin-top: 20px;
        padding: 15px;
        border: 1px solid #444;
        background-color: #1e1e1e;
        border-radius: 8px;
      }

      @media (max-width: 600px) {
        .container {
          padding: 10px;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <h1>Ridged Chips</h1>

      <div class="options">
        <h3>Select what you're bringing:</h3>

        <label>
          <input type="checkbox" id="pizzaDough" /> Triple Fried Pizza Dough
        </label>

        <label>
          <input type="checkbox" id="meatballs" /> Frozen Meatballs
        </label>

        <label> <input type="checkbox" id="medley" /> Vegetable Medley </label>

        <label> <input type="checkbox" id="ham" /> Black Forest Ham </label>

        <label>
          Dessert:
          <select id="dessert">
            <option value="None">None</option>
            <option value="German Chocolate Cake">German Chocolate Cake</option>
            <option value="Key Lime Pie">Key Lime Pie</option>
          </select>
        </label>

        <label>
          <input type="checkbox" id="mozzSticks" /> Mozzarella Sticks
        </label>

        <label> <input type="checkbox" id="chips" /> Ridged Chips </label>
      </div>

      <div class="result" id="result"></div>
    </div>

    <script>
      // Function to check selected items and update the result
      function checkItems() {
        const resultDiv = document.getElementById("result");
        let result = "";

        const bringPizzaDough = document.getElementById("pizzaDough").checked;
        const bringMeatballs = document.getElementById("meatballs").checked;
        const bringMedley = document.getElementById("medley").checked;
        const bringHam = document.getElementById("ham").checked;
        const bringDessert = document.getElementById("dessert").value;
        const bringMozzSticks = document.getElementById("mozzSticks").checked;
        const bringChips = document.getElementById("chips").checked;

        // Check for pizza dough
        switch (bringPizzaDough) {
          case true:
            result +=
              "Listen, ah, bring that triple fried pizza dough, piping hot.<br>";
            break;
          case false:
            result +=
              "No pizza dough? That's fine, maybe you can bring some frozen meatballs instead.<br>";
            break;
        }

        // Check for meatballs
        switch (bringMeatballs) {
          case true:
            result +=
              "You can warm up the frozen meatballs either here or at home.<br>";
            break;
        }

        // Check for vegetable medley
        switch (bringMedley) {
          case true:
            result +=
              "If you're bringing a vegetable medley, bring it along with the croute de te.<br>";
            break;
          case false:
            result +=
              "No vegetable medley? You could bring some lunch meat instead.<br>";
            break;
        }

        // Check for black forest ham
        switch (bringHam) {
          case true:
            result +=
              "Bring a pound and a half, or two pounds of Black Forest Ham, with a Dijon mustard spread.<br>";
            break;
        }

        // Check for dessert
        switch (bringDessert) {
          case "German Chocolate Cake":
            result +=
              "You could bring a German chocolate cake for dessert.<br>";
            break;
          case "Key Lime Pie":
            result +=
              "You'll be a big hit with the dudes if you bring Key Lime Pie, a la mode, I'm talking about ice cream on the side.<br>";
            break;
          case "None":
          default:
            // No dessert action needed
            break;
        }

        // Check for mozzarella sticks
        switch (bringMozzSticks) {
          case true:
            result +=
              "Cube up those hot mozzarella sticks and put them in some marinara sauce, have them on standby.<br>";
            break;
        }

        // Check for ridged chips
        switch (bringChips) {
          case true:
            result +=
              "Don't forget the sour cream and onion dip as long as you bring ridged chips!<br>";
            break;
          case false:
            result +=
              "You must bring ridged chips for the sour cream and onion dip!<br>";
            break;
        }

        result +=
          "<br><strong>Additional Notes:</strong> And you have got to have a bite of my homemade ziti, I'm gonna warm her up, she's been in the freeze.";

        // Update result in the div
        resultDiv.innerHTML = result;
      }

      // Event listeners for auto-updating the result when selections change
      document
        .getElementById("pizzaDough")
        .addEventListener("change", checkItems);
      document
        .getElementById("meatballs")
        .addEventListener("change", checkItems);
      document.getElementById("medley").addEventListener("change", checkItems);
      document.getElementById("ham").addEventListener("change", checkItems);
      document.getElementById("dessert").addEventListener("change", checkItems);
      document
        .getElementById("mozzSticks")
        .addEventListener("change", checkItems);
      document.getElementById("chips").addEventListener("change", checkItems);

      // Initial run to show default values
      checkItems();
    </script>
  </body>
</html>
```