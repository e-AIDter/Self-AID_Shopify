<table><th><tr><td><a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click <a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> to jump to the right TUTORIAL file.</td></tr></th></table>

# IMPROVE NAVIGATION
TUTORIAL x.0 `Breadcrumb NAVIGATION`

If you have been around since the birth of the World Wide Web then you might have no issues porting from one Webpage to another Webpage.

Most people do need some form of AccessibleNav to get around your store & trust you me that when the more successful you are the more Products you have & the higher the chances are getting lost!

Go ahead, try out the steps outlined below or if it's too much for you, freely email eaidter@gmail.com to hire us at minimal cost.

### REMINDER / TIPS</b>

   - [Duplicate](https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes) your theme first to keep it as a back-up before trying this advanced coding
   - Keyboard shortcut to find specific text line: Place cursor on the code editor screen and hold `CTRL + F`


## ADD A BREADCRUMBS TO YOUR WEBSTOREFRONT

<ol>
<li>From your Shopify admin, go to <b>Online Store</b> &gt; <b>Themes</b>.
<li>Find the theme you want to edit, then click <b>Actions</b> &gt; <b>Edit code</b>.
<li>Create a new snippet:

<li> Click the <b>Snippets</b> folder, then click <b>Add a new snippet</b>.

   <ol>
<li>Name the snippet <q><i>breadcrumbs.</i></q>
<li> Click <b>Create snippet</b>:
   </ol>

<li>Copy the following Liquid code and paste it into the code editor for the `breadcrumbs.liquid` snippet:
   <ol>
<li><pre><code>{% unless template == 'index' or template == 'cart' or template == 'list-collections' %}<br/>...<br/>{% endif %}<br/><![CDATA[</nav>]]><br/>{% endunless %}</code>  </pre>
   </ol>

<li>Click <b>Save</b>
<li>Open `theme.liquid` file
<li>Paste the following code in `theme.liquid`
    <ol>
<li><pre><code> {% render 'breadcrumbs' %} </code></pre>
    </ol>
<li>Click <b>Save</b>
</ol>

Viola! Well done, You shown one does not need an app to do this, 

## CUSTOMIZATIONS

To edit the `breadcrumbs.liquid` & customize what it shows or to use different separator characters for the links.

Find ( <kbd>CTRL</kbd> + <kbd>F</kbd> ) all `&rsaquo;` text nodes that are within the `span` elements

    <span aria-hidden="true">&rsaquo;</span>

Replace it with your preferred separator characters!!

<table><tr><td><a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click <a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> to jump to the right TUTORIAL file.</td></tr></table>
