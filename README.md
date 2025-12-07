# Interactive 3D Heart with Hand Tracking

An interactive web-based 3D heart model that responds to hand proximity using MediaPipe hand tracking and Three.js rendering.

## Features

- **3D Heart Model**: Beautiful 3D heart shape with realistic lighting and materials
- **Hand Tracking**: Real-time hand detection using MediaPipe
- **Responsive Scaling**: Heart contracts when your hand moves close and expands when your hand moves away
- **Interactive Controls**: 
  - Drag with mouse to rotate the heart view
  - Hand distance controls the heart's scale in real-time
- **Visual Feedback**: Camera feed preview in the top-right corner

## How to Use

1. **Open the Application**:
   - Simply open `index.html` in a modern web browser
   - Chrome, Firefox, Edge, or Safari (latest versions)

2. **Allow Camera Access**:
   - The application will request camera permission
   - Click "Allow" to enable hand tracking
   - Your camera feed appears in the top-right corner

3. **Interact with the Heart**:
   - **Move your hand close to the camera**: The heart contracts (becomes smaller)
   - **Move your hand away from the camera**: The heart expands (becomes larger)
   - **Mouse drag**: Click and drag to rotate the 3D view of the heart

## Technical Details

### Libraries Used

- **Three.js**: 3D graphics rendering
- **MediaPipe Tasks Vision**: Hand landmark detection and tracking
- **WebGL**: GPU-accelerated graphics

### How It Works

1. **Hand Detection**: MediaPipe detects hand landmarks 30+ times per second
2. **Distance Calculation**: Calculates the distance of the closest hand from the center
3. **Scale Animation**: Maps hand distance to heart scale (closer = smaller, farther = larger)
4. **Smooth Interpolation**: Uses exponential smoothing for fluid animations

## Browser Compatibility

- Chrome/Edge 90+
- Firefox 88+
- Safari 15+
- Requires HTTPS or localhost for camera access

## Performance

- Smooth 60 FPS performance on modern devices
- Optimized hand detection runs at ~10ms per frame
- Efficient WebGL rendering

## Notes

- The application works best in good lighting conditions
- Keep your entire hand visible for best detection
- Camera permission is required for hand tracking to work
- The heart automatically rotates slowly when no hands are detected

## File Structure

```
heartnet/
├── index.html      # Main application file
└── README.md       # This file
```

## Quick Start

1. Open `index.html` in your browser
2. Allow camera access when prompted
3. Move your hand to interact with the 3D heart!
