---
layout: page
---

# About Me

<img src="/images/luyao-sun.jpg" class="floatpic">

Here is **Luyao Sun (Leo Sun)**.<br>

I am currently pursuing an **M.Sc. in Artificial Intelligence and Robotics** at the [School of Data Science (SDS)](https://sds.cuhk.edu.cn/), **The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)**. Before joining CUHK-Shenzhen, I received my **B.Eng. in Intelligent Medical Engineering** from the **School of Medicine, Nankai University**. My current research focuses on learning-based intelligent systems, with particular interests in reinforcement learning, world-model-based decision making, embodied intelligence, and brain-computer interfaces.<br>

---

## Research Interests

**Reinforcement Learning · World Models · Vision-Language-Action (VLA) Models · Brain-Computer Interfaces (BCI)**

---

## Education

<div class="timeline">
  <div class="timeline-progress"></div>

  <div class="timeline-item timeline-item--current">
    <div class="timeline-dot" style="background: #ffffff;">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">
          M.Sc. in Artificial Intelligence and Robotics
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
        School of Data Science (SDS). 
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

---

## Work Experience

<div class="timeline">
  <div class="timeline-progress"></div>

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
  var timelines = document.querySelectorAll('.timeline');

  timelines.forEach(function(timeline) {
    var timelineProgress = timeline.querySelector('.timeline-progress');
    var items = timeline.querySelectorAll('.timeline-item');

    if (!timelineProgress || !items.length) return;

    // Reveal timeline items when they enter the viewport
    if ('IntersectionObserver' in window) {
      var observer = new IntersectionObserver(function(entries) {
        entries.forEach(function(entry) {
          if (entry.isIntersecting) {
            entry.target.classList.add('in-view');
          }
        });
      }, {
        rootMargin: '0px 0px -15% 0px'
      });

      items.forEach(function(item) {
        observer.observe(item);
      });

    } else {
      items.forEach(function(item) {
        item.classList.add('in-view');
      });
    }

    // Update the progress line for each timeline independently
    function updateProgress() {
      var rect = timeline.getBoundingClientRect();
      var totalHeight = timeline.offsetHeight;
      var windowH = window.innerHeight;

      var lineTop = 30;
      var lineBottom = 30;
      var lineHeight = totalHeight - lineTop - lineBottom;

      if (rect.top < windowH && rect.bottom > 0) {
        var scrolled = Math.min(
          1,
          Math.max(
            0,
            (windowH - rect.top - lineTop) /
            (totalHeight - lineTop + windowH * 0.4)
          )
        );

        timelineProgress.style.height =
          Math.min(scrolled * lineHeight, lineHeight) + 'px';
      }
    }

    window.addEventListener(
      'scroll',
      updateProgress,
      { passive: true }
    );

    updateProgress();
  });
})();
</script>

If you are interested in my research or potential collaborations, feel free to reach out to me at **luyaosun@link.cuhk.edu.cn**.

---

## Publications

<div class="publications-grid">

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/VRISE.png" alt="VRISE: A Balance Assessment Approach for Parkinson's Disease">
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

## News and Updates

<div class="news-grid">

  <div class="news-card news-card--milestone">
    <div class="news-meta">
      <span class="news-date">2026</span>
      <span class="news-tag news-tag--milestone">Education</span>
    </div>
    <p>
      Joined the <a href="https://sds.cuhk.edu.cn/" target="_blank">
      School of Data Science (SDS)</a> at
      <strong>The Chinese University of Hong Kong, Shenzhen</strong>
      to pursue an <strong>M.Sc. in Artificial Intelligence and Robotics</strong>.
    </p>
  </div>

  <div class="news-card news-card--research">
    <div class="news-meta">
      <span class="news-date">2026</span>
      <span class="news-tag news-tag--research">Research</span>
    </div>
    <p>
      Currently conducting research in areas including
      <strong>Vision-Language-Action (VLA) models, Reinforcement Learning,
      and World Models</strong>.
    </p>
  </div>

  <div class="news-card news-card--research">
    <div class="news-meta">
      <span class="news-date">2026</span>
      <span class="news-tag news-tag--research">Research</span>
    </div>
    <p>
      Currently conducting research on the application of
      <strong>signal processing methods to medical diagnosis</strong>.
    </p>
  </div>

  <div class="news-card news-card--milestone">
    <div class="news-meta">
      <span class="news-date">2024</span>
      <span class="news-tag news-tag--milestone">Education</span>
    </div>
    <p>
      Received my B.Eng. degree in
      <strong>Intelligent Medical Engineering</strong>
      from the School of Medicine,
      <strong>Nankai University</strong>.
    </p>
  </div>

  <div class="news-card news-card--publication">
    <div class="news-meta">
      <span class="news-date">2023</span>
      <span class="news-tag news-tag--publication">Publication</span>
    </div>
    <p>
      Our work
      <a href="https://doi.org/10.1109/CYBER59472.2023.10256589"
         target="_blank" rel="noopener">
        <strong>
          Virtual Reality-Induced Symptoms and Effects (VRISE):
          A Balance Assessment Approach for Parkinson's Disease
        </strong>
      </a>
      was published at
      <strong>IEEE CYBER 2023</strong>.
    </p>
  </div>

  <div class="news-card news-card--milestone">
    <div class="news-meta">
      <span class="news-date">2020</span>
      <span class="news-tag news-tag--milestone">Education</span>
    </div>
    <p>
      Began my undergraduate studies in
      <strong>Intelligent Medical Engineering</strong>
      at the School of Medicine,
      <strong>Nankai University</strong>.
    </p>
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
