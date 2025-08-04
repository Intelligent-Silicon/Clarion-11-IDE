# Clarion 11 IDE Colour Mode

The Clarion 11 IDE permits different colour modes to be used.

### Toolbar Color Schemes.

This encompasses, toolbars and flyout pinnable pads.

An online topic & discussion can be found here at :

[ClarionHub.com - Custom Themes and Color Schemes for the IDE](https://clarionhub.com/t/custom-themes-and-color-schemes-for-the-ide/126) 

[ClarionHub.com - Share your custom syntax highlighting scheme here!](https://clarionhub.com/t/share-your-custom-syntax-highlighting-scheme-here/453/1)

The XML files responsible for the colour of the IDE can be found in :

```%CWroot%\data\resources\ColorThemes```

which translates to:

 ```C:\Clarion11\data\resources\ColorThemes```.

Its this folder, where you import or add your own Toolbar color scheme XML files.

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
| VSDark.xml |
| Win8Blue.xml |
| Win10Blue.xml |

You can select one of these colour schemes to colour the IDE by clicking on 
```Tools, Options, IDE, Appearance, scroll down to 'Select the Toolbar color scheme', and select one of the above from the drop down list box.```




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

ARGB numbers range from 0 to 255, and the negative 32bit integer is calculated using Bshift, if you fancy building your own Clarion tool to modify the colour scheme XML files.

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
![DockTabStripAppearance](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabStripAppearance.png)

```
<DockTabStripAppearance>
  <xGradientBegin>-65536</xGradientBegin>      <!-- Dark red (#FF0000) -->
  <xGradientEnd>-25856</xGradientEnd>          <!-- Light red (#FF6A6A) -->
  <xTextColor>-1</xTextColor>                  <!-- Brilliant red (#FF0000) -->
</DockTabStripAppearance>
```


### \<DockPadTitleAppearance>



### \<DockTabAppearance>

### \<ApplicationHeaderAppearance>

### \<StartPageAppearance>

### \<ButtonAppearance>

### \<GripAppearance>

### \<ImageMarginAppearance>

### \<MenuItemAppearance>

### \<MenuStripAppearance>

### \<OverflowButtonAppearance>

### \<RaftingContainerAppearance>

### \<SeparatorAppearance>

### \<StatusStripAppearance>

### \<ToolStripAppearance>


<StartPageAppearance>
  <xGradientBegin>-16777216</xGradientBegin>        <!-- Black -->
  <xGradientEnd>-14540253</xGradientEnd>            <!-- Dark gray -->
  <xSecondaryColor>DimGray</xSecondaryColor>        <!-- Soft dark gray -->
  <xPrimaryColor>-5592406</xPrimaryColor>           <!-- Deep muted purple -->
  <xButtonImageColor>-16744448</xButtonImageColor>  <!-- Teal (good pop on dark) -->
  <xGridHeaderColor>DarkGray</xGridHeaderColor>     <!-- For grid header contrast -->
  <xGridBodyColor>Black</xGridBodyColor>            <!-- Main background -->
  <xGridAltBodyColor>DimGray</xGridAltBodyColor>    <!-- Alternating row shade -->
  <xGridLineColorr>SlateGray</xGridLineColorr>      <!-- Grid lines -->
  <xGridHoverColorr>SteelBlue</xGridHoverColorr>    <!-- Hover effect -->
</StartPageAppearance>