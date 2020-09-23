<div align="center">

## Bypass the Screensaver password


</div>

### Description

When compiled this code makes a change in the registry to make the screensaver NOT use a password
 
### More Info
 
You could burn the application to a CD so that it autoruns when inserted(even when the screensaver is running) It will then make a registry change so that you will not be prompted with a password.

DOES NOT WORK WITH XP

Don't Know about win2000


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Raymond Weier](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/raymond-weier.md)
**Level**          |Beginner
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |Delphi 5, Delphi 4
**Category**       |[Registry](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/registry__7-36.md)
**World**          |[Delphi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/delphi.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/raymond-weier-bypass-the-screensaver-password__7-786/archive/master.zip)





### Source Code

```
uses registry;
procedure TForm1.Create;
Var
	Reg:=Tresitry.Create;
	Reg.Rootkey:=HKEY_CURRENT_USER;
	If Reg.Openkey('Control Panel\Desktop', True);
	Then
		Reg.WriteBool('ScreenSaveUsePassword', False);
		Reg.Free;
	Halt;
end;
```

