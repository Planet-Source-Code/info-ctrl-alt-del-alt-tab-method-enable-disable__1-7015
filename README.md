<div align="center">

## Ctrl\+Alt\+Del  &  Alt\+Tab  Method  \(Enable/Disable\)


</div>

### Description

This coding will let you ENABLE and DISABLE the Ctrl + Alt + Del Method and also the Alt + Tab Method. Have Fun. Please Vote for Me.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[iNfO](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/info.md)
**Level**          |Beginner
**User Rating**    |4.2 (25 globes from 6 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__1-1.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/info-ctrl-alt-del-alt-tab-method-enable-disable__1-7015/archive/master.zip)

### API Declarations

```
'- Made By: iNfO
'- About: These 2 functions let you enable and
'- disable the Ctrl+ Alt + Del Method and the
'- Alt + Tab Method
Public Declare Function SystemParametersInfo2 Lib "user32" Alias "SystemParametersInfoA" (ByVal uAction As Long, ByVal uParam As Long, lpvParam As Any, ByVal fuWinIni As Long) As Long
Public Const SPI_SCREENSAVERRUNNING = 97
Public Sub CtrlAltDel_Disable()
'in a button or anywhere,
'put this: ctrlaltdel_disable
 Dim syssend As Long
 syssend& = SystemParametersInfo2(SPI_SCREENSAVERRUNNING, True, False, 0)
End Sub
Public Sub CtrlAltDel_Enable()
'in a button or anywhere,
'put this: ctrlaltdel_enable
 Dim syssend As Long
 syssend& = SystemParametersInfo2(SPI_SCREENSAVERRUNNING, False, True, 0)
End Sub
```


### Source Code

```
'- You will need:
'-        2 Command Buttons
Private Sub Form_Load()
'- Sets the Captions for the Buttons
Command1.Caption = "Disable"
Command2.Caption = "Enable"
End Sub
Private Sub Command1_Click()
'- This disables the Ctrl + Alt + Del Method
'- and the Alt + Tab Method
CtrlAltDel_Disable
End Sub
Private Sub Command2_Click()
'This enables the Ctrl + Alt + Del Method
'- and the Alt + Tab Method
CtrlAltDel_Enable
End Sub
```

