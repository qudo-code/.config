# .conf
Resources for setting up Linux environment.

## Install Core Apps
`sudo pacman -S discord telegram-desktop signal-desktop xclip rofi-emoji flameshot`

`yay -S slack-desktop notion-app spotify visual-studio-code-bin`

## I3 Mods
### Extra Keybinds
```
# Killing apps requires an extra key (Shift)
bindsym $mod+Shift+q kill

# Screenshots with flameshot
bindsym Print exec flameshot gui

# Quick browser access
bindsym $mod+q exec --no-startup-id brave

# Emoji keyboard in rofi
bindsym $mod+period exec rofi -modi emoji -show emoji
```
### Mod Key -> Alt
`set $mod Mod1`
### Resize Mode w/Vim Keys
```
# resize window (you can also use the mouse for that)
mode "resize" {
        # These bindings trigger as soon as you enter the resize mode
        bindsym h resize shrink width 10 px or 10 ppt
        bindsym j resize grow height 10 px or 10 ppt
        bindsym k resize shrink height 10 px or 10 ppt
        bindsym l resize grow width 10 px or 10 ppt

        # back to normal: Enter or Escape or $mod+r
        bindsym Return mode "default"
        bindsym Escape mode "default"
        bindsym $mod+r mode "default"
}

bindsym $mod+r mode "resize"
```
### Move/Focus w/Vim Keys
```
# change focus
bindsym $mod+h focus left
bindsym $mod+j focus down
bindsym $mod+k focus up
bindsym $mod+l focus right

# move focused window
bindsym $mod+Shift+h move left
bindsym $mod+Shift+j move down
bindsym $mod+Shift+k move up
bindsym $mod+Shift+l move right
```
### Removed Arrow Keys
Removed all arrow key actions as they conflict with VSCode bindings.
```
# bindsym $mod+Left focus left
# bindsym $mod+Down focus down
# bindsym $mod+Up focus up
# bindsym $mod+Right focus right
# bindsym $mod+Shift+Left move left
# bindsym $mod+Shift+Down move down
# bindsym $mod+Shift+Up move up
# bindsym $mod+Shift+Right move right
# bindsym Left resize shrink width 10 px or 10 ppt
# bindsym Down resize grow height 10 px or 10 ppt
# bindsym Up resize shrink height 10 px or 10 ppt
# bindsym Right resize grow width 10 px or 10 ppt
# Pressing left will shrink the window’s width.
# Pressing right will grow the window’s width.
# Pressing up will shrink the window’s height.
# Pressing down will grow the window’s height.
```
### Split Horizontal w/C
`bindsym $mod+c split h`
### Wallpaper Location
`exec --no-startup-id sleep 1 && feh --bg-fill /home/qudo/Pictures/wallpaper.jpg`
## Download i3 Endevour Config
`curl https://raw.githubusercontent.com/qudo-code/.config/main/i3-config-endevour --output .config/i3/config`

## Download i3 Blocks Endevour Config
`curl https://raw.githubusercontent.com/qudo-code/.config/main/i3blocks-endevour --output .config/i3/i3locks.conf`
# VSCode Keybinds
Go to File -> Preferences -> Keyboard Shortcuts.

_*Note:* Remove arrow key bingings in i3 config for these to work._

- Copy Line Down/Up: `Shift + Alt + Down/Up`
- Move Line Down/Up: `Alt + Down/Up`
