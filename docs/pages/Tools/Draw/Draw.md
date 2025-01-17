---
layout: page
title: Draw
permalink: /tools/draw
parent: Tools
---

# Draw

The Draw tool is an advanced vector data creation and editing tool supporting a multi-user environment. Users can create and manage their own files which can have points, lines, and polygons as well as arrows and text to support annotation. Files can be viewed between users and features copied from one file to another.

## Tool Configuration

There are five files that are group editable with the correct permission. The group authentication is set an environment variable in the .env file during startup. These files are meant as collaborative layers that a only a few people will manage and contribute to do to the potential of race conditions on who did the last edit.

### Example Tool Tab Variables

```javascript
{
    "intents": [
        "Polygon_1_Alias",
        "Polygon_2_Alias",
        "Polygon_3_Alias",
        "Line_Alias",
        "Point_Alias"
    ],
    "preferredTags": [
        "campaign1",
        "campaign2",
        "science1",
        "science2",
        "plan1",
        "plan2",
        "done"
    ],
    "hoverLengthOnLines": false
    "leadsCanEditFileInfo": false
}
```

_"intents"_: The names in quotes will be the group file names.  
_"preferredTags"_: Users can attach tags or keyword to files to organize them. Preferred Tags are curated tags and promoted over user generated ones.  
_"hoverLengthOnLines"_: If true, the hover text for line features will include the total length of the line in meters.
_"leadsCanEditFileInfo"_: If true, lead roles can edit the file info, (name, description, tags, folder, make private) of any user's public file.

## Tool Use

The Draw Tool has three panels: one for making files and controlling the intial feature creation, another for editing features and their properties, and lastly a panel for controlling the edit history. You can navigate between the panels by clicking on the icons at the top: Pencil icon (default) for panel 1, Shapes icon for panel 2, and Clock icon for panel 3.

### Panels

![](/MMGIS/assets/images/draw_panels.jpg)

#### Panel 1

This panel creates files, manages them, and is where you initially make features.

- To create a file, type in a new file name where it says "New File" at the top. The feature type defaults to "Map", which can hold all the different vector types (point, line, polygon) and annotations (arrows and text). Left-click the '+' sign or hit return in the 'New File' area to create the file. It will appear below the 'Lead Maps' Other

#### Panel 2

The shapes panel shows all the currently drawn features is a list. It serves as a quick way to view, select (and group select with CTRL and SHIFT) and navigate to the cooresponding features on the map. The bottom section allows users to copy selected features to other files.

#### Panel 3

The history panel shows a complete history of the current working file. Every drawing action can be undone here.
