---
title: MilkyTracker, Sunvox Keybinds as TSV
date: 2024-12-22T03:04:10.241Z
---
```
Ctrl-Alt-Space (cycles thru pattern/instrument/sampler section)	
Alt-Enter	Switch between full screen and windowed display (Windows & SDL)
Shift-Command-F	Switch between full screen and windowed display (OS X)
Shift-M	Mute current channel
Ctrl-Shift-M	Invert muting
Shift-U	Un-mute all
Ctrl-Shift-T	Open a new tab
Ctrl-Shift-W	Close current tab
Ctrl-Shift-Left	Select previous tab
Ctrl-Shift-Right	Select next tab
Alt-=	Increment instrument number of all notes in the current selection
Alt--	Decrement instrument number of all notes in the current selection
Ctrl-Shift-=	Increment instrument number of all notes in the current track under the cursor
Ctrl-Shift--	Decrement instrument number of all notes in the current track under the cursor
F1…F8	Select octave
"Ctrl-Shift-1…8"
Space	Toggle pattern editor focus (edit mode on/off)
Enter	Play song from current order
Ctrl-Enter	Play current pattern from beginning
Shift-Enter	Play current pattern from cursor position
Shift-F9	Play current pattern from beginning (same as Ctrl-Enter)
Shift-F10	Play current pattern from position after the first quarter of the pattern length
Shift-F11	Play current pattern from position after the second quarter of the pattern length
Shift-F12	Play current pattern from position after the third quarter of the pattern length
Alt-Space	Play song from current row (stop and return when keys are released)
Shift-Space	Play row by row
Esc	Stop
Ctrl-F	Toggle song follow
Ctrl-P	Toggle prospective pattern view
Ctrl-W	Toggle pattern wrapping
Ctrl-L	Toggle pattern change behavior (live mode)
Ctrl-O	Load song
Ctrl-S	Save song
Ctrl-Shift-S	Save song as…
Ctrl-Q	Exit program
Alt-F4	Exit program
Cursor keys	Move around
Tab	Jump to next channel
Ctrl-Tab	Jump to previous channel
PageUp	Jump 16 rows up
PageDown	Jump 16 rows down
Home	Jump to first row
End	Jump to last row
F9	Jump to beginning of the pattern
F10	Jump to position ¼ through the pattern
F11	Jump to position halfway through the pattern
F12	Jump to position ¾ through the pattern
Ctrl-Z	Undo
Ctrl-Y	Redo
Shift-Cursor keys	Select block
Shift-Alt-Cursor keys	Extend block
Ctrl-A	Select entire pattern
Ctrl-X	Cut
Ctrl-C	Copy
Ctrl-V	Paste
Ctrl-Shift-V	Convert current pattern to sample
Ctrl-I	Interpolate values
Delete	Delete note/instrument/volume/effect/parameter
Shift-Del	Delete note, volume and effect at cursor
Ctrl-Del	Delete volume and effect at cursor
Alt-Delete	Delete effect at cursor
Insert	Insert space on current track at cursor position
Shift-Insert	Insert row at cursor position
Alt-Backspace	Insert space on current track at cursor position (alternative for keyboards with no Insert key)
Shift-Alt-Backspace	Insert row at cursor position (alternative for keyboards with no Insert key)
Backspace	Delete previous note
Shift-Backspace	Delete previous row
The key right of LShift	Enter key-off
The key below Esc	Enter key-off (Windows only)
1	Enter key-off (OS X only)
Alt-Plus or Shift-J	Increase Add value
Alt-Minus or Shift-H	Decrease Add value
Ctrl-J	Increase BPM by 1
Ctrl-H	Decrease BPM by 1
Ctrl-K	Increase BPM by 5
Ctrl-G	Decrease BPM by 5
Alt-I	Load Instrument (current slot)
Mousedrag selection	move selection
Shift+Mousedrag selection	clones selection (when 'advanced dnd' is enabled in Misc-tab in config)
Alt-F7	Transpose current instrument in block down
Alt-F8	Transpose current instrument in block up
Shift-F7	Transpose current instrument in track down
Shift-F8	Transpose current instrument in track up
Ctrl-F7	Transpose current instrument in pattern down
Ctrl-F8	Transpose current instrument in pattern up
Alt-F1	Transpose all instruments in block down
Alt-F2	Transpose all instruments in block up
Shift-F1	Transpose all instruments in track down
Shift-F2	Transpose all instruments in track up
Ctrl-F1	Transpose all instruments in pattern down
Ctrl-F2	Transpose all instruments in pattern up
Ctrl-Shift up/down	Select next/previous sample
Shift & drag	Quick draw
Shift & drag	Quick draw
Ctrl & drag	Resize selection
Alt & drag	Move selection or loop range
Ctrl-Alt-A	Advanced edit
Ctrl-Alt-C	Configuration
Ctrl-Alt-D	Disk Operations
Ctrl-Alt-I	Instrument editor
Ctrl-Alt-R	Disk Recorder
Ctrl-Alt-S	Sample Editor
Ctrl-Alt-T	Transpose
Ctrl-Alt-X	Main Screen
Ctrl-Alt-Z	Toggle Scopes
```

Sunvox Keybinds

```
undo	CTRL + Z
redo	CTRL + Y or SHIFT + CTRL + Z
new project or object (module/pattern/...)	CTRL + N
navigation	LEFT,RIGHT,UP,DOWN, PAGEUP,PAGEDOWN, HOME,END,TAB
selection	SHIFT + UP/DOWN/LEFT/RIGHT
selection begin	CTRL + (
selection end	CTRL + )
select all	CTRL + A
cut	CTRL + X or SHIFT + DELETE
copy	CTRL + C
paste	CTRL + V or SHIFT + INSERT
duplicate / clone	CTRL + D
detach: detach the selected modules from the rest or convert the clones to the normal patterns;	CTRL + H
insert an empty note and shift the pattern content down; or just insert something	INSERT (or Command+I on Mac)
delete previous note and shift the pattern content up; or just delete something	BACKSPACE
delete	DELETE (or Fn+Backspace on Mac)
exit the application	ESC
new project	CTRL + SHIFT + N
load project	CTRL + O
save project	CTRL + S
save project to BACKUP.sunvox	CTRL + B
set octave number	F1...F8
octave up	SHIFT + )
octave down	SHIFT + (
play current note (in the pattern editor) and copy it to the brush	CTRL + E
play current line (in the pattern editor) and copy it to the brush	CTRL + L
paste from the brush	CTRL + G
edit mode ON/OFF	SPACE
increase the edit step	CTRL + '='
decrease the edit step	CTRL + '-'
insert ""Note OFF"" (==)	CAPSLOCK or '~'
insert a special command ""Set Pitch"" (SP)	K
insert a special command ""Previous Track"" (<<)	SHIFT + K
paste and mix	CTRL + M
select track	CTRL + T
interpolate values	CTRL + I
interpolate velocity	CTRL + U
transpose up (+1 semitone)	SHIFT + '='
transpose down (-1 semitone)	SHIFT + '-'
transpose octave up (+12 semitones)	SHIFT + ']'
transpose octave down (-12 semitones)	SHIFT + '['
place selected events evenly	CTRL + P
cyclic shift up	SHIFT + 7
cyclic shift down	SHIFT + 8
randomize module controllers	CTRL + R
module link/unlink	SHIFT + mouse movement
write the value to the pattern	SHIFT + controller value change
next module	SHIFT + >
previous module	SHIFT + <
next synth	CTRL + >
previous synth	CTRL + <
next module horizontally (to the right)	CTRL + RIGHT
previous module horizontally (to the left)	CTRL + LEFT
next module vertically (below)	CTRL + DOWN
previous module vertically (above)	CTRL + UP
toggle mute	CTRL + 1
toggle solo	CTRL + 2
toggle bypass	CTRL + 3
unmute all modules	CTRL + 4
find a module	CTRL + F
change the size of all modules	SHIFT + scroll wheel
change the size of the selected module	CTRL + scroll wheel
Description	Keys
play/stop	F9
play from beginning	F10
play pattern	F11
stop	F12
record start/stop	SHIFT + F9
play from the pattern cursor	SHIFT + F10
go to beginning	SHIFT + F12
write a microtone (Set Pitch XXYY command) to the pattern	SHIFT + touch
first button on the left	Y or ENTER
last button on the right	N
cancel	ESC
buttons from left to right	1...9
```