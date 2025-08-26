# OWB Entity and Model Structure Guide
This is a quick guide incase anyone has to debug this area of the mod and/or decides to help me with them

##Entities
The entities are set up in a three level hierarchy in order to allow the fastest addition of new unique assets and expanded equipment
### ``owb_base_entity``

This is defined by an entity base, a weapon, and if applicable a vehicle and a frame. Special infantry clones the base infantry and changes relevent pieces of it (for example spec ops and mutants)

Also within this file is references to animation id's defined in the .gfx file of each archetype of unit. These states should not be changed, unless adding a new equipment archetype unit (such as tank/new robot/fireteams)

### ``graphical_cultures``
These directly clone the relevent entities in ``owb_base_entity`` and simply switches the pdxmesh. Sometimes attachments must be switched, which may create more entities. All of these still have relevent clones in the ``owb_base_entity`` file.

Culture are assign in the ``mod/common/graphical_cultures.txt``. These cultures are then assigned to countries in the common/countries files.

### ``retexutre_xxx``
These also clone from the ``owb_base_entity`` file and are for SPECIFIC retextures. They follow the same format as the above

## PDX Mesh Files
