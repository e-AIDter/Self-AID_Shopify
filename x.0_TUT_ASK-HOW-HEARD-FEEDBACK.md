<table><th><tr><td><a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click <a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> to jump to the right TUTORIAL file.</td></tr></th></table>



# ASK FEEDBACK
<q>
How did you hear about our webstorefront?</q>
TUTORIAL x.0 `Sectioned Theme` 

## REMINDER

   - [Duplicate](https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes) your theme first to keep it as a back-up before trying this advanced coding
   - Keyboard shortcut to find specific text line: Place cursor on the code editor screen and hold `CTRL + F`

## CREATE A FORM

To create the How did you hear about us? form:

2. From your Shopify backend, go to __Online Store__ > __Themes__.

2. Find the theme you want to edit, and then click __Actions__ > __Edit code__.

2. In the __Snippets__ directory, click __Add a new snippet__.

2. Create the snippet:
  5. Name your snippet `hear-about-us` __MUST__.
  5. Click __Create snippet__.

2. In your new `hear-about-us.liquid` snippet, paste the following code:

    ```css
    <style>
    #how-did-you-hear-about-us--label,
    #how-did-you-hear-about-us-other--label {
        font-weight: bold;
    ...
    })()
    </script>
    ```
2. Click __Save__.

:mountain_bicyclist:You are determined to complete all the steps above, never to give up or ever email eaidter@gmail.com to hire them with minimal cost!

## INCLUDE THE SNIPPET INTO YOUR CART PAGE!

To include the `hear-about-us.liquid` snippet into your cart page:

3. In the Sections directory, click `cart-template.liquid`. 
  + Alternatively, click `cart.liquid` in the __Templates directory__.

3. Press <kbd> Ctrl + F </kbd> & find
```html
    </form>
```
 in the file. Once found, one line ABOVE the 
```html
    </form>
```
word, paste the following code:

`{% render 'hear-about-us' %}`

3. Click __Save__.

3. ?!??

3. :whale: <q><i>You... did... it..</i></q>


## ADD SOME THEME SETTINGS FOR FUTURE MODIFICATION & USE

5. In the config directory, click `settings_schema.json`.

5. Paste the following coding:

```json
{
"name": "Hear About Us",
"settings": [
    {
    ...
        "label": "Color",
        "default": "#ff0000"
    }
]
},
```
3. Click __Save__.

## MAKE THE FORM REQUIRED

This part is entirely optional if you must.

4. In the Sections directory, click `cart-template.liquid`. 
  + Alternatively, click `cart.liquid` in the __Templates directory__.

4. Press <kbd> Ctrl + F </kbd> & find `novalidate`

4. Replace the `novalidate` with the following codings:

    {% unless settings.hau_form_validation %}novalidate{% endunless %}

4. Click __Save__.

4. In the theme editor, click __Theme settings__ on the sidebar.

4. Click the "Hear About Us" tab.

4. Under Form Validation, make sure the Enable form validation setting is enabled.


<table><th><tr><td>:bell: You can customise the error messages displayed by modifying the `Error message` and `Other field` error message text field settings. You can also customise the error color by changing the `Color` setting under "Error Styling".</td></tr></th></table>


## SETTINGS

To customize the options in the _How did you hear about us?_ drop-down menu, you can edit the options using the theme settings within the __theme editor__.

4. In the theme editor, click __Theme settings__.

4. Click the "Hear About Us" tab.

4. Under __Form__ options, add or remove options, separated by commas.

4. Click __Save__.


<table><th><td>:bell: Note</td><tr><td>`Other` option will be added in automatically.</td></tr></th></table>

## ...FAQ?!

Q: Where will I see the data?
A:

Q: If no listed option is the answer, can perhaps type something in?
A: Yes, selects `Other`, a text box in which they can type an answer will appear below the drop-down menu.

Q: Can this be includes in e-mail notifications?
A: Yes. 
1. Go to your __Notifications__ page in your backend, and add the following codings to your __New order email template__:
    He/She/They heard about us through {% if attributes.how-did-you-hear-about-us-other == blank %}{{ attributes.how-did-you-hear-about-us }}{% else %}{{ attributes.how-did-you-hear-about-us-other }}{% endif %}.
1. Click __Save__.

<meta name="generator" content="LibreOffice 7.0.4.2 (GNU/Linux)">
<table cellspacing="0" border="0"> <colgroup width="109" span="10"></colgroup> <tbody><tr> <td height="174" align="center"><br></td> <td align="center">L<br>I<br>G<br>H<br>T</td> <td align="center">S<br>U<br>p<br>p<br>l<br>y</td> <td align="center">M<br>I<br>n<br>i<br>m<br>a<br>l</td> <td align="center">D<br>A<br>w<br>n</td> <td align="center">D<br>E<br>b<br>u<br>t</td> <td align="center">N<br>A<br>r<br>r<br>a<br>t<br>i<br>v<br>e</td> <td align="center">B<br>O<br>u<br>n<br>d<br>l<br>e<br>s<br>s</td> <td align="center">V<br>E<br>n<br>t<br>u<br>r<br>e</td> <td align="center">V<br>I<br>n<br>t<br>a<br>g<br>e</td> </tr> <tr> <td height="21" align="left">This customization<br/>found in<br/>Theme settings?</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> </tr> </tbody></table>

<table><th><tr><td><a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click <a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> to jump to the right TUTORIAL file.</td></tr></th></table>
