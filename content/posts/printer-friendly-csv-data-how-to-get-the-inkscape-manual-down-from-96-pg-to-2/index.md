---
title: printer friendly csv data - how to get the inkscape manual down from 96 pg to 2
date: 2025-06-03T01:52:21.879Z
---
using the firefox extension Table To CSV by Igorlogius <https://github.com/igorlogius/tbl2csv>

* copy as text (csv)
* use # marks to declare the headings
* the html page uploads the csv and parses it with javascript 

The script formats each table into its own div and uses css float to create a 2 col layout. When printing i set size to 50% because its a little wonky but good enough for me. It got it down from 96 pages to 1 double sided.



```javascript
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>2 Col CSV Layout Formatter</title>
  <style>
    body {
      font-family: sans-serif;
      margin: 2rem;
    }

    .container {
      column-count: 2;
      column-gap: 2rem;
    }

    .section {
      break-inside: avoid;
      border: 1px solid #ccc;
      padding: 1rem;
      margin-bottom: 1rem;
      background: #fdfdfd;
      box-shadow: 0 0 5px rgba(0,0,0,0.05);
    }

    h2 {
      margin-top: 0;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 0.5rem;
    }

    th, td {
      border: 1px solid #aaa;
      padding: 4px 8px;
      text-align: left;
    }

    input {
      margin-bottom: 2rem;
    }
  </style>
</head>
<body>

<input type="file" id="csvFileInput" accept=".csv" />
<div class="container" id="output"></div>

<script>
document.getElementById('csvFileInput').addEventListener('change', function (e) {
  const file = e.target.files[0];
  if (!file) return;

  const reader = new FileReader();
  reader.onload = function (event) {
    const text = event.target.result;
    parseCSVSections(text);
  };
  reader.readAsText(file);
});

function parseCSVSections(csvText) {
  const lines = csvText.split(/\r?\n/);
  const container = document.getElementById('output');
  container.innerHTML = '';

  let currentTitle = '';
  let currentData = [];
  const sections = [];

  function flush() {
    if (currentTitle && currentData.length) {
      sections.push({ title: currentTitle, rows: currentData });
    }
    currentData = [];
  }

  for (const line of lines) {
    if (line.trim().startsWith('#')) {
      flush();
      currentTitle = line.replace(/^#\s*/, '').trim();
    } else if (line.trim()) {
      currentData.push(line.split(','));
    }
  }
  flush();

  for (const section of sections) {
    const div = document.createElement('div');
    div.className = 'section';

    const h2 = document.createElement('h2');
    h2.textContent = section.title;
    div.appendChild(h2);

    const table = document.createElement('table');
    const [headers, ...rows] = section.rows;

    const thead = document.createElement('thead');
    const trHead = document.createElement('tr');
    headers.forEach(h => {
      const th = document.createElement('th');
      th.textContent = h;
      trHead.appendChild(th);
    });
    thead.appendChild(trHead);
    table.appendChild(thead);

    const tbody = document.createElement('tbody');
    rows.forEach(row => {
      const tr = document.createElement('tr');
      row.forEach(cell => {
        const td = document.createElement('td');
        td.textContent = cell;
        tr.appendChild(td);
      });
      tbody.appendChild(tr);
    });
    table.appendChild(tbody);

    div.appendChild(table);
    container.appendChild(div);
  }
}
</script>

</body>
</html>

```