# Rainmeter CPU Per-Core Graph

![Rainmeter Per-Core Graph Screenshot](https://github.com/QinnShou/RM-PerCoreGraph/blob/main/plugin%20screenshot%202.png)

(Windows Task Manager/Rainmeter skin)

## Description
The "CPU Usage Per-Core Graph" is a Rainmeter skin plugin designed to visually display CPU usage for each logical processor. This plugin offers unique features like automatic margin adjusting and per-core coloring, making it an essential tool for monitoring CPU performance in a visually appealing way.

## Features
- **Per-Core CPU Usage Visualization**: Displays CPU usage for each of your computer's logical processors.
- **Per-Core Coloring**: Different colors for each CPU core, enhancing the visual distinction between cores.
- **Automatic Margin Adjusting**: Ensures that the graph is always aligned and presented neatly.
- **Customizable Appearance**: Options to change graph width, height, and colors according to core type manually (P-core/E-core).

## Installation
1. Ensure you have [Rainmeter](https://www.rainmeter.net/) installed.
2. Download the `.rmskin` file from the [releases page](<github-release-link>).
3. Double-click the downloaded file to install the skin.

## Usage
- Load the skin through Rainmeter's Manage interface.
- Edit the .ini file to customize the appearance.

# Customization
You can customize the following aspects:
- Graph size (`GraphW`, `GraphH` for each graph width and height).
- Padding size (`GraphWPad`, `GraphHPad` for width and height padding).
- Core Coloring (RGB format #LR, #LG, #LB, #LA; #ELR, #ELG, #ELB, #ELA).
- Option of rounded corner.

### Graph auto-margin/size formula
   ```ini
   X=((CurrentColumn+1)*GraphWPad)+((CurrentColumn*GraphW)
   Y=((CurrentRow+1)*GraphHPad)+((CurrentRow)*GraphH)
   W=GraphW
   H=GraphH
   ```
The margin of 6x4 is used by default. Modify variables of [CPUXXGraphWrapper] by the end of the ini for other margins.

### Rounded corner config by YeyeBBC
   ```ini
   ; ShapeValue=Rectangle [Relative X][Relative Y][Width][Height][Cornor radius X][Cornor radius Y]
   ShapeValue=Rectangle 0,0,#GraphW#,#GraphH#,4,4
   ```

### Core Coloring
By default, the plugin uses the regular color settings (Line and Solid Fill, white and gray) for P-cores. These are your CPU's primary cores focused on delivering maximum performance. E-core is colored green by default.
To switch the graph color scheme for a specific core to the E-core coloring, manually update the relevant `[CPUxGraph]` section in the `.ini` file to use `#ESR`, `#ESG`, `#ESB`, and `#ESA` for the `SolidColor` and `#ELR`, `#ELG`, `#ELB`, and `#ELA` for the `PrimaryColor`.

To adjust these settings, edit the `[Variables]` section in the `.ini` file.

## Authors
QinnShou (author of script)
YeyeBBC (author of several function)
ChatGPT by OpenAI (assisting with basic script structure, rainmeter Q&A, writting this readme.md)

## License
This project is licensed under the Creative Commons Attribution-Non-Commercial-Share Alike 3.0 License. See the [LICENSE](LICENSE.md) file for more details.





