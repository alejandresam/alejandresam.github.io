---
layout: home
# Remove author_profile: true from here to prevent a second sidebar profile
# author_profile: true
---

<div class="page__content"> 
 <h1 id="welcome-to-my-personal-portfolio" style="text-align: center; margin-top: 1em; margin-bottom: 0.5em;">Welcome!</h1>
 <p class="lead" style="text-align: center; font-size: 1.2em; line-height: 1.5; color: #333;">
   I'm Samantha Alejandre, an Electrical & Computer Engineering M.S. Student at <span style="font-weight: bold;">UCLA</span>.
   Explore my work in Machine Learning, Data Science, and Artificial Intelligence, alongside my academic journey and personal projects.
 </p>

 <h2 class="archive__item-title" style="margin-top: 2em;">Latest Blog Posts</h2>
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

 <p style="text-align: center; margin-top: 2em;"><a href="{{ '/blog/' | relative_url }}" class="btn btn--primary">View All Blog Posts &rarr;</a></p>

 <h2 class="archive__item-title" style="margin-top: 2em;">Featured Projects</h2>
 <p style="text-align: center;">Discover my key projects in machine learning, data science, and AI on the <a href="{{ '/projects/' | relative_url }}">Projects page</a>.</p>

 {# Example structure for featured projects. Replace with your actual projects. #}
 <div class="feature__wrapper" style="margin-bottom: 2em;">
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

 <p style="text-align: center;">For more projects, please visit my <a href="{{ '/projects/' | relative_url }}">Projects page</a>.</p>

 <h2 class="archive__item-title" style="margin-top: 2em;">Connect With Me</h2>
 <p style="text-align: center;">You can find me on these platforms:</p>
 <ul style="list-style: none; padding: 0; text-align: center;">
   {% for link in site.author.links %}
     {% if link.url %}
       <li style="display: inline-block; margin: 0 10px;">
         <a href="{{ link.url }}" target="_blank" rel="noopener noreferrer">
           {% if link.icon %}<i class="{{ link.icon | default: 'fas fa-link' }}" aria-hidden="true"></i>{% endif %} {{ link.label }}
         </a>
       </li>
     {% endif %}
   {% endfor %}
 </ul>
</div>