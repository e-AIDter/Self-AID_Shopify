<button class="d-block d-md-none"> <a class="dropdown-item" href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a>          </button> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click here to jump to the right TUTORIAL file.

# CUSTOM TEXT FOR ATC BUTTON
TUTORIAL 1.0 `Sectioned Theme` | [CONSIDERATION](https://github.com/e-AIDter/Self-AID_Shopify/blob/main/Consideration_CHG-ATC-BTN.md)

Changing text of Add To Cart (ATC) button on product page. Button functionality does not change (perform the same as an actual ATC button). This is recommended for products with the following settings:

   - PRE-ORDER for products that have went out-of-stock.
   - BULK PURCHASE with dateline.
   - /or products that need longer than the usual to fulfil.

You are required to complete all the steps below or email at eaidter@gmail.com to hire us with minimal cost.

### REMINDER / TIPS</b>

   - [Duplicate](https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes) your theme first to keep it as a back-up before trying this advanced coding
   - Keyboard shortcut to find specific text line: Place cursor on the code editor screen and hold `CTRL + F`

## ADD A NEW PRODUCT TEMPLATE

1. From your Shopify admin, go to <b>Online Store</b> > <b>Themes</b>.

2. Find the theme you want to edit, and then click <b>Actions</b> > <b>Edit code</b>.

3. In the Templates directory, click <b>Add a new template</b> and follow according as below:
    - Create a new template for `product`
    - Template type `liquid`
    - File name > replace 'alternate' to `pre-order` (or to any of your preferred name and this will change the struction below)
    
    Next, click <b>Create template</b> and the new created template file for `product.pre-order.liquid` will open in the code editor.

4. Find the following code within the new created template file:

       {% section 'product-template' %}

    Replace it with:

       {% section 'product-pre-order-template' %}
    
    In the same file, look for a `<script>` tag that contains this line of code:
  
       addToCart: {{ 'products.product.add_to_cart' | t | json }},

    Replace it with:

       addToCart: {{ 'Pre-order' | json }},

Next, click <b>Save</b>.


## ADD A NEW SECTION

1. In the Sections directory, click <b>Add a new section</b> and add the following
    - Create a new section called `product-pre-order-template`

    Next, click <b>Create section</b> and the new created section file for `product-pre-order-template.liquid` will open in the code editor.

2. Delete all of the default code, so that the new created section file is blank.

3. Find and open file named `product-template.liquid` under the Sections directory.

4. Select and copy all of the content from this file, and paste it into your new `product-pre-order-template.liquid` file.

5. In your new product-pre-order-template.liquid file, find and replace the Add to cart button text.

    Look for this code:

       <span data-add-to-cart-text>
         {% unless current_variant.available %}
         {{ 'products.product.sold_out' | t }}
         {% else %}
         {{ 'products.product.add_to_cart' | t }}
         {% endunless %}
       </span>

      Replace it with:

       <span data-add-to-cart-text>
         {{ 'Pre-order' | json | remove: '"' }}
       </span>

Next, click <b>Save</b>.

## ASSIGN THE TEMPLATE TO SPECIFIC PRODUCTS

1. From your Shopify admin, go to <b>Products</b> > <b>All products</b>

2. Click the name of the product you want to make available for pre-order

3. Scroll down to find <b>Theme templates</b> and change the template to product.pre-order in the drop-down option

4. Click <b>Save</b>

TIPS: Use [bulk editor](https://help.shopify.com/en/manual/online-store/themes/os20/theme-structure/templates#bulk-template-changes) to assign the template to more than 3 products

## OTHER SETTINGS

Refer to Github file - [Consideration_CHG-ATC-BTN](https://github.com/e-AIDter/Self-AID_Shopify/blob/main/Consideration_CHG-ATC-BTN.md)
