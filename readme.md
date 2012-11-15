Cat error pages for Nginx
=========================


Was bored, made this see notes.


Installation
----------

###1st method


Easiest way is to put ```error/``` folder into your webserver root dir add f.e. ```error_page 404 =/404.html;``` to config, restart and it should work.

###2nd method


If you want to server error pages from different dir you need to add this to your config: (there's probably better way to do this but I'm too lazy to check).

```
   error_page 404 /404.html;

   location = /404.html; {
   root /your/path/to/file/dir;
   }
   location = /koty.css; { 
   root /your/path/to/file/dir; 
   }
   location = /koty/404.jpg; {
   root /your/path/to/file/dir;
   }
```

I didn't like this method so I just created new vhost to serve css/imgs, edited htmls with links to vhost - you can see it in action here [error 404](http://img.nekomimi.pl/404) and [error 401](http://img.nekomimi.pl/test) (just click cancel when prompted for pass)

Notes
-----

All cats images are taken from [here](https://secure.flickr.com/photos/girliemac/sets/72157628409467125/) and are licensed under the [CC Attribution license](https://creativecommons.org/licenses/by/2.0/deed.en).