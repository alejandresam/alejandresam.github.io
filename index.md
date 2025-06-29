---
layout: home
---

<div class="page__content">

  <!-- Intro text -->
  <h2 class="archive__item-title" style="text-align: center;">Featured Projects</h2>
  <p style="text-align: center;">Explore key projects in machine learning, data science, and AI.</p>

  <!-- Swiper container -->
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <!-- Slide 1 -->
      <div class="swiper-slide">
        <div class="feature__item">
          <img src="/assets/images/chess-rl.jpg" alt="Chess RL Transformer" />
          <h3 class="archive__item-title">
            <a href="/projects/#chess-rl-transformer" rel="permalink">Chess RL Transformer</a>
          </h3>
          <p class="archive__item-excerpt">
            Autoregressive transformer for chess moves with 98%+ accuracy. Integrated interactive UI with Stockfish enhancements.
          </p>
          <a href="/projects/#chess-rl-transformer" class="btn btn--primary">Learn More →</a>
        </div>
      </div>
      
      <!-- Slide 2 -->
      <div class="swiper-slide">
        <div class="feature__item">
          <img src="/assets/images/semg-keystroke.jpg" alt="SEMG Keystroke Decoder" />
          <h3 class="archive__item-title">
            <a href="/projects/#semg-keystroke-decoder" rel="permalink">SEMG Keystroke Decoder</a>
          </h3>
          <p class="archive__item-excerpt">
            Deep learning model for SEMG keystroke analysis with innovative architecture.
          </p>
          <a href="/projects/#semg-keystroke-decoder" class="btn btn--primary">Learn More →</a>
        </div>
      </div>
      
      <!-- Slide 3 -->
      <div class="swiper-slide">
        <div class="feature__item">
          <img src="/assets/images/changebot.jpg" alt="ChangeBot" />
          <h3 class="archive__item-title">
            <a href="/projects/#changebot" rel="permalink">ChangeBot</a>
          </h3>
          <p class="archive__item-excerpt">
            A RAG-based chatbot automating email responses and reducing bounce rates.
          </p>
          <a href="/projects/#changebot" class="btn btn--primary">Learn More →</a>
        </div>
      </div>
    </div>

    <!-- Optional navigation arrows -->
    <div class="swiper-button-next"></div>
    <div class="swiper-button-prev"></div>

    <!-- Optional pagination dots -->
    <div class="swiper-pagination"></div>
  </div>

  <!-- Optional: Link to view all projects -->
  <p style="text-align: center; margin-top: 2em;">
    <a href="{{ '/projects/' | relative_url }}" class="btn btn--primary">View All Projects &rarr;</a>
  </p>

</div>