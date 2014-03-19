#conky
#=====

#una pequegna configuracion de mi concky

# Use Xft?
use_xft yes
xftfont Monospace:size=7
xftalpha 0.8
text_buffer_size 2048
 
# Update interval in seconds
update_interval 1
 
# This is the number of times Conky will update before quitting.
# Set to zero to run forever.
total_run_times 0
 
# Create own window instead of using desktop (required in nautilus)
    own_window yes
    own_window_transparent yes
    own_window_type desktop
    own_window_hints undecorated,below,sticky,skip_taskbar,skip_pager
 
# Use double buffering (reduces flicker, may not work for everyone)
double_buffer yes
 
# Minimum size of text area
#minimum_size 200 0
minimum_size 200 200
maximum_width 240
 
 
# Draw shades?
draw_shades no
 
# Draw outlines?
draw_outline no
 
# Draw borders around text
draw_borders no
 
# Stippled borders?
stippled_borders 0
 
# border margins
#border_margin 5
 
# border width
border_width 1
 
# Default colors and also border colors
default_color grey
#default_shade_color black
#default_outline_color white
own_window_colour 333333
 
# Text alignment, other possible values are commented
#alignment top_left
alignment top_right
#alignment bottom_left
#alignment bottom_right
 
# Gap between borders of screen and text
# same thing as passing -x at command line
#gap_x 30
gap_x 12
gap_y 60
 
# Subtract file system buffers from used memory?
no_buffers yes
 
# set to yes if you want all text to be in uppercase
uppercase no
 
# number of cpu samples to average
# set to 1 to disable averaging
cpu_avg_samples 2
 
# number of net samples to average
# set to 1 to disable averaging
net_avg_samples 2
 
# Force UTF8? note that UTF8 support required XFT
override_utf8_locale yes
 
# Add spaces to keep things from moving about?  This only affects certain objects.
use_spacer none
 
TEXT
Kernel
 +
 | + Manjaro ${kernel}
 +
Time
 +
 | + ${time %H:%M:%S} ${time %d %b %Y}
 +
System
 +
 | + CPU: ${cpu cpuX}%
 | '--->Core1 : ${cpu cpu4}%
 | '--->Core2 : ${cpu cpu1}%
 | '--->Core3 : ${cpu cpu2}%
 | '--->Core4 : ${cpu cpu3}%
 | + RAM: $memperc%
 | '--->${mem} memoría usada.
 | '--->${memeasyfree} memoría total libre.
 | '--->${memmax} total RAM disponible.
 | + Temp: ${hwmon temp 1}ºC
 | + /: ${fs_free /root}/${fs_size /root}
 | + /media/Datos: ${fs_free /media/datos}/${fs_size /media/datos}
 | + Baterry: ${battery BAT1}
 +
Net
 +
 | + Up: ${upspeed wlp2s0}kb/s (${totalup wlp2s0})
 | + Down: ${downspeed wlp2s0}kb/s (${totaldown wlp2s0})
 +
Processes
 +
 | + NAME $alignr  PID     CPU
 | + ${top name 1} $alignr ${top pid 1} ${top cpu 1}
 | + ${top name 2} $alignr ${top pid 2} ${top cpu 2}
 | + ${top name 3} $alignr ${top pid 3} ${top cpu 3}
 | + ${top name 4} $alignr ${top pid 4} ${top cpu 4}
 | + ${top name 5} $alignr ${top pid 5} ${top cpu 5}
 | + ${top name 6} $alignr ${top pid 6} ${top cpu 6}
 | + ${top name 7} $alignr ${top pid 7} ${top cpu 7}
 | + ${top name 8} $alignr ${top pid 8} ${top cpu 8}
 +
Shortcuts
 +
 | + Alt+F2$alignr Run Dialog
 | + Alt+F3$alignr Alt Menu
 | + Super+Space$alignr Main Menu
 | + Super+Tab$alignr Client Menu
 | + Super+t$alignr Terminal
 | + Super+f$alignr File Manager
 | + Super+e$alignr Editor
 | + Super+m$alignr Media Player
 | + Super+w$alignr Web Browser
 | + Super+h$alignr Task Manager
 | + Super+l$alignr Lock Screen
 | + Super+v$alignr Volume Control
 | + Super+x$alignr Logout
 | + PrtSc$alignr Screenshot
