# move-to-next-monitor
A bash script to move a window to another monitor. Designed to be invoked with a keyboard shortcut.

Move the current window to the next monitor.

Only works on a horizontal monitor setup. Also works only on one X screen (which is the most common case).

Modified a bunch by Trevor Klar in 2020, adding directional control and a window reset. Also fixed bug where different sized screens would make the script work strangely. 

Props to [http://icyrock.com/blog/2012/05/xubuntu-moving-windows-between-monitors/]([http://icyrock.com/blog/2012/05/xubuntu-moving-windows-between-monitors/) for writing the original version of this script.

Unfortunately, both "xdotool getwindowgeometry --shell $window_id" and checking "-geometry" of "xwininfo -id $window_id" are not sufficient, as the first command does not respect panel/decoration offsets and the second will sometimes give a "-0-0" geometry. This is why we resort to "xwininfo".
