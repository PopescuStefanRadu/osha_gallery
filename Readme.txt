Osha Gallery
============

Features
--------
- Reorder images from the node view page
- Bulk upload for image fields with unlimited number of values from the node view page
- Adds two tabs ("Reorder images", "Bulk Upload") for the above features


Dependencies
------------
- Colorbox
    - Libraries
- Field formatter settings
- Gallery formatter
- Image
- Manual crop
- Plupload integration
- Entity

Installation
------------
Install and enable all modules in the dependency list. Enable Osha Gallery module.

Download the latest 1.x version of Plupload ( currently 1.5.8 ) from
http://www.plupload.com/download/ and extract the contents of the folder into
sites/all/libraries so that there's a sites/all/libraries/plupload/js/plupload.full.js
file. Remove the examples folder from sites/all/libraries/plupload/.


Configuration
-------------

In modules administration page (admin/modules) you can choose which fields this module
should affect by clicking on the "Configure" link from the Osha gallery module.

Make sure the image fields you want this module to affect have Number of values set to
"Unlimited".

