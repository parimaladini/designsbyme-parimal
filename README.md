# My Portfolio

Welcome to my portfolio! This site showcases my design work in a modern, responsive gallery layout.

## Features

- **Responsive Design:** Looks great on desktop and mobile devices.
- **Dynamic Gallery:** Images are loaded from a designated folder.
- **Smooth Animations:** Seamless transitions when expanding images.
- **Minimalist Aesthetic:** Clean, modern layout focusing on the artwork.

## Technology Stack

- **HTML**
- **Tailwind CSS** for styling
- **JavaScript** for interactivity

## How It Works

1. **Gallery View:**
   - Each design is displayed as a card with a partial preview (cropped or zoomed-in view).
   - Hovering over a card reveals a zoom effect.

2. **Image Expansion:**
   - Clicking on a card opens a full-sized image in a modal (lightbox-style view).
   - Click anywhere outside the image to close the modal.

## Adding New Designs

1. Save your images in the `images/` folder.
2. Update the `images` array in the JavaScript section with your new image filenames.

```javascript
const images = ['design1.jpg', 'design2.jpg', 'design3.jpg', 'design4.jpg'];
```

## Example Code

### HTML Structure

```html
<div class="container mx-auto p-4">
    <h1 class="text-4xl font-bold text-center mb-8">My Portfolio</h1>
    <div id="gallery" class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
        <!-- Images will be loaded here dynamically -->
    </div>
</div>
```

### Tailwind CSS Styling

```html
<img src="images/design1.jpg" alt="design1" class="w-full h-48 object-cover transform hover:scale-110 transition duration-300">
```

### JavaScript for Modal Functionality

```javascript
const modal = document.getElementById('modal');
const modalImg = document.getElementById('modal-img');

document.querySelectorAll('#gallery img').forEach(img => {
    img.addEventListener('click', () => {
        modal.classList.add('active');
        modalImg.src = img.src;
    });
});

modal.addEventListener('click', () => {
    modal.classList.remove('active');
});
```
