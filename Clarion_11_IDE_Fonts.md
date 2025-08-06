# Clarion 11 IDE Fonts

The Clarion 11 IDE has a section where the Fonts for the IDE can be set. The GUI doesnt provide any facility to change the text colour and there isnt an option in the ```ClarionProperties.xml``` file. Font colours are set by changing the theme, discussed in [Clarion 11 IDE Colour Mode](Clarion_11_IDE_Colour_Mode.md).

You can find this Font section in ```Clarion 11 IDE:Tools, Options, IDE, Fonts```.

The first dropdown list box lists the different parts of the IDE and below that the Font thats in use: 

| IDE Part | Default Font Name | Default Size |
| --- | --- | --- |
| Dialogs | Segoe UI | 9 |
| List Controls | Segoe UI | 9 |
| Start Page | Segoe UI | 17 |
| Text Editor, Output Window, (Proportional Font). | Courier New  | 12 |


These settings are stored in the ```%UserProfile%\AppData\Roaming\SoftVelocity\Clarion\11.0\ClarionProperties.xml``` file.

```
<Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
        <Element value="ListControls|List Controls|Segoe UI,9" />
        <Element value="StartPage|Start Page|Segoe UI,17" />
        <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Courier New,12" />
    </Array>
</Properties>
<Properties name="AppGen Dialogs">
    <DlgFontName value="Segoe UI" />
    <DlgFontSize value="9" />
    <DlgFontStyle value="400" />
</Properties>
```

In order to gain more real estate in the IDE, choosing a legible font is important. These 3 fonts listed below ship with Windows 11 by default and are sometimes touted as suitable for Developers.

Obviously another major factor for a chosen font is the monitor that will be displaying it. These fonts work very well on the lowest quality laptop monitor, bright light situations with monitor washout and suitable for aging coders defying cataracts.

| \# | Shortest Font First | Widest Font First |
| --- | --- | --- |
| 1. | Verdana | Verdana |
| 2. | Tahoma | Tahoma |
| 3. | Noto Sans | Noto Sans |



Reset the IDE ```Clarion 11 IDE:Tools, Reset IDE Settings```, click the ```Exit``` button that appears in the popup window and then close the IDE. This has the effect of resetting the flyout pinnable pads back to their default positions but it leaves the Font settings the same. Below are sections which show the different parts of the IDE with different font settings. To change the font, close the IDE before making any change to the ClarionProperties.xml file.

Default Settings:

```Clarion 11 IDE:Tools, Options, IDE, Appearance```
Ambience: Clarion 

DockTabs Style: Firefox

Toolbar Colour Scheme: Default

Use Small Icons on Toolbars: Ticked


Default App: Invoice.app

Default Dct: Invoice.dct

Screenshots: StartPage, Dictionary, AppGen, Window Formatter, Listbox Formatter, Embed Tree, Embed Source


### Font Test 1 - Default Fonts 

```
<Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
        <Element value="ListControls|List Controls|Segoe UI,9" />
        <Element value="StartPage|Start Page|Segoe UI,17" />
        <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Courier New,12" />
    </Array>
</Properties>
<Properties name="AppGen Dialogs">
    <DlgFontName value="Segoe UI" />
    <DlgFontSize value="9" />
    <DlgFontStyle value="400" />
</Properties>
```

StartPage - Segoe UI 17
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest1/FontTest1-StartPage.png)

Dictionary - Segoe UI 9
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest1/FontTest1-Dct.png)

AppGen - Segoe UI 9
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest1/FontTest1-AppGen.png)

Window Formatter - Segoe UI 9 
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest1/FontTest1-WindowFormatter.png)

Listbox Formatter - Segoe UI 9 
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest1/FontTest1-ListboxFormatter.png)

Embed Tree - Segoe UI 9
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest1/FontTest1-Embeds.png)

Embed Source - Courier New 12
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest1/FontTest1-EmbedSource.png)


### Installing Cascadia Code

Cascadia Code is a new font designed by Microsoft specifically for Developers. Its now the default font in Visual Studio. 

It can be downloaded from here: https://github.com/microsoft/cascadia-code

Installation Steps:

- Go to the Releases section on the GitHub page. (https://github.com/microsoft/cascadia-code/releases)

- Download the latest .zip file (look for one labeled something like ttf or variable).

- Unzip the file and locate the .ttf font files.

- Right-click on each font file and select Install or Install for all users.

Reload Clarion and select Cascadia Code, and then reload Clarion IDE once more.



### Font Test 2 - Verdana, Cascadia Code

```
<Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
        <Element value="ListControls|List Controls|Verdana,9" />
        <Element value="StartPage|Start Page|Verdana,17" />
        <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Cascadia Code,10" />
    </Array>
</Properties>
<Properties name="AppGen Dialogs">
    <DlgFontName value="Verdana" />
    <DlgFontSize value="9" />
    <DlgFontStyle value="400" />
</Properties>
```

StartPage - Verdana 17
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest2/FontTest2-StartPage.png)

Dictionary - Verdana 9
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest2/FontTest2-Dct.png)

AppGen - Verdana 9
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest2/FontTest2-AppGen.png)

Window Formatter - Verdana 9 
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest2/FontTest2-WindowFormatter.png)

Listbox Formatter - Verdana 9 
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest2/FontTest2-ListboxFormatter.png)

Embed Tree - Verdana 9
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest2/FontTest2-Embeds.png)

Embed Source - Cascadia Code 10
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest2/FontTest2-EmbedSource.png)




StartPage
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Tahoma-Font-StartPage.png)

AppGen Tree - 3 more procedures visible - PrintInvoice, PrintMailingLabels, PrintPRO:KeyProductSKU
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Tahoma-Font-AppGen-Tree.png)

Embed Tree - 3 more embed nodes - Maximize, Maximize Generated Code, Maximized
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Tahoma-Font-Embeds.png)

Embed Source - 2 less lines of code - missing Rel1::Icon and Rel1::Level
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Tahoma-Font-EmbedEditor-Source.png)

So 2nd variation is to reduce the size of Text Editor Font. 

```
<Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
        <Element value="ListControls|List Controls|Tahoma,9" />
        <Element value="StartPage|Start Page|Tahoma,17" />
        <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Tahoma,9" />
    </Array>
</Properties>
<Properties name="AppGen Dialogs">
    <DlgFontName value="Tahoma" />
    <DlgFontSize value="9" />
    <DlgFontStyle value="400" />
</Properties>
```
This time more lines are visible in the Text Editor.


Embed Source - 6 more lines of code.
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Tahoma-Font-EmbedEditor-Source-9.png)

Problem is Courier New is a nice fixed font to use for coding, and Clarion 6 used MS Sans Serif, so lets see how that looks and compares.

MS Sans Serif doesnt appear to ship with Windows 11, so trying out the Sans Serif Collection at the original size of 12.
```
<Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
      <Element value="ListControls|List Controls|Tahoma,9" />
      <Element value="StartPage|Start Page|Tahoma,17" />
      <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Sans Serif Collection,12" />
    </Array>
  </Properties>
  <Properties name="AppGen Dialogs">
    <DlgFontName value="Tahoma" />
    <DlgFontSize value="9" />
    <DlgFontStyle value="400" />
  </Properties>
```
Embed Source - SansSerif Collection Size 12.
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/SansSerif-Font-EmbedEditor-Source-12.png)


```
<Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
      <Element value="ListControls|List Controls|Tahoma,9" />
      <Element value="StartPage|Start Page|Tahoma,17" />
      <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Sans Serif Collection,9" />
    </Array>
  </Properties>
  <Properties name="AppGen Dialogs">
    <DlgFontName value="Tahoma" />
    <DlgFontSize value="9" />
    <DlgFontStyle value="400" />
  </Properties>
```

Embed Source - SansSerif Collection Size 9 - Still unusable!
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/SansSerif-Font-EmbedEditor-Source-9.png)


Cascadia Code is a new font designed by Microsoft specifically for Developers. Its now the default font in Visual Studio. 

It can be downloaded from here: https://github.com/microsoft/cascadia-code

Installation Steps:

- Go to the Releases section on the GitHub page. (https://github.com/microsoft/cascadia-code/releases)

- Download the latest .zip file (look for one labeled something like ttf or variable).

- Unzip the file and locate the .ttf font files.

- Right-click on each font file and select Install or Install for all users.

Reload Clarion and select Cascadia Code, and then reload Clarion once more.

```
  <Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
      <Element value="ListControls|List Controls|Tahoma,9" />
      <Element value="StartPage|Start Page|Tahoma,17" />
      <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Cascadia Code,12" />
    </Array>
  </Properties>
  <Properties name="AppGen Dialogs">
    <DlgFontName value="Tahoma" />
    <DlgFontSize value="9" />
    <DlgFontStyle value="400" />
  </Properties>
```
Embed Source - Cascadia Code Size 12 - Nice, but less lines visible.
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Cascadia-Code-Font-EmbedEditor-Source-12.png)


```
  <Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
      <Element value="ListControls|List Controls|Tahoma,9" />
      <Element value="StartPage|Start Page|Tahoma,17" />
      <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Cascadia Code,9" />
    </Array>
  </Properties>
  <Properties name="AppGen Dialogs">
    <DlgFontName value="Tahoma" />
    <DlgFontSize value="9" />
    <DlgFontStyle value="400" />
  </Properties>
```

Embed Source - Cascadia Code Size 9 - Nice, more lines but a bit too small, especially on this tiny low quality laptop screen.
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Cascadia-Code-Font-EmbedEditor-Source-9.png)

```
  <Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
      <Element value="ListControls|List Controls|Cascadia Code,10" />
      <Element value="StartPage|Start Page|Cascadia Code,17" />
      <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Cascadia Code,10" />
    </Array>
  </Properties>
  <Properties name="AppGen Dialogs">
    <DlgFontName value="Cascadia Code" />
    <DlgFontSize value="10" />
    <DlgFontStyle value="400" />
  </Properties>
```
Embed Source - Cascadia Code Size 10 - Nice, more lines and usable, especially on this tiny low quality laptop screen.
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Cascadia-Code-Font-EmbedEditor-Source-10.png)

Now the ```Tahoma``` is just a little bit too thin, the i's and l's dont have much space between them, so a short in height font but one thats wide might be better
for this low quality laptop monitor. Verdana is another font which fits that bill, so using this as a font with the sizes shown below, lets have a look at how it compares.
```
  <Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
      <Element value="ListControls|List Controls|Verdana,9" />
      <Element value="StartPage|Start Page|Verdana,17" />
      <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Cascadia Code,10" />
    </Array>
  </Properties>
  <Properties name="AppGen Dialogs">
    <DlgFontName value="Verdana" />
    <DlgFontSize value="9" />
    <DlgFontStyle value="400" />
  </Properties>
```
Start Page
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Verdana-Font-StartPage.png)
  
AppGen Tree
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Verdana-Font-AppGen-Tree.png) 

Window Formatter
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Verdana-Font-WindowFormatter.png)

Listbox Formatter
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Verdana-Font-WindowFormatter-Listbox.png)

Embeds
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/Verdana-Font-Embeds.png)




However there is a section where it appears themes can be added.

You can find this section in ```Tools, Options, Text Editor, XML Schemas```.

The schemas listed here can be found in the following folder:

```C:\Clarion11\data\schemas```

Searching for information on .addins and what might be possible turns up these links:

At this stage it probably a good idea to find out what version of SharpDevelop was licenced by SoftVelocity.

https://www.c-sharpcorner.com/article/writing-an-addin-for-sharpdevelop-1-0-with-visual-studio-20/

https://blog.myget.org/post/2013/07/16/how-sharpdevelop-uses-myget-and-nuget.html

https://sdesmedt.wordpress.com/2007/02/16/add-your-own-programming-language-to-sharpdevelop-part-1-make-your-templates-available/

https://www.codeproject.com/Articles/12587/Building-Applications-with-the-SharpDevelop-Core

https://stackoverflow.com/questions/32908595/sharpdevelop-developing-plugins

https://sourceforge.net/projects/sdclassdiagram/

https://www.codeproject.com/Articles/33792/FindReferences-of-N-Order-SharpDevelop-Add-In

https://www.youtube.com/watch?v=w76hgcNFu8A


