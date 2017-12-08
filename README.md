﻿![Logo](https://raw.github.com/strohne/Facepager/master/icons/icon_facepager.png)

Facepager was made for fetching public available data from Facebook, Twitter and other JSON-based API. 
All data is stored in a SQLite database and may be exported to csv. 

### Current status

- Please be aware of API upgrades by Facebook. API version 2.3 is no longer supported and automatically redirected to some higher version. Change the version in the base path to `v2.10` or `v2.11`
- Facebook now only provides limited fields by default. Use the `fields`-parameter (left side) to specify the data you want (right side, comma delimited). The available fields are listed in the Facebook Graph API reference, e.g. https://developers.facebook.com/docs/graph-api/reference/page/
- If you use the pre-release version 3.9: the preset handling is under construction. If your presets vanish a) make sure to install the newest version and b) rename your custom presets according to the new naming scheme. In the new naming scheme the version number is concatenated with a dot instead of an underscore.

### Installer

Installation packages for each versions are available on the [releases page](https://github.com/strohne/Facepager/releases). Database files may be incompatible between versions.

- Windows: Download and execute the latest installer from the [releases page](https://github.com/strohne/Facepager/releases).
- Mac OS X: Unzipp the file from the [releases page](https://github.com/strohne/Facepager/releases), drag & drop the App to your "Applications" folder. When a warning about the the source pop's up you should allow the installation of non-app-store applications (go to "System Preferrences>Security & Privacy" and check "Anywhere"). If you do not want to change your security settings permanently, you may open the Facepager by CTRL+Click on the icon (each time on startup).
- Linux: There is no binary release, see src/readme.txt for steps to run under linux.

### Getting started

1. Click "New Database" in the toolbar to create a blank database
2. Add Facebook IDs by clicking "Add Nodes" in the toolbar. Enter the last part of a Facebook page, e.g. enter "Tatort" for the page "http://www.facebook.com/Tatort". Alternatively you can enter "me" as reference to yourself.
3. Select the Facebook tab and set Resource to `<Object ID>`, clear all parameters. Alternatively you can set Resource to `<page>` and add a parameter which replaces `<page>` (left side) by `<Object ID>` (right side).
4. In the Facebook tab click on "Login to Facebook" and login to get a valid access token. Notice: the access token is like a password to Facebook. Since it may be printed in the status log and saved in the application settings don't give anyone untrusted access to your computer or to the status log.
5. Select one or more nodes in the view and click "Fetch data". Look at the status log (make sure "Log all requests" was enabled) to see how the URL is assembled from your settings.
6. Click "Expand nodes" in the toolbar and select one of the new child nodes. The raw data is shown to the right.
7. Change the column setup according to your needs by adding keys found in the raw data into the "Custom Table Columns" area. Don't forget to click "Apply Column Setup".
8. For further information, click the "help" button and try the default presets

### Getting help

Try the [help button](http://strohne.github.io/Facepager/) built into Facepager.

You can get help regarding specific problems in the [Facepager Usergroup on Facebook](https://www.facebook.com/groups/136224396995428/). If you want to be informed about updates please follow the [Facebook Page](https://www.facebook.com/groups/136224396995428/).


### Citation

[Jünger, Jakob](https://ipk.uni-greifswald.de/kommunikationswissenschaft/dr-jakob-juenger/) / [Keyling, Till](http://tillkeyling.com/) (2017). Facepager. An application for generic data retrieval through APIs. Source code and releases available at https://github.com/strohne/Facepager/.

### Licence


MIT License

Copyright (c) 2017 Jakob Jünger and Till Keyling

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

