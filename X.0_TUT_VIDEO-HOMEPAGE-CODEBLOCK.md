<a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click here to jump to the right TUTORIAL file.

# VIDEO ON HOMEPAGE
TUTORIAL x.0 `Video On Homepage`

In this tutorial, we're going to teach you how to add a background video section to your Shopify store.

Go ahead, try out the steps outlined below or if it's too much for you, freely email eaidter@gmail.com to hire us at minimal cost.

### REMINDER / TIPS</b>

   - [Duplicate](https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes) your theme first to keep it as a back-up before trying this advanced coding
   - Keyboard shortcut to find specific text line: Place cursor on the code editor screen and hold `CTRL + F`


## ADD CODINGS
<ol>
<li>From your Shopify backend, go to <b>Online Store</b> &gt; Themes.
<li>Find the theme you want to edit, and then click <b>Actions</b> &gt; <b>Edit code</b>.
<li>Scroll down to <b>Sections</b> directory and click <b><i>add a new section</i></b>
<li>Name your section e.g video-background
<li>Replace with the following code
	<ul>
	<li> <pre> <code>{%- if section.blocks.size > 0 -%}<br/>{%- for block in section.blocks -%}<br/>...<br/>{% endschema %} </code> </pre> <ul>
<li> Click on <b>Save</b>
<li> Go to <b>Settings</b> and click on files
<li> Upload the video you want as background
<li> Copy video url
<li>  Go to <b>Online Store</b> and next to the theme you just edited <b>Click</b> on customize
<li>  On the left, <b>Click</b> on <b>Add section</b> and choose video-background
<li> Paste the video url
<li> Click on <b>Save</b>
</ol>

## CUSTOMIZATION

In the `____-__-___-___` file, locate and make adjustment accordingly.

For the position of your button relative to the bottom of the browser, edit the position_from_bottom value:

    {%- assign img_url = block.settings.image | img_url: '1x1' | replace: '_1x1.', '_{width}x.' -%}    

To change how far a customer needs to scroll down to trigger the button appearance, edit the vertical_offset_for_trigger value:

    {% assign vertical_offset_for_trigger = 300 %}
    
The color scheme and sizing can be adjusted under the `<style>` tag to fit your theme. Locate them and change accordingly.

Next, click <b>Save</b>.

<a href="https://github.com/e-AIDter/Self-AID_Shopify/find/main"> Go to file </a> :point_left::point_left::point_left: Feeling a little lost navigating a code repositry? Click here to jump to the right TUTORIAL file.
