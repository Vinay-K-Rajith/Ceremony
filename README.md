# Video Keyboard Controller Setup

## Files Required
- `index.html` - Main HTML file (created)
- `kv.mp4` - Your video file (place in same directory as index.html)

## How to Use

### 1. Place Your Video
Copy your `kv.mp4` file into the `d:\Vellaku\` directory alongside `index.html`.

### 2. Open in Browser
- Double-click `index.html`, OR
- Open with: `file:///d:/Vellaku/index.html` in your browser, OR
- Use a local server (recommended for better compatibility):
  ```
  python -m http.server 8000
  # Then open: http://localhost:8000
  ```

### 3. Keyboard Controls
| Key | Action |
|-----|--------|
| **1** | Play Section 1 (0-4s), loop between 3-4s |
| **2** | Play Section 2 (4-9s), loop between 8-9s |
| **3** | Play Section 3 (9-14s), loop between 13-14s |
| **4** | Play Section 4 (14-16s), loop between 15-16s |
| **5** | Play remaining video (16s to end) continuously |

## Features

✅ Full-screen video background  
✅ First frame shown on page load  
✅ Real-time video time display  
✅ Loop status indicator  
✅ Progress bar at bottom  
✅ Visual keyboard guide on screen  
✅ Smooth seeking between sections  
✅ No audio during playback (muted)  

## Customization

To adjust section timings, edit the `sections` object in the JavaScript:

```javascript
const sections = {
    1: { start: 0, end: 4, loopStart: 3, loopEnd: 4, name: 'Section 1' },
    // Modify start, end, loopStart, loopEnd values as needed
};
```

## Browser Compatibility

Works best in:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)

## Troubleshooting

**Video not loading:**
- Ensure `kv.mp4` is in the same folder as `index.html`
- Check browser console for errors (F12)
- Verify video format is supported (MP4 with H.264 codec)

**Looping not working:**
- Check your video duration matches the loop timings
- Browser autoplay policies may require user interaction first

**Local file access issues:**
- Use a local HTTP server instead of opening the file directly
- Modern browsers restrict file:// access for security
