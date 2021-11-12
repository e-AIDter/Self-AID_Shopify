<button class="d-block d-md-none"> <a class="dropdown-item" href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a>          </button> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click here to jump to the right TUTORIAL file.

# CUSTOM FIELDS
TUTORIAL 3.0 `Sectioned Theme`

Features to collect custom details for order using line item properties.

What is 'line item properties'?
Line item properties is used for custom form fields to the product page and reflect on customer's order seen on backend.

   - Checkbox / Checkbox group options
   - Dropdown options
   - Radio button options
   - Short text box
   - Long text box
   
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
    - File name > replace 'alternate' to `customizable` (or to any of your preferred name and this will change the struction below)
    
    Next, click <b>Create template</b> and the new created template file for `product.customizable.liquid` will open in the code editor.

4. Find the following code within the new created template file:

       {% section 'product-template' %}

    Replace it with:

       {% section 'product-customizable-template' %}

Next, click <b>Save</b>.

## ADD A NEW SECTION

1. In the Sections directory, click <b>Add a new section</b> and add the following
    - Create a new section called `product-customizable-template`

    Next, click <b>Create section</b> and the new created section file for `product-customizable-template.liquid` will open in the code editor.

2. Delete all of the default code, so that the new created section file is blank.

3. Find and open file named `product-template.liquid` under the Sections directory.

4. Select and copy all of the content from this file, and paste it into your new `product-customizable-template.liquid` file.

Next, click <b>Save</b>.

## CREATE CUSTOM FORM FIELDS

Generate the HTML and Liquid code for each form fields.

   - Use Shopify tool: [Shopify UI Elements Generator tool](https://ui-elements-generator.myshopify.com/pages/line-item-property)
   - Auto preview panel provided while you create your custom field.
   - Copy the generated code from the box in the Grab your code section.

### PASTE THE COPIED CODES

   - Under the Section directory, open file named `product-customizable-template.liquid`

      Find the code `type="submit"` << This code is wrap within the Add to cart button family code.

   - The copied generated codes is paste above the Add to cart button family code /or at any position.

      TIPS: Assign the template to your specific product and preview the changes made. Reposition, save the changes, preview again. Repeat the steps until it is in the right position on your product page.
    
### ASSIGN THE CUSTOMIZABLE TEMPLATE TO SPECIFIC PRODUCTS

1. From your Shopify admin, go to <b>Products</b> > <b>All products</b>

2. Click the name of the product you want to make available for pre-order

3. Scroll down to find <b>Theme templates</b> and change the template to product.customizable in the drop-down option

4. Click <b>Save</b>

TIPS: Use [bulk editor](https://help.shopify.com/en/manual/online-store/themes/os20/theme-structure/templates#bulk-template-changes) to assign the template to more than 3 products

## SHOW THE CUSTOM DETAILS ON CART PAGE
This code checks each line item to see if it has any line item properties, and displays them if they exist.

1. In the Sections directory, click cart-template.liquid /or cart.liquid (depending on your theme).

    Find the line containing the code `{{ item.product.title }}`. On a new line below, paste the following code:

       {% assign property_size = item.properties | size %}
       {% if property_size > 0 %}
         {% for p in item.properties %}
           {% assign first_character_in_key = p.first | truncate: 1, '' %}
           {% unless p.last == blank or first_character_in_key == '_' %}
             {{ p.first }}:
             {% if p.last contains '/uploads/' %}
               <a class="lightbox" href="{{ p.last }}">{{ p.last | split: '/' | last }}</a>
             {% else %}
               {{ p.last }}
             {% endif %}
             <br>
           {% endunless %}
         {% endfor %}
       {% endif %}

Next, click <b>Save</b>.

## UPDATE CART PAGE TO WORK FOR CUSTOM FIELDS FIELDS

1. In the Sections directory, click cart-template.liquid /or cart.liquid (depending on your theme).

      Find (CTRL+F) all `a` tag that has an `href` value starting with
      
       /cart/change
        
      Replace it with
      
       /cart/change?line={{ forloop.index }}&quantity=0

2. Update item quantity fields in the cart

    Any fields that display item quantities in your cart will also need to be updated to work with custom line item properties:

      Find (CTRL+F) all `input` tag that has a `name` value of
      
       updates[{{ item.id }}]
        
      Replace it with

       updates[]
       
Next, click <b>Save</b>.
       
## OPTIONAL - SHOW CUSTOM DETAILS IN EMAIL NOTIFICATION
Repeat these steps for any other email notifications that you want to include line item properties.

1. From your Shopify admin, go to <b>Settings</b> > <b>Notifications</b>

2. Click the name of the notification template that you want to add line item properties to.

    Find the following code:

       {{ line.title }}

    Replace it with:

       {{ line.title }}{% for p in line.properties %}{% unless p.last == blank %} - {{ p.first }}: {{ p.last }}{% endunless %}{% endfor %}

Next, click <b>Save</b>.
