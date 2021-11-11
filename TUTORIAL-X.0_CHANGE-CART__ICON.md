# HOW ABOUT ANOTHER ICON PLEASE?
`TUTORIAL X.0 `CHANGE CART ICON`

Sure do remember the first few styling mods for the early few storefronts rolled out. That is, <q>The cart icon sure needs some more touch to it...</q>
   
Well, here is a simple outline to get that done! Be it that you do have the time or, am taking up the challenge to prove that you do have the stuff to be a future programmer in the ecom side of things..

Go ahead, try out the steps outlined below or if it's too much for you, freely email eaidter@gmail.com to hire us at minimal cost.

## REMINDER / TIPS

   - [Duplicate](https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes) your theme first to keep it as a back-up before trying this advanced coding
   - Keyboard shortcut to find specific text line: Place cursor on the code editor screen and hold <kbd>`CTRL + F`

## From the Backend

1. From your Shopify backend, go to  __Theme__ > __Snippets__
2. Search for the file the cart icon is at _e.g_ card-icon
3. <kbd>`Ctrl + A`<kbd>  > __Delete__
4. Search the Web for a cool icon that is freely available for commercial use.
5. Copy to Clipboard, go back to backend & paste it.
6. Next, click <b>Save.
  - ![SAVE](ipfs://ipfs.io/)

### Not of Size?

1. From your Shopify backend, go to <b>Assets directory
2. Click on `theme.css` file.
  - <i> For the BASIC store theme, it is called `theme.scss.css`.
3. Add the following CSS to the very bottom:
  - `.icon-cart { content: "\e600"; }`
  - <i>You may adjust the `px` unit other than `25px`.
4.  Next, click <b>Save.
  - ![SAVE](ipfs://ipfs.io/)
5.  
6.  

```css
.icon-cart {
  content: "\e600"; }
```

Go ahead & see how it will looks like on the online store!
