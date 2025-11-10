# Copilot Instructions for 1113211014 Portfolio Website

## Project Overview
This is a responsive portfolio website built with Bootstrap 5, featuring image carousels, accordions, and custom styling. The project consists of three main HTML files with different layout patterns and components.

## Architecture & Structure

### Main Files
- `index.html`: Personal portfolio page with gradient background, avatar, and accordions
- `index1.html`: Product showcase page with grid layouts and testimonials
- `III.html`: Photo gallery with carousel and grid layout

### Directory Structure
```
├── image/       # Main images folder
├── image1/      # Secondary images folder (used in III.html)
└── *.html       # HTML files in root directory
```

## Key Patterns & Conventions

### Bootstrap Integration
- Bootstrap 5.3.8 is loaded via CDN for all pages
- Both CSS and JS bundles are included with integrity hashes
```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js"></script>
```

### Component Patterns

1. Carousels
```html
<div id="carouselExample" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <!-- carousel-item elements -->
  </div>
  <!-- navigation buttons -->
</div>
```

2. Accordions
```html
<div class="accordion" id="accordionExample">
  <div class="accordion-item">
    <h2 class="accordion-header">
      <!-- accordion buttons -->
    </h2>
    <div id="collapseOne" class="accordion-collapse collapse">
      <!-- accordion content -->
    </div>
  </div>
</div>
```

### CSS Conventions
- Custom styles are defined inline within `<style>` tags in each HTML file
- Responsive breakpoints follow Bootstrap's conventions
- Image styling uses consistent object-fit patterns:
  ```css
  .card img {
    height: [fixed-height];
    object-fit: cover;
    width: 100%;
  }
  ```

## Image Handling
- Use relative paths for images: `./image/` or `./image1/`
- Always include fallback images using onerror:
  ```html
  onerror="this.onerror=null;this.src='https://via.placeholder.com/800x600?text=No+Image';"
  ```

## Common Tasks

### Adding New Images
1. Place image files in the appropriate directory (`image/` or `image1/`)
2. Use relative paths in HTML
3. Include proper alt text and error handling

### Creating New Sections
1. Follow existing section structure with semantic HTML5 elements
2. Use Bootstrap grid classes for layout
3. Maintain consistent spacing with `my-*` and `py-*` classes

### Responsive Design
- Use Bootstrap's responsive classes (`col-*`)
- Include mobile-specific adjustments in media queries
- Test across breakpoints (mobile, tablet, desktop)

## Best Practices
1. Maintain consistent class naming across components
2. Follow Bootstrap's grid system for layouts
3. Keep image dimensions optimized for web
4. Use semantic HTML elements
5. Include proper alt text for images

## Testing
- Test carousel functionality
- Verify accordion interactions
- Check responsive layouts at all breakpoints
- Validate image loading and fallbacks