# CUSTOM PRODUCT PAGE TABS
TUTORIAL 2.0 `Sectioned Theme`

Recommendation for product page with custom tabs.

You are required to complete all the steps below or email at eaidter@gmail.com to hire us with minimal cost.

### REMINDER / TIPS

   - [Duplicate](https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes) your theme first to keep it as a back-up before trying this advanced coding
   - Keyboard shortcut to find specific text line: Place cursor on the code editor screen and hold `CTRL + F`
   
## ADDING THE TABS AND CSS

1. From your Shopify admin, go to <b>Online Store</b> > <b>Themes</b>.

2. Find the theme you want to edit, and then click <b>Actions</b> > <b>Edit code</b>.

3. Under <b>Section</b> directory, open file name `product-template.liquid`

      locate the product description:
              
       {{ product.description }}
       
      Replace it with the following code:
      
       <div>
          <ul class="tabs">
            <li><a href="#tab-1">Info</a></li>
            <li><a href="#tab-2">Shipping</a></li>
            <li><a href="#tab-3">Returns</a></li>
          </ul>
         <div id="tab-1">
          {{ product.description }}
         </div>
         <div id="tab-2">
          {% render 'shipping' %}
          </div>
          <div id="tab-3">
          {{ pages.returns.content }}
         </div>
       </div>
       
IMPORTANT | UNDERSTANDING

In the above coding, the tab titled "Info / Shipping / Returns" can be amended to your preferred names.

#1. `{{ product.description }}` The information that is added to your specific product's descriptions.

#2. `{% render 'shipping' %}` You will need to add or render it from a file under snippet directory. This allows you to add custom html. Otherwise, you can consider changing it to #3

#3. `{{ pages.returns.content }}` Replace the text 'returns' to the URL handle. Example; the back of the url handle is /size-chart, it should look like this {{ pages.size-chart.content }}
       
4. Add the following CSS to the very bottom:

       <style>
          ul.tabs {
            border-bottom: 1px solid #DDDDDD;
            display: block;
            margin: 0 0 20px;
            padding: 0;
          }
          ul.tabs li {
            display: block;
            float: left;
            height: 30px;
            margin-bottom: 0;
            padding: 0;
            width: auto;
          }
          ul.tabs li a {
            -moz-border-bottom-colors: none;
            -moz-border-image: none;
            -moz-border-left-colors: none;
            -moz-border-right-colors: none;
            -moz-border-top-colors: none;
            background: none repeat scroll 0 0 #6bb4a7;
            border-color: #DDDDDD !important;
            border-style: solid;
            border-width: 1px 1px 0 1px;
            display: block;
            font-size: 13px;
            height: 29px;
            line-height: 30px;
            margin: 0;
            padding: 0 20px;
            text-decoration: none;
            width: auto;
            color: white;
            border-bottom:none !important;
          }
          ul.tabs li a.active {
            background: none repeat scroll 0 0 #f5f5dc;
            border-left-width: 1px;
            border-top-left-radius: 2px;
            border-top-right-radius: 2px;
            color: #4c555f;
            height: 35px;
            margin: 0 0 0 -1px;
            font-weight: bold;
            letter-spacing:1px;

            position: relative;
            top: -4px;
          }
          ul.tabs li:first-child a.active {
            margin-left: 0;
          }
          ul.tabs li:first-child a {
            border-top-left-radius: 2px;
            border-width: 1px 1px 0;
          }
          ul.tabs li:last-child a {
            border-top-right-radius: 2px;
          }
          ul.tabs:before, ul.tabs:after {
            content: " ";
            display: block;
            height: 0;
            overflow: hidden;
            visibility: hidden;
            width: 0;
          }
          ul.tabs:after {
            clear: both;
          }
       </style>
        
Next, click <b>Save</b>.

## ADD jQuery

Under <b>Assets</b> directory, open file name `theme.js`, and the following JavaScript code at the very bottom:

    $(document).ready(function() {
      $('ul.tabs').each(function(){
        var active, content, links = $(this).find('a');
        active = links.first().addClass('active');
        content = $(active.attr('href'));
        links.not(':first').each(function () {
          $($(this).attr('href')).hide();
        });
        $(this).find('a').click(function(e){
          active.removeClass('active');
          content.hide();
          active = $(this);
          content = $($(this).attr('href'));
          active.addClass('active');
          content.show();
          return false;
        });
      });
    });
    
Next, click <b>Save</b>.

   
