## Monitor your 3D Prints in Home Assistant and NodeRed using AI Vision (GPT4)

This NodeRed flow was designed for use with ha-bambulab https://github.com/greghesp/ha-bambulab, but can be modified for use with any video stream that you have available in Home Assistant. It is a NodeRed flow that accepts camera streams as an input and outputs a state (quality 1-10), and a text description of the print quality that GPT4 sees.

This project is still in the works and contributions are appreciated!

[![ha states screen](https://raw.githubusercontent.com/myrakrusemark/3D-Print-Quality-Monitor-HA-NodeRes-GPT4-Vision-/main/other/ha-states.png "ha states screen")](https://raw.githubusercontent.com/myrakrusemark/3D-Print-Quality-Monitor-HA-NodeRes-GPT4-Vision-/main/other/ha-states.png "ha states screen")

##Required NodeRed Nodes
- node-red-contrib-string
- node-red-contrib-image-tools
- node-red-contrib-simple-gpt-vision

## Setup
- Import flows.json into NodeRed running as an add-on for Home Assistant.
- Update the "Printer Cameras List" Inject node to include a list of printer names.
[![nodered printers list](https://raw.githubusercontent.com/myrakrusemark/3D-Print-Quality-Monitor-HA-NodeRes-GPT4-Vision-/main/other/printers-list.png)](https://raw.githubusercontent.com/myrakrusemark/3D-Print-Quality-Monitor-HA-NodeRes-GPT4-Vision-/main/other/printers-list.png)
- The flow is set to run once every 10 minutes. Its about 1 US cent to process the 1280x720 image from a Bambu printer. Over the course of a four hour print, the processing cost is about 25 cents.
- Notification action and action flows are not yet finished.

## Samples in sample-chatgpt-tests
[![Sample tests](https://raw.githubusercontent.com/myrakrusemark/3D-Print-Quality-Monitor-HA-NodeRes-GPT4-Vision-/main/sample-chatgpt-tests/Screenshot%202024-02-10%20121304.png "Sample tests")](https://github.com/myrakrusemark/3D-Print-Quality-Monitor-HA-NodeRes-GPT4-Vision-/tree/main/sample-chatgpt-tests "Sample tests")

## Appreciated Contributions
- Update Notification/Actions to apply toward the specific printers when there are multiple printers
- Update flows to make it simpler for use with any camera stream
- More readable and comprehensive documentation
- Support for other Vision models
- Deliver relevant photo in the Companion App notification
- Better visibility of black models
- Prompt Optimization




