# 🎮 Retro-Modern Tetris

A unique dual-mode Tetris game that seamlessly transforms between 1985 retro ASCII style and 2025 modern 3D graphics with a single click.

## [Live DEMO](https://jvibeschool.com/tetris/)

## 🌟 Game Features

### 🕹️ Dual Mode Experience
- **Retro Mode (1985)**: Authentic ASCII art with monochrome green terminal aesthetics
- **Modern Mode (2025)**: Beautiful 3D blocks with glassmorphism UI and gradient effects
- **One-Click Toggle**: Switch between modes instantly by clicking "RETRO" or "2025"

### 🎵 Dynamic Audio System
- **Retro Mode**: Classic 8-bit beep sounds using square wave oscillators
- **Modern Mode**: Rich, layered audio with sine, triangle, and sawtooth waves
- **Context-Aware**: Different sounds for movement, rotation, landing, line clears, and game over

### 🎨 Visual Excellence
- **Retro Mode**: 
  - Pure ASCII characters (`#`, `|`, `+`, `-`)
  - Monospace Courier New font
  - Classic green-on-black terminal colors
  - Authentic 1985 PC gaming feel

- **Modern Mode**:
  - 3D gradient blocks with realistic lighting
  - Glassmorphism UI with blur effects
  - Animated rainbow gradients
  - Grid background for precise positioning
  - Metallic base plate for realistic physics feel

### 🎯 Classic Gameplay
- **7 Original Pieces**: I, O, T, S, Z, J, L with authentic rotation patterns
- **Original Scoring**: 40/100/300/1200 points for 1/2/3/4 lines
- **Progressive Difficulty**: Speed increases every 10 lines cleared
- **Smooth Controls**: Responsive keyboard input with proper collision detection

## 🎮 Controls

| Key | Action |
|-----|--------|
| `←` `→` | Move left/right |
| `↓` | Soft drop |
| `↑` | Rotate piece |
| `SPACE` | Hard drop |
| `R` | Restart game |
| `ESC` | Pause/Resume |

## 🚀 Quick Start

1. **Download**: Save `tetris.html` and `tetris.svg` to the same folder
2. **Open**: Double-click `tetris.html` or open in any modern web browser
3. **Play**: Use arrow keys to control pieces
4. **Switch Modes**: Click "RETRO" or "2025" to toggle between styles

## 📱 Browser Compatibility

- ✅ Chrome 66+
- ✅ Firefox 60+
- ✅ Safari 12+
- ✅ Edge 79+

*Requires Web Audio API support for sound effects*

---

## 👨‍💻 Developer Guide

### 🛠️ Technology Stack

#### Frontend
- **HTML5**: Semantic structure and canvas-free rendering
- **CSS3**: Advanced features including:
  - CSS Grid for perfect block alignment
  - Linear gradients and animations
  - Backdrop filters for glassmorphism
  - Custom properties for theming
- **Vanilla JavaScript (ES6+)**: Pure JavaScript implementation
  - Classes and modules
  - Arrow functions and destructuring
  - Template literals for dynamic HTML

#### Audio System
- **Web Audio API**: Real-time audio synthesis
  - OscillatorNode for tone generation
  - GainNode for volume control
  - BiquadFilterNode for audio filtering
  - Dynamic frequency modulation

### 🏗️ Architecture

```
tetris.html
├── CSS Styles
│   ├── Base styles (retro mode)
│   └── Modern mode overrides (.modern-style)
├── HTML Structure
│   ├── Game container
│   ├── Game board
│   ├── Info panel
│   └── Game over overlay
└── JavaScript Game Engine
    ├── Tetris class (main game logic)
    ├── Audio system (Web Audio API)
    ├── Rendering system (DOM manipulation)
    └── Input handling (keyboard events)
```

### 🎯 Core Components

#### Game Engine (`Tetris` class)
```javascript
class Tetris {
    constructor()     // Initialize game state
    spawnNewPiece()   // Generate random pieces
    checkCollision() // Physics detection
    placePiece()      // Lock pieces to board
    clearLines()      // Line clearing logic
    updateDisplay()   // Render current state
}
```

#### Audio System
```javascript
initAudio()           // Initialize Web Audio Context
playRetroSound()      // 8-bit square wave synthesis
playModernSound()     // Rich multi-oscillator audio
playSound()           // Mode-aware sound dispatcher
```

#### Rendering Pipeline
1. **State Calculation**: Combine board state with current piece
2. **Mode Detection**: Check current visual mode
3. **DOM Generation**: Create appropriate HTML structure
4. **Style Application**: Apply CSS classes and inline styles
5. **Audio Feedback**: Trigger contextual sound effects

### 🎨 Styling System

#### CSS Architecture
- **Base Layer**: Retro mode styles (default)
- **Modern Layer**: `.modern-style` class overrides
- **Component-Based**: Modular CSS for each game element
- **Responsive**: Flexible layout adapting to content

#### Color Schemes
```css
/* Retro Mode */
--retro-bg: #000000
--retro-fg: #00ff00
--retro-border: #00ff00

/* Modern Mode */
--modern-gradient: linear-gradient(135deg, #667eea, #764ba2)
--modern-glass: rgba(255, 255, 255, 0.1)
--modern-shadow: 0 25px 50px rgba(0, 0, 0, 0.4)
```

### 🔧 Customization Guide

#### Adding New Piece Types
1. Define shape in `this.pieces` object
2. Add rotation states in `this.rotations` object
3. Create CSS class for modern mode styling
4. Update piece type storage system

#### Modifying Audio
1. Extend `playRetroSound()` for new 8-bit effects
2. Add cases to `playModernSound()` for rich audio
3. Update `playSound()` dispatcher
4. Consider audio context state management

#### Styling Modifications
1. Update base CSS for retro mode changes
2. Add `.modern-style` overrides for modern mode
3. Maintain visual consistency across modes
4. Test responsive behavior

### 📊 Performance Considerations

- **60fps Target**: Game loop optimized for smooth animation
- **Memory Management**: Efficient array operations for board state
- **Audio Optimization**: Proper oscillator cleanup to prevent memory leaks
- **DOM Efficiency**: Minimal DOM manipulation per frame

### 🧪 Testing Checklist

#### Functionality
- [ ] All 7 pieces spawn and rotate correctly
- [ ] Collision detection works in all scenarios
- [ ] Line clearing removes correct rows
- [ ] Scoring system matches original Tetris
- [ ] Game over triggers appropriately

#### Audio
- [ ] All sounds play in both modes
- [ ] No audio artifacts or clicks
- [ ] Proper volume levels
- [ ] Audio context resumes after user interaction

#### Visual
- [ ] Mode switching works seamlessly
- [ ] All animations are smooth
- [ ] Responsive layout on different screen sizes
- [ ] Color schemes are consistent

### 🚀 Deployment

1. **Static Hosting**: Upload `tetris.html` and `tetris.svg` to any web server
2. **CDN**: Use for faster global delivery
3. **PWA**: Add service worker for offline play
4. **Mobile**: Consider touch controls for mobile devices

### 📄 License

This project is open source. Feel free to modify and distribute.

---

*Built with ❤️ for retro gaming enthusiasts and modern web developers*
