<table><th><tr><td><a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click <a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> to jump to the right TUTORIAL file.</td></tr></th></table>



# GIFT WRAP OPTION IN CART PAGE
TUTORIAL x.0 `Sectioned Theme`

As a young padawan myself, would like to share the pitfalls of following through a well written tutorial!

Perhaps after this share, you would be more primed to be avoiding these mistakes that could just be between you & getting that coding to visual!
   
:mountain_bicyclist:You are pumped to complete all the steps below, never to give up or ever email eaidter@gmail.com to hire them with minimal cost. 

### REMINDER / TIPS</b>

   - [Duplicate](https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes) your theme first to keep it as a back-up before trying this advanced coding
   - Keyboard shortcut to find specific text line: Place cursor on the code editor screen and hold `CTRL + F`

## WHY MAKE A PRODUCT?

_Translation_ : You are making a Webpage about the gift wrappingoption that you so kindly offer, so yeah

1. From your Shopify admin, go to __Products__ > __All__ products.

1. Click __Add product__.

1. <q><i>Fill in all about Gift Wrapping, ok? You got this!</i><q>

1. Click __Save__.


## MAKE A MENU?


2. From your Shopify admin, go to __Online Store__ > __Navigation__.

2. Click __Add menu__.

2. Name your menu :arrow_right:" Gift wrapping":arrow_left: __MUST__

2. Add the "[product](#WHY MAKE A PRODUCT?)" you just made to the menu:
  3. Click __Add menu__ item, and then enter a Name e.g <i>wrap a gift!</i>
  3. In the __Link__ field, __select Products__, and then select the "[product](#WHY MAKE A PRODUCT?)" you just made again.
  3. Click __Add__.

  3. Click __Save__.


## CREATE THE CODE SNIPPET (FUN PART)
### FLAT RATE

4. From your Shopify backend, go to __Online Store__ > __Themes__.

4. Find the theme you want to edit, and then click __Actions__ > __Edit code__.

4. In the __Snippets__ directory, click __Add a new snippet__.

4. Name your snippet `gift-wrapping` and click __Create snippet__.

4. Paste the coding below:

    ```liquid
    {% if linklists.gift-wrapping.links.size > 0 and
    linklists.gift-wrapping.links.first.type == 'product_link' %}
    
    ...
    
    {% endif %}
    ```

### PER CART ITEM BASIS

5. From your Shopify backend, go to __Online Store__ > __Themes__.

5. Find the theme you want to edit, and then click __Actions__ > __Edit code__.

5. In the __Snippets__ directory, click __Add a new snippet__.

5. Name your snippet `gift-wrapping` and click __Create snippet__.

5. Paste the coding below:

    ```liquid
    {% if linklists.gift-wrapping.links.size > 0 and
    linklists.gift-wrapping.links.first.type == 'product_link' %}
    
    ...
    
    {% endif %}
    ```


### INCLUDE THE SNIPPET CODING

To include the gift-wrapping snippet in your cart template:

7. In the __Sections__ directory, click `cart-template.liquid`. If your theme doesn't have a `cart-template.liquid`, then click `cart.liquid` in the __Templates__ directory.

7. Press <kbd> Ctrl + F </kbd> & find
```html
    </form>
```
 in the file. Once found, one line ABOVE the 
```html
    </form>
```
word, paste the following code:

    {% render 'gift-wrapping' %}

7. Click __Save__.

7. ?!??

7. :whale: <q><i>You... did... it..</i></q>


<table><th><tr><td><a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click <a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> to jump to the right TUTORIAL file.</td></tr></th></table>
