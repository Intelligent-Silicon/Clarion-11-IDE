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


### Font Test 3 - Tahoma, Cascadia Code

```
<Properties name="CoreProperties.ComponentsFont">
    <Array name="ListOfFonts">
        <Element value="ListControls|List Controls|Tahoma,9" />
        <Element value="StartPage|Start Page|Tahoma,17" />
        <Element value="TextEditor|Text Editor, Output Window (Proportional Font)|Cascadia Code,11" />
    </Array>
</Properties>
<Properties name="AppGen Dialogs">
    <DlgFontName value="Tahoma" />
    <DlgFontSize value="9" />
    <DlgFontStyle value="400" />
</Properties>
```

StartPage - Tahoma 17
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest3/FontTest3-StartPage.png)

Dictionary - Tahoma 9
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest3/FontTest3-Dct.png)

AppGen - Tahoma 9
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest3/FontTest3-AppGen.png)

Window Formatter - Tahoma 9 
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest3/FontTest3-WindowFormatter.png)

Listbox Formatter - Tahoma 9 
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest3/FontTest3-ListboxFormatter.png)

Embed Tree - Tahoma 9
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest3/FontTest3-Embeds.png)

Embed Source - Cascadia Code 10
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/FontChanges/FontTest3/FontTest3-EmbedSource.png)





### Conclusion

Comparing each image of different parts of the IDE, in their own seperate browser window in order to Alt-Tab between the two, in terms of ledgability, ```Verdana``` seems to be a good font for the general IDE, but ```Courier New``` stills seems to have the edge for the text editor when using the Default Colour Scheme.

A "Dark Mode" colour scheme could still alter all of that.




