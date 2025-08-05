# Clarion 11 IDE Fonts

The Clarion 11 IDE has a section where the Fonts for the IDE can be set. The GUI doesnt provide any facility to change the text colour and there isnt an option in the XML sections below.

You can find this section in ```Tools, Options, IDE, Fonts```.

The first dropdown list box lists the different parts of the IDE and below that the Font thats in use: 

| Section | Font Name | Size |
| --- | --- | --- |
| Dialogs | Segoe UI | 9 |
| List Controls | Segoe UI | 9 |
| Start Page | Segoe UI | 17 |
| Text Editor, Output Window, (Proportional Font). | Courier New  | 12 |


These settings are stored in the ```C:\Users\[Username]\AppData\Roaming\SoftVelocity\Clarion\11.0\ClarionProperties.xml``` file.

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

Font's in terms of shortest in height suitable for developers. (Shortest first). The shorter the font, the more real estate you can gain from the Clarion IDE.

| \# | Font Name | 
| --- | --- |  
| 1. | Tahoma |
| 2. | Open Sans |
| 3. | Noto Sans |
| 4. | Inter |
| 5. | Roboto |
| 6. | Cascadia Code |




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


