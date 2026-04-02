---
layout: default
title: NoAnyStory
---

<div class="home-header">
  <h1>No<span>Any</span>Story</h1>
  <p>It feels real. It reads real. But it's all scripted — and that's what makes it hit different.</p>
</div>

<div class="nav-tabs" id="navTabs">
  <button class="nav-tab active" data-filter="all">All Stories</button>
  <button class="nav-tab" data-filter="school-life">School Life</button>
  <button class="nav-tab" data-filter="emotional">Emotional</button>
  <button class="nav-tab" data-filter="comedy">Comedy</button>
  <button class="nav-tab" data-filter="slice-of-life">Slice-of-Life</button>
  <button class="nav-tab" data-filter="romance">Romance</button>
  <button class="nav-tab" data-filter="coming-soon">Coming Soon</button>
</div>

<div class="stories-grid" id="storiesGrid">

  <a href="{{ '/stories/notun-pakhi' | relative_url }}" class="story-card" data-tags="school-life emotional slice-of-life">
    <div class="card-genre">
      <span class="tag">School Life</span>
      <span class="tag mood">Emotional</span>
      <span class="tag" style="background: rgba(201, 160, 220, 0.1); color: #c9a0dc; border-color: rgba(201, 160, 220, 0.15);">Slice-of-Life</span>
    </div>
    <h3>Notun Pakhi</h3>
    <p class="card-desc">Ek naam jo maine diya tha bina jaane… aur ab wo ek yaad ban chuka hai. 10th class ka ek ladka, 7th class ki ek ladki, aur beech me bas chhote chhote moments.</p>
    <div class="card-footer">
      <span class="card-lang">Hinglish / Bangla</span>
      <span class="read-link">Read Story →</span>
    </div>
  </a>

  <a href="{{ '/stories/notun-pakhi-s2' | relative_url }}" class="story-card" data-tags="school-life comedy slice-of-life">
    <div class="card-genre">
      <span class="tag">School Life</span>
      <span class="tag mood" style="background: rgba(109, 179, 242, 0.12); color: #6db3f2; border-color: rgba(109, 179, 242, 0.15);">Comedy</span>
      <span class="tag" style="background: rgba(201, 160, 220, 0.1); color: #c9a0dc; border-color: rgba(201, 160, 220, 0.15);">Slice-of-Life</span>
    </div>
    <h3>Notun Pakhi — S2</h3>
    <p class="card-desc">Wo wapas aayi. Ek saal baad, wahi school, wahi canteen. Par ab main door se dekhne wala nahi raha — ab dosti hai, hansi hai, aur beech me kuch aur bhi.</p>
    <div class="card-footer">
      <span class="card-lang">Hinglish / Bangla</span>
      <span class="read-link">Read Story →</span>
    </div>
  </a>

  <a href="{{ '/stories/notun-pakhi-s3' | relative_url }}" class="story-card" data-tags="school-life romance slice-of-life">
    <div class="card-genre">
      <span class="tag">School Life</span>
      <span class="tag" style="background: rgba(239, 68, 68, 0.1); color: #f87171; border-color: rgba(239, 68, 68, 0.15);">Romance</span>
      <span class="tag" style="background: rgba(201, 160, 220, 0.1); color: #c9a0dc; border-color: rgba(201, 160, 220, 0.15);">Slice-of-Life</span>
    </div>
    <h3>Notun Pakhi — S3</h3>
    <p class="card-desc">12th aur 9th. College aur school. Same campus, different worlds — par ab dono worlds merge ho rahe hain. Romance, rooftop scenes, aur wo feelings jo ab chupaye nahi chup rahi.</p>
    <div class="card-footer">
      <span class="card-lang">Hinglish / Bangla</span>
      <span class="read-link">Read Story →</span>
    </div>
  </a>

  <a href="{{ '/stories/the-last-message' | relative_url }}" class="story-card" data-tags="emotional drama">
    <div class="card-genre">
      <span class="tag" style="background: rgba(239, 68, 68, 0.1); color: #f87171; border-color: rgba(239, 68, 68, 0.15);">Drama</span>
      <span class="tag mood">Heartbreak</span>
    </div>
    <h3>The Last Message</h3>
    <p class="card-desc">Mr. X aur Ms. Y. Ek random chat se shuru hua, "goodnight stupid" tak pahuncha, aur phir ek din — bas silence. Na fight, na reason. Sirf "apna khayal rakhna" aur ek ending.</p>
    <div class="card-footer">
      <span class="card-lang">Hinglish</span>
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
