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
        'thumbnail_rectangle' : '295x200',
        'thumbnail_minisquare': '50x50',
    }
    ```
    
 * to display the large version of the images in galleries, [Image Lightbox from Osvaldas Valutis](http://osvaldas.info/image-lightbox-responsive-touch-friendly)
 is used, please pay credit if you keep it.
 If you want another _lightbox_ you have to edit `article.html`
 * there will be _social_ links (just links!) for every article, icons from
 [Font Awesome by Dave Gandy](http://fontawesome.io) are used for this, please pay credit if you also use them. If you dont want to use them, just add `NO_SOCIAL_BUTTONS = True` to your `pelicanconf.py`
 * if necessary you can show some copyright hints at the bottom of the page by including a `copyright` metadata-field in your article file.
 * you can show a small round preview image (avatar) in front of each article link by adding `SHOW_TEASER_IMAGES = True` to your `pelicanconf.py`. The `thumbnail_minisquare` thumbnails of the first image of the gallery will be used for this, so this option makes sense if you regularly use galleries.
 * if you regularly use galleries you can also enable the optional thumbs-index-mode by setting `INDEX_USE_THUMBS = True` in your `pelicanconf.py` - again the first image of the gallery will be used
 
## Screenshots
### Article
![a screenshot of the theme](screenshot_new.jpg?raw=true)

### Article list, default
![a screenshot of the theme](screenshot_list_default.jpg?raw=true)

### Article list, Avatars
![a screenshot of the theme](screenshot_list_avatars.jpg?raw=true)

### Article list, Thumb View
![a screenshot of the theme](screenshot_index_thumbs.jpg?raw=true)
