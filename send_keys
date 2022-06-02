#NoEnv  ; Recommended for performance and compatibility with future AutoHotkey releases.
; #Warn  ; Enable warnings to assist with detecting common errors.
SendMode Input  ; Recommended for new scripts due to its superior speed and reliability.
SetWorkingDir %A_ScriptDir%  ; Ensures a consistent starting directory.

#include Variables.ahk

WinWait, %Caption1% ; Caption is taken from Variables.ahk

Send #1      ; Win 1

WinWait, %Caption3%
Sleep 500

if WinExist( Caption3 )
    WinActivate
Sleep 500
Send {Enter}

WinWait, %Caption2% ; Caption is taken from Variables.ahk
Sleep 500
Send {Up}
Sleep 500

if WinExist( Caption2 )
    WinActivate
Sleep 500
Send {Tab}
Sleep 500
Send {Tab}
Sleep 500
Send ^c      ; Ctrl c

if WinExist( Caption1 )
    {
    WinActivate ; Use the window found by WinExist.
    Sleep 500
    Send ^v          ; Ctrl v
    Sleep 500
    Send {Enter}
    }

Sleep 500

IfWinNotActive, %Caption2%
    Send #1     ; Win 1
Sleep 500
Send ^q  ; Ctrl q
