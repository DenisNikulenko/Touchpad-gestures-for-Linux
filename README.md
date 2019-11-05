# Touchpad-gesture

1. sudo gpasswd -a $USER input - проверка
2. sudo apt-get install libinput-tools - уст. пакета libinput-tools
3. sudo apt-get install ruby - уст. ruby
4. sudo gem install fusuma - уст. пакета fusuma
5. sudo apt-get install xdotool
6. mkdir -p ~/.config/fusuma   
7. nano ~/.config/fusuma/config.yml
-----------------------------------------------------------------------------------
# CONFIG.YML
```ruby
swipe:
  3:
    left:
      command: 'xdotool key alt+Left'
    right:
      command: 'xdotool key alt+Right'
    up:
      command: 'xdotool key ctrl+alt+Up'
      threshold: 1.5
    down:
      command: 'xdotool key ctrl+alt+Down'
      threshold: 1.5
  4:
    left:
      command: 'xdotool key super+Left'
    right:
      command: 'xdotool key super+Right'
    up:
      command: 'xdotool key super'
    down:
      command: 'xdotool key super+ctrl+d'
pinch:
  2:
    in:
      command: 'xdotool key ctrl+plus'
      threshold: 0.1
    out:
      command: 'xdotool key ctrl+minus'
      threshold: 0.1

threshold:
  swipe: 0.4
  pinch: 0.4

interval:
  swipe: 0.7
  pinch: 0.4
```
  -----------------------------------------------------------------------------
  
  9. which fusuma - показать путь к fusuma
  10. gnome-session-properties - авто запуск приложений
  11. добавить путь к fusuma
  
  Полезнные ссылки:
  1. [Fusuma](https://github.com/iberianpig/fusuma)
  2. [xdotol](https://github.com/jordansissel/xdotool/blob/master/xdotool.pod)
  3. [LIBINPUT-GESTURES](https://github.com/bulletmark/libinput-gestures)
