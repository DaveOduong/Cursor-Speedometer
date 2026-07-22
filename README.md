##Cursor Speedometer

A lightweight web application that measures your mouse cursor's movement speed in real time. As you move the cursor across the screen, the application calculates its speed in **pixels per second (px/s)** and records the highest speed reached during the session.

---

## Overview

Cursor Speedometer tracks the position of your mouse and continuously calculates how fast it is moving by measuring the distance traveled between consecutive mouse events.

The application displays:

- Current cursor speed
- Maximum speed reached during the session

The interface is minimal, responsive, and updates smoothly in real time.

---

## Features

- Real-time cursor speed measurement
- Displays speed in **pixels per second (px/s)**
- Tracks maximum cursor speed
- Smooth speed updates using `requestAnimationFrame()`
- Automatically resets speed to zero when the cursor stops moving
- Modern dark-themed interface
- Responsive design
- No external libraries or frameworks required

---

## Technologies Used

- HTML5
- CSS3
- Vanilla JavaScript

---

## How It Works

The application listens for mouse movement events across the browser window.

For every movement:

1. Records the current cursor position.
2. Calculates the horizontal and vertical movement.
3. Computes the straight-line (Euclidean) distance between the previous and current positions.
4. Measures the elapsed time.
5. Calculates speed using:

```
Speed = Distance ÷ Time
```

where:

- Distance is measured in pixels.
- Time is measured in seconds.

The speed is displayed instantly, while the highest recorded speed is saved until the page is refreshed.

---

## Formula Used

```
Distance = √((x₂ − x₁)² + (y₂ − y₁)²)

Speed = Distance / Time
```

---

## Displayed Information

| Metric | Description |
|---------|-------------|
| Current Speed | Current cursor movement speed in pixels per second |
| Max Speed | Highest cursor speed recorded during the current session |

---

## Running the Project

1. Download the project files.
2. Open `index.html` in any modern web browser.
3. Move your mouse around the page.
4. Watch the current speed and maximum speed update in real time.

No installation or internet connection is required.

---

## Project Structure

```
CursorSpeedometer/
│
├── index.html
└── README.md
```

---

## Example

If your cursor moves:

- **300 pixels**
- in **0.1 seconds**

The calculated speed will be:

```
300 ÷ 0.1 = 3,000 px/s
```

The application will display:

```
Current Speed: 3,000 px/s
```

If this is the fastest movement so far, it also updates:

```
Max Speed: 3,000 px/s
```

---

## Future Improvements

- Speed graph over time
- Average cursor speed
- Session statistics
- Distance traveled counter
- Click counter
- Drag speed measurement
- Adjustable measurement units
- Fullscreen tracking mode
- Export session statistics
- Dark/Light mode toggle

---

## Educational Value

This project demonstrates:

- Mouse event handling
- Real-time animation
- Euclidean distance calculations
- Time-based motion analysis
- DOM manipulation
- Performance API (`performance.now()`)
- `requestAnimationFrame()`
- Responsive web design

---

## License

This project is free to use for educational and personal purposes.

---

## Author

Created as a web-based JavaScript project demonstrating real-time mouse movement tracking and speed calculation using browser event handling and animation techniques.
