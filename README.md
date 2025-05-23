# LLM Art Gallery

A GitHub Pages site for showcasing AI-generated artwork, automatically organized by categories.

## Structure

- `_art/` - Directory containing all your art pieces as markdown files
- `images/` - Directory for storing all artwork images
- `_layouts/` - Contains the templates for different page types
- `_config.yml` - Jekyll configuration file

## Adding New Artwork

1. Create a new markdown file in the `_art/` directory
2. Add the following front matter at the top of the file:

```yaml
---
layout: art
title: Your Art Title
image: /images/your-image.jpg
categories:
  - Category1
  - Category2
date: YYYY-MM-DD
---
```

3. Add your artwork image to the `images/` directory
4. Write your content below the front matter

## Categories

Categories are automatically generated based on the `categories` field in your art pieces' front matter. Each category will have its own page showing all artwork in that category.

## Local Development

To run the site locally:

1. Install Ruby and Jekyll
2. Run `bundle install` to install dependencies
3. Run `bundle exec jekyll serve` to start the local server
4. Visit `http://localhost:4000` in your browser

## Deployment

The site will automatically deploy to GitHub Pages when you push to the main branch. Make sure your repository settings have GitHub Pages enabled and set to use the main branch.

## Customization

- Edit `_config.yml` to change site-wide settings
- Modify the layouts in `_layouts/` to change the appearance
- Add custom CSS in the layout files or create a new CSS file

# LLM Art Collection

**Disclaimer**:

The works in this repository are intentionally generated using language models, often to the point of inconvenience. Any apparent sense of inherent meaning or truth within the art pieces should be considered *within* the narrative of the art project. These pieces are not intended to reflect the author's or the system's perspective, but rather to explore the possibilities of machine-generated creativity.

I hope to extend some of my learning from this process to some kind of formalism eventually, but I intend to retain this repo as a purely artistic endeavor. Any properties of the art that appear "emergent" are not meant to be seen as any form of conclusion or truth statement. The author encourages all to avoid falling into the trap of seeking *meaning*, *consistency*, or *structure* from a system that inherently cannot hold such qualities.

Lastly, some of the pieces may veer into strange or unsettling territory. This art can get a bit *spooky*, and at times may flirt with parody, conspiratorial themes, or absurdist oddities. Embrace the weirdness—it's all part of the experiment.

---

### Rap Songs  
A collection of rap tracks generated through LLMs, exploring themes of absurdism, self-reflection, and social critique. These works play with rhyme schemes and lyricism while engaging with machine-driven creativity.

### Poems and Prose  
A mix of poetry and prose pieces, ranging from experimental storytelling to traditional verse. These writings use the language model's creativity to explore the intersection of narrative, metaphor, and language.

### Dialogs  
A series of conversational pieces created by interacting with the model in a dialogue format. These may range from deeply philosophical exchanges to surreal, absurdist interactions, showcasing the potential for AI-driven communication.

### mirrorproof (symbolic OS weirdness)  
A space for exploring the weirdness inherent in the LLM's symbolic systems. This section houses pieces that delve into recursive patterns, AI logic, and the strangeness of machine-generated thinking, often blurring the lines between art and computation.

### Formalism Sketches  
Conceptual sketches of formal frameworks or systems inspired by the creative process within the LLM space. These writings aim to capture the theoretical structures that may emerge from the art, exploring the intersection of symbolism, computation, and meaning.
