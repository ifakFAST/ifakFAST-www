# ifak*FAST* Mediator

## Modular platform for process monitoring and supervisory control

The ifak*FAST* Mediator enables the composition and integration of modules that provide specific functionality for generic automation needs including data acquisition, visualization, alarm management and control. It can be used to build SCADA-like applications by combining generic modules like data acquisition with application specific modules, e.g. for asset management or online sensor quality evaluation.

The Mediator core is responsible for supervision and integration of the modules and provides time series data management and role-based rights management. Higher-level functionality needs to be provided by modules. A module is a software component with a specific configuration model (typically in form of an XML file) that defines a set of variables. A variable represents a runtime changing value with timestamp and quality, e.g. a measurement or set-point. A module may read and write variables and the configuration of other modules and may provide specific services for use by other modules.

Running the Mediator requires [.Net Core 3.1](https://www.microsoft.com/net/download). Future versions of the Mediator will allow for creating modules with Java.

The Mediator core and all generic modules in this repository are licensed under the MIT License. We offer [professional support](mailto:fast@ifak.eu) for development and customization of ifak*FAST* based solutions.

## Available generic modules

### Module **IO**

* Used for signal-based data acquisition, e.g. via OPC DA or OPC UA
* Extensible through adapters for different protocols
* Configuration of scheduling and historization

### Module **Dashboard**

* Provides a web-based dashboard for visualization and interaction
* A dashboard consists of a set of customizable views, e.g. for IO and alarms and events
* Extensible by providing your own views in form of single-page web apps

### Module **EventLog**

* Used for management of events (like warnings and alarms) that are sent by modules
* Enables the acknowledgement and reset of warnings and alarms
* Enables notifications to users, e.g. by e-mail

### Module **Simba# Control** (not part of open-source distribution)

* Enables model-based supervisory control solutions
* Define control model by flow-based diagrams with [SIMBA#](https://simba.ifak.eu/)
* Evaluate control solution by integrated simulation of process and control model

## Quick Start
1. Get the [latest release](https://github.com/ifakFAST/Mediator.Net/releases/latest)
2. Unzip
3. Run: Either start *Run.bat* on Windows or type *sh Run.bat* on Linux
4. Navigte to http://localhost:8082/ using the browser
5. Login with user name and password, for default values see ReadMe.txt

## Further documentation
* IO adapter implementation for custom data sources: [HowTo_AdapterIO](https://github.com/ifakFAST/Mediator.Net/blob/master/Doc/HowTo_AdapterIO.md)
* Module implementation for application logic: [HowTo_Modules](https://github.com/ifakFAST/Mediator.Net/blob/master/Doc/HowTo_Modules.md)
* Dashboard view implementation for application specific user interfaces: [HowTo_DashboardViews](https://github.com/ifakFAST/Mediator.Net/blob/master/Doc/HowTo_DashboardViews.md)
