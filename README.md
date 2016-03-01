# zerodistraction

_zerodistraction_ is a theme for [Pelican](https://github.com/getpelican).
The idea was to build a very simple theme without much distraction - just focus on the content. 

## good to know

 * the theme supports displaying image galleries, you will need the 
 gallery plugin and the 
 [patched version of thumbnailer plugin](https://github.com/eingrossfilou/pelican-plugins/tree/patch-1/thumbnailer)
    (thanks to eingrossfilou) if you want to use it without changing anything.
    You need to add the following to your pelicanconf.py:
    ```
    PLUGIN_PATH = 'plugins'
    PLUGINS = ["gallery", "thumbnailer"]
    
    #thumbnailer config
    IMAGE_PATH = "images"
    THUMBNAIL_DIR = "images"
    THUMBNAIL_KEEP_NAME = True
    THUMBNAIL_KEEP_DIR_STRUCT = True
    THUMBNAIL_SIZES = {
        'thumbnail_square': '259',
        'thumbnail_wide': '389x?',
        'thumbnail_tall': '?x250',
    }
    ```
    
 * to display the large version of the images in galleries, [Image Lightbox from Osvaldas Valutis](http://osvaldas.info/image-lightbox-responsive-touch-friendly)
 is used, please pay credit if you keep it.
 If you want another _lightbox_ you have to edit `article.html`
 * there will be _social_ links (nothing more!) for every article, icons from
 [Font Awesome by Dave Gandy](http://fontawesome.io) are used for this, please pay credit if you also use them
 
## Screenshot
![a screenshot of the theme](screenshot.jpg?raw=true)


