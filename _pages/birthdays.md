---
permalink: /birthdays/
title: "Birthdays"
---

<p id="bday-summary"></p>

<h2>Coming up</h2>
<ul id="bday-upcoming"></ul>

<h2>All birthdays by month</h2>
<div id="bday-bymonth"></div>

<script>
const BIRTHDAYS = [{"name":"Jonah","month":1,"day":3,"year":null},{"name":"Nana","month":1,"day":3,"year":null},{"name":"Angel Walker-Werth","month":1,"day":20,"year":null},{"name":"Gabriel Jacobs","month":1,"day":28,"year":null},{"name":"Kira Withrow","month":1,"day":31,"year":null},{"name":"Annie Lowe","month":2,"day":1,"year":null},{"name":"Nikki (Aunt)","month":2,"day":2,"year":null},{"name":"Jackson Upmann","month":2,"day":3,"year":null},{"name":"Rosalee Kirschel","month":2,"day":3,"year":null},{"name":"Brittany Piddington","month":2,"day":4,"year":null},{"name":"Rickard Tan","month":2,"day":8,"year":null},{"name":"Kes","month":2,"day":9,"year":1998},{"name":"Quinn","month":2,"day":16,"year":1996},{"name":"Mom","month":2,"day":25,"year":1971},{"name":"McKayla","month":3,"day":2,"year":2001},{"name":"Thea Showalter","month":3,"day":10,"year":2025},{"name":"John","month":3,"day":14,"year":1997},{"name":"Thomas WW","month":3,"day":23,"year":null},{"name":"Amy Nasir","month":4,"day":5,"year":null},{"name":"Lee","month":4,"day":8,"year":2000},{"name":"Rosie","month":4,"day":8,"year":null},{"name":"Clementine","month":4,"day":21,"year":null},{"name":"Carolyn","month":4,"day":23,"year":null},{"name":"Ben","month":4,"day":24,"year":1997},{"name":"Sophia","month":5,"day":5,"year":null},{"name":"Jon Hersey","month":5,"day":11,"year":null},{"name":"Tom Nowak","month":5,"day":22,"year":null},{"name":"Carrie-Ann","month":5,"day":25,"year":null},{"name":"Quinn Theobald","month":5,"day":26,"year":null},{"name":"Joe","month":5,"day":27,"year":1998},{"name":"Jon Woz","month":5,"day":27,"year":null},{"name":"Stephanie","month":5,"day":31,"year":null},{"name":"Persephone","month":6,"day":5,"year":null},{"name":"Nadia Gutierrez","month":6,"day":19,"year":2011},{"name":"Justyna Piantek Pawlowska","month":6,"day":23,"year":2025},{"name":"Katie","month":6,"day":24,"year":1993},{"name":"Dylan Fritts","month":6,"day":29,"year":null},{"name":"Randy Vollrath","month":6,"day":30,"year":null},{"name":"Amelia G","month":6,"day":30,"year":null},{"name":"Maddie","month":6,"day":30,"year":1998},{"name":"Ryan and Sean","month":7,"day":3,"year":null},{"name":"Bryan","month":7,"day":4,"year":null},{"name":"Caleb Emery","month":7,"day":5,"year":null},{"name":"Isadora Kolar","month":7,"day":10,"year":null},{"name":"Arthur Zey","month":7,"day":11,"year":null},{"name":"Andrew Dowdy","month":7,"day":15,"year":null},{"name":"Eli Walls","month":7,"day":16,"year":2026},{"name":"Zena Matthews","month":7,"day":21,"year":null},{"name":"Erek","month":7,"day":23,"year":null},{"name":"John","month":7,"day":30,"year":2025},{"name":"Uncle Davy","month":8,"day":1,"year":null},{"name":"Adina","month":8,"day":9,"year":null},{"name":"Ross","month":8,"day":27,"year":null},{"name":"Tum","month":9,"day":4,"year":null},{"name":"Sarah Fleegal","month":9,"day":8,"year":null},{"name":"Abad Julio","month":9,"day":9,"year":null},{"name":"Maitlyn","month":9,"day":12,"year":null},{"name":"Becca Mitchell","month":9,"day":13,"year":null},{"name":"Annie Vinther Sanz","month":9,"day":18,"year":null},{"name":"Eli","month":9,"day":28,"year":null},{"name":"James Valliant","month":9,"day":29,"year":null},{"name":"Aaron Isleman","month":9,"day":30,"year":null},{"name":"Bria Livengood","month":10,"day":27,"year":1998},{"name":"Frebby","month":11,"day":3,"year":null},{"name":"Maddox Locher","month":11,"day":7,"year":null},{"name":"Ashley Harris","month":11,"day":7,"year":null},{"name":"Juan!!!!","month":11,"day":11,"year":null},{"name":"Schuyler Kleinfelter","month":11,"day":16,"year":null},{"name":"James Wicken-Greene","month":11,"day":17,"year":null},{"name":"Patrick Healey","month":12,"day":9,"year":null},{"name":"Skyler","month":12,"day":17,"year":null},{"name":"Allie","month":12,"day":27,"year":null}];
const MONTHS = ["January","February","March","April","May","June","July","August","September","October","November","December"];
function nextOccurrence(b, today) {
  let c = new Date(today.getFullYear(), b.month - 1, b.day);
  const t0 = new Date(today.getFullYear(), today.getMonth(), today.getDate());
  if (c < t0) c = new Date(today.getFullYear() + 1, b.month - 1, b.day);
  return c;
}
function render() {
  const today = new Date();
  const t0 = new Date(today.getFullYear(), today.getMonth(), today.getDate());
  const items = BIRTHDAYS.map(b => {
    const c = nextOccurrence(b, today);
    const days = Math.round((c - t0) / 86400000);
    const turns = b.year ? c.getFullYear() - b.year : null;
    return { b, c, days, turns };
  }).sort((a, z) => a.days - z.days || a.b.name.localeCompare(z.b.name));
  document.getElementById("bday-summary").textContent = BIRTHDAYS.length + " birthdays tracked. Next up: " + items[0].b.name + " on " + MONTHS[items[0].b.month - 1] + " " + items[0].b.day + ".";
  const ul = document.getElementById("bday-upcoming");
  items.forEach(({ b, days, turns }) => {
    const when = days === 0 ? "today!" : days === 1 ? "tomorrow" : "in " + days + " days";
    const li = document.createElement("li");
    li.innerHTML = "<strong></strong> \u2014 " + MONTHS[b.month - 1] + " " + b.day + (turns && turns >= 1 ? " (turns " + turns + ")" : "") + " \u2014 " + when;
    li.querySelector("strong").textContent = b.name;
    if (days === 0) li.style.fontWeight = "bold";
    ul.appendChild(li);
  });
  const byMonth = document.getElementById("bday-bymonth");
  MONTHS.forEach((m, i) => {
    const inMonth = BIRTHDAYS.filter(b => b.month === i + 1).sort((a, z) => a.day - z.day || a.name.localeCompare(z.name));
    if (!inMonth.length) return;
    const h = document.createElement("h3"); h.textContent = m; byMonth.appendChild(h);
    const list = document.createElement("ul");
    inMonth.forEach(b => {
      const li = document.createElement("li");
      li.textContent = b.name + " \u2014 " + m + " " + b.day + (b.year ? " (" + b.year + ")" : "");
      list.appendChild(li);
    });
    byMonth.appendChild(list);
  });
}
render();
</script>
