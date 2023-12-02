# Rainmeter Per-Core Graph

![Rainmeter Per-Core Graph Screenshot](https://github.com/QinnShou/RM-PerCoreGraph/blob/main/plugin%20screenshot.png)

(Left:Windows Task Manager / Right: Rainmeter skin)

## Introduction

Welcome to "Rainmeter Per-Core Graph," a highly functional Rainmeter skin crafted for detailed monitoring of CPU utilization across all 24 cores. This skin features a unique 6x4 grid layout and is designed to provide a comprehensive view of your CPU's performance with an emphasis on customization and user experience.

## Features

- **Per-Core CPU Monitoring**: Displays the utilization of each of the 24 CPU cores, offering a detailed perspective on your CPU's performance.
- **6x4 Grid Layout**: Organizes core data in a user-friendly 6x4 grid, making it easy to read and interpret CPU activity.
- **Customizable Appearance**: Allows for personalization in sizing and coloring, with special emphasis on color differentiation for P-core/E-core types.
- **Real-Time Updates**: Keeps you informed with dynamic, real-time data, ensuring you always have the latest information.
- **Resource Efficiency**: Optimized for minimal impact on system resources, combining functionality with efficiency.

## Getting Started

To get started with "Rainmeter Per-Core Graph," download the `.rmskin` package from this repository. Make sure Rainmeter is installed on your system (version [specify version] or higher is recommended). Follow the instructions in the **Installation Guide** below to seamlessly integrate the skin into your desktop.

## Installation Guide

1. **Install Rainmeter**: If not already installed, download and install Rainmeter from [Rainmeter's official website](https://www.rainmeter.net/).
2. **Download and Install the Skin**: Obtain the `.rmskin` file from this repository and double-click to install.
3. **Load the Skin**: Right-click the Rainmeter icon in the system tray, navigate to `Skins`, find "Rainmeter Per-Core Graph", and load it.
4. **Customize**: Right-click on the skin for customization options. Adjust the size, color, and other settings to match your desktop theme.

## Customizing the Skin

"Rainmeter Per-Core Graph" offers extensive customization options, allowing you to tailor the skin's appearance to your personal taste. You can adjust colors for P-cores and E-cores, as well as modify graph padding and size. Below are the steps to customize these elements:

### Adjusting Core Colors
The skin allows separate color configurations for P-cores and E-cores using RGB variables. To customize these colors:

1. **Access the Skin's INI File**: Open the skin's `.ini` file in a text editor.
2. **Locate the Color Variables**: Find the variables for core colors. For P-cores, look for variables prefixed with `L` for lines and `S` for solid colors (e.g., `LR`, `LG`, `LB`, `LA` for line color and `SR`, `SG`, `SB`, `SA` for solid color). For E-cores, variables start with `E` (e.g., `ELR`, `ELG`, `ELB`, `ELA` for line color and `ESR`, `ESG`, `ESB`, `ESA` for solid color).
3. **Edit the RGB Values**: Change these values to your desired colors. For example:
   ```ini
   ; P-core Line Color (White)
   LR=255
   LG=255
   LB=255
   LA=120
   
   ; E-core Line Color (Light Green)
   ELR=220
   ELG=255
   ELB=220
   ELA=120

 ### Modifying Graph Padding and Size

Customize the padding and size of the graphs as follows:

1. **Open the INI File**: Again, in the skin's .ini file.
2. **Adjust Size and Padding Variables**: Modify variables like GraphW, GraphH, GraphWPad, and GraphHPad to change graph dimensions and spacing. For instance:
   ```ini
   GraphW=60       ; Width of each graph
   GraphH=60       ; Height of each graph
   GraphWPad=10    ; Horizontal padding
   GraphHPad=10    ; Vertical padding

### Applying Customizations

After making changes:

1. **Save the INI File**: Confirm all modifications are saved.
2. **Refresh the Skin**: Right-click the Rainmeter icon in the system tray, find your skin, and select 'Refresh' to apply your customizations.

These steps allow you to personalize the "Rainmeter Per-Core Graph" to better suit your desktop environment and visual preferences.

## Acknowledgments and Contributions

This project was developed with assistance from ChatGPT, an AI language model by OpenAI, which provided valuable support in writing and structuring the Rainmeter skin. We appreciate the contribution of ChatGPT in the development process.

Your feedback and contributions to this project are welcome. Please feel free to file issues or submit pull requests with your improvements.

## License

"Rainmeter Per-Core Graph" is released under the Creative Commons Attribution-Non-Commercial-Share Alike 3.0 License.
