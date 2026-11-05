PZ MAP EDITOR - THE TILES FOLDER
================================

Everything the editor knows about tiles lives in this folder. It is kept next to the program, so it
is still here every time the editor starts, and it can be copied to another PC or backed up by
copying the folder.

There are two ways to add tiles. Use either one, or both.

  1. Use the importer.   File > Tile Tools (or Tiles > Tile Tools in the building editor).
     Files imported there are copied into this folder automatically.
  2. Copy the files in yourself, as described below.

The editor looks at this folder when it starts, whenever its window is clicked after being in the
background, and when "Check for new files" is pressed in the Tile Tools window. New files are
picked up without restarting.


THE FOLDERS
-----------

  sheets\      Tilesheets: the PNG (or WebP) pictures that hold many tiles in a grid.
  custom\      Single pictures used as one tile each.
  catalogs\    TileZed catalog text files, for the building editor.
  tiledefs\    The game's .tiles files (for example newtiledefinitions.tiles), for the lot files.
  Rules.txt    (optional) the Project Zomboid Rules.txt used for the map colours.
  Blends.txt   (optional) TileZed's Blends.txt, so the lot files blend the edges between ground types.
  Tilesets.txt Included (from the game, revision 135). Room and furniture meta data for the building editor; replace it with a newer one if needed.
  dressing.txt (optional) tile choices for clutter and decay; editable.
  library.json The editor's notes about the files (groups, tile sizes, colour choices).
  data\        More of the editor's own notes.

Do not edit library.json or the data folder by hand. If library.json is deleted nothing is lost:
the pictures are read again and the editor works out the tile sizes and groups afresh. Group names
and colour choices set in the Tile Tools window would be forgotten.


SHEETS
------

Copy tilesheet PNG or WebP files into  sheets\
  * The file name, without .png, is the sheet name. A file called  walls_exterior_01.png  gives the
    tiles  walls_exterior_01_0,  walls_exterior_01_1  and so on. The number is the position counted
    along each row from the top left, so index = row x columns + column.
  * Use the same names as the game and TileZed, so Rules.txt and the building catalogs find their tiles.
  * Names are made lower case. Letters, digits, underscores and hyphens are kept.
  * The tile size is worked out from the picture: a sheet 8 tiles wide with tiles twice as tall as
    wide. If the guess is wrong, open the Tile Tools window and set the tile width and height.
  * A sub-folder name becomes the group name for the sheets inside it. For example
    sheets\Walls\walls_exterior_01.png goes in the group "Walls". Groups only organise the list.
  * To remove a sheet, delete its file (or use Remove in the Tile Tools window).
  * To replace a sheet, copy the new file over the old one with the same name.
  * RAR archives cannot be placed here. Extract them first, or use the importer, which opens them.


CUSTOM TILES
------------

Copy single PNG or WebP pictures into  custom\
  * Each picture becomes one tile named  custom_<file name>.
  * A square picture is treated as a floor texture, a tall picture as an object, and a wide picture
    as a floor diamond. Change the kind in the Tile Tools window if that is wrong.
  * Which map colour uses a custom tile is chosen in the Tile Tools window.


CATALOGS (BUILDING EDITOR)
--------------------------

Copy TileZed's  BuildingTiles.txt,  BuildingTemplates.txt  and  BuildingFurniture.txt  into  catalogs\
They are read when the building editor starts and again whenever they change. Their tile choices
and furniture then appear in the building editor's tile pickers and in the clutter and decay dialog.


TILE DEFINITIONS AND BLENDS (LOT FILES)
---------------------------------------

Copy the game's .tiles files (in the game's media folder, for example newtiledefinitions.tiles) into  tiledefs\
and TileZed's Blends.txt into this folder. The mod export reads them when it builds the lot files.
A RAR or ZIP archive with any of these files (and Rules.txt or the catalogs) can also be added in Tile Tools:
each file is put in its folder automatically. Archives of up to 2 GB are accepted.


RULES.TXT
---------

Copy the game's Rules.txt into this folder (next to this file). It is read when the editor starts and
whenever it changes. It tells the editor which tiles each map colour places.


THE BUILD 42 TILES ARE RECOMMENDED
----------------------------------

The editor works without them and draws stand-in pictures, but with the Build 42 tilesheets in the sheets folder
(or imported in Tile Tools) the 3D view, the 3D building editor and the exported map look like the game.
The file name must match the sheet name, for example blends_natural_01.png. This only has to be done once.


THE EDITOR DOES NOT CONTAIN ANY GAME ART
----------------------------------------

This folder starts empty. Tilesheets and catalogs come from your own copy of Project Zomboid or
TileZed. Project Zomboid is a trademark of The Indie Stone Ltd.
