---
layout: post
title: Displaying ArcGIS feature services in QGIS on Mac
date: 2017-07-11 08:56
categories: qgis arcgis mac
description: If you use macOS and QGIS, then you know you have to go to kyngchaos.com and download the necessary dependency framework (GDAL complete). You may also know that there are some things that behave differently in the mac version of Q versus Linux, Windows, etc.
---

If you use macOS and QGIS, then you know you have to go to kyngchaos.com and download the necessary dependency framework (GDAL complete). You may also know that there are some things that behave differently in the mac version of Q versus Linux, Windows, etc.

One of these differences is the lack of a native Add ArcGisFeatureServer Layer from a Server option, which is present on Windows and Linux operating systems. Strange right...? Here are some steps to get around this frustrating lack of functionality.

### Enable experimental plugins within the QGIS plugin repository
By default, experimental plugins are disabled in QGIS.
1. Open QGIS
2. Navigate to Plugins - Manage and Install PLugins
3. Go to Settings on the left hand side
4. Check the second box "Show also experimental plugins"

### Search for the ArcGIS REST API Connector plugins
1. Select the 'All' option on the left hand side at the top within the Plugins dialogue
2. Type 'arcgis' in the Search bar
3. Select the ArcGIS REST API Connector plugin
4. Install Plugin
