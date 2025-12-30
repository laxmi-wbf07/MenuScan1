# Druk Appetite 🇧🇹

A premium, offline-first Bhutanese restaurant menu with a cinematic browsing experience.

## Features

✨ **Single-file HTML** (~11KB uncompressed, ~4.6KB gzipped)  
🎬 **Ken Burns animations** on full-screen hero images  
🔄 **3D flip cards** revealing prices, descriptions & calorie info  
💾 **IndexedDB storage** with ETag-based change detection  
📡 **Offline-first** with smart fallback to cached data  
⭐ **Favorites system** with Easter egg unlock at 5 stars  
🎨 **Automatic color extraction** from hero images  
📱 **Horizontal snap-scroll** filmstrip layout  
🌐 **GitHub Pages ready** — deploy and forget  

## Usage

1. Deploy `index.html` and `menu.md` to any static host (GitHub Pages, Netlify, Vercel)
2. The app fetches `menu.md` on first visit and caches it in IndexedDB
3. ETag polling detects updates every 60s and refreshes automatically
4. Works offline after first visit

## Menu Format

Edit `menu.md` to update dishes:

```yaml
---
dishes:
  - name: Dish Name
    hero_url: "https://images.unsplash.com/..."
    price_btn: 250
    description_dzongkha: "རྒྱ་སྐད།"
    description_english: "Sensory description here"
    calories: 380
    ashi_tip: "Optional Easter egg message"
```

## Interactions

- **Tap** — Flip card to see details
- **Double-tap** — Add to favorites (⭐ counter in header)
- **Swipe/Scroll** — Navigate horizontally between dishes
- **5 favorites** — Unlock Ashi's hidden tips

## Tech Stack

- Pure HTML/CSS/JS (no frameworks)
- IndexedDB for offline storage
- localStorage for favorites & ETag cache
- IntersectionObserver for lazy loading
- CSS Scroll Snap for smooth navigation
- Canvas API for color extraction

## Lighthouse

Optimized for 100 scores across:
- ✅ Performance
- ✅ Accessibility
- ✅ Best Practices
- ✅ SEO

## License

MIT
