<table><th><tr><td><a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click <a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> to jump to the right TUTORIAL file.</td></tr></th></table>



# OPEN LINKS IN NEW TAB
TUTORIAL x.0

This makes all links in your webstorefront open in a new tab. A quick copy & paste guide by Shopofy! Used 'till this day that enchances some user experience struggling to keep _tabs_ on which pages that they had visited last..
   
:arrow_heading_up:This guide should not have you to write to eaidter@gmail.com to hire us with minimal cost.

### REMINDER / TIPS</b>

   - [Duplicate](https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes) your theme first to keep it as a back-up before trying this coding nevertheless!
   - Keyboard shortcut to find specific text line: Place cursor on the code editor screen and hold `CTRL + F`

## BABY STEPS


1. From your Shopify admin, go to __Online Store__ > __Themes__.

2. Find the theme you want to edit, and then click __Actions__ > __Edit code__.

3. In the `Assets` directory, click one of the following:
     + `theme.js`
     + `theme.js.liquid`
     + `custom.js`
   
4. __Paste__ the following code at the bottom of the file:
   
```javascript
       var links = document.links;
       for (let i = 0, linksLength = links.length ; i < linksLength ; i++) {
         if (links[i].hostname !== window.location.hostname) { links[i].target = '_blank'; } }
```
   
5. Click __Save__.

5. And, You're done:exclamation:

