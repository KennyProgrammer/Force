# AssetManager imporvments

 - Add new section of Asset Manager is relationship between relative and full paths, reason it because i
already build application to final excecutable and because path was fullpath it breaks game when 
its game folder moves to another directory, so i decided to resctructured the Asset System.
- Now all function like GetAssetBy_ returns refs to actuall asset that stores in GAssets, and if not return globally stack allocated InvalidAsset.
This returning by ref fix bugs with replacing data into GAssets if data not current.
- Now assets can be imported to already existing GAssets.
- RemoveAsset now support removing only .ext file & local ref in GAssets and not touch the physical file.
- Fix _RemoveLinkedAssets that not remove .ext file removes only from GAssets.
- Fix bug with IterateOver function, if directory not exist we skip the iteration.
- Update _UpdateLinkedAssetsRelativePath to support copying.
- Fix _RenameLinkedAssets to support actuall properly renaming.
- Finally fix asset system! A think:)

This hole stuff also affect on ProjectBrowser that also little rectructured with moving items.


# ProjectBrowser remove hole buch stuff from
 - Rename MoveAssetToDirectory to MoveAsset, and MoveAssetToDirectory1 to MoveAssetItem, and MoveAssetFolderToDirectory1 to MoveAssetFolder.
 - Remove BrowserItemType, fully replaced by AssetType.
 - SubItem renamed to HierarchyNodeRecursive.
 - Fixed bug to not allow go back on SubBarPanel if directory tree has identical folders.
 - Rewrite behaviour of DrawThumbnail.
 - Create OpenAsset function and rename OpenItem/Directory to OpenAssetItem and OpenAssetFolder.
 - Group the asset manipulation code.
 - Rewrite Drag & Drop Files/Folder API.
 - MoveAsset, with behaviours for file (MoveAssetItem) and folder (MoveAssetFolder) is updated to relative path and using FileSystem::CopyFile/CopyFolder
 - Fix PasteAsset + with additional checks and changes few small thing.
 - Fixed start dragging. Add delta to resolution of 5 px to start drag.
 - Remove strange possibleCopy variable that was do nothing.
 - Remove unused selectedThumbnailInFrame variable.
 - Add new folder icon.
 - Fix bug that max scrolled area with button + image, but not include text.
 - Rename DrawThumbnailWithInputText to DrawThumbnailEdit.
 - Remove AssetCreationData and AssetModificationState_NewAsset.
 - Rewrite behavior of DrawThumbnailEdit, now edit state have two state Create and Rename.
 - In future fix bug with is we copy from selectedDirectory to copyDirectory where selectedDirectory == copyDirectory.   
 #New
 - Assets Importing state now have its own progress dialog. + 
 - Assets Importing starts now only if user focused on main window. +
 - Replace AssetModificationState by AssetImportType, AssetChangeType, AssetChangeGType, AssetChangeState. + 
 - FileWatcher now change Assets directory and all its files and sub-directories. +
 - Import Assets if they was modifyed outside Force. (Working...)
 - Import Asset or Assets if they was modified inside Force. (Created, Renamed, Removed, Moved) -
 - Import Asset or Assets using Drag Drop. -
   
# Tests
   
## Deletion:

Delete single folder:              +
Delete single file:                +
Delete folder with content:
  - Folder with Folder:            +
  - Folder with File:              +
  - Folder with Files and Folders: +

## Moving

Move forward single file:                     +
Move forward single folder:                   +
Move backward single file:                    +
Move backward single folder:                  +
Move forward folder with file:                +
Move backward folder with file:               +
Move forward folder with folder:              ++++- (Works but when select one of nested folders after moving it copy asset in GAssets.) 
                                                  Now its working what the hell? Im not fix anything :( 
                                                  Now when folder with 2 folders and more (duplicated ID when saving) (Fixed)
Move backward folder with folder:             +
Move backward folder with folders and files:  +
Move forward folder with folders and files:   +

## Copying / Pasting

Copy forward single folder:                   +
Copy backward single folder:                  +
Copy forward single file:                     + 
Copy backward single file:                    +
Copy forward folder with folder:              +
Copy backward folder with folder:             +
Copy forward folder with file:                +
Copy backward folder with file:               +
Copy backward folder with folders and files:  +
Copy forward folder with folders and files:   +

# Renaming

Rename single file:                   +
Rename single folder:                 +
Rename folder with files and folders: +
