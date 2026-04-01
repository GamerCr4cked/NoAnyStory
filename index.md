---
layout: default
title: NoAnyStory
---

<div class="home-header">
  <h1>No<span>Any</span>Story</h1>
  <p>Real stories, raw feelings — unfiltered aur bina kisi mask ke.</p>
</div>

<div class="nav-tabs" id="navTabs">
  <button class="nav-tab active" data-filter="all">All Stories</button>
  <button class="nav-tab" data-filter="school-life">School Life</button>
  <button class="nav-tab" data-filter="emotional">Emotional</button>
  <button class="nav-tab" data-filter="coming-soon">Coming Soon</button>
</div>

<div class="stories-grid" id="storiesGrid">

  <a href="{{ '/stories/notun-pakhi' | relative_url }}" class="story-card" data-tags="school-life emotional">
    <div class="card-genre">
      <span class="tag">School Life</span>
      <span class="tag mood">Emotional</span>
    </div>
    <h3>Notun Pakhi</h3>
    <p class="card-desc">Ek naam jo maine diya tha bina jaane… aur ab wo ek yaad ban chuka hai. 10th class ka ek ladka, 7th class ki ek ladki, aur beech me bas chhote chhote moments.</p>
    <div class="card-footer">
      <span class="card-lang">Hinglish / Bangla</span>
      <span class="read-link">Read Story →</span>
    </div>
  </a>

  <div class="story-card coming-soon" data-tags="coming-soon">
    <div class="card-genre">
      <span class="tag" style="opacity:0.5">???</span>
    </div>
    <h3>Coming Soon</h3>
    <p class="card-desc">Nayi kahani jald hi aayegi…</p>
    <div class="card-footer">
      <span class="card-lang">—</span>
      <span class="read-link">Soon</span>
    </div>
  </div>

</div>

<script>
  document.querySelectorAll('.nav-tab').forEach(tab => {
    tab.addEventListener('click', () => {
      document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
      tab.classList.add('active');
      const filter = tab.dataset.filter;
      document.querySelectorAll('.story-card').forEach(card => {
        if (filter === 'all') {
          card.style.display = '';
        } else {
          card.style.display = card.dataset.tags.includes(filter) ? '' : 'none';
        }
      });
    });
  });
</script>
