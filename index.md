---
layout: home
title: mirrorproof
---

# Welcome to mirrorproof

A collection of AI-generated art and symbolic explorations, organized by categories and automatically generated from the file system.

## Categories

{% assign categories = site.art | map: "categories" | uniq | sort %}
<div class="category-grid">
  {% for category in categories %}
    <a href="{{ '/categories/' | append: category | downcase | relative_url }}" class="category-card">
      <h2>{{ category }}</h2>
      {% assign category_art = site.art | where_exp: "item", "item.categories contains category" %}
      <p>{{ category_art.size }} pieces</p>
    </a>
  {% endfor %}
</div>

## Latest Artwork

<div class="art-grid">
  {% for art in site.art limit:6 %}
    <div class="art-card">
      {% if art.audio %}
        <div class="audio-preview">
          <audio controls>
            <source src="{{ art.audio | relative_url }}" type="audio/mpeg">
          </audio>
        </div>
      {% endif %}
      <div class="art-content">
        <h3><a href="{{ art.url | relative_url }}">{{ art.title }}</a></h3>
        <div class="art-excerpt">
          {{ art.content | strip_html | truncatewords: 30 }}
        </div>
        <div class="art-categories">
          {% for category in art.categories %}
            <a href="{{ '/categories/' | append: category | downcase | relative_url }}" class="category-tag">{{ category }}</a>
          {% endfor %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<style>
.category-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 2rem;
  margin: 2rem 0;
}

.category-card {
  background: #f8f9fa;
  padding: 2rem;
  border-radius: 8px;
  text-decoration: none;
  color: inherit;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.category-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.art-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
  gap: 2rem;
  margin: 2rem 0;
}

.art-card {
  background: white;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
  display: flex;
  flex-direction: column;
}

.art-card:hover {
  transform: translateY(-5px);
}

.audio-preview {
  padding: 1rem;
  background: #f8f9fa;
  border-bottom: 1px solid #eee;
}

.audio-preview audio {
  width: 100%;
}

.art-content {
  padding: 1.5rem;
}

.art-card h3 {
  margin: 0 0 1rem 0;
}

.art-card h3 a {
  color: inherit;
  text-decoration: none;
}

.art-excerpt {
  color: #666;
  margin-bottom: 1rem;
  line-height: 1.6;
}

.art-categories {
  margin-top: auto;
}

.category-tag {
  display: inline-block;
  background: #f0f0f0;
  padding: 0.25rem 0.75rem;
  border-radius: 15px;
  font-size: 0.875rem;
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
  text-decoration: none;
  color: inherit;
  transition: background 0.3s ease;
}

.category-tag:hover {
  background: #e0e0e0;
}
</style> 