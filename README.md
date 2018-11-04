# Production OOP

The Production OOP program is a mock manufacturing management
application that makes use of several tenets of object oriented
design and programming.

## Getting Started

To use this program, simply include the package files in your Java project and instantiate objects using the subclasses of the **Product** abstract class, which implments the **Item** and **Comparable<>** interfaces. The two primary class types used to create objects are **AudioPlayer** and **MoviePlayer** which both implement the **MultimediaControls** interface. The **MoviePlayer** class also includes an inner class **Screen** to store the details of the built-in display.
The intended use is to instantiate several objects of both **AudioPlayer** and **MoviePlayer** types and store into one ArrayList, which may be sorted because of the implementation of the **Comparable** interface.


### Prerequisites

This program should run on any modern JRE version (8+).

### Opening in IDE (tested in IntelliJ IDEA Ulitimate 2018.2)

Simply import the **com.wyattbyroade.productionoop** package into a new or existing project and use the following syntax to instantiate objects:
```java
AudioPlayer audioplayer1 = new AudioPlayer(String name, String audioSpecification);
```
\- or - 
```java
Screen screenParam = new Screen(String resolution, int refreshrate, int responsetime);

MoviePlayer moviePlayer1 = new MoviePlayer(String nameInput, Screen screenParam, MonitorType monitorType);
```
### Installation and Use

Clone repository from github: git clone https://github.com/wabyroade/ProductionOOP.git

* Navigate to production output folder of java compiler:
```
cd [repository_root]/out/production/ProductionOOP
```
* Run the java command with the fully qualified name of the driver class as the argument:
```
java com.wyattbyroade.productionoop.Main
```

### Expected output with default test driver:
```
Manufacturer : OracleProduction
Serial Number : 3
Date : Sun Nov 04 10:24:39 EST 2018
Name : DBPOWER MK101
Resolution :  720x480
Refresh Rate : 40
Response Time : 22
Monitor Type : LCD
Manufacturer : OracleProduction
Serial Number : 4
Date : Sun Nov 04 10:24:39 EST 2018
Name : Pyle PDV156BK
Resolution : 1366x768
Refresh Rate : 40
Response Time : 22
Monitor Type : LED
Manufacturer : OracleProduction
Serial Number : 2
Date : Sun Nov 04 10:24:39 EST 2018
Name : Walkman
Audio Spec : WAV
Type : AUDIO
Manufacturer : OracleProduction
Serial Number : 1
Date : Sun Nov 04 10:24:39 EST 2018
Name : iPod Mini
Audio Spec : MP3
Type : AUDIO
```
<br><br>
## Application Design


### Class Diagram (generated by IntelliJ IDEA)
![Class diagram generated by IntelliJ IDEA](https://raw.githubusercontent.com/wabyroade/ProductionOOP/master/Package%20productionoop.png)

### Methods specified by Item interface:
```java
*  String manufacturer = "OracleProduction";
*  void setProductionNumber(int productionNumberInput);
*  void setName(String nameInput);
*  String getName();
*  Date getManufactureDate();
*  int getSerialNumber();
```

### Methods specified by MultimediaControl interface:
```java
*  void play();
*  void stop();
*  void previous();
*  void next();
```

### Methods specified by the ScreenSpec interface:
```java
*  String getResolution();
*  int getRefreshRate();
*  int getResponseTime();
```
## Educational Concepts:
* **Interfaces** - Three interfaces were created to ensure consistent operation and interaction across multiple class types.
* **Abstract Classes** - The use of the **Product** abstract class gives the inherited concrete classes certain common fields and methods.
* **Polymorphism** - The above-mentioned abstract class and interfaces allow the objects to be handled with the same data types and methods.
* **Generics** - Certain data storage types and methods have been designed to work with different types of objects.
* **Enum types** - The ItemType and MonitorType enums are reference types used to define a set of constants for the types of objects and utilize them.
