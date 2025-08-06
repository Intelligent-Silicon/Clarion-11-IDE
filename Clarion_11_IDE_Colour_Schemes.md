# Clarion 11 IDE Colour Schemes

The Clarion 11 IDE permits different colour modes to be used. 

These settings affect the #Develop parts of the IDE, and not the main AppGen & Dct part's of the IDE.

[Toolbar Color Schemes](Clarion_11_IDE_Colour_Schemes.md#toolbar-color-schemes)

[ARGB numbers](Clarion_11_IDE_Colour_Schemes.md#argb-numbers)

[\<docktabstripappearance>](Clarion_11_IDE_Colour_Schemes.md#docktabstripappearance)

[\<dockpadtitleappearance>](Clarion_11_IDE_Colour_Schemes.md#dockpadtitleappearance)

[\<docktabappearance-active>](Clarion_11_IDE_Colour_Schemes.md#docktabappearance-active)

[\<docktabappearance-inactive>](Clarion_11_IDE_Colour_Schemes.md#docktabappearance-inactive)

[\<docktabappearance-padactive>](Clarion_11_IDE_Colour_Schemes.md#docktabappearance-padactive)

[\<docktabappearance-padhide>](Clarion_11_IDE_Colour_Schemes.md#docktabappearance-padhide)

[\<docktabappearance-padhideover>](Clarion_11_IDE_Colour_Schemes.md#docktabappearance-padhideover)

[\<applicationheaderappearance>](Clarion_11_IDE_Colour_Schemes.md#applicationheaderappearance)

[\<startpageappearance>](Clarion_11_IDE_Colour_Schemes.md#startpageappearance)

[\<buttonappearance>](Clarion_11_IDE_Colour_Schemes.md#buttonappearance)

[\<buttonappearance-checkedappearance>](Clarion_11_IDE_Colour_Schemes.md#buttonappearance-checkedappearance)

[\<buttonappearance-pressedappearance>](Clarion_11_IDE_Colour_Schemes.md#buttonappearance-pressedappearance)

[\<buttonappearance-selectedappearance>](Clarion_11_IDE_Colour_Schemes.md#buttonappearance-selectedappearance)

[\<gripappearance>](Clarion_11_IDE_Colour_Schemes.md#gripappearance)

[\<imagemarginappearance>](Clarion_11_IDE_Colour_Schemes.md#imagemarginappearance)

[\<menuitemappearance>](Clarion_11_IDE_Colour_Schemes.md#menuitemappearance)

[\<menustripappearance>](Clarion_11_IDE_Colour_Schemes.md#menustripappearance)

[\<overflowbuttonappearance>](Clarion_11_IDE_Colour_Schemes.md#overflowbuttonappearance)

[\<raftingcontainerappearance>](Clarion_11_IDE_Colour_Schemes.md#raftingcontainerappearance)

[\<separatorappearance>](Clarion_11_IDE_Colour_Schemes.md#separatorappearance)

[\<statusstripappearance>](Clarion_11_IDE_Colour_Schemes.md#statusstripappearance)

[\<toolstripappearance>](Clarion_11_IDE_Colour_Schemes.md#toolstripappearance)




### Toolbar Color Schemes

This encompasses, toolbars and flyout pinnable pads.

An online topic & discussion can be found here at :

[ClarionHub.com - Custom Themes and Color Schemes for the IDE](https://clarionhub.com/t/custom-themes-and-color-schemes-for-the-ide/126) 

[ClarionHub.com - Share your custom syntax highlighting scheme here!](https://clarionhub.com/t/share-your-custom-syntax-highlighting-scheme-here/453/1)

The XML files responsible for the colour of the IDE can be found in :

```%CWroot%\data\resources\ColorThemes```

which translates to:

 ```C:\Clarion11\data\resources\ColorThemes```.

Its this folder, where you import or add your own "Toolbar" but should be called "IDE" color scheme XML files.

The standard Toolbar colour schemes which ship with Clarion are:
| Colour Scheme |
| --- |
| Default.xml |
| Office2003Blue.xml |
| Office2003Olive.xml |
| Office2003Silver.xml |
| Office2007.xml |
| OfficeBlack.xml |
| OfficeClassic.xml |
| OfficeXP.xml |
| SerenityBlue.xml |
| Win8Blue.xml |
| Win10Blue.xml |

You can select one of these colour schemes to colour the IDE by clicking on 
```Tools, Options, IDE, Appearance, scroll down to 'Select the Toolbar color scheme', and select one of the above from the drop down list box.```

If you are editing individual sections and elements in one of the colour scheme XML files, its enough to select ```Tools, Options, IDE, Appearance, OK button``` to trigger the reloading of the colour scheme, if the one selected is the same one being editted at the same time in another program like Notepad++.


The XML file consists of different sections to represent the different parts of the IDE.
```
<DockTabStripAppearance>
<DockPadTitleAppearance>
<DockTabAppearance>
<ApplicationHeaderAppearance>
<StartPageAppearance>
<ButtonAppearance>
<GripAppearance>
<ImageMarginAppearance>
<MenuItemAppearance>
<MenuStripAppearance>
<OverflowButtonAppearance>
<RaftingContainerAppearance>
<SeparatorAppearance>
<StatusStripAppearance>
<ToolStripAppearance>
```

Within each section there will be a number of elements some of which will be paired eg
```<xGradientBegin>``` & ```<xGradientEnd>```, ```<xActiveTextColor>``` & ```<xInactiveTextColor>```, ```<xActiveBackColorGradientBegin>``` & ```<xActiveBackColorGradientEnd>``` with ```<xInactiveBackColor>```.

### ARGB Numbers
The numbers within these elements are predominantly negative numbers eg -16777216. These are whats called ARGB (Alpha, Red, Green, Blue) number formats which are stored in a 32-bit integer (Clarion Long). You can also use basic colour names, like Red, White & Blue, and colour names like WhiteSmoke, ControlLight, ActiveBorder and GradientActiveCaption. 

You can find a full list of these named system colors in the [.NET SystemColors Class](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.systemcolors?view=net-9.0) documentation. It includes colors like ControlLight, ActiveBorder, GradientActiveCaption, and many others used in Windows UI elements.
For a more visual and OS-specific breakdown, this [GitHub gist of Windows system colors](https://gist.github.com/zaxbux/64b5a88e2e390fb8f8d24eb1736f71e0) is good. It shows the RGB and hex values for each color, grouped by UI category—like window borders, captions, controls, and text.

ARGB numbers range from 0 to 255, and the negative 32bit integer is calculated using Bshift, if you fancy building your own Clarion tool to modify the colour scheme XML files, or you can simply click the ellipse button next to the drop down list box listing the Toolbar colour schemes.

```Clarion
ARGBColor  LONG
Alpha      BYTE
Red        BYTE
Green      BYTE
Blue       BYTE

    Code
    ARGBColor = BShift(Alpha,24) + BShift(Red,16) + BShift(Green,8) + Blue
```

 
### \<DockTabStripAppearance>

Default 
```
<DockTabStripAppearance>
    <xGradientBegin>-986896</xGradientBegin>
    <xGradientEnd>-197380</xGradientEnd>
    <xTextColor>-6250336</xTextColor>
</DockTabStripAppearance>
```
To show what the \<DockTabStripAppearance> section affects in the IDE, the elements are coloured shades of Red to hilight easily, in 3 views, the Start page, the AppGen and the Dictionary view.

```
<DockTabStripAppearance>
  <xGradientBegin>-65536</xGradientBegin>      <!-- Dark red (#FF0000) -->
  <xGradientEnd>-25856</xGradientEnd>          <!-- Light red (#FF6A6A) -->
  <xTextColor>-16711936</xTextColor>           <!-- Lime Green (#00FF00) -->
</DockTabStripAppearance>
```
Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabStripAppearance/StartPage.png)

Dictionary
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabStripAppearance/Dct.png)

App Gen
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabStripAppearance/AppGen.png)



### \<DockPadTitleAppearance>

Default
```
<DockPadTitleAppearance>
    <xActiveBackColorGradientBegin>-460552</xActiveBackColorGradientBegin>
    <xActiveBackColorGradientEnd>-460552</xActiveBackColorGradientEnd>
    <xActiveTextColor>Gray</xActiveTextColor>
    <xInactiveBackColor>-986896</xInactiveBackColor>
    <xInactiveTextColor>Gray</xInactiveTextColor>
</DockPadTitleAppearance>
```

```
<DockPadTitleAppearance>
  <xActiveBackColorGradientBegin>-65536</xActiveBackColorGradientBegin>     <!-- Dark red (#FF0000) -->
  <xActiveBackColorGradientEnd>-25856</xActiveBackColorGradientEnd>         <!-- Light red (#FF6A6A) -->
  <xActiveTextColor>-16711936</xActiveTextColor>                            <!-- Lime Green (#00FF00) -->
  <xInactiveBackColor>-16744448</xInactiveBackColor>                        <!-- Green (#008000) -->
  <xInactiveTextColor>-256</xInactiveTextColor>                             <!-- Yellow (#FFFF00) -->
</DockPadTitleAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockPadTitleAppearance/StartPage.png)

Dictionary
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockPadTitleAppearance/Dct.png)

App Gen
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockPadTitleAppearance/AppGen.png)


### \<DockTabAppearance> \<Active>
Default
```
<Active>
    <xGradientBegin>-986896</xGradientBegin>
    <xGradientEnd>-986896</xGradientEnd>
    <xEdgeColor>-8355712</xEdgeColor>
    <xTextColor>-10066330</xTextColor>
</Active>
```

```
<Active>
    <xGradientBegin>-65536</xGradientBegin>       <!-- Deep Red (#FF0000) -->
    <xGradientEnd>-25856</xGradientEnd>           <!-- Light Red (#FF6A6A) -->
    <xEdgeColor>-16711936</xEdgeColor>            <!-- Lime Green (#00FF00) -->
    <xTextColor>-256</xTextColor>                 <!-- Yellow (#FFFF00) -->
</Active>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/Active/StartPage.png)

Dictionary
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/Active/Dct.png)

App Gen
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/Active/AppGen.png)


### \<DockTabAppearance> \<Inactive>
Default
```
<Inactive>
    <xGradientBegin>-986896</xGradientBegin>
    <xGradientEnd>-986896</xGradientEnd>
    <xTextColor>-10066330</xTextColor>
    <xEdgeColor>-855310</xEdgeColor>
</Inactive>
```

```
<Inactive>
    <xGradientBegin>-65536</xGradientBegin>       <!-- Deep Red (#FF0000) -->
    <xGradientEnd>-25856</xGradientEnd>           <!-- Light Red (#FF6A6A) -->
    <xTextColor>-256</xTextColor>                 <!-- Yellow (#FFFF00) -->
    <xEdgeColor>-16711936</xEdgeColor>            <!-- Lime Green (#00FF00) -->   
</Inactive>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/Inactive/StartPage.png)

Dictionary
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/Inactive/Dct.png)

App Gen
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/Inactive/AppGen.png)


### \<DockTabAppearance> \<PadActive>
Default
```
<PadActive>
    <xGradientBegin>-986896</xGradientBegin>
    <xGradientEnd>-986896</xGradientEnd>
    <xEdgeColor>Gray</xEdgeColor>
    <xTextColor>-12566464</xTextColor>
</PadActive>
```

```
<PadActive>
    <xGradientBegin>-65536</xGradientBegin>       <!-- Deep Red (#FF0000) -->
    <xGradientEnd>-25856</xGradientEnd>           <!-- Light Red (#FF6A6A) -->
    <xEdgeColor>-16711936</xEdgeColor>            <!-- Lime Green (#00FF00) -->
    <xTextColor>-256</xTextColor>                 <!-- Yellow (#FFFF00) -->
</PadActive>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/PadActive/StartPage.png)

Dictionary
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/PadActive/Dct.png)

App Gen
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/PadActive/AppGen.png)

### \<DockTabAppearance> \<PadHide>
Default
```
<PadHide>
    <xGradientBegin>-3876102</xGradientBegin>
    <xGradientEnd>-3876102</xGradientEnd>
    <xEdgeColor>-3876102</xEdgeColor>
    <xTextColor>-10066330</xTextColor>
</PadHide>
```

```
<PadHide>
  <xGradientBegin>-65536</xGradientBegin>       <!-- Deep Red (#FF0000) -->
  <xGradientEnd>-25856</xGradientEnd>           <!-- Light Red (#FF6A6A) -->
  <xEdgeColor>-16711936</xEdgeColor>            <!-- Lime Green (#00FF00) -->
  <xTextColor>-256</xTextColor>                 <!-- Yellow (#FFFF00) -->
</PadHide>
```
Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/PadHide/StartPage.png)

Dictionary
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/PadHide/Dct.png)

App Gen
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/DockTabAppearance/PadHide/AppGen.png)

### \<DockTabAppearance> \<PadHideOver>
Default
```
<PadHideOver>
    <xGradientBegin>-6373643</xGradientBegin>
    <xGradientEnd>-6373643</xGradientEnd>
    <xEdgeColor>-6373643</xEdgeColor>
    <xTextColor>-12566464</xTextColor>
</PadHideOver>
```

```
<PadHideOver>
    <xGradientBegin>-65536</xGradientBegin>       <!-- Deep Red (#FF0000) -->
    <xGradientEnd>-25856</xGradientEnd>           <!-- Light Red (#FF6A6A) -->
    <xEdgeColor>-16711936</xEdgeColor>            <!-- Lime Green (#00FF00) -->
    <xTextColor>-256</xTextColor>                 <!-- Yellow (#FFFF00) -->
</PadHideOver>
```

Hovering the Mouse over any of the hidden tabs does not change the colour, it just makes the pad flyout.


### \<ApplicationHeaderAppearance>
Default
```
<ApplicationHeaderAppearance>
    <xGradientBegin>-460552</xGradientBegin>
    <xGradientEnd>-460552</xGradientEnd>
</ApplicationHeaderAppearance>
```

```
<ApplicationHeaderAppearance>
  <xGradientBegin>-65536</xGradientBegin>       <!-- Deep Red (#FF0000) -->
  <xGradientEnd>-25856</xGradientEnd>           <!-- Light Red (#FF6A6A) -->
</ApplicationHeaderAppearance>
```

App Gen
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ApplicationHeaderAppearance/AppGen.png)


### \<StartPageAppearance>
For these changes to appear, besides reselecting ```Appearance``` in the IDE, you need to click on the ```StartPage``` for a refresh to occur.

Default
```
<StartPageAppearance>
    <xGradientBegin>Silver</xGradientBegin>
    <xGradientEnd>-2039584</xGradientEnd>
    <xSecondaryColor>-2039584</xSecondaryColor>
    <xPrimaryColor>-2039584</xPrimaryColor>
    <xButtonImageColor>-14584098</xButtonImageColor>
    <xGridHeaderColor>-1842205</xGridHeaderColor>
    <xGridBodyColor>-1</xGridBodyColor>
    <xGridAltBodyColor>-1</xGridAltBodyColor>
    <xGridLineColorr>-4934476</xGridLineColorr>
    <xGridHoverColorr>-4599318</xGridHoverColorr>
</StartPageAppearance>
```

```
<StartPageAppearance>
    <xGradientBegin>-65536</xGradientBegin>       <!-- Deep Red (#FF0000) -->
    <xGradientEnd>-25856</xGradientEnd>           <!-- Light Red (#FF6A6A) -->
    <xSecondaryColor>-2039584</xSecondaryColor>   
    <xPrimaryColor>-2039584</xPrimaryColor>       
    <xButtonImageColor>-14584098</xButtonImageColor>
    <xGridHeaderColor>-1842205</xGridHeaderColor>
    <xGridBodyColor>-1</xGridBodyColor>
    <xGridAltBodyColor>-1</xGridAltBodyColor>
    <xGridLineColorr>-4934476</xGridLineColorr>
    <xGridHoverColorr>-4599318</xGridHoverColorr>
</StartPageAppearance>
```
Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/StartPageAppearance/Gradient/StartPage.png)

```
<StartPageAppearance>
    <xGradientBegin>Silver</xGradientBegin>
    <xGradientEnd>-2039584</xGradientEnd>
    <xSecondaryColor>-256</xSecondaryColor>       <!-- Yellow (#FFFF00) -->
    <xPrimaryColor>-65536</xPrimaryColor>         <!-- Red (#FF0000) -->       
    <xButtonImageColor>-14584098</xButtonImageColor>
    <xGridHeaderColor>-1842205</xGridHeaderColor>
    <xGridBodyColor>-1</xGridBodyColor>
    <xGridAltBodyColor>-1</xGridAltBodyColor>
    <xGridLineColorr>-4934476</xGridLineColorr>
    <xGridHoverColorr>-4599318</xGridHoverColorr>
</StartPageAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/StartPageAppearance/PrimarySecondary/StartPage.png)

```
<StartPageAppearance>
    <xGradientBegin>Silver</xGradientBegin>
    <xGradientEnd>-2039584</xGradientEnd>
    <xSecondaryColor>-2039584</xSecondaryColor>   
    <xPrimaryColor>-2039584</xPrimaryColor>    
    <xButtonImageColor>-16711936</xButtonImageColor>    <!-- Green (#00FF00) -->
    <xGridHeaderColor>-65536</xGridHeaderColor>         <!-- Red (#FF0000) -->
    <xGridBodyColor>-23296</xGridBodyColor>             <!-- Orange (#FFA500-ish) -->
    <xGridAltBodyColor>-256</xGridAltBodyColor>         <!-- Yellow (#FFFF00) -->
    <xGridLineColorr>-16776961</xGridLineColorr>        <!-- Blue (#0000FF) -->
    <xGridHoverColorr>-8388480</xGridHoverColorr>       <!-- Purple (#800080) -->
</StartPageAppearance>
```
Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/StartPageAppearance/Grid/StartPage.png)


### \<ButtonAppearance> \<CheckedAppearance>
Default
```
<CheckedAppearance>
    <xBackground>-3874305</xBackground>
    <xBorderHighlight>-13395457</xBorderHighlight>
    <xGradientBegin>0</xGradientBegin>
    <xGradientEnd>0</xGradientEnd>
    <xGradientMiddle>0</xGradientMiddle>
    <xHighlight>-3874305</xHighlight>
    <xPressedBackground>-6697729</xPressedBackground>
    <xSelectedBackground>-6697729</xSelectedBackground>
</CheckedAppearance>
```

```
<CheckedAppearance>
    <xBackground>-65536</xBackground>               <!-- Red (#FF0000) -->
    <xBorderHighlight>-256</xBorderHighlight>       <!-- Yellow (#FFFF00) -->
    <xGradientBegin>0</xGradientBegin>
    <xGradientEnd>0</xGradientEnd>
    <xGradientMiddle>0</xGradientMiddle>
    <xHighlight>-3874305</xHighlight>
    <xPressedBackground>-6697729</xPressedBackground>
    <xSelectedBackground>-6697729</xSelectedBackground>
</CheckedAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ButtonAppearance/CheckedAppearance/Background/StartPage.png)

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ButtonAppearance/CheckedAppearance/Background/StartPage2.png)



```
<CheckedAppearance>
    <xBackground>-3874305</xBackground>
    <xBorderHighlight>-13395457</xBorderHighlight>
    <xGradientBegin>-65536</xGradientBegin>             <!-- Red (#FF0000) -->
    <xGradientMiddle>-23296</xGradientMiddle>           <!-- Orange (#FFA500) -->
    <xGradientEnd>-256</xGradientEnd>                   <!-- Yellow (#FFFF00) -->
    <xHighlight>-3874305</xHighlight>
    <xPressedBackground>-6697729</xPressedBackground>
    <xSelectedBackground>-6697729</xSelectedBackground>
</CheckedAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ButtonAppearance/CheckedAppearance/Gradient/StartPage.png)


```
<CheckedAppearance>
    <xBackground>-3874305</xBackground>
    <xBorderHighlight>-13395457</xBorderHighlight>
    <xGradientBegin>0</xGradientBegin>
    <xGradientEnd>0</xGradientEnd>
    <xGradientMiddle>0</xGradientMiddle>
    <xHighlight>-65536</xHighlight>                         <!-- Red highlight (#FF0000) -->
    <xPressedBackground>-256</xPressedBackground>           <!-- Yellow pressed state (#FFFF00) -->
    <xSelectedBackground>-16711936</xSelectedBackground>    <!-- Green selected state (#00FF00) -->
</CheckedAppearance>

```
Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ButtonAppearance/CheckedAppearance/Highlight/StartPage.png)

### \<ButtonAppearance> \<PressedAppearance>
Default
```
<PressedAppearance>
    <xBorder>-13395457</xBorder>
    <xBorderHighlight>-13395457</xBorderHighlight>
    <xGradientBegin>-6697729</xGradientBegin>
    <xGradientEnd>-6697729</xGradientEnd>
    <xGradientMiddle>-6697729</xGradientMiddle>
    <xHighlight>-6763521</xHighlight>
</PressedAppearance>
```

```
<PressedAppearance>
    <xBorder>-65536</xBorder>                               <!-- Red (#FF0000) -->
    <xBorderHighlight>-256</xBorderHighlight>               <!-- Yellow (#FFFF00) -->
    <xGradientBegin>-6697729</xGradientBegin>
    <xGradientEnd>-6697729</xGradientEnd>
    <xGradientMiddle>-6697729</xGradientMiddle>
    <xHighlight>-6763521</xHighlight>
</PressedAppearance>
```
No Visible Change

```
<PressedAppearance>
    <xBorder>-13395457</xBorder>
    <xBorderHighlight>-13395457</xBorderHighlight>
    <xGradientBegin>-65536</xGradientBegin>             <!-- Red (#FF0000) -->
    <xGradientEnd>-256</xGradientEnd>                   <!-- Yellow (#FFFF00) -->
    <xGradientMiddle>-23296</xGradientMiddle>           <!-- Orange (#FFA500) -->
    <xHighlight>-6763521</xHighlight>
</PressedAppearance>
```
Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ButtonAppearance/PressedAppearance/Gradient/StartPage.png)


```
<PressedAppearance>
    <xBorder>-13395457</xBorder>
    <xBorderHighlight>-13395457</xBorderHighlight>
    <xGradientBegin>-6697729</xGradientBegin>
    <xGradientEnd>-6697729</xGradientEnd>
    <xGradientMiddle>-6697729</xGradientMiddle>
    <xHighlight>-65536</xHighlight>                 <!-- Red (#FF0000) -->
</PressedAppearance>
```
No Visible Change

### \<ButtonAppearance> \<SelectedAppearance>
Default
```
<SelectedAppearance>
    <xBorder>-13395457</xBorder>
    <xBorderHighlight>-13395457</xBorderHighlight>
    <xGradientBegin>-4005633</xGradientBegin>
    <xGradientEnd>-4005633</xGradientEnd>
    <xGradientMiddle>-4005633</xGradientMiddle>
    <xHighlight>-3874305</xHighlight>
</SelectedAppearance>
```

```
<SelectedAppearance>
    <xBorder>-65536</xBorder>                               <!-- Red (#FF0000) -->
    <xBorderHighlight>-256</xBorderHighlight>               <!-- Yellow (#FFFF00) -->
    <xGradientBegin>-4005633</xGradientBegin>
    <xGradientEnd>-4005633</xGradientEnd>
    <xGradientMiddle>-4005633</xGradientMiddle>
    <xHighlight>-3874305</xHighlight>
</SelectedAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ButtonAppearance/SelectedAppearance/Border/StartPage.png)

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ButtonAppearance/SelectedAppearance/Border/StartPage2.png)


```
<SelectedAppearance>
    <xBorder>-13395457</xBorder>
    <xBorderHighlight>-13395457</xBorderHighlight>
    <xGradientBegin>-65536</xGradientBegin>             <!-- Red (#FF0000) -->
    <xGradientEnd>-256</xGradientEnd>                   <!-- Yellow (#FFFF00) -->
    <xGradientMiddle>-23296</xGradientMiddle>           <!-- Orange (#FFA500) -->
    <xHighlight>-3874305</xHighlight>
</SelectedAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ButtonAppearance/SelectedAppearance/Gradient/StartPage.png)

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ButtonAppearance/SelectedAppearance/Gradient/StartPage2.png)

```
<SelectedAppearance>
    <xBorder>-13395457</xBorder>
    <xBorderHighlight>-13395457</xBorderHighlight>
    <xGradientBegin>-4005633</xGradientBegin>
    <xGradientEnd>-4005633</xGradientEnd>
    <xGradientMiddle>-4005633</xGradientMiddle>
    <xHighlight>-65536</xHighlight>             <!-- Red (#FF0000) -->
</SelectedAppearance>
```

No Visible Change

### \<GripAppearance>
Default
```
<GripAppearance>
    <xDark>-4671304</xDark>
    <xLight>-1</xLight>
</GripAppearance>
```

```
<GripAppearance>
    <xDark>-65536</xDark>               <!-- Red (#FF0000) -->
    <xLight>-256</xLight>               <!-- Yellow (#FFFF00) -->
</GripAppearance>
```
No Visible Change

### \<ImageMarginAppearance>
Default
```
<ImageMarginAppearance>
    <Normal>
        <xGradientBegin>-197380</xGradientBegin>
        <xGradientEnd>-986896</xGradientEnd>
        <xGradientMiddle>-460552</xGradientMiddle>
    </Normal>
    <Revealed>
        <xGradientBegin>-394759</xGradientBegin>
        <xGradientEnd>-855310</xGradientEnd>
        <xGradientMiddle>-657931</xGradientMiddle>
    </Revealed>
</ImageMarginAppearance>
```

```
    <Normal>
        <xGradientBegin>-65536</xGradientBegin>         <!-- Red (#FF0000) -->
        <xGradientEnd>-256</xGradientEnd>               <!-- Yellow (#FFFF00) -->
        <xGradientMiddle>-23296</xGradientMiddle>       <!-- Orange (#FFA500) -->
    </Normal>
```  
    
Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ImageMarginAppearance/Normal/StartPage.png)

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ImageMarginAppearance/Normal/StartPage2.png)

```
    <Revealed>
        <xGradientBegin>-65536</xGradientBegin>         <!-- Red (#FF0000) -->
        <xGradientEnd>-256</xGradientEnd>               <!-- Yellow (#FFFF00) -->
        <xGradientMiddle>-23296</xGradientMiddle>       <!-- Orange (#FFA500) -->
    </Revealed>
```

No Visible Changes

### \<MenuItemAppearance>
Default
```
<MenuItemAppearance>
    <xBorder>-13395457</xBorder>
    <xPressedGradientBegin>-197380</xPressedGradientBegin>
    <xPressedGradientEnd>-460552</xPressedGradientEnd>
    <xPressedGradientMiddle>-657931</xPressedGradientMiddle>
    <xSelected>-3874305</xSelected>
    <xSelectedGradientBegin>-4005633</xSelectedGradientBegin>
    <xSelectedGradientEnd>-4005633</xSelectedGradientEnd>
</MenuItemAppearance>
```

```
<MenuItemAppearance>
    <xBorder>-65536</xBorder>                               <!-- Red highlight (#FF0000) -->
    <xPressedGradientBegin>-197380</xPressedGradientBegin>
    <xPressedGradientEnd>-460552</xPressedGradientEnd>
    <xPressedGradientMiddle>-657931</xPressedGradientMiddle>
    <xSelected>-3874305</xSelected>
    <xSelectedGradientBegin>-4005633</xSelectedGradientBegin>
    <xSelectedGradientEnd>-4005633</xSelectedGradientEnd>
</MenuItemAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/MenuItemAppearance/Border/StartPage.png)


```
<MenuItemAppearance>
    <xBorder>-13395457</xBorder>
    <xPressedGradientBegin>-65536</xPressedGradientBegin>       <!-- Red (#FF0000) -->
    <xPressedGradientEnd>-256</xPressedGradientEnd>             <!-- Yellow (#FFFF00) -->
    <xPressedGradientMiddle>-23296</xPressedGradientMiddle>     <!-- Orange (#FFA500) -->
    <xSelected>-3874305</xSelected>
    <xSelectedGradientBegin>-4005633</xSelectedGradientBegin>
    <xSelectedGradientEnd>-4005633</xSelectedGradientEnd>
</MenuItemAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/MenuItemAppearance/Gradient/StartPage.png)

 
```
<MenuItemAppearance>
    <xBorder>-13395457</xBorder>
    <xPressedGradientBegin>-197380</xPressedGradientBegin>
    <xPressedGradientEnd>-460552</xPressedGradientEnd>
    <xPressedGradientMiddle>-657931</xPressedGradientMiddle>
    <xSelected>-65536</xSelected>                               <!-- Red highlight (#FF0000) -->
    <xSelectedGradientBegin>-4005633</xSelectedGradientBegin>
    <xSelectedGradientEnd>-4005633</xSelectedGradientEnd>
</MenuItemAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/MenuItemAppearance/Selected/StartPage.png)

```
<MenuItemAppearance>
    <xBorder>-13395457</xBorder>
    <xPressedGradientBegin>-197380</xPressedGradientBegin>
    <xPressedGradientEnd>-460552</xPressedGradientEnd>
    <xPressedGradientMiddle>-657931</xPressedGradientMiddle>
    <xSelected>-3874305</xSelected>
    <xSelectedGradientBegin>-65536</xSelectedGradientBegin>     <!-- Red (#FF0000) -->
    <xSelectedGradientEnd>-23296</xSelectedGradientEnd>         <!-- Orange (#FFA500) -->
</MenuItemAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/MenuItemAppearance/SelectedGradient/StartPage.png)

### \<MenuStripAppearance>
Default
```
<MenuStripAppearance>
    <xBorder>-8355712</xBorder>
    <xGradientBegin>-986896</xGradientBegin>
    <xGradientEnd>-197380</xGradientEnd>
</MenuStripAppearance>
```

```
<MenuStripAppearance>
    <xBorder>-65536</xBorder>                       <!-- Red (#FF0000) -->
    <xGradientBegin>-986896</xGradientBegin>
    <xGradientEnd>-197380</xGradientEnd>
</MenuStripAppearance>
```
Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/MenuStripAppearance/Border/StartPage.png)


The next two examples reverse the order of Red and Green. You can see some pads have their border coloured. This appears to be a bug in the #Develop IDE.
```
<MenuStripAppearance>
    <xBorder>-8355712</xBorder>
    <xGradientBegin>-65536</xGradientBegin>         <!-- Red (#FF0000) -->
    <xGradientEnd>-23296</xGradientEnd>             <!-- Orange (#FFA500) -->
</MenuStripAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/MenuStripAppearance/Gradient/StartPage.png)


### \<OverflowButtonAppearance>
Default
```
<OverflowButtonAppearance>
    <xGradientBegin>-657931</xGradientBegin>
    <xGradientEnd>-6250336</xGradientEnd>
    <xGradientMiddle>-855310</xGradientMiddle>
</OverflowButtonAppearance>
```

```
<OverflowButtonAppearance>
    <xGradientBegin>-65536</xGradientBegin>         <!-- Red (#FF0000) -->
    <xGradientEnd>-256</xGradientEnd>               <!-- Yellow (#FFFF00) -->
    <xGradientMiddle>-23296</xGradientMiddle>       <!-- Orange (#FFA500) -->
</OverflowButtonAppearance>
```
Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/OverflowButtonAppearance/StartPage.png)


### \<RaftingContainerAppearance>
Default
```
<RaftingContainerAppearance>
    <xGradientBegin>-986896</xGradientBegin>
    <xGradientEnd>-197380</xGradientEnd>
</RaftingContainerAppearance>
```

```
<RaftingContainerAppearance>
    <xGradientBegin>-65536</xGradientBegin>     <!-- Red (#FF0000) -->
    <xGradientEnd>-23296</xGradientEnd>         <!-- Orange (#FFA500) -->
</RaftingContainerAppearance>
```
No Visible Change


### \<SeparatorAppearance>
Default
```
  <SeparatorAppearance>
    <xDark>-4342339</xDark>                 
    <xLight>-1</xLight>              
  </SeparatorAppearance>
```

```
<SeparatorAppearance>
    <xDark>-65536</xDark>                   <!-- Red (#FF0000) -->
    <xLight>-23296</xLight>                 <!-- Orange (#FFA500) -->
</SeparatorAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/SeparatorAppearance/StartPage.png)


### \<StatusStripAppearance>
Default
```
<StatusStripAppearance>
    <xGradientBegin>-986896</xGradientBegin>
    <xGradientEnd>-197380</xGradientEnd>
</StatusStripAppearance>
```

```
<StatusStripAppearance>
    <xGradientBegin>-65536</xGradientBegin>     <!-- Red (#FF0000) -->
    <xGradientEnd>-23296</xGradientEnd>         <!-- Orange (#FFA500) -->
</StatusStripAppearance>
```
No Visible Change


### \<ToolStripAppearance>
Default
```
<ToolStripAppearance>
    <xBorder>-855310</xBorder>
    <xContentPanelGradientBegin>-986896</xContentPanelGradientBegin>
    <xContentPanelGradientEnd>-197380</xContentPanelGradientEnd>
    <xDropDownBackground>-131587</xDropDownBackground>
    <xGradientBegin>-197380</xGradientBegin>
    <xGradientEnd>-986896</xGradientEnd>
    <xGradientMiddle>-460552</xGradientMiddle>
    <xPanelGradientBegin>-986896</xPanelGradientBegin>
    <xPanelGradientEnd>-197380</xPanelGradientEnd>
  </ToolStripAppearance>
```

```
<ToolStripAppearance>
    <xBorder>-65536</xBorder>               <!-- Red (#FF0000) --> 
    <xContentPanelGradientBegin>-986896</xContentPanelGradientBegin>
    <xContentPanelGradientEnd>-197380</xContentPanelGradientEnd>
    <xDropDownBackground>-131587</xDropDownBackground>
    <xGradientBegin>-197380</xGradientBegin>
    <xGradientEnd>-986896</xGradientEnd>
    <xGradientMiddle>-460552</xGradientMiddle>
    <xPanelGradientBegin>-986896</xPanelGradientBegin>
    <xPanelGradientEnd>-197380</xPanelGradientEnd>
</ToolStripAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ToolStripAppearance/Border/StartPage.png)


```
<ToolStripAppearance>
    <xBorder>-855310</xBorder>              
    <xContentPanelGradientBegin>-65536</xContentPanelGradientBegin>     <!-- Red (#FF0000) -->
    <xContentPanelGradientEnd>-23296</xContentPanelGradientEnd>         <!-- Orange (#FFA500) -->
    <xDropDownBackground>-131587</xDropDownBackground>
    <xGradientBegin>-197380</xGradientBegin>
    <xGradientEnd>-986896</xGradientEnd>
    <xGradientMiddle>-460552</xGradientMiddle>
    <xPanelGradientBegin>-986896</xPanelGradientBegin>
    <xPanelGradientEnd>-197380</xPanelGradientEnd>
  </ToolStripAppearance>
```
No Visible Change


```
<ToolStripAppearance>
    <xBorder>-855310</xBorder>              
    <xContentPanelGradientBegin>-986896</xContentPanelGradientBegin>
    <xContentPanelGradientEnd>-197380</xContentPanelGradientEnd>
    <xDropDownBackground>-65536</xDropDownBackground>           <!-- Red (#FF0000) -->
    <xGradientBegin>-197380</xGradientBegin>
    <xGradientEnd>-986896</xGradientEnd>
    <xGradientMiddle>-460552</xGradientMiddle>
    <xPanelGradientBegin>-986896</xPanelGradientBegin>
    <xPanelGradientEnd>-197380</xPanelGradientEnd>
  </ToolStripAppearance>
```

Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ToolStripAppearance/DropDownBackground/StartPage.png)


```
<ToolStripAppearance>
    <xBorder>-855310</xBorder>              
    <xContentPanelGradientBegin>-986896</xContentPanelGradientBegin>
    <xContentPanelGradientEnd>-197380</xContentPanelGradientEnd>
    <xDropDownBackground>-131587</xDropDownBackground>
    <xGradientBegin>-65536</xGradientBegin>                         <!-- Red (#FF0000) -->
    <xGradientEnd>-256</xGradientEnd>                               <!-- Yellow (#FFFF00) -->
    <xGradientMiddle>-23296</xGradientMiddle>                       <!-- Orange (#FFA500) -->
    <xPanelGradientBegin>-986896</xPanelGradientBegin>
    <xPanelGradientEnd>-197380</xPanelGradientEnd>
</ToolStripAppearance>
```
Start Page
![Image](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ColourSchemes/Discovery/ToolStripAppearance\Gradient/StartPage.png)


```
<ToolStripAppearance>
    <xBorder>-855310</xBorder>              
    <xContentPanelGradientBegin>-986896</xContentPanelGradientBegin>
    <xContentPanelGradientEnd>-197380</xContentPanelGradientEnd>
    <xDropDownBackground>-131587</xDropDownBackground>
    <xGradientBegin>-197380</xGradientBegin>
    <xGradientEnd>-986896</xGradientEnd>
    <xGradientMiddle>-460552</xGradientMiddle>
    <xPanelGradientBegin>-65536</xPanelGradientBegin>       <!-- Red (#FF0000) -->
    <xPanelGradientEnd>-23296</xPanelGradientEnd>           <!-- Orange (#FFA500) -->
</ToolStripAppearance>
```

No Visible Change