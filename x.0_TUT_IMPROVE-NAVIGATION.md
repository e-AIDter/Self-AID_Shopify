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


## ABLE THROUGH FREEMIUM THEME SETTINGS?

<!-- meta name="generator" content="LibreOffice 7.0.4.2 (GNU/Linux)"> -->
<table cellspacing="0" border="0"> <colgroup width="109"></colgroup> <colgroup width="29"></colgroup> <colgroup width="28"></colgroup> <colgroup width="31"></colgroup> <colgroup width="28" span="3"></colgroup> <colgroup width="29"></colgroup> <colgroup width="27"></colgroup> <tbody><tr> <td height="174" align="center"><br></td> <td align="center">L<br>I<br>G<br>H<br>T</td> <td align="center">S<br>U<br>p<br>p<br>l<br>y</td> <td align="center">M<br>I<br>n<br>i<br>m<br>a<br>l</td> <td align="center">D<br>A<br>w<br>n</td> <td align="center">D<br>E<br>b<br>u<br>t</td> <td align="center">N<br>A<br>r<br>r<br>a<br>t<br>i<br>v<br>e</td> <td align="center">B<br>O<br>u<br>n<br>d<br>l<br>e<br>s<br>s</td> <td align="center">V<br>E<br>n<br>t<br>u<br>r<br>e</td> </tr> <tr> <td height="41" align="left">breadcrumbs<br>Settings?</td> <td align="center">:heavy_check_mark:</td> <td align="center">:heavy_check_mark:</td> <td align="center">:heavy_check_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> <td align="center">:negative_squared_cross_mark:</td> </tr> </tbody></table>

<table><tr><td><a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click <a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> to jump to the right TUTORIAL file.</td></tr></table>
