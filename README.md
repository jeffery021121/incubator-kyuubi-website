<!---
  Licensed under the Apache License, Version 2.0 (the "License");
  you may not use this file except in compliance with the License.
  You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

  Unless required by applicable law or agreed to in writing, software
  distributed under the License is distributed on an "AS IS" BASIS,
  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  See the License for the specific language governing permissions and
  limitations under the License. See accompanying LICENSE file.
-->

# Apache Kyuubi site

## Usage

The site is generated with [Hugo](https://gohugo.io/).

To generate a site you need only one binary. Follow the install guide from the hugo site. (Typically all the package managers
contain dedicated package, but as the hugo is written in go it's also possible to download the single binary from the release page).

After the installation you can generate the site with:

`hugo`

And the site will be generated to the `content` sub directory.

This repository contains both the source and the rendered version of the site.
__Always execute a `hugo` before the commit, to refresh the content folder.__

To improve/develop the site, you can use

```
hugo server
```

which starts a standalone auto-refreshed web server.

## Content

### Release/news
To create a new release, create a file in  ```src/release``` directory. The file name should be ```<version>.md```where version is the release version.

Example: src/release/1.2.0.md

```
---
title: release *** available
date: 2021-XX-XX
linked: true
---
For more information check ...
```

`linked: true` attribute means, that it will be displayed on the release page and under the documentation menu. 
Please remove it from the previous release.

To creat news, create a file in ```src/news``` directory with the similar way. 

Note: date is used to sort the releases when the latests are displayed in the site.

### Update Docs
The docs are hosted on readthedocs.
