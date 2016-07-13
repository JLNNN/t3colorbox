.. include:: Images.txt

.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. ==================================================
.. DEFINE SOME TEXTROLES
.. --------------------------------------------------
.. role::   underline
.. role::   typoscript(code)
.. role::   ts(typoscript)
   :class:  typoscript
.. role::   php(code)


Constants / Reference
^^^^^^^^^^^^^^^^^^^^^

|img-9|  *Constants Editor*
plugin.t3colorbox

.. ### BEGIN~OF~TABLE ###

.. container:: table-row

   Property
         includejquerycore
   
   Data type
         boolean
   
   Description
         Add jQuery core script.
   
   Default
         0


.. container:: table-row

   Property
         theme
   
   Data type
         options[1,2,3,4,5,6]
   
   Description
         Sets the theme (style) for the colorbox. 1=theme1 (2=theme2 … 6 = theme6)
         
         See the Screenshot section.
   
   Default
         1


.. container:: table-row

   Property
         themepath
   
   Data type
         string
   
   Description
         Path/file for custom CSS
		 If set, this style (CSS file) will be used. Put something like
         "fileadmin/layout/colorbox/mystyle.css" in here.
         
         The value above (plugin.t3colorbox.style) is deactivated.
         To reactivate the built-in styles you have to delete this constant!
   
   Default


.. container:: table-row

   Property
         slideshow
   
   Data type
         boolean
   
   Description
         Image groups are presented in an autoscrolling slideshow.
         
         If this value is empty, the standard value from the colorbox script (0) is taken.
   
   Default
	


.. container:: table-row

   Property
         slideshowAuto
   
   Data type
         options[true,false]
   
   Description
         Start the slideshow automatically.
		 "Enable slideshow" must be on of course...
		 Set to false to turn off the automatic slideshowstart.
   
   Default
         false


.. container:: table-row

   Property
         slideshowSpeed
   
   Data type
         integer
   
   Description
         Sets the speed of the slideshow:in milliseconds
		 If this value is empty, the standard value from the colorbox script (2500) is taken.
   
   Default


.. container:: table-row

   Property
         imagegroup
   
   Data type
         options[1,2,3]
   
   Description
         Define the use of imagegroups:
		 1 = group per page: cycle through all lightbox-images on the page
		 2 = group per contentelement: cycle through all lightbox-images within a content element
		 3 = single image: every lightbox image opens in a separate lightbox windows (no back/forward)
   
   Default
		 1


.. container:: table-row

   Property
         maxWidth
   
   Data type
         string
   
   Description
         Set a maximum width for loaded content. px or %
   
   Default
         95%


.. container:: table-row

   Property
         maxHeight
   
   Data type
         string
   
   Description
         Set a maximum height for loaded content. px or %
   
   Default
         95%


.. container:: table-row

   Property
         cboxcommand
   
   Data type
         string

   Description
         Reference at http://www.jacklmoore.com/colorbox Settings.
         
         If you add more than one value don't forget the dash:
         
         ::

            opacity:0.45,slideshowSpeed:1000,

			
.. container:: table-row

   Property
         cboxversion
   
   Data type
         options
   
   Description
         Sets the version of the colorbox
   
   Default
         latest


.. ###### END~OF~TABLE ######

All other possible colorbox options (there are a lot!) can be set through the cboxcommand string.
Reference at http://www.jacklmoore.com/colorbox

