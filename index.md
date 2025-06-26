---
layout: home
# Remove author_profile: true from here to prevent a second sidebar profile
# author_profile: true
---

<div class="page__content">
 {# The welcome message and introduction will be managed by the theme's default settings and the tagline in _config.yml #}

 {# Removed "Latest Blog Posts" section and its content #}

 <h2 class="archive__item-title" style="margin-top: 2em; text-align: center;">Featured Projects</h2>
 <p style="text-align: center; margin-bottom: 2em;">Discover my key projects in machine learning, data science, and AI.</p>

 {# Modified to use a horizontal scrollable container #}
 <div class="projects-horizontal-scroll">
   <div class="feature__item">
     <div class="archive__item">
       <h3 class="archive__item-title" itemprop="headline">
         <a href="/projects/#chess-rl-transformer" rel="permalink">Chess RL Transformer</a>
       </h3>
       <p class="archive__item-excerpt" itemprop="description">Built an autoregressive transformer for chess move prediction (FEN sequences), achieving 98%+ legal move accuracy and developing an open-source UI for interactive play. Co-leading GRPO (Reinforcement Learning) refinement with Stockfish.</p>
       <a href="/projects/#chess-rl-transformer" class="btn btn--primary">Learn More &rarr;</a>
     </div>
   </div>

   <div class="feature__item">
     <div class="archive__item">
       <h3 class="archive__item-title" itemprop="headline">
         <a href="/projects/#semg-keystroke-decoder" rel="permalink">SEMG Keystroke Decoder</a>
       </h3>
       <p class="archive__item-excerpt" itemprop="description">Engineered and evaluated deep learning models (Conv-GRU, LSTM, Transformer) for SEMG-to-QWERTY keystroke decoding, identifying Conv-GRU as optimal architecture with a 2x Character Error Rate (CER) improvement.</p>
       <a href="/projects/#semg-keystroke-decoder" class="btn btn--primary">Learn More &rarr;</a>
     </div>
   </div>

   <div class="feature__item">
     <div class="archive__item">
       <h3 class="archive__item-title" itemprop="headline">
         <a href="/projects/#changebot" rel="permalink">ChangeBot</a>
       </h3>
       <p class="archive__item-excerpt" itemprop="description">Led a 6-member team in developing "ChangeBot," a RAG-based chatbot to generate personalized emails for local representatives, reducing misdirected emails by 33%.</p>
       <a href="#changebot" class="btn btn--primary">Learn More &rarr;</a>
     </div>
   </div>
 </div>

 <p style="text-align: center; margin-top: 2em;"><a href="{{ '/projects/' | relative_url }}" class="btn btn--primary">View All Projects &rarr;</a></p>

 {# Removed "Connect With Me" section #}

</div>