<table><th><tr><td><a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click <a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> to jump to the right TUTORIAL file.</td></tr></th></table>



# SHOW REMAINING INVENTORY
<q>
How to show remaining inventory in webstorepages?</q>
TUTORIAL x.0 `Sectioned Theme` 

Ever wonder to to have a count of what is remaining in inventory to those browsing the websstore?

Yeah me too once, but now it is time for your turn from <q>wonder to done it!</q>!


## REMINDER

   - [Duplicate](https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes) your theme first to keep it as a back-up before trying this advanced coding
   - Keyboard shortcut to find specific text line: Place cursor on the code editor screen and hold `CTRL + F`

## EDIT THEME.LIQUID (DEBUT)


3. From your Shopify backend, go to __Online Store__ > __Themes__.

3. Find the theme you want to edit, and then click __Actions__ > __Edit code__.

3. From the ___Layout directory___, open `theme.liquid`.

3. Press <kbd> Ctrl + F </kbd> & find
```html
    </head>
```
 in the file. Once found, one line ABOVE the 
```html
    </head>
```
word, paste the following code:

    ```javascript
    <script> var variantStock = {}; </script>
    ```
3. Click __Save__.

## PROGRESS ON!

- Open `product-template.liquid` to add this feature to product pages.
- Open `featured-product.liquid` to add this feature to the featured product  the home page.

7. Press <kbd> Ctrl + F </kbd> & find
```liquid
    {% form 'product
```
 in the file. Once found, one line ABOVE the 
```liquid
    {% form 'product
```
line, paste the following code:

    {% comment %}

<table><th><td>:bell: Note</td><tr><td>You may freely change the viisible wording on the above codings where it is to your satisfaction.</td></tr></th></table>

8. Lastly, at the very bottom, add the following codings:

    ```liquid
    <script>
  {% for variant in product.variants %}
    variantStock[{{- variant.id -}}] = {{ variant.inventory_quantity }};
  {% endfor %}
    </script>
    ```
9. Click __Save__.



## ARE WE THERE YET? (DEBUT 17.9.0 & LATER)

7. Open `theme.js.liquid` or `theme.js`.

7. Press <kbd> Ctrl + F </kbd> & find
```javascript
    theme.Product = (function()
```
 in the file. Once found, one line :arrow_down:BELOW:arrow_down: the 
```javascript
    theme.Product = (function()
```
line, paste the following code:

    inventoryHtml: '.inventoryWrapper',

8. In the same file, press <kbd> Ctrl + F </kbd> & find
    ```javascript
    _setProductState: function(evt) {
    ```
 in the file. Once found, one line :arrow_down:BELOW:arrow_down: the 
    ```javascript
    _setProductState: function(evt) {
    ```
line, paste the following code:

    ```javascript
    var inventoryWrapper = this.container.querySelector(this.selectors.inventoryHtml);
    ```

8. In the same function, press <kbd> Ctrl + F </kbd> & find
    ```javascript
    if (!variant) {
    ```
   in the same function. Once found, juft before the `}`, paste the following code:

    ```javascript
    var inventoryWrapper = this.container.querySelector(this.selectors.inventoryHtml);
    ```

9. Click __Save__.

7. ?!??

7. :whale: <q><i>You... did... it..</i></q>

:mountain_bicyclist:At this stage once completed all the steps above successfully, without ever ever emailing eaidter@gmail.com to hire them with minimal cost... You should really ought to think about joinging us!!

<meta name="generator" content="LibreOffice 7.0.4.2 (GNU/Linux)">
<table cellspacing="0" border="0"> <colgroup width="109" span="10"></colgroup> <tbody><tr> <td height="174" align="center"><br></td> <td align="center">L<br>I<br>G<br>H<br>T</td> <td align="center">S<br>U<br>p<br>p<br>l<br>y</td> <td align="center">M<br>I<br>n<br>i<br>m<br>a<br>l</td> <td align="center">D<br>A<br>w<br>n</td> <td align="center">D<br>E<br>b<br>u<br>t</td> <td align="center">N<br>A<br>r<br>r<br>a<br>t<br>i<br>v<br>e</td> <td align="center">B<br>O<br>u<br>n<br>d<br>l<br>e<br>s<br>s</td> <td align="center">V<br>E<br>n<br>t<br>u<br>r<br>e</td> <td align="center">V<br>I<br>n<br>t<br>a<br>g<br>e</td> </tr> <tr> <td height="21" align="left">This customization<br/>found in<br/>Theme settings?</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:heavy_check_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> </tr> </tbody></table>

<table><th><tr><td><a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click <a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> to jump to the right TUTORIAL file.</td></tr></th></table>
