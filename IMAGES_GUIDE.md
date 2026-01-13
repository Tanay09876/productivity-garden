# How to Add Plant Images

## 📁 Folder Structure

The app expects images in this structure:

```
assets/
├── basic/
│   ├── moonbell_fern.png
│   ├── dewdrop_moss.png
│   ├── whisper_wort.png
│   ├── glimmergrass.png
│   └── starlight_sprout.png
├── rare/
│   ├── crystalbark_sapling.png
│   ├── dreamweaver_vine.png
│   ├── phoenix_bloom.png
│   ├── shadowleaf_orchid.png
│   └── timekeeper_rose.png
└── extinct/
    ├── dradonbreath_lily.png
    ├── void_lotus.png
    ├── eternalfrost_pine.png
    ├── starfall_mushroom.png
    └── worldtree_seedling.png
```

## 📝 Required Images (15 total)

### Basic Plants (5):
1. `moonbell_fern.png` - A gentle fern
2. `dewdrop_moss.png` - Sparkling moss
3. `whisper_wort.png` - Rustling leaves
4. `glimmergrass.png` - Shimmering grass
5. `starlight_sprout.png` - Glowing sprout

### Rare Plants (5):
1. `crystalbark_sapling.png` - Crystalline bark
2. `dreamweaver_vine.png` - Purple spiraling vine
3. `phoenix_bloom.png` - Warm flower
4. `shadowleaf_orchid.png` - Dark blue orchid
5. `timekeeper_rose.png` - Clock-like rose

### Extinct Plants (5):
1. `dradonbreath_lily.png` - Fiery lily (note: typo in original)
2. `void_lotus.png` - Dark lotus
3. `eternalfrost_pine.png` - Frozen pine
4. `starfall_mushroom.png` - Glowing mushroom
5. `worldtree_seedling.png` - Ancient tree

## 🎨 Image Requirements

- **Format**: PNG with transparency
- **Size**: 512x512 pixels (or any square size)
- **Style**: Consistent artistic style across all plants
- **Background**: Transparent
- **File size**: Keep under 500KB each for performance

## 🖼️ How Images Are Used

1. **During Growth**: Emoji placeholders are shown (🌰→🌱→🌿→🌾→🌲→🌺)
2. **After Harvest**: Actual plant image is displayed
3. **In Plantdex**: Plant image shows once discovered
4. **Fallback**: If image fails to load, shows 🌺 emoji

## 🎨 Where to Get Images

### Option 1: AI Image Generation
Use tools like:
- DALL-E
- Midjourney
- Stable Diffusion
- Leonardo.ai

Prompt examples:
- "Magical moonbell fern plant, fantasy style, transparent background, game asset"
- "Mystical dewdrop moss with sparkling droplets, RPG game icon, PNG"

### Option 2: Create Your Own
- Use Photoshop, GIMP, or Procreate
- Draw in your preferred style
- Export as PNG with transparency

### Option 3: Commission an Artist
- Hire on Fiverr, Upwork
- Request all 15 plants in consistent style
- Specify: 512x512px, PNG, transparent background

### Option 4: Use Icon Libraries
Modify icons from:
- Flaticon.com
- Icons8.com
- TheNounProject.com

## 🔧 Testing Images

After adding images:

1. Open `index.html` in browser
2. Plant and harvest a few seeds
3. Check if images load correctly
4. Open browser console (F12) to see any loading errors
5. Check Plantdex to see all discovered plants

## 📊 Image Loading Logic

The app tries to load images like this:

```javascript
const image = new Image();
image.src = `assets/${tier}/${plant.icon}`;
image.onerror = () => {
    // Falls back to emoji 🌺
};
```

## 🚨 Troubleshooting

**Images don't show?**
- Check file names match exactly (case-sensitive!)
- Verify folder structure is correct
- Check browser console for 404 errors
- Ensure files are PNG format

**Images are too large?**
- Compress with TinyPNG.com
- Resize to 512x512 max
- Use PNG-8 instead of PNG-24 if no transparency needed

**Images look pixelated?**
- Use higher resolution source
- Export at 2x size (1024x1024) then scale down
- Use vector formats when possible

## 📦 Quick Start Option

If you don't have images yet:

1. The app works perfectly with emoji placeholders
2. Images are only shown AFTER harvest
3. You can add images gradually as you create/find them
4. The game is fully playable without any images

## 🎨 Placeholder Images

I've created simple SVG placeholders in the assets folder.
These are basic colored circles to help you test the image system.

To use real images, just replace these files with your PNG images!

---

**Need help creating images? Let me know what style you want!**
