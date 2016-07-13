

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


Advanced Configuration
----------------------

All possible colorbox options
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
can be set through the *cboxcommand* string in your template in the constants section.
Reference at `http://www.jacklmoore.com/colorbox <http://www.jacklmoore.com/colorbox>`_ chapter Settings.

Example for disabling the ability to loop back to the beginning of the group when on the last element
and disabling the left and right arrow keys for navigating between the items in a group.

::

   plugin.t3colorbox.cboxcommand = loop:false,arrowKey:false,



Important: Options with text value need quotation marks.

::

   plugin.t3colorbox.cboxcommand = transition:"fade",


   
   
Using your own labels
^^^^^^^^^^^^^^^^^^^^^

T3Colorbox comes with some translations: de, fr, es, it, nl, dk, cs, pl, ru, pt-BR

If you need a different language or another expression you can set the following values through the cboxcommand string (constants):

================    =====================================================     ======================================
Property            Standard value / text (en)                                Example syntax (de)
================    =====================================================     ======================================
current:            "image {current} of {total}"                              Current:"Foto {current} von {total}",
                    {current} is replaced by the actual image number
                    {total} is replaced by the number of pictures
previous:           "previous"                                                previous:"zurück",
next:               "next"                                                    next:"weiter",
close:              "close"                                                   close:"schließen",
slideshowStart:     "Start Slideshow"                                         slideshowStart:"Slideshow starten",
slideshowStop:      "Stop Slideshow"                                          slideshowStop:"Slideshow stoppen",
================    =====================================================     ======================================


So you have to put something like:

::

   plugin.t3colorbox.cboxcommand = close:"mach's zu",

in your template to change the text of the close command.

*Note: Not all labels are used in every style.*


