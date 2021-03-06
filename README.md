
<p align="center"><img width=12.5% src="https://raw.githubusercontent.com/simonmoreau/timestamp/master/TimeStamp/Resources/Icon.png"></p>
<h1 align="center">
  Time Stamper
</h1>

<h4 align="center">Keep track and manage the origin and authoring date of every Autodesk® Revit® element.</h4>

# Overview

Keep track and manage the origin and authoring date of every Revit element.

By adding some revision information on every element of a given Revit model, Time Stamper allows you to keep track of your model's history. With all the information, you can:

* Keep track of the origin and authoring date of each element in complex project
* Quickly compare two versions of a Revit file and graphically display their differences
* Create view filters for every linked Revit files
* Create a schedule of all linked models, along with their authoring date and origin
* Export these information in IFC, and get them on your favorite project review software.

For more information about the inner working of Time Stamper, please visit [Model TimeStamp](http://bim42.com/2015/07/model-timestamp/).

![Overview](https://raw.githubusercontent.com/simonmoreau/timestamp/master/TimeStamp/Resources/TimeStamper.gif)

# Getting Started

Edit _TimeStamp.csproj_, and make sure that the following lines a correctly pointing to your Revit installation folder:
* Line 50:     <HintPath>$(ProgramW6432)\Autodesk\Revit 2019\RevitAPI.dll</HintPath>
* Line 54:     <HintPath>$(ProgramW6432)\Autodesk\Revit 2019\RevitAPIUI.dll</HintPath>

Open the solution in Visual Studio 2017, buid it, and click on "Attach to process" to run Revit in debug mode. You can found more detail on how to run and debug a Revit addin in this [great blog post](http://archi-lab.net/debugging-revit-add-ins/).

## Installation

There is two ways to install this plugin in Revit:

### The easy way

Download the installer on the [Autodesk App Exchange](https://apps.autodesk.com/RVT/en/Detail/Index?id=232313135819866372&appLang=en&os=Win64)

### The (not so) easy way

You install Time Stamper just [like any other Revit add-in](http://help.autodesk.com/view/RVT/2018/ENU/?guid=GUID-4FFDB03E-6936-417C-9772-8FC258A261F7), by copying the add-in manifest (_"TimeStamp.addin"_), the assembly DLL (_"TimeStamp.dll"_) and the associated help file (_"TimeStampHelp.html"_) to the Revit Add-Ins folder (%APPDATA%\Autodesk\Revit\Addins\2019).

If you specify the full DLL pathname in the add-in manifest, it can also be located elsewhere. However, this DLL, its dependanties and help files must be locted in the same folder.

## Built With

* .NET Framework 4.7 and [Visual Studio Community](https://www.visualstudio.com/vs/community/)
* The Visual Studio Revit C# and VB add-in templates from [The Building Coder](http://thebuildingcoder.typepad.com/blog/2017/04/revit-2018-visual-studio-c-and-vb-net-add-in-wizards.html)

# Development

Want to contribute? Great, I would be happy to integrate your improvements!

To fix a bug or enhance an existing module, follow these steps:

* Fork the repo
* Create a new branch (`git checkout -b improve-feature`)
* Make the appropriate changes in the files
* Add changes to reflect the changes made
* Commit your changes (`git commit -am 'Improve feature'`)
* Push to the branch (`git push origin improve-feature`)
* Create a Pull Request

# Bug / Feature Request

If you find a bug (values not added, error while running the application, ...), kindly open an issue [here](https://github.com/simonmoreau/timestamp/issues/new) by including a screenshot of your problem and the expected result.

If you'd like to request a new function, feel free to do so by opening an issue [here](https://github.com/simonmoreau/timestamp/issues/new). Please include workflows samples and their corresponding results.

# License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

# Contact information

This software is an open-source project mostly maintained by myself, Simon Moreau. If you have any questions or request, feel free to contact me at [simon@bim42.com](mailto:simon@bim42.com) or on Twitter [@bim42](https://twitter.com/bim42?lang=en).

# Revision list

| **Version Number** | **Version Description** |
| :-------------: |:-------------|
1.2.0|Support for Autodesk® Revit® 2019 Version.
1.1.0|Add revision information on all elements or only in the active view. Keep or override previous data. Support for Autodesk® Revit® 2018 Version.
1.0.0|First release