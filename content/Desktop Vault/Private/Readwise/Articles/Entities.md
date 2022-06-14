# Entities

![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article0.00998d930354.png)

## Metadata
- Author: [[Base Classes]]
- Full Title: Entities
- Category: #articles
- URL: https://qodotplugin.github.io/docs/entities.html#updating-your-fgd

## Highlights
- There are three main types of entities:
  Point Classes
  Solid Classes
  Base Classes
  A point entity is a position in 3D space. They work well for spawn locations, pickups, and instancing Godot scenes.
  Solid classes are pieces of geometry with special properties, like doors and breakable walls. You can use these entities to tie scripts and other functionality to brushes in the world. Collision and meshes are optional as well.
  Base classes are empty; they only contain properties as a template for other classes. They’re handy when needed, but never required.
  Keep in mind that “Entities” and “Classes” mean the same thing for this entire page. Qodot calls them classes, Trenchbroom calls them entities. Neither of these systems inherently interact with the classes found in GDscript or C#, they are completely separate.
- Creating an FGD file
  This should be your first step before adding any entities for a brand new Godot project.
  FGD fles (Forge Game Data) hold definitions for entities. They are required to make Trenchbroom and QodotMap understand custom entities.
  While you can piggyback off of Qodot.fgd included in all installations of Qodot, this puts your custom entities at risk if you choose to update Qodot, since Qodot.fgd will be overwritten with the defaults.
  It is safer to create a unique FGD file for your game that goes with the custom Trenchbroom game config created earlier in the Applying Textures guide.
  Right-click on the Filesystem dock and click Create New Resource. Make a QodotFGDFile:
  I recommend saving this file as your_game_name_fgd.tres so it’s easy to search for “fgd” or just your game’s name the Filesystem dock. Mine is practice_fgd.tres.
  Change the Fgd Name to your game’s name.
  Note
  You have to set the Fgd Name so it doesn’t conflict with the “Qodot” namespace, otherwise Trenchbroom will discard your FGD.
  FGDs by default contain example entity definitions, which we don’t need as Qodot.fgd contains all of these already. It helps to start an FGD with a completely clean entity definitions array, so you can focus on adding new entities not covered by Qodot.fgd.
- Adding an Entity Definition to an FGD
  With your FGD open, click on the Entity Definitions array to open it. Drop your new entity definition into any empty slot in the list.
  We still need to update the Trenchbroom game config to include our new entity definitions. Later we’ll make sure the QodotMap node catches wind of the new entity definitions.
- Adding required Entity Definitions to your FGD
  Before trying to consider your FGD complete, you may want to include worldspawn layer and group functionality in your FGD. These are kept as classes in Qodot.fgd, and are recommended to copy-over into all custom FGDs.
  These entities are:
  worldspawn_solid
  worldspawn_base
  group_solid
  You can expect them to work out of the box and not require changing, so they can be left in the /addons/qodot folder and updated as needed.
