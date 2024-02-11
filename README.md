# .conf
Resources for setting up Linux environment.

## Install Core Apps
`sudo -S pacman discord telegram-desktop signal-desktop xclip`

`yay -S slack-desktop notion-app spotify visual-studio-code-bin`

## Download i3 Endevour Config
`curl https://raw.githubusercontent.com/qudo-code/.config/main/i3-config-endevour --output .config/i3/config`

## Download i3 Blocks Endevour Config
`curl https://raw.githubusercontent.com/qudo-code/.config/main/i3blocks-endevour --output .config/i3/i3locks.conf`

## I3 Mods
### Extra Keybinds
```js
bindsym $mod+Shift+q kill
bindsym Print exec flameshot gui
bindsym $mod+q exec --no-startup-id brave
bindsym $mod+period exec rofi -modi emoji -show emoji
```
### Mod Key -> Alt
`set $mod Mod1`
### Resize Mode w/Vim Keys
```
# resize window (you can also use the mouse for that)
mode "resize" {
        # These bindings trigger as soon as you enter the resize mode

        # Pressing left will shrink the window’s width.
        # Pressing right will grow the window’s width.
        # Pressing up will shrink the window’s height.
        # Pressing down will grow the window’s height.
        bindsym h resize shrink width 10 px or 10 ppt
        bindsym j resize grow height 10 px or 10 ppt
        bindsym k resize shrink height 10 px or 10 ppt
        bindsym l resize grow width 10 px or 10 ppt

        # same bindings, but for the arrow keys
        bindsym Left resize shrink width 10 px or 10 ppt
        bindsym Down resize grow height 10 px or 10 ppt
        bindsym Up resize shrink height 10 px or 10 ppt
        bindsym Right resize grow width 10 px or 10 ppt

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
### Splic Horizontal w/C
`bindsym $mod+c split h`
### Wallpaper
`exec --no-startup-id sleep 1 && feh --bg-fill /home/qudo/Pictures/wallpaper.jpg`
