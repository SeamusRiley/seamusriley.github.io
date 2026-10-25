---
title: "Stage Productions"
layout: single
sidebar:
  nav: false
author_profile: false
permalink: /stage-productions/
excerpt: 'See Also <a href="/books/">Books I Have Read</a>, <a href="/movies-shows/">Movies &amp; Shows</a>'
---

See Also <a href="/books/">Books I Have Read</a>, <a href="/movies-shows/">Movies &amp; Shows</a>

## Seen

<table class="sortable">
<thead>
<tr><th>Rating</th><th>Name</th><th>Author</th><th>Recommender</th></tr>
</thead>
<tbody>
<tr><td>1/2 Nice</td><td>Come From Away</td><td>Irene Sankoff and David Hein</td><td>Patrick Healey</td></tr>
<tr><td>1/2 Nice</td><td>The Guy Who Didn&#x27;t Like Musicals</td><td>Nick and Matt Lang</td><td>Lee O&#x27;Dell</td></tr>
<tr><td>2/2 Wonderful</td><td>Hamilton</td><td>Lin-Manuel Miranda</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td>Les Miserables</td><td>Alain Boublil and Claude-Michel Schönberg</td><td>&mdash;</td></tr>
</tbody>
</table>

## Want to See

- 9-5
  - Written by Dolly Parton

<style>
table.sortable th{cursor:pointer}
table.sortable th.srt[data-dir="asc"]::after{content:" ▴"}
table.sortable th.srt[data-dir="desc"]::after{content:" ▾"}
</style>
<script>
document.querySelectorAll('table.sortable').forEach(function(tbl){
  var ths = tbl.querySelectorAll('thead th');
  function key(td){
    var t = td.textContent.trim().toLowerCase();
    if (t === '—') return '~~~~';
    return t.replace(/^(the|a|an)\s+/, '');
  }
  ths.forEach(function(th, i){
    th.title = 'Click to sort';
    th.addEventListener('click', function(){
      var tbody = tbl.querySelector('tbody');
      var rows = Array.prototype.slice.call(tbody.querySelectorAll('tr'));
      var asc = th.getAttribute('data-dir') !== 'asc';
      ths.forEach(function(o){ o.removeAttribute('data-dir'); o.classList.remove('srt'); });
      th.setAttribute('data-dir', asc ? 'asc' : 'desc');
      th.classList.add('srt');
      rows.sort(function(a, b){
        var x = key(a.children[i]), y = key(b.children[i]);
        return (x < y ? -1 : x > y ? 1 : 0) * (asc ? 1 : -1);
      });
      rows.forEach(function(r){ tbody.appendChild(r); });
    });
  });
});
</script>
