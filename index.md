---
layout: home
# Remove author_profile: true from here to prevent a second sidebar profile
# author_profile: true
-
<div class="hero__content">
+header:
+  overlay_color: "rgba(0, 0, 0, 0)" # Set overlay color to fully transparent
+  overlay_filter: 0 # No filter effect
+  title: "" # Explicitly remove the title from this banner section
+---
+
+<div class="hero__content">
   <i class="fas fa-graduation-cap" style="font-size: 3em; color: #00897B; margin-bottom: 0.3em;"></i> {# A subtle graduation cap icon for UCLA #}
   <h1 id="welcome-to-my-personal-portfolio">Samantha Alejandre</h1>
   <p class="lead">Electrical & Computer Engineering M.S. Student at <span style="font-weight: bold;">UCLA</span></p>
   <p class="lead" style="font-size: 1.1em; margin-top: 0.5em;">Machine Learning | Data Science | Artificial Intelligence</p>
 </div>
 
 <h2 class="archive__item-title">About This Site</h2>
 <p>Here you'll find information about:</p>
 <ul>
   <li>My academic background and experiences.</li>
   <li>My research publications and ongoing projects.</li>
   <li>Personal projects and creative endeavors.</li>
   <li>My blog where I share thoughts on various topics.</li>
 </ul>
 <p>Feel free to explore and connect with me!</p>
 
 <h2 class="archive__item-title">Latest Blog Posts</h2>
 {# Displays up to 3 most recent blog posts #}
 {% for post in site.posts limit: 3 %}
   <article class="archive__item">
     <h3 class="archive__item-title" itemprop="headline">
       <a href="{{ post.url | relative_url }}" rel="permalink">{{ post.title }}</a>
     </h3>
     <p class="archive__item-excerpt" itemprop="description">{{ post.excerpt | markdownify | remove: "<p>" | remove: "</p>" }}</p>
     <p class="page__meta"><i class="far fa-calendar-alt" aria-hidden="true"></i> <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>{% if post.last_modified_at %} &nbsp; <i class="fas fa-fw fa-pencil-alt" aria-hidden="true"></i> <time datetime="{{ post.last_modified_at | date_to_xmlschema }}">{{ post.last_modified_at | date: "%B %d, %Y" }}</time>{% endif %}</p>
     <a href="{{ post.url | relative_url }}" class="btn btn--primary">Read More</a>
   </article>
 {% endfor %}
 
 <h2 class="archive__item-title">Featured Projects</h2>
 <p>(You can add brief summaries and links to your projects here. We'll create a dedicated projects page later.)</p>
 
 {# Example structure for featured projects. Replace with your actual projects. #}
 <div class="feature__wrapper">
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
 
 <p>For more projects, please visit my <a href="{{ '/projects/' | relative_url }}">Projects page</a>.</p>
 
 <h2 class="archive__item-title">Connect With Me</h2>
 <p>You can find me on these platforms:</p>
 <ul>
   {% for link in site.author.links %}
     {% if link.url %}
       <li>
         <a href="{{ link.url }}" target="_blank" rel="noopener noreferrer">
           {% if link.icon %}<i class="{{ link.icon | default: 'fas fa-link' }}" aria-hidden="true"></i>{% endif %} {{ link.label }}
         </a>
       </li>
     {% endif %}
   {% endfor %}
 </ul>