<button class="d-block d-md-none"> <a class="dropdown-item" href="/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a>          </button>

# BACK TO TOP BUTTON
TUTORIAL 3.0 `Sectioned Theme`

This feature is ideally for long scrolling webpage, and with a click on this button will bring you back to the top of the current page.

You are required to complete all the steps below or email at eaidter@gmail.com to hire us with minimal cost.

### REMINDER / TIPS</b>

   - [Duplicate](https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes) your theme first to keep it as a back-up before trying this advanced coding
   - Keyboard shortcut to find specific text line: Place cursor on the code editor screen and hold `CTRL + F`

## ADD SNIPPET
1. From your Shopify admin, go to <b>Online Store</b> > <b>Themes</b>.

2. Find the theme you want to edit, and then click <b>Actions</b> > <b>Edit code</b>.

3. In the Snippets directory, click <b>Add a new snippet</b> and and add the following
    - Create a new snippet called `back-to-the-top`

    Next, click <b>Create snippet</b> and the new created file for `back-to-the-top.liquid` will open in the code editor.

4. Paste the following code into the new created back-to-the-top file:

       {% comment %}
          Reduce below value if you need the back to the top button to appear higher up on the page.
          That value is in pixels.
        {% endcomment %}
        {% assign vertical_offset_for_trigger = 300 %}

       {% comment %}
          Vertical offset from bottom of browser for the position of the button.
       {% endcomment %}
       {% assign position_from_bottom = '6em' %}

        <a id="BackToTop" href="#" title="Back to the top" class="back-to-top hide">
          <span>Back to the top</span> <i class="fa fa-arrow-circle-o-up fa-2x"></i>
        </a>
       {{ '//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.min.css' | stylesheet_tag }}
       
       <style>
          .back-to-top {
            position: fixed;
            bottom: {{ position_from_bottom }};
            right: 0px;
            text-decoration: none;
            color: #999;
            background-color: #eee;
            font-size: 16px;
            padding: 0.3em;
            -webkit-border-top-left-radius: 3px;
            -webkit-border-bottom-left-radius: 3px;
            -moz-border-radius-topleft: 3px;
            -moz-border-radius-bottomleft: 3px;
            border-top-left-radius: 3px;
            border-bottom-left-radius: 3px;
            z-index: 60000;
          }
          .back-to-top i {
            vertical-align: middle;
          }
          .back-to-top span {
            padding-left: 0.5em;
          }
          .back-to-top i + span {
            padding-left: 0;
          }
          .back-to-top:hover {
            text-decoration: none;
            color: #555;
          }
          .hide {
            display: none!important;
          }
       </style>
       <script>
            (function() {
            function trackScroll() {
                var scrolled = window.pageYOffset;
                var coords = {{ vertical_offset_for_trigger }};

                if (scrolled > coords) {
                goTopBtn.classList.remove('hide');
                }
                if (scrolled < coords) {
                goTopBtn.classList.add('hide');
                }
            }

            function backToTop() {
                if (window.pageYOffset > 0) {
                window.scrollBy(0, -80);
                setTimeout(backToTop, 0);
                }
            }

            var goTopBtn = document.querySelector('.back-to-top');

            window.addEventListener('scroll', trackScroll);
            goTopBtn.addEventListener('click', backToTop);
            })();
       </script>
        
Next, click <b>Save</b>.

## INCLUDE THE SNIPPET

1. Under Layouts folder, open the `theme.liquid` file

2. Find (CTRL+F) `</body>` or scroll to the bottom of the file.

    Right above the closing `</body>` tag, paste this code:

       {% render 'back-to-the-top' %}
        
## CUSTOMIZATION

In the `back-to-the-top` snippet file, locate and make adjustment accordingly.

For the position of your button relative to the bottom of the browser, edit the position_from_bottom value:

    {% assign position_from_bottom = '6em' %}
    
To change how far a customer needs to scroll down to trigger the button appearance, edit the vertical_offset_for_trigger value:

    {% assign vertical_offset_for_trigger = 300 %}
    
The color scheme and sizing can be adjusted under the `<style>` tag to fit your theme. Locate them and change accordingly.

Next, click <b>Save</b>.
