# Flickr Photosets Browser

A simple web app for showing photosets from a Flickr user chronologically.

## Usage

1. Get Flickr API key for your application from http://www.flickr.com/services/apps/create/apply/
2. Get your Flickr user ID by using e.g. http://idgettr.com/
3. Paste the contents of this app to your web app folder
4. Add the following snippet to your html.
    <script type="text/javascript">
      flickrphotosets.api_key = "your_flickr_api_key";
      flickrphotosets.user_id = "target_user_id";
    
      jQuery(function() {
        flickrphotosets.init('#flickrphotos');
      });
    </script>
5. Add `<div id="flickrphotos"></div>` to your html

### Widget

This app also provides a simple widget for showing most recent photosets. It 
is suitable for narrower spaces such as sidebar. To use it, replace the snippet 
in step 4 with
    <script type="text/javascript">
      flickrphotosets.api_key = "your_flickr_api_key";
      flickrphotosets.user_id = "target_user_id";
      flickrphotosets.link_url = "link_to_your_proper_gallery_page";

      jQuery(function() {
        flickrphotosets.initWidget('#flickrphotos');
      });
    </script>

### Wordpress plugin

For historical reasons, this repository also includes a Wordpress plugin. To 
use it, paste the directory to wp-content/plugins and edit plugin settings in
Wordpress settings -> Flickr photosets

### Depedencies

* jQuery (tested with 1.7.1)
* jQuery scrollTo (1.4.2, http://flesler.blogspot.com/2007/10/jqueryscrollto.html)
* jQuery hashchange (1.3, http://benalman.com/projects/jquery-hashchange-plugin/)
* Fancybox (1.3.4, http://fancybox.net/)
    * jQuery easing (1.3)
    * jQuery mousewheel (3.0.4)

All these are bundled with the app.
 