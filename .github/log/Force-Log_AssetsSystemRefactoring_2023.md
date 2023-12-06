# AssetManager imporvments

- Linked Assets system will be removed, because it always cause troubles, and handle linked assets in one folder-asset it really bad, because sometimes can be removed, or reassigned, or
copying and pasting, cutted and pasted in another directory, or assets can even be reimported because user change it outside Force aswell. All that kinda stuff not garantie
that actual assets UID will be the same, or that UID's that was initially stay that same. Other reason for that - folders don't need to know about linked assets at all because
in other words we can find that folders once and say for example some it in some kinda list for Assets Preview to preview, or find that group of assets from Assets as actual
instnaces to play around. +

- Remove relative paths from asset .ext file. Why? +
 1. Assets extension file not need to store relative path in .ext file because we easly
 can get full path of asset by UID (get UID -> find .ext file -> cut the rest path and let only Assets/...)
 2. Because when asset will be packed, all asset data will in there, so in this case with not playing with
 paths at all, its all about data only.
 
- Remove UpdateAssetFolderDesc, UpdateAssetFolderDesc, UpdateAssetFolderLinkedAssetsRelativePath,
RemoveLinkedAssets, UpdateLinkedAssetsRelativePath, RenameLinkedAssets and replace all this shitty
stuff with new MoveAsset() API. This function handle three main actions: Copying, Moving, and Renaming.

- Remove AssetImportFlags_UpdateDescParentFolder = 1 << 0 // Updates the parent folder description (i.e add imported asset to parent folder .ext) becase LinkedAssets API
was removed.

- Change CreateExt, fixed bug that when we create new asset from existing (outAsset) it originally modifiy exising asset UID to new.

- Add new AssetExtCreateFlags for CreateExt.

- Add RemoveSubAssetsFromGAssets as replacement for  RemoveLinkedAssets.

- Remove reading RelativePath from ApplyNewRelativePathOfExt because we not storing this anymore.

# AssetsBrowser

- Completly redo the MoveAsset function, now it matches to new AssetManager::MoveAsset() API, handle
more errors that can be displayed to user, and this complelty different algorithm handling assets that was before.

- Completly redo the RenameAsset function, now it use new AssetManager::MoveAsset() API.

- Remove countBackwardSinceCopy, countForwardSinceCopy and stupid DIRECTIONS during moving, because
MoveAseet() now use different algorithm. 

- Completly redo PasteAssets() function now it use new AssetManager::MoveAsset() API.

- Remove UpdateAssetFileExt, UpdateAssetFolderExt because MoveAsset change it behavioir this no longer need.

- Add MoveAssets()

Test: 
 - Rename (+)
 - Copying (+)
 - Copying if exist generate new valid name (-)
 - Moving (+)
 - Cut + Paste (+)
 - Deletion (+)
 
 - Copying Multiple (+)
 - Moving Multiple (+)
 - Cut + Paste Multiple (+)
 - Deletion Multiple (+)
 
 Bug: Create new folder it not creates .ext file. +

// FIXME: UID of asset not be identical (2 assets with identical UID == break second asset, because from GetAssetByUID 
// return first asset that may have physical file, and second not (and we require second))
// Result if 2 assets with same UID it will not add second asset to GAssets and we cannot get second version of asset with same UID and
// here it will display second asset as first version of itself (witch is not currect)


- Fix Shift selection. +

Themes (D, W, S)
Language (E, R)
Graphics API (Dx11, Dx10)



// TODO: From _AssetsDebugStates_ where displays asset database, make a new panel for assetdebug data base.

Add this after moving or copying asset.
	
	// Update the AssetInfo if it displayed.
	PanelInspector::UpdateAssetInfo();

	// Update Script Project if itemPath is .cs file.
	if (what.extension() == ".cs")
		Project::Get()->UpdateScriptProject(ProcessInfo());
				
											
	Maybe add this after MoveAsset success?
						
	// Update the AssetInfo if it displayed.
	PanelInspector::UpdateAssetInfo();
	
	
// Save for future maybe:

// Record the back state if we copy buffer not empty.
if (!copiedDirectory.empty())
	countBackwardSinceCopy += count_parentPath;