
;==========================================================
;
;
;   ██████╗  ██████╗ ██╗  ██╗   ██╗██████╗  █████╗ ██████╗
;   ██╔══██╗██╔═══██╗██║  ╚██╗ ██╔╝██╔══██╗██╔══██╗██╔══██╗
;   ██████╔╝██║   ██║██║   ╚████╔╝ ██████╔╝███████║██████╔╝
;   ██╔═══╝ ██║   ██║██║    ╚██╔╝  ██╔══██╗██╔══██║██╔══██╗
;   ██║     ╚██████╔╝███████╗██║   ██████╔╝██║  ██║██║  ██║
;   ╚═╝      ╚═════╝ ╚══════╝╚═╝   ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝
;
;
;   To learn more about how to configure Polybar
;   go to https://github.com/jaagr/polybar
;
;   The README contains alot of information
;
;==========================================================

;==========================================================
;                   VARIAVEIS                          ====
;==========================================================

[colors]
peach = #FFCD98
lime = #CADC79
salmon = #d97464
darkgrey = #2e2e2e
lightgrey = #444444


background = #444444
foreground = ${xrdb:color7:#222}
foreground-alt = ${xrdb:color7:#222}
primary = ${xrdb:color1:#222}
secondary = ${xrdb:color2:#222}
alert = ${xrdb:color3:#222}

;Cor= #73000000
;background = ${xrdb:color0:#222}
;foreground = ${xrdb:color7:#222}
;foreground-alt = ${xrdb:color7:#222}

xcolor0 = ${xrdb:color0}
xcolor1 = ${xrdb:color1}
xcolor2 = ${xrdb:color2}
xcolor3 = ${xrdb:color3}
xcolor4 = ${xrdb:color4}
xcolor5 = ${xrdb:color5}
xcolor6 = ${xrdb:color6}
xcolor7 = ${xrdb:color7}
xcolor8 = ${xrdb:color8}
xcolor9 = ${xrdb:color9}
xcolor10 = ${xrdb:color10}
xcolor11 = ${xrdb:color11}
xcolor12 = ${xrdb:color12}
xcolor13 = ${xrdb:color13}
xcolor14 = ${xrdb:color14}
xcolor15 = ${xrdb:color15}
;background = ${xrdb:background}
;foreground = ${xrdb:foreground}
;foreground = #888888
;foreground-alt = #555555

;===============================================================================================================================================================================================================

[bar/top]
monitor = ${env:MONITOR:eDP-1}
width = 100%
height = 27
;offset-x = 1%
;offset-y = 1%
;radius = 6.0
fixed-center = false

background = ${colors.background}
foreground = ${colors.foreground}

;line-size = 3
;line-color = #f00

border-top-size = 4
border-top-color = ${colors.background}
border-bottom-size = 4
border-bottom-color = ${colors.xcolor1}

;padding-left = 0
;padding-right = 2

module-margin-left = 0
module-margin-right = 0

font-0 = fixed:pixelsize=10;1
font-1 = unifont:fontformat=truetype:size=8:antialias=false;0
font-2 = siji:pixelsize=10;1
font-3 = FontAwesome:pixelsize=10;1
font-4 = featherpatched:pixelsize=10;1
font-5 = Powerline Extra Symbols:pixelsize=33;16


modules-left = date arrow1 bspwm 
modules-center = msgbate space 
modules-right = space filesystem space memory space cpu space pulseaudio space wlan space temperature space battery arrow2 menud

;tray-position = right
;tray-padding = 2
;tray-transparent = true
;tray-background = #0063ff

wm-restack = bspwm
;wm-restack = i3

;override-redirect = true

;scroll-up = bspwm-desknext
;scroll-down = bspwm-deskprev

;scroll-up = i3wm-wsnext
;scroll-down = i3wm-wsprev

cursor-click = pointer
cursor-scroll = ns-resize

;===============================================================================================================================================================================================================

[module/open]
type = custom/text
content-foreground = ${colors.foreground}
content = ""
click-left = ~/.config/polybar/scripts/menu.sh options

[module/close]
type = custom/text
content-foreground = ${colors.blue}
content = ""
click-left = ~/.config/polybar/scripts/menu.sh options


;==========================================================
;                      DECORAÇÕES                      ====      
;==========================================================

[module/arrow1]
type = custom/text
content = ""
content-foreground = ${colors.xcolor1}
content-background = ${colors.background}

[module/arrow2]
type = custom/text
content = "     "
content-foreground = ${colors.xcolor1}
content-background = ${colors.background}

[module/space]
type = custom/text
content = " = "
content-foreground = ${colors.background}
content-background = ${colors.background}

;==========================================================
;                      MENU                            ====     
;==========================================================

[module/menud]
type = custom/script
interval = 10
format = <label>
format-prefix = " "
format-prefix-padding  = 1
format-prefix-foreground =#EE0143
format-background = ${colors.xcolor1}
exec = whoami
click-left = ~/.config/polybar/scripts/menu.sh options


;==========================================================
;                      Relatótio de Máquina            ====     
;==========================================================

[module/rmaquina]
type = custom/script
interval = 10
;format = <label>
format-prefix = ""
format-prefix-padding  = 1
format-prefix-foreground =#EE0143
exec = whoami
click-left = ~/.config/polybar/scripts/RelatorioMaquina.sh &

;==========================================================
;                      NVIDIA                          ====     
;==========================================================

[module/nvidia]
type = custom/script
interval = 1
format = "<label>"
format-prefix = 
click-left = "optirun -b none nvidia-settings -c :8"
exec = ~/.config/polybar/scripts/nvidia.sh

;==========================================================
;                      Mensagem Batteria               ====     
;==========================================================
[module/msgbate]
type = custom/script
interval = 10
exec = ~/.config/polybar/scripts/MsgBateria.sh



;===========================================================
;                    FILESYSTEM                         ====
;===========================================================

[module/filesystem]
type = internal/fs
interval = 25

mount-0 = /

format-mounted = <label-mounted>
format-mounted-prefix = " "
format-mounted-foreground = ${colors.xcolor7}

label-mounted = %percentage_used%%
label-unmounted = %mountpoint% not mounted
label-unmounted-foreground = ${colors.xcolor7}

;===========================================================
;                    BSPWM                              ====
;===========================================================

[module/bspwm]
type = internal/bspwm

pin-workspaces = true
inline-mode = true
enable-click = true
enable-scroll = true
reverse-scroll = true

format = <label-state>

label-focused = %name% 
label-focused-background = ${colors.background}
;label-focused-underline= ${colors.xcolor1}
label-focused-padding = 2

label-occupied = %name% 
label-occupied-padding = 2

label-urgent = %name% 
label-urgent-background = ${colors.xcolor1}
label-urgent-padding = 2

label-empty = %name% 
label-empty-foreground = ${colors.xcolor1}
label-empty-padding = 2


;===========================================================
;                    CPU                                ====
;===========================================================


[module/cpu]
type = internal/cpu
interval = 0.5
format = <label>
format-prefix = " "
format-prefix-foreground = ${colors.xcolor7}
;format-underline = #f90000
label = %percentage:2%%

ramp-coreload-0 = ▁
ramp-coreload-1 = ▂
ramp-coreload-2 = ▃
ramp-coreload-3 = ▄
ramp-coreload-4 = ▅
ramp-coreload-5 = ▆
ramp-coreload-6 = ▇
ramp-coreload-7 = █

;===========================================================
;                    MEMORY                             ====
;===========================================================

[module/memory]
type = internal/memory
interval = 2
format = <label> <bar-used>
format-prefix = " "
format-prefix-foreground = ${colors.xcolor7}
;format-underline = #4bffdc
label = %mb_used%

;bar-used-indicator =
bar-used-width = 15
bar-used-foreground-0 = ${colors.xcolor2}
bar-used-foreground-1 = #557755
bar-used-foreground-2 = #f5a70a
bar-used-foreground-3 = #ff5555
;bar-used-fill = |
;bar-used-empty = |
bar-used-empty-foreground = ${colors.xcolor7}

bar-used-indicator = ""
bar-used-fill = 
bar-used-empty = 

;===========================================================
;                    WLAN                               ====
;===========================================================

[module/wlan]
type = internal/network
interface = wlp2s0
interval = 0.5

format-connected = <ramp-signal> <label-connected>
;format-connected-underline = #9f78e1
label-connected = %essid%

format-disconnected =
;format-disconnected = <label-disconnected>
;format-disconnected-underline = ${self.format-connected-underline}
;label-disconnected = %ifname% disconnected
;label-disconnected-foreground = ${colors.foreground-alt}

ramp-signal-0 = 
ramp-signal-1 = 
ramp-signal-2 = 
ramp-signal-3 = 
ramp-signal-4 = 
ramp-signal-foreground = ${colors.xcolor7}

[module/eth]
type = internal/network
interface = eth0
interval = 3.0

format-connected-underline = #55aa55
format-connected-prefix = " "
format-connected-prefix-foreground = ${colors.foreground-alt}
label-connected = %local_ip%

format-disconnected =
;format-disconnected = <label-disconnected>
;format-disconnected-underline = ${self.format-connected-underline}
;label-disconnected = %ifname% disconnected
;label-disconnected-foreground = ${colors.foreground-alt}


;===========================================================
;                    DATE                               ====
;===========================================================

[module/date]
type = internal/date
interval = 1

date = 
date-alt = "  %d/%m/%Y"

time = "   %H:%M:%S "
time-alt = "   %H:%M:%S "

format-foreground = ${colors.xcolor7}
format-background = ${colors.xcolor1}

label = " %date% %time% "

;===========================================================
;                    PULSEAUDIO                         ====
;===========================================================

[module/pulseaudio]
type = internal/pulseaudio

format-volume = <label-volume> <bar-volume>
label-volume =  %percentage%%
label-volume-foreground = ${root.foreground}

label-muted = 🔇 muted
label-muted-foreground = #666

bar-volume-width = 10
bar-volume-foreground-0 = #55aa55
bar-volume-foreground-1 = #55aa55
bar-volume-foreground-2 = #55aa55
bar-volume-foreground-3 = #55aa55
bar-volume-foreground-4 = #55aa55
bar-volume-foreground-5 = #f5a70a
bar-volume-foreground-6 = #ff5555
bar-volume-gradient = false
bar-volume-indicator = 
bar-volume-indicator-font = 2
bar-volume-fill = 
bar-volume-fill-font = 2
bar-volume-empty = 
bar-volume-empty-font = 2
bar-volume-empty-foreground = ${colors.foreground-alt}


;===========================================================
;                    BATTERY                            ====
;===========================================================

[module/battery]
type = internal/battery
battery = BAT1
adapter = ACAD
full-at = 98


format-charging = <animation-charging> <label-charging>
format-charging-foreground = ${colors.xcolor7}
format-discharging = <ramp-capacity> <label-discharging>
format-discharging-foreground = ${colors.xcolor7}
format-full = <label-full>
format-full-foreground = ${colors.xcolor7}

label-charging = "%percentage%% "
label-discharging = "%percentage%% "
label-discharging-foreground = ${colors.xcolor7}
label-full = "  %percentage%% "

ramp-capacity-0 = 
ramp-capacity-0-foreground = ${colors.xcolor7}
ramp-capacity-1 = 
ramp-capacity-1-foreground = ${colors.xcolor7}
ramp-capacity-2 = 
ramp-capacity-3 = 
ramp-capacity-4 = 

animation-charging-0 = 
animation-charging-1 = 
animation-charging-2 = 
animation-charging-3 = 
animation-charging-4 = 
animation-charging-foreground = ${colors.xcolor7}
animation-charging-framerate = 750

animation-discharging-0 = 
animation-discharging-1 = 
animation-discharging-2 = 
animation-discharging-3 = 
animation-discharging-4 = 
animation-discharging-foreground = ${colors.xcolor7}
animation-discharging-framerate = 750

;===========================================================
;                    TEMPERATURE                        ====
;===========================================================

[module/temperature]
type = internal/temperature
thermal-zone = 0
warn-temperature = 60
hwmon-path = /sys/devices/platform/coretemp.0/hwmon/hwmon2/temp1_input

format = <ramp> <label>
format-warn = <ramp> <label-warn>

label = %temperature-c%
label-warn = %temperature-c%
label-warn-foreground = ${colors.secondary}

ramp-0 = 
ramp-1 = 
ramp-2 = 
ramp-3 = 
ramp-4 = 
ramp-foreground = ${colors.xcolor7}



[global/wm]
margin-top = 5
margin-bottom = 5

; vim:ft=dosini

