# goautoit

Expose [AutoIt](https://www.autoitscript.com/site/) functionality from Go.

It uses directly the `AutoItX3_x64.dll`

This is a fork of [shadow1163/goautoit](https://github.com/shadow1163/goautoit) with some additional functionality (for example it adds `WinKill`, `WinMenuSelectItem`, ...).

## Install

```golang
go get -u github.com/panta/goautoit
```

## Example

- open notepad
- type some string into notepad, eg: **"hello world"**
- close notepad without saving

```golang
goautoit.Run("notepad.exe")
goautoit.WinWait("Untitled")
goautoit.Send("hello world")
goautoit.WinClose("Untitled")
```
