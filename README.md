# zips

This repository contains the release zips for ResolveURL.<br>
Include this directory with your repo to always have the latest updates from ResolveURL release repository

```xml
<dir>
    <info compressed="false">https://raw.githubusercontent.com/zoreu/script.module.resolveurl/repo/addons.xml</info>
    <checksum>https://raw.githubusercontent.com/zoreu/script.module.resolveurl/repo/addons.xml.md5</checksum>
    <datadir zip="true">https://raw.githubusercontent.com/zoreu/script.module.resolveurl/repo/zips/</datadir>
</dir>
```

I am in no way responsible for the urls being resolved by 3rd parties. This script only resolves video content from legitimate file lockers without prejudice. If this script is being used by 3rd parties to resolve content that you feel infringes upon your Intellectual Property then please take your complaints to the actual website or developer linking to such content and not me. This script in no way searches the web for any content whatsoever.

## script.module.resolveurl

Include the script in your addon.xml

```xml
<requires>
    <import addon="script.module.resolveurl" version="5.1.0"/>
</requires>
```

Import ResolveUrl and use it

```xml
import resolveurl
if resolveurl.HostedMediaFile(url):
    resolved = resolveurl.resolve(url)
```

## script.module.resolveurl.xxx

Adult Resolver Extension for ResolveURL

Include both the scripts in your addon.xml

```xml
<requires>
    <import addon="script.module.resolveurl" version="5.1.0"/>
    <import addon="script.module.resolveurl.xxx" version="2.1.0"/>
</requires>
```

Call the resolveurl from your addon to resolve the XXX hosts.

```python
import resolveurl
import xbmcvfs
xxx_plugins_path = 'special://home/addons/script.module.resolveurl.xxx/resources/plugins/'
if xbmcvfs.exists(xxx_plugins_path):
    resolveurl.add_plugin_dirs(xbmcvfs.translatePath(xxx_plugins_path))

if resolveurl.HostedMediaFile(url):
    resolved = resolveurl.resolve(url)
```








