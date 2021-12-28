# RSS-Bridge pour YunoHost

[![Niveau d'intégration](https://dash.yunohost.org/integration/rss-bridge.svg)](https://dash.yunohost.org/appci/app/rss-bridge) ![](https://ci-apps.yunohost.org/ci/badges/rss-bridge.status.svg) ![](https://ci-apps.yunohost.org/ci/badges/rss-bridge.maintain.svg)  
[![Installer RSS-Bridge avec YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=rss-bridge)

*[Read this readme in english.](./README.md)*
*[Lire ce readme en français.](./README_fr.md)*

> *Ce package vous permet d'installer RSS-Bridge rapidement et simplement sur un serveur YunoHost.
Si vous n'avez pas YunoHost, regardez [ici](https://yunohost.org/#/install) pour savoir comment l'installer et en profiter.*

## Vue d'ensemble

RSS-Bridge is a PHP project capable of generating RSS and Atom feeds for websites that don't have one. It can be used on webservers or as a stand-alone application in CLI mode.

Important: RSS-Bridge is not a feed reader or feed aggregator, but a tool to generate feeds that are consumed by feed readers and feed aggregators. Find a list of feed aggregators on Wikipedia.

### Supported sites/pages (main)

 * `FlickrExplore` : [Latest interesting images](http://www.flickr.com/explore) from Flickr
 * `GoogleSearch` : Most recent results from Google Search
 * `GooglePlus` : Most recent posts of user timeline
 * `Twitter` : Return keyword/hashtag search or user timeline
 * `Identi.ca` : Identica user timeline (Should be compatible with other Pump.io instances)
 * `YouTube` : YouTube user channel, playlist or search
 * `Cryptome` : Returns the most recent documents from [Cryptome.org](http://cryptome.org/)
 * `DansTonChat`: Most recent quotes from [danstonchat.com](http://danstonchat.com/)
 * `DuckDuckGo`: Most recent results from [DuckDuckGo.com](https://duckduckgo.com/)
 * `Instagram`: Most recent photos from an Instagram user
 * `OpenClassrooms`: Lastest tutorials from [fr.openclassrooms.com](http://fr.openclassrooms.com/)
 * `Pinterest`: Most recent photos from user or search
 * `ScmbBridge`: Newest stories from [secouchermoinsbete.fr](http://secouchermoinsbete.fr/)
 * `Wikipedia`: highlighted articles from [Wikipedia](https://wikipedia.org/) in English, German, French or Esperanto
 * `Bandcamp` : Returns last release from [bandcamp](https://bandcamp.com/) for a tag
 * `ThePirateBay` : Returns the newest indexed torrents from [The Pirate Bay](https://thepiratebay.se/) with keywords
 * `Facebook` : Returns the latest posts on a page or profile on [Facebook](https://facebook.com/)

Plus [many other bridges](bridges/) to enable, thanks to the community

### Output format

Output format can take several forms:

 * `Atom` : ATOM Feed, for use in RSS/Feed readers
 * `Mrss` : MRSS Feed, for use in RSS/Feed readers
 * `Json` : Json, for consumption by other applications.
 * `Html` : Simple html page.
 * `Plaintext` : raw text (php object, as returned by print_r)
 

**Version incluse :** 2021.04.25~ynh1

**Démo :** https://wtf.roflcopter.fr/rss-bridge/

## Captures d'écran

![](./doc/screenshots/screenshot_rss-bridge_welcome.png)

## Avertissements / informations importantes

## Configuration

### Enabling/Disabling bridges

By default, the script creates `whitelist.txt` and adds the main bridges (see above). you can edit it:

 * to enable extra bridges (one bridge per line)
 * to disable main bridges (remove the line)
 * to enable all bridges (just one wildcard `*` as file content)

As a matter  of simplicity, this YunoHost package enables every bridge by default.

#### Multi-users support

This is application is public and there's no notion of user.

## Documentations et ressources

* Site officiel de l'app : https://github.com/RSS-Bridge/rss-bridge
* Documentation officielle de l'admin : https://github.com/RSS-Bridge/rss-bridge/wiki
* Dépôt de code officiel de l'app : https://github.com/RSS-Bridge/rss-bridge
* Documentation YunoHost pour cette app : https://yunohost.org/app_rss-bridge
* Signaler un bug : https://github.com/YunoHost-Apps/rss-bridge_ynh/issues

## Informations pour les développeurs

Merci de faire vos pull request sur la [branche testing](https://github.com/YunoHost-Apps/rss-bridge_ynh/tree/testing).

Pour essayer la branche testing, procédez comme suit.
```
sudo yunohost app install https://github.com/YunoHost-Apps/rss-bridge_ynh/tree/testing --debug
ou
sudo yunohost app upgrade rss-bridge -u https://github.com/YunoHost-Apps/rss-bridge_ynh/tree/testing --debug
```

**Plus d'infos sur le packaging d'applications :** https://yunohost.org/packaging_apps