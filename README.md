GIOS client
===========
When run it consumes one particular (for now hardcoded) dust monitoring station for dust data each half an hour and displays it


Run
---
Run in chromium

    --verbose
    --app=URL
    -kiosk
    
on Mac chrome
    /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome -kiosk --disable-web-security --user-data-dir=/tmp/chrometempwork --app="file:///Users/zakrzewm/git/gios-client/gios.html"

Disable security (for development only) to avoid CORS issues when loading app from file:///

    /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --disable-web-security --user-data-dir=/tmp/chrometempwork file:///Users/zakrzewm/git/gios-client/gios.html

chromium-browser --disable-web-security --user-data-dir=/tmp/chrometempwork file:///opt/gios-web-client/gios.html

export DISPLAY=:0.0
nohup chromium-browser -kiosk --disable-web-security --user-data-dir=/tmp/chrometempwork file:///opt/gios-web-client/gios.html  >/tmp/nohup_chrome.out &
