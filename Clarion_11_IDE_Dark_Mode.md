# Clarion 11 IDE DarkMode

This colour scheme is what is known as a Dark Mode colour scheme. Dark modes are designed to save on battery life when used on laptops, provide a high contrast look to programs which can help in bright & poor light situations and generally helps to provide less eye strain and damage both short and long term when using a program for long periods of time.


# Colour Standards

Choosing colours should try to meet WCAG (Web Content Accessibility Guidelines) guidelines which is a set of internationally recognized standards developed by the W3C to make digital content more accessible to people with disabilities. Even though you may be only designing the Dark Mode for your personal use, the standards can help you focus on choosing the right colours to suit your eyesight and machine.

WCAG is built around four foundational principles:
| Principle | Meaning | 
| --- | --- |
| Perceivable | Content must be presented in ways users can perceive (e.g. alt text for images) | 
| Operable | Users must be able to interact with the interface (e.g. keyboard navigation) | 
| Understandable | Content and UI must be easy to understand and use (e.g. clear instructions) | 
| Robust | Content must work reliably across technologies, including assistive tools | 

Without getting into the Versions: WCAG 2.0, 2.1, and the latest, WCAG 2.2 and Conformance Levels:
- Level A: Basic accessibility

- Level AA: Recommended standard for legal compliance

- Level AAA: Highest level, often not feasible for all content

Most organisations tend to aim for AA conformance. 

[WCAG 2.0 is ISO/IEC 40500:2012](https://www.w3.org/TR/WCAG20/).




# Choosing colours to make Dark Mode.
Putting aside the UDL Syntax Highlighting which controls the look of the Text Editor and Embed Source Editor, this page concentrates on the colour selection process.

Firstly there is the [WebAim Contrast Check](https://webaim.org/resources/contrastchecker/) which helps to identify the contrast levels between the background and foreground colours. 

[Use of Colour](https://www.w3.org/WAI/WCAG22/quickref/?showtechniques=141#use-of-color)

[Resize Text](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html)



| WCAG Version | Level | Output Type | Ratio 
| --- | --- | --- | --- | 
| 2.0 | AA | Normal Text to Background | 4.5:1 |
| 2.1 | AAA | Normal Text to Background | 7:1 | 
| 2.0 | AA | Large Text to Background | 3:1 |
| 2.1 | AAA | Large Text to Background | 4.5:1 |
| 2.1 | AA | Graphics | 3:1 |
| 2.1 | AA | User Interface Components (eg input borders) to Background | 3:1 |

[Contrast Minimum](https://www.w3.org/TR/wcag2ict-22/#contrast-minimum)

[Resize Text](https://www.w3.org/TR/wcag2ict-22/#resize-text)

[Images of Text](https://www.w3.org/TR/wcag2ict-22/#images-of-text)

[Non-text contrast](https://www.w3.org/TR/wcag2ict-22/#non-text-contrast)

[Text spacing](https://www.w3.org/TR/wcag2ict-22/#text-spacing)

[Context on Hover or Focus](https://www.w3.org/TR/wcag2ict-22/#content-on-hover-or-focus)

[No Keyboard Trap](https://www.w3.org/TR/wcag2ict-22/#no-keyboard-trap)

[Character Key Shortcuts](https://www.w3.org/TR/wcag2ict-22/#character-key-shortcuts)

[Pause, Stop, Hide](https://www.w3.org/TR/wcag2ict-22/#pause-stop-hide)

[Seizures and Physical Reactions](https://www.w3.org/TR/wcag2ict-22/#seizures-and-physical-reactions)

and more...



Colour Wheels help identify harmonious colours and complementary colours. A good website for picking colours and identify complimentary colours is [Paletton.com](https://paletton.com). The website will calculate automatically based on an initial chosen colour.

MS Windows also has a [Colour Picker](https://learn.microsoft.com/en-us/windows/powertoys/color-picker) included in its Power Toys, which can be handy for select the colours seen elsewhere in a Dark Mode.

If you are lacking in ideas for a dark mode colour scheme, the [Colorffy.com](https://colorffy.com/dark-theme-generator) website provides a handy Dark Mode colour generator which lets you cycle through different colours for a dark mode. Just click the ```Generate``` button to cycle through the colours.

https://colorffy.com/dark-theme-generator?colors=bffb9f-121212

# Converting Colours from Hex to Decimal

| Actions | Value |
| --- | --- |
| Take a Hex number | #4C4569 |
| Add alpha FF for full opacity | #FF4C4569 | 
| Convert from Hex to Decimal using Windows Calculator| 4281150511 |
| If the value is greater than 2147483647, - subtract 2^32 (4294967296) | -13,816,785 |

 

| Type | -0 | -10 | -20 | -30 | -40 | -50 |
| --- | --- | --- | --- | --- | --- | --- |
| Primary Colour | #4c4569 | #5e5779 | #716b88 | #847e99 | #9893a9 | #aca7ba |
| Surface Colour | #121212 | #282828 | #3f3f3f | #575757 | #717171 | #8b8b8b |
| Tonal Surface colour | #18171a | #2d2c2f | #444345 | #5b5b5d | #747476 | #8f8e90 |

### Background Colours
 
| Type | -0 | -10 | -20 | -30 | -40 | -50 |
|------|--------|--------|--------|--------|--------|--------|
| Hex  | #4c4569 | #5e5779 | #716b88 | #847e99 | #9893a9 | #aca7ba |
| Dec  | -12500663 | -10982343 | -9438664 | -7992215 | -6577063 | -5161910 |

| Type | -0 | -10 | -20 | -30 | -40 | -50 |
|------|--------|--------|--------|--------|--------|--------|
| Hex  | #21251f | #363934 | #4c4f4a | #636661 | #7b7e79 | #949693 |
| Dec  | -15715297 | -13619116 | -12500630 | -10197983 | -8421503 | -7048805 |

 
### Text Colours
 
| Type | -0 | -10 | -20 | -30 | -40 | -50 |
|------|--------|--------|--------|--------|--------|--------|
| Hex  | #121212 | #282828 | #3f3f3f | #575757 | #717171 | #8b8b8b |
| Dec  | -15790338 | -14079702 | -12500671 | -10000529 | -7385471 | -6447715 |

 
### Selected Background Colours
 
| Type | -0 | -10 | -20 | -30 | -40 | -50 |
|------|--------|--------|--------|--------|--------|--------|
| Hex  | #18171a | #2d2c2f | #444345 | #5b5b5d | #747476 | #8f8e90 |
| Dec  | -15658758 | -13948145 | -12434875 | -10066307 | -7457898 | -6710880 |

 
### Selected Text Colours

| Type |       -0 |      -10 |      -20 |      -30 |      -40 |      -50 |
|------|----------|----------|----------|----------|----------|----------|
| Hex  |  #bffb9f |  #c7fcaa |  #cefcb5 |  #d6fdbf |  #ddfdca |  #e4fed5 |
| Dec  | -4199393 | -4015798 | -3832203 | -3648609 | -3465014 | -3281419 |
 


### Background Colours
| Type |        -0 |       -10 |       -20 |       -30 |       -40 |       -50 |
|------|----------:|----------:|----------:|----------:|----------:|----------:|
| Hex  |   #4c4569 |   #5e5779 |   #716b88 |   #847e99 |   #9893a9 |   #aca7ba |
| Dec  | -12500663 | -10982343 |  -9438664 |  -7992215 |  -6577063 |  -5161910 |

| Type |        -0 |       -10 |       -20 |       -30 |       -40 |       -50 |
|------|----------:|----------:|----------:|----------:|----------:|----------:|
| Hex  |   #21251f |   #363934 |   #4c4f4a |   #636661 |   #7b7e79 |   #949693 |
| Dec  | -15715297 | -13619116 | -12500630 | -10197983 |  -8421503 |  -7048805 |

### Text Colours
| Type |        -0 |       -10 |       -20 |       -30 |       -40 |       -50 |
|------|----------:|----------:|----------:|----------:|----------:|----------:|
| Hex  |   #121212 |   #282828 |   #3f3f3f |   #575757 |   #717171 |   #8b8b8b |
| Dec  | -15790338 | -14079702 | -12500671 | -10000529 |  -7385471 |  -6447715 |

### Selected Background Colours
| Type |        -0 |       -10 |       -20 |       -30 |       -40 |       -50 |
|------|----------:|----------:|----------:|----------:|----------:|----------:|
| Hex  |   #18171a |   #2d2c2f |   #444345 |   #5b5b5d |   #747476 |   #8f8e90 |
| Dec  | -15658758 | -13948145 | -12434875 | -10066307 |  -7457898 |  -6710880 |

### Selected Text Colours
| Type |        -0 |       -10 |       -20 |       -30 |       -40 |       -50 |
|------|----------:|----------:|----------:|----------:|----------:|----------:|
| Hex  |   #bffb9f |   #c7fcaa |   #cefcb5 |   #d6fdbf |   #ddfdca |   #e4fed5 |
| Dec  |  -4199393 |  -4015798 |  -3832203 |  -3648609 |  -3465014 |  -3281419 |



<DockTabStripAppearance>
  <xGradientBegin>-13878737</xGradientBegin>      <!-- #ff2d2c2f -13,816,785 -->
  <xGradientEnd>-25856</xGradientEnd>          <!-- #ff444345 -12,303,547-->
  <xTextColor>-16711936</xTextColor>           <!-- Lime Green (#00FF00) -->
</DockTabStripAppearance>



Button Text
Button Background


# Backgrounds

# Text Colours

# 