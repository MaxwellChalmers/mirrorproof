---
layout: default
title: Categories
---

# Categories

Browse all artwork by category:

<div class="category-grid">
  {% assign categories = site.art | map: "categories" | uniq | sort %}
  {% for category in categories %}
    <a href="{{ '/categories/' | append: category | downcase | relative_url }}" class="category-card">
      <h2>{{ category }}</h2>
      {% assign category_art = site.art | where_exp: "item", "item.categories contains category" %}
      <p>{{ category_art.size }} pieces</p>
    </a>
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
</style> 