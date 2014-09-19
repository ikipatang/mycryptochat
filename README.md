# MyCryptoChat PHP v1.0.4#

MyCryptoChat is a simple PHP encrypted chat rooms manager. Everything is encrypted on the client side, so noone can spy on what you say.

## First version ##
The first version was in ASP.Net MVC. You can find it here: http://mycryptochat.codeplex.com/

## Test it! ##
You can test it here: http://chat.howtommy.net/

## Features: ##

    KISS, only 2 buttons : "create a chat room" and "send a message"
    The encryption is done by your browser, so the server doesn't know what you say
    Every chat room has an expiration time (15 minutes to ... forever!)
    Data is encrypted/decrypted in the browser using 256 bits AES
    You can change the encryption key in your browser to set your own key
    Number of online users on the chat is displayed
    Uses Vizhash to generate an avatar for each user
    You can set the chat room to self destroy if more than one person goes on it


Based on Zerobin's Javascript code http://sebsauvage.net/wiki/doku.php?id=php:zerobin
Also uses Javascript Vizhash of SamEtMax http://sametmax.com/vizhash-js-notre-implementation-libre-de-hash-visuel-utilisant-html5-canvas/

## Setup ##

    Download the zip file
    Unzip it
    Copy and paste the content on your server
    Give the read/write permissions to "db/chatrooms.sqlite" and "db/logs.txt"
    Change the seed in "inc/constants.php"
    Enjoy! :)


## Requirements ##

    PHP 5.4
    PDO for SQLite


## Changelog ##

    v1.0.4
        Now chat rooms can last forever ;)
        You can add the possibility to delete a chat room, with or without a password
        You can set an expiration time for chatrooms (default: 60 days without a message)
        The version number is now displayed are transformed in 
		(so you can press SHIFT+RETURN)
        When you click on a nickname, it adds "@nickname: " in the text field
    v1.0.3
        XSS break fix
        Better key creation in JavaScript
        Now tests run on index.php to check that everything is ok (PDO, PDO_SQLite, rights to edit files, etc.)
        Now there are logs in "db/logs.txt" if some issues appear with the database file


## Known bugs ##

    The number of visitors doesn't work


## License ##
LGPL

## Author ##
Tommy of HowTommy.net http://blog.howtommy.net<br>
Contact : http://blog.howtommy.net/?d=2010/01/01/01/01/01-me-contacter

## Source ##
https://mycryptochatphp.codeplex.com/