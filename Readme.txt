Osha Gallery
============

Features
--------
- Reorder images from the node view page
- Bulk upload for image fields with unlimited number of values from the node view page
- Adds two tabs ("Reorder images", "Bulk Upload") for the above features
- Creates a cover image display field from your images which opens on click the gallery in a colorbox


Dependencies
------------
- Colorbox
    - Libraries 2.x module
- Field formatter settings
- Gallery formatter
- Image
- Manual crop
- Plupload integration
- Entity

Installation
============

Download all modules in the dependency list. Download Osha Gallery module.

Bulk upload:
---------------
Download the latest 1.x version of Plupload ( currently 1.5.8 ) from
http://www.plupload.com/download/ and extract the contents of the folder into
sites/all/libraries so that there's a sites/all/libraries/plupload/js/plupload.full.js
file. Remove the examples folder from sites/all/libraries/plupload/.

Enable plupload module.

Manual Crop:
---------------
Download and install Libraries 2.x module.

The two javascript libraries required by this module can be found at:
- http://odyniec.net/projects/imgareaselect/jquery.imgareaselect-0.9.10.zip
- https://github.com/desandro/imagesloaded/archive/v2.1.2.tar.gz

Next download and extract the imagesLoaded plugin, rename the extracted folder to
"jquery.imagesloaded" and place it under "sites/all/libraries". The plugin should
now be located at "sites/all/libraries/jquery.imagesloaded/jquery.imagesloaded.min.js".

Please note that the 3.x version can also be used, but it depends on jQuery 1.5
which can only be obtained by installing the jQuery Update module.

Now download and extract the imgAreaSelect plugin, rename extracted folder to
"jquery.imgareaselect" and copy it into "sites/all/libraries". The plugin should
now be located at "sites/all/libraries/jquery.imgareaselect/scripts/jquery.imgareaselect.min.js".

Enable Manual Crop module.
Read configuration.



Configuration
=============

General:
-------

In modules administration page (admin/modules) you can choose which fields this module
should affect by clicking on the "Configure" link from the Osha gallery module.

Make sure the image fields you want this module to affect have Number of values set to
"Unlimited".

Manual Crop:
-----------
You need to configure your image styles before you
can start cropping. Go to Administration » Configuration » Media » Image styles
and click on the "edit" link for the styles that need a Manual Crop effect.

Add and configure one of the Manual Crop effects, you'll notice that the Manual
Crop effect will always become the first effect in the list. This is because
cropping should always be done first, otherwise the result will be unpredictable.

Next go to Administration » Structure » Content types and click on the "manage fields"
link (the Field UI module should be activated) for the content type that should
allow cropping. Now click on the "edit" link of the image field, so you can enable
and configure Manual Crop (open the "Manual Crop" fieldset) for the current field.

After saving the settings you should return to the content type overview and click
on "manage display" so you can set the (cropped) image style that should be used.

Manual Crop adds a "?c=md5_hash" query string parameter to the image url so the
at client-side cached image gets refreshed whenever the crop selection changes.
To prevent an SEO impact, this can be disabled by unchecking the
"Reload cache-control" setting at admin/config/media/manualcrop.



