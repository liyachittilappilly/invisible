

# Invisibility Cloak 🧙‍♂️✨

![Invisibility Cloak Demo](https://img.shields.io/badge/Status-Active-brightgreen) ![Python](https://img.shields.io/badge/Python-3.6%2B-blue) ![License](https://img.shields.io/badge/License-MIT-green)

A real-time "invisibility cloak" effect using computer vision! Step through the digital door and disappear from view - at least in the camera feed. While it might not make you literally invisible to life's chaos, it's a refreshing escape from unnecessary drama.

## Features

- **Real-time Background Replacement**: Seamlessly replaces colored objects with background imagery
- **Customizable Color Detection**: Easily configure which color to make "invisible" (pink by default)
- **Doraemon Door Effect**: Creates a magical portal effect when passing through
- **Simple Interface**: Minimal controls for easy operation
- **Performance Optimized**: Efficient processing for smooth real-time effects

## How It Works

The invisibility cloak effect is achieved through computer vision techniques:

1. **Background Capture**: The system first captures a static background scene
2. **Color Detection**: It then detects objects of a specific color (pink in the demo) in real-time
3. **Mask Creation**: A binary mask is created to identify areas with the target color
4. **Background Replacement**: The colored areas are replaced with the corresponding background pixels
5. **Real-time Processing**: All processing happens at ~30 FPS for a seamless experience

## Installation

### Prerequisites

- Python 3.6 or higher
- A working webcam
- OpenCV-compatible system

### Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/invisibility-cloak.git
   cd invisibility-cloak
   ```

2. Install the required packages:
   ```bash
   pip install opencv-python numpy
   ```

3. Run the application:
   ```bash
   python invisibility_cloak.py
   ```

## Usage

1. **Start the Application**: Run the script and position yourself in front of the camera.
2. **Capture Background**: Press 'b' to capture the background scene (make sure no colored objects are in view).
3. **Activate Cloak**: Press 'c' to activate the invisibility effect.
4. **Disappear**: Hold up a pink object (or wear pink clothing) and watch it become "invisible"!
5. **Adjust Settings**: Use the following keys to fine-tune the effect:
   - Press '+' to increase color sensitivity
   - Press '-' to decrease color sensitivity
6. **Exit**: Press 'q' to close the application.

### Controls

| Key | Action |
|-----|--------|
| b   | Capture background |
| c   | Toggle invisibility effect |
| +   | Increase color sensitivity |
| -   | Decrease color sensitivity |
| q   | Exit application |

## Requirements

- Python 3.6+
- OpenCV (cv2)
- NumPy
- A working webcam
- A pink object or clothing (or any color you configure)

## Customization

You can easily customize the cloak by modifying these parameters in the code:

- `target_color`: Change the color to detect (default: pink)
- `color_sensitivity`: Adjust how strictly the color is matched
- `blur_amount`: Control the amount of blur applied to the mask edges
- `min_area`: Minimum area size to consider as part of the cloak

## Technical Details

The project uses several computer vision techniques:

- **Color Thresholding**: HSV color space detection for robust color identification
- **Morphological Operations**: Opening and closing to clean up the mask
- **Gaussian Blurring**: To smooth edges and create a more realistic effect
- **Bitwise Operations**: To combine the foreground and background seamlessly

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by the classic Doraemon "Anywhere Door"
- Technique based on [this computer vision tutorial](https://lnkd.in/d2JMveec)
- Thanks to the OpenCV community for their amazing library

---

**Note**: This application uses your webcam only for local processing. No video data is transmitted or stored.

> "Sometimes you need to build something magical to remember." - Liya
