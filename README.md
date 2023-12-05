# Rainmeter Per-Core Graph

![Rainmeter Per-Core Graph Screenshot](https://github.com/QinnShou/RM-PerCoreGraph/blob/main/plugin%20screenshot%202.png)

(Left:Windows Task Manager / Right: Rainmeter skin)

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

## Customization
You can customize the following aspects:
- Graph dimensions variables (`GraphW`, `GraphH` for each graph width and height).
- Padding variables (`GraphWPad`, `GraphHPad` for width and height padding).

### P-Core and E-Core Coloring
This plugin supports distinct coloring options for different CPU core types:

- **P-Core (Performance Core) Coloring**: By default, the plugin uses the regular color settings (Line and Solid Fill) for P-cores. These are your CPU's primary cores focused on delivering maximum performance.
- **E-Core (Efficiency Core) Coloring**: For CPUs with efficiency cores, you can use the enhanced color settings (E-Line and E-Solid) to visually differentiate these cores in the graph. This is particularly useful for processors that combine high-performance and high-efficiency cores.

To switch the graph color scheme for a specific core to the E-core coloring, manually update the relevant `[CPUxGraph]` section in the `.ini` file to use `#ESR`, `#ESG`, `#ESB`, and `#ESA` for the `SolidColor` and `#ELR`, `#ELG`, `#ELB`, and `#ELA` for the `PrimaryColor`.

To adjust these settings, edit the `[Variables]` section in the `.ini` file.

Example of graph section source code:
   ``ini
   [CPU5Graph]
   Meter=#MeterValue#
   MeasureName=MeasureCPU5
   X=((6*#GraphWPad#)+(5*#GraphW#))
   Y=((1*#GraphHPad#)+(0*#GraphH#))
   W=#GraphW#
   H=#GraphH#
   PrimaryColor=#LR#,#LG#,#LB#,#LA#
   SolidColor=#SR#,#SG#,#SB#,#SA#
   AntiAlias=#AntiAliasValue#
   ``

   ``ini
   [CPU17Graph]
   Meter=#MeterValue#
   MeasureName=MeasureCPU17
   X=((6*#GraphWPad#)+(5*#GraphW#))
   Y=((3*#GraphHPad#)+(2*#GraphH#))
   W=#GraphW#
   H=#GraphH#
   PrimaryColor=#ELR#,#ELG#,#ELB#,#ELA#
   SolidColor=#ESR#,#ESG#,#ESB#,#ESA#
   AntiAlias=#AntiAliasValue#
   ``

## Contributing
Contributions to improve the plugin are welcome. Please feel free to fork the repository, make your changes, and submit a pull request.

## License
This project is licensed under the Creative Commons Attribution-Non-Commercial-Share Alike 3.0 License. See the [LICENSE](LICENSE.md) file for more details.

## Acknowledgments
This project was significantly aided by ChatGPT-4 from OpenAI, which provided invaluable assistance in the development of the "CPU Usage Per-Core Graph" skin and the composition of this README.md. Special thanks to OpenAI for creating such a powerful tool, and to the Rainmeter community for their continued support and inspiration.


