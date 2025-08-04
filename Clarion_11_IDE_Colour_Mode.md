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
To show what the \<DockTabStripAppearance> section affects in the IDE, the elements are coloured shades of Red to hilight easily, in 3 views, the Start page, the AppGen and the Dictionary view.

```
<DockTabStripAppearance>
  <xGradientBegin>-65536</xGradientBegin>      <!-- Dark red (#FF0000) -->
  <xGradientEnd>-25856</xGradientEnd>          <!-- Light red (#FF6A6A) -->
  <xTextColor>-1</xTextColor>                  <!-- Brilliant red (#FF0000) -->
</DockTabStripAppearance>
```
Start Page
![DockTabStripAppearance-Start](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabStripAppearance/DockTabStripAppearance-Start.png)
App Gen
![DockTabStripAppearance-App](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabStripAppearance/DockTabStripAppearance-App.png)
Dct
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabStripAppearance/DockTabStripAppearance-Dct.png)

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
  <xActiveBackColorGradientBegin>-65536</xActiveBackColorGradientBegin>     <!-- Deep Red -->
  <xActiveBackColorGradientEnd>-25856</xActiveBackColorGradientEnd>         <!-- Bright Red -->
  <xActiveTextColor>-256</xActiveTextColor>                                 <!-- Yellow Text -->
  <xInactiveBackColor>-16711936</xInactiveBackColor>                        <!-- Green Background -->
  <xInactiveTextColor>-16753920</xInactiveTextColor>                        <!-- Blue Text -->
</DockPadTitleAppearance>
```
Start Page
![DockTabStripAppearance-Start](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockPadTitleAppearance/DockPadTitleAppearance-Start.png)
App Gen
![DockTabStripAppearance-App](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockPadTitleAppearance/DockPadTitleAppearance-App.png)
Dct
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockPadTitleAppearance/DockPadTitleAppearance-Dct.png)

### \<DockTabAppearance>
Default
```
<DockTabAppearance>
    <Active>
        <xGradientBegin>-986896</xGradientBegin>
        <xGradientEnd>-986896</xGradientEnd>
        <xEdgeColor>-8355712</xEdgeColor>
        <xTextColor>-10066330</xTextColor>
    </Active>
    <Inactive>
        <xGradientBegin>-986896</xGradientBegin>
        <xGradientEnd>-986896</xGradientEnd>
        <xTextColor>-10066330</xTextColor>
        <xEdgeColor>-855310</xEdgeColor>
    </Inactive>
    <PadActive>
        <xGradientBegin>-986896</xGradientBegin>
        <xGradientEnd>-986896</xGradientEnd>
        <xEdgeColor>Gray</xEdgeColor>
        <xTextColor>-12566464</xTextColor>
    </PadActive>
    <PadHide>
        <xGradientBegin>-3876102</xGradientBegin>
        <xGradientEnd>-3876102</xGradientEnd>
        <xEdgeColor>-3876102</xEdgeColor>
        <xTextColor>-10066330</xTextColor>
    </PadHide>
    <PadHideOver>
        <xGradientBegin>-6373643</xGradientBegin>
        <xGradientEnd>-6373643</xGradientEnd>
        <xEdgeColor>-6373643</xEdgeColor>
        <xTextColor>-12566464</xTextColor>
    </PadHideOver>
</DockTabAppearance>
  ```
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
    <xTextColor>-256</xTextColor>                 <!-- Bright Yellow (#FFFF00) -->
</Active>
```
Start Page
![DockTabStripAppearance-Start](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/Active/DockTabAppearanceActive-Start.png)
App Gen
![DockTabStripAppearance-App](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/Active/DockTabAppearanceActive-App.png)
Dct
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/Active/DockTabAppearanceActive-Dct.png)

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
    <xTextColor>-256</xTextColor>                 <!-- Bright Yellow (#FFFF00) -->
    <xEdgeColor>-16711936</xEdgeColor>            <!-- Lime Green (#00FF00) -->   
</Inactive>
```
Start Page
![DockTabStripAppearance-Start](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/Inactive/DockTabAppearanceInactive-Start.png)
App Gen
![DockTabStripAppearance-App](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/Inactive/DockTabAppearanceInactive-App.png)
Dct
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/Inactive/DockTabAppearanceInactive-Dct.png)

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
    <xTextColor>-256</xTextColor>                 <!-- Brilliant Yellow (#FFFF00) -->
</PadActive>
```

Start Page
![DockTabStripAppearance-Start](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/PadActive/DockTabAppearancePadActive-Start.png)
App Gen
![DockTabStripAppearance-App](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/PadActive/DockTabAppearancePadActive-App.png)
Dct
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/PadActive/DockTabAppearancePadActive-Dct.png)

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
  <xTextColor>-256</xTextColor>                 <!-- Bright Yellow (#FFFF00) -->
</PadHide>
```
Start Page
![DockTabStripAppearance-Start](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/PadHide/DockTabAppearancePadHide-Start.png)
App Gen
![DockTabStripAppearance-App](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/PadHide/DockTabAppearancePadHide-App.png)
Dct
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/PadHide/DockTabAppearancePadHide-Dct.png)

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
    <xTextColor>-256</xTextColor>                 <!-- Bright Yellow (#FFFF00) -->
</PadHideOver>
```

Hovering the Mouse over any of the hidden tabs does not change the colour, which is why you see no change.

Start Page
![DockTabStripAppearance-Start](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/PadeHideOver/DockTabAppearancePadeHideOver-Start.png)
App Gen
![DockTabStripAppearance-App](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/PadeHideOver/DockTabAppearancePadeHideOver-App.png)
Dct
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/DockTabAppearance/PadeHideOver/DockTabAppearancePadeHideOver-Dct.png)


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

![DockTabStripAppearance-Start](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ApplicationHeaderAppearance/ApplicationHeaderAppearance-Start.png)
App Gen
![DockTabStripAppearance-App](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ApplicationHeaderAppearance/ApplicationHeaderAppearance-App.png)
Dct
![DockTabStripAppearance-Dct](https://github.com/Intelligent-Silicon/Clarion-11-IDE/blob/main/ApplicationHeaderAppearance/ApplicationHeaderAppearance-Dct.png)


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