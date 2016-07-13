

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


FAQ
---


Clickenlarge Images in RTE
^^^^^^^^^^^^^^^^^^^^^^^^^^

If you want to use the colorbox for images in the TYPO3 RTE (rich text
editor), do the following.

#. Go to the extension manager and click on the extension “htmlArea RTE”
   and there check “Enable images in the RTE[enableImages]”. After that
   click on “Update”.

#. Include the static template “Clickenlarge Rendering (rtehtmlarea) “.

#. Insert the image in RTE and set on “Click-enlarge” option.

There is no need for an extension like the RTE Lightbox (ext key:
rtelightbox).


tx\_news
^^^^^^^^

Integration in the tx\_news extension for the single view can be done
by editing the fluid-templates “MediaImage.html”. (As always copy the corresponding template to a local folder in fileadmin)

Edit the template “Partials\Detail\MediaImage.html” an add to the
a-tag: class="t3colorbox" data-rel="news-single"

::

   <div class="mediaelement mediaelement-image">
    <f:if condition="{settings.detail.media.image.lightbox}">
     <f:then>
      <a class="t3colorbox" data-rel="news-single" title="{mediaElement.caption}" href="{f:uri.image(src:'uploads/tx_news/{mediaElement.content}' maxWidth:'800')}">
       <f:image src="uploads/tx_news/{mediaElement.content}" title="{mediaElement.title}" alt="{mediaElement.alt}" maxWidth="{settings.detail.media.image.maxWidth}" />
      </a>
     </f:then>
     <f:else>
      <f:image src="uploads/tx_news/{mediaElement.content}" title="{mediaElement.title}" alt="{mediaElement.alt}" maxWidth="{settings.detail.media.image.maxWidth}" />
     </f:else>
    </f:if>
   </div>

tt\_news
^^^^^^^^

Integration in the tt\_news extension for single and list view can be done by Typoscript.


Single View
"""""""""""

::

   plugin.tt_news.displaySingle.image.imageLinkWrap {
    JSwindow = 0
    directImageLink = 1
    linkParams.ATagParams.dataWrap = class="t3colorbox" data-rel="cbox{field:uid}"
    width = {$styles.content.imgtext.linkWrap.width}
    height = {$styles.content.imgtext.linkWrap.height}
   }


List view
"""""""""

::

   plugin.tt_news.displayList.image.imageLinkWrap {
    enable = 1
    JSwindow = 0
    directImageLink = 1
    linkParams.ATagParams.dataWrap = class="t3colorbox" data-rel="cbox{field:uid}"
    width = {$styles.content.imgtext.linkWrap.width}
    height = {$styles.content.imgtext.linkWrap.height}
   }

Other extensions
^^^^^^^^^^^^^^^^

Integration in any other extension is quite easy: just add somehow (typoscript or template) 
class="t3colorbox" data-rel="cbox{sometext}"
to your image links