# WholeFoodsWarner
A simple tampermonkey script that warns you with a ding when a delivery slot is available, because we all need our organic leaves during a pandemic.

Note 3 things to use this script : 

1 ) this assumes use of Tampermonkey, which is a chrome extension.

2 ) Chrome has some strict policies with regards to how it allows autoplay sounds. This won't work correctly unless you set a key
in your Windows Registry.
 - Open up the registry editor from the start menu. ( you can search 'regedit' to find it )
 - Navigate to HKEY_LOCAL_MACHINE > SOFTWARE > Policies > Google > Chrome > AutoplayWhitelist
 - Then create an entry named "1" with a value of "https://www.amazon.com/gp/buy/shipoptionselect/handlers/display.html?hasWorkingJavascript=1". The folders for this key might not exist. If not, just make them. 
 
3 ) Fill your shopping cart, and then navigate to the delivery selection page. Leave the page open. This script will reload the page
every 60 seconds and then make a ding when your able to complete your order. 

This script depends upon jquery parsing the page. Wholefoods does not have a notification API, so this is hack. That means if wholefoods
changes the page, bans reloads, signs you out against your will, or does basically anything, this script is likely to break. I won't be
maintaining this. I only wrote this because of Covid-19, and thought someone else might make use of it. I make no promises. 
