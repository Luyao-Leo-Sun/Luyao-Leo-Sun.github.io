---
layout: page
---

# About Me

<img src="/images/luyao-sun.jpg" class="floatpic">

Here is **Luyao Sun (Leo Sun)**.<br>

I am currently an **MSc student** at the [School of Data Science (SDS)](https://sds.cuhk.edu.cn/), **The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)**. My research interests include **Reinforcement Learning, World Models, Vision-Language-Action (VLA) models, and Brain-Computer Interfaces (BCI)**. Before joining CUHK-Shenzhen, I received my **B.Eng. in Intelligent Medical Engineering** from the **School of Medicine, Nankai University**. My current research focuses on learning-based intelligent systems, with particular interests in reinforcement learning, world-model-based decision making, embodied intelligence, and multimodal intelligent systems.<br>

## Education

<div class="timeline">
  <div class="timeline-progress"></div>

  <div class="timeline-item timeline-item--current">
    <div class="timeline-dot" style="background: #ffffff;">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">
          MSc Student
          <span class="timeline-sep">|</span>
          <span class="timeline-company">
            <a href="https://www.cuhk.edu.cn/en" target="_blank">
              The Chinese University of Hong Kong, Shenzhen
            </a>
          </span>
        </div>
        <span class="timeline-time">2026 - Present</span>
      </div>
      <div class="timeline-details">
        School of Data Science (SDS). Research interests include Reinforcement Learning,
        World Models, Vision-Language-Action (VLA) models, and Brain-Computer Interfaces (BCI).
      </div>
    </div>
  </div>

  <div class="timeline-item">
    <div class="timeline-dot" style="background: #ffffff;">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">
          B.Eng. in Intelligent Medical Engineering
          <span class="timeline-sep">|</span>
          <span class="timeline-company">
            <a href="https://en.nankai.edu.cn/" target="_blank">
              Nankai University
            </a>
          </span>
        </div>
        <span class="timeline-time">2020 - 2024</span>
      </div>
      <div class="timeline-details">
        School of Medicine, Nankai University.
      </div>
    </div>
  </div>

</div>

## Work Experience

<div class="timeline">
  <div class="timeline-progress" id="timeline-progress"></div>

  <div class="timeline-item">
    <div class="timeline-dot" style="background: #ffffff;">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">
          Management Staff & Instructor
          <span class="timeline-sep">|</span>
          <span class="timeline-company">
            Xueersi Peiyou, Tianjin
          </span>
        </div>
        <span class="timeline-time">Jul. 2024 - Dec. 2024</span>
      </div>
      <div class="timeline-details">
        Worked in both management and teaching roles at Xueersi Peiyou in Heping District, Tianjin.
      </div>
    </div>
  </div>

</div>

<script>
(function() {
  var timelineProgress = document.getElementById('timeline-progress');
  var timeline = document.querySelector('.timeline');
  if (!timelineProgress || !timeline) return;

  var items = timeline.querySelectorAll('.timeline-item');

  // IntersectionObserver for in-view class
  if ('IntersectionObserver' in window) {
    var observer = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('in-view');
        }
      });
    }, { rootMargin: '0px 0px -15% 0px' });

    items.forEach(function(item, idx) {
      if (idx < 3) {
        // Reveal first 3 immediately on load (still gets the stagger transition)
        item.classList.add('in-view');
      } else {
        observer.observe(item);
      }
    });
  } else {
    items.forEach(function(item) { item.classList.add('in-view'); });
  }

  // Scroll progress bar
  window.addEventListener('scroll', function() {
    var rect = timeline.getBoundingClientRect();
    var totalHeight = timeline.offsetHeight;
    var windowH = window.innerHeight;
    var lineTop = 30;
    var lineBottom = 30;
    var lineHeight = totalHeight - lineTop - lineBottom;

    if (rect.top < windowH && rect.bottom > 0) {
      var scrolled = Math.min(1, Math.max(0, (windowH - rect.top - lineTop) / (totalHeight - lineTop + windowH * 0.4)));
      timelineProgress.style.height = Math.min(scrolled * lineHeight, lineHeight) + 'px';
    }
  }, { passive: true });
})();
</script>

If you are interested in my research or potential collaborations, feel free to reach out to me at **luyaosun [at] link.cuhk.edu.cn**.


---

## Publications

<div class="publications-grid">

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/vrise.png" alt="VRISE: A Balance Assessment Approach for Parkinson's Disease">
      <a href="https://doi.org/10.1109/CYBER59472.2023.10256589"
         class="publication-overlay"
         target="_blank"
         rel="noopener">
        <span>View Paper</span>
      </a>
    </div>

    <div class="publication-info">

      <div class="publication-title">
        <a href="https://doi.org/10.1109/CYBER59472.2023.10256589"
           target="_blank"
           rel="noopener">
          Virtual Reality-Induced Symptoms and Effects (VRISE): A Balance Assessment Approach for Parkinson's Disease
        </a>
      </div>

      <div class="publication-authors">
        Bingqing Wei,
        Yuhan Fan,
        Yaxuan Wu,
        Shouwang Huang,
        <strong class="author-highlight">Luyao Sun</strong>,
        Yugen You,
        Ningbo Yu
      </div>

      <div class="publication-conference">
        <span class="pub-venue">
          2023 IEEE 13th International Conference on CYBER Technology in Automation, Control, and Intelligent Systems (CYBER)
        </span>
        <a href="https://doi.org/10.1109/CYBER59472.2023.10256589"
           target="_blank"
           rel="noopener">[paper]</a>
      </div>

      <div class="publication-details">
        IEEE CYBER 2023 · pp. 962–967
      </div>

    </div>
  </div>

</div>

<script>
(function() {
  if ('IntersectionObserver' in window) {
    var observer = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('animate-in');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.08, rootMargin: '0px 0px -40px 0px' });
    document.querySelectorAll('.publication-card').forEach(function(card) {
      observer.observe(card);
    });
  } else {
    document.querySelectorAll('.publication-card').forEach(function(card) {
      card.classList.add('animate-in');
    });
  }
})();
</script>

---

## Research Interests

**Reinforcement Learning · World Models · Vision-Language-Action (VLA) Models · Brain-Computer Interfaces (BCI)**

---

## News and Updates

<div class="news-grid">
  <div class="news-card news-card--publication">
    <div class="news-meta">
      <span class="news-date">February 2026</span>
      <span class="news-tag news-tag--publication">Publication</span>
    </div>
    <p>First-Author Paper: <a href="https://www.tandfonline.com/doi/abs/10.1080/03610918.2026.2635000"><strong>Innovative covariance-based framework: symmetry assessment and exponentiality testing under multiplicative distortion measurement Errors</strong></a> Now Officially Published in <a href="https://www.tandfonline.com/journals/lssp20">Communications in Statistics - Simulation and Computation</a></p>
  </div>

  <div class="news-card news-card--milestone">
    <div class="news-meta">
      <span class="news-date">Jan 2026</span>
      <span class="news-tag news-tag--milestone">Milestone</span>
    </div>
    <p>Excited to have received an offer from Apple!</p>
  </div>

  <div class="news-card news-card--milestone">
    <div class="news-meta">
      <span class="news-date">March 2025</span>
      <span class="news-tag news-tag--milestone">Milestone</span>
    </div>
    <p>Thrilled to have received an offer from UPenn Engineering!</p>
  </div>

  <div class="news-card news-card--publication">
    <div class="news-meta">
      <span class="news-date">August 2024</span>
      <span class="news-tag news-tag--publication">Publication</span>
    </div>
    <p>First-Author Paper: <a href="https://onlinelibrary.wiley.com/doi/10.1002/sam.11708"><strong>A New Logarithmic Multiplicative Distortion for Correlation Analysis</strong></a> Now Officially Published in <a href="https://onlinelibrary.wiley.com/journal/19321872">Statistical Analysis and Data Mining</a> (JCR Q1)</p>
  </div>
</div>

<script>
(function() {
  if ('IntersectionObserver' in window) {
    var observer = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('animate-in');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.08, rootMargin: '0px 0px -60px 0px' });
    document.querySelectorAll('.news-card').forEach(function(card) {
      observer.observe(card);
    });
  } else {
    document.querySelectorAll('.news-card').forEach(function(card) {
      card.classList.add('animate-in');
    });
  }
})();
</script>
