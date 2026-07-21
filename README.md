# keybard (it's not misspelt)

![Keybard](https://github.com/poggersv2/keybard/blob/main/assets/readme/case_render.png)

## Overview
**keybard** is a custom mechanical keyboard designed for Hackclub Keeb. Its a modified 60% layout, extended with a dedicated arrow key cluster and a column of macro keys on the side. 

The board is powered by a Raspberry Pi Pico (Orpheus Pico) and uses a sandwich mount case.

## Features
- **Layout:** Modified 60% + Arrow Keys + Macro Column
- **Microcontroller:** Raspberry Pi Pico / Orpheus Pico (RP2040)
- **Mounting Style:** Sandwich Mount
- **Firmware:** RMK with VIA support

## Why I Built It
Standard 60% keyboards are great for desk space but I wanted to have the arrow keys for productivity (and also games).

## What I Learned
Designing and building this board from scratch was kindda difficult: 

### 1. Switch Matrix 
Routing the matrix while making it look decent was hard.

### 2. Tolerances 
When designing the case, I found it hard to imagine the actual size of everything. The maths was a little hard to understand, but that got easier over time.

### 3. CAD
Before this project, I didn't really know how to use Fusion. I had to learn everything from scratch.

## Hardware Details

### Schematic
![Schematic](https://github.com/poggersv2/keybard/blob/main/assets/readme/schematic.png?raw=true)

### PCB
![PCB](https://github.com/poggersv2/keybard/blob/main/assets/readme/pcb.png?raw=true)
![PCB Front](https://github.com/poggersv2/keybard/blob/main/assets/readme/pcb_front.png?raw=true)
![PCB Back](https://github.com/poggersv2/keybard/blob/main/assets/readme/pcb_back.png?raw=true)

### Case
![Case](https://github.com/poggersv2/keybard/blob/main/assets/readme/case.png?raw=true)

## Firmware
### How to Compile and Flash
### 1. Get the Firmware
1. Go to the **Actions** tab at the top of this GitHub repository.
2. Click on the latest successful run of the **Build RMK firmware** workflow.
3. Scroll down to the **Artifacts** section at the bottom of the page.
4. Download the compiled firmware `.zip` file and extract it to find your `.uf2` file.

### 2. Flash to the Keyboard
1. Unplug your keyboard.
2. Hold down the **BOOTSEL** button on your Raspberry Pi Pico.
3. While holding the button, plug the keyboard back into your computer via USB. 
4. A new mass storage drive will appear on your computer.
5. Drag and drop the `.uf2` firmware file into this drive.
6. The Pico will automatically reboot, and your keyboard is ready to use!

## Customization
### Keymap Editing (Vial)
This firmware is pre-configured with **Vial** , meaning you can remap your keys, setup macros, and change layers without needing to recompile firmware.

1. Download the Vial app or use the Web UI at [vial.rocks](https://vial.rocks/).
2. Plug in your keyboard and click **Authorize** (if using the web version) or let the app detect it.
3. Remap to your hearts content!

