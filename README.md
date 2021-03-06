# Climber Selection Bar
> Horizontal selection bar with initial selection capabilities. Selections through both click and swipes.

## Purpose and Description
The selection bar that also serves as a "trigger" for initial selections. For feature list see screenshots below.

Works only with Qlik Sense 3.0 and up!!

## Screenshots
1. Field - Standard horizontal selection from any field in the application. Intended for use with Year/Month field but will of course work with any field.  
![Alt text](./screenshots/screenshot_field.PNG?raw=true "Horizontal field selection")
2. Variable - For variable selection of single ("always one selected") variable. Typical use is for currency selection.  
![Alt text](./screenshots/screenshot_variable.PNG?raw=true "Horizontal variable selection")
3. Flags - Easy country selection where you don't have room for a map but want something that looks nice.  
![Alt text](./screenshots/screenshot_flag.PNG?raw=true "Screenshot flags")
4. Initial selection - Any field/variable can be set for an initial selection using an expression or comma separated list.  
![Alt text](./screenshots/screenshot_initial_selection.PNG?raw=true "Screenshot initial selection")
5. Date range picker (Experimental!) - Drop down calendar for selection of dates
![Alt text](./screenshots/screenshot_date_range_picker.PNG?raw=true "Date Range Picker")
## Installation

1. Download the latest version of Qlik Sense (3.0 or higher)
2. Qlik Sense Desktop
	* To install, copy all files in the .zip file to folder "C:\Users\[%Username%]\Documents\Qlik\Sense\Extensions\cl-horizontalselectionbar\"
3. Qlik Sense Server
	* See instructions [how to import an extension on Qlik Sense Server](http://help.qlik.com/en-US/sense/Subsystems/ManagementConsole/Content/import-extensions.htm)

## Configuration

* Select the typ of list you need (Field,Variable,Flag or Date Range Picker) 
* Enter a reference to:
	* Field - Any field or an expression that works as a dimension
	* Variable - Has to be an existing variable created either in the script or the gui. Selectable variables are entered in a comma separated list.
	* Flag - Select a field that has a country name corresponding with the flag names. (Has to be a perfect match with the flag name so check the list of flags if you are not sure.)
	* Date Range Picker - A field holding a date field with a "complete" set of dates. (i.e. no gaps in the timeline) It uses the DateFormat variable for the date format, both to parse the dates and when selections are made. If the Today expression is left blank it default to Now().
* Add a field label 
* Add an initial selection if you want. This will also work with expressions such as "=Year(Today())-1".
* You can set initial selections to be updated once per session or every time you move to a sheet.

## Alignment alternatives
1. Left - All lists aligned to the left  
![Alt text](./screenshots/screenshot_align_left.PNG?raw=true "Align Left")
2. Right - All lists aligned to the right (Sometimes works well with two selection bars combined on the top row. One right-aligned and one left-aligned)   
![Alt text](./screenshots/screenshot_align_right.PNG?raw=true "Align Right")
3. Center - All lists as closed to the center as possible. (Leaves sides empty if space is available.) 
![Alt text](./screenshots/screenshot_align_center.PNG?raw=true "Align Center")
4. Center Spread - All lists centered but with outermost lists pushed towards the edges. (Works well when you want to use the full screen width for one selection bar object with multiple lists.)  
![Alt text](./screenshots/screenshot_align_centerspread.PNG?raw=true "Align Center Spread")
5. Stack - All lists on top of eachother. (Works when using more than one grid height of the selection bar. Also good for smaller screens.)
![Alt text](./screenshots/screenshot_align_stacked.PNG?raw=true "Align Stacked")

## Contributing
Contributing to this project is welcome. The process to do so is outlined below:

1. Create a fork of the project
2. Work on whatever bug or feature you wish
3. Create a pull request (PR)

I cannot guarantee that I will merge all PRs.

## Known issues
Initial selections will not work on calculated dimensions/autogenerated date fields.

## Author

**Karl Fredberg Sjöstrand @ Climber**
* http://github.com/ClimberAB


## Change Log

See [CHANGELOG](CHANGELOG.yml)

## License & Copyright
The software is made available "AS IS" without any warranty of any kind under the MIT License (MIT).

See [Additional license information for this solution.](LICENSE.md)