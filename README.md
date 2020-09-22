<div align="center">

## Get the seperate RGB values of a Colour


</div>

### Description

It turns the Decimal format of a colour value (example: 16777215) into three seperate values containing the seperate Red, Green, and Blue values. (example: red = 255, green = 255, blue = 255).
 
### More Info
 
Input the colour that you wish to turn into its seperate RGB values. This should be in Decimal format.

Just make sure to keep the types as Long (&) because using an Integer (%) causes an overflow in the Red Value.

Returns the Red, Green, and Blue value from a colour.

'None.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Davy Cook](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/davy-cook.md)
**Level**          |Beginner
**User Rating**    |5.0 (25 globes from 5 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0, VB Script, ASP \(Active Server Pages\) 
**Category**       |[Custom Controls/ Forms/  Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/custom-controls-forms-menus__1-4.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/davy-cook-get-the-seperate-rgb-values-of-a-colour__1-9347/archive/master.zip)

### API Declarations

```
'None.
```


### Source Code

```
Dim blue&, green&, red&, colour&
Blue& = Int(Colour& / 65536)
Green& = Int((Colour& - (65536 * Blue&)) / 256)
Red& = Colour& - (Blue& * 65536) - (Green& * 256)
'to return the colour to its original decimal format
Colour& = RGB(Red&, Green&, Blue&)
```

