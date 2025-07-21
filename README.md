# SML Fancy Browser Data
## Updating Mods
 1. Update the DLL in `/mods/`
 2. If necessary, update the mod thumbnail in `/thumbnails/`
 3. Go to `browserdata.json`, and update the `Version` property of the mod to the new version number, and update the `PublishTime` property to the Unix timestamp of the time you are updating it. I use https://www.unixtimestamp.com/
## Adding Mods
 1. Add the DLL to `/mods/`
 2. Add the thumbnail PNG to `/thumbnails/`
	 - The file can have any name, but for consistency, please name it the Harmony ID + .png (for example, the mod `synapsium.notes.plus`'s thumbnail is named `synapsium.notes.plus.png`)
 3. Go to `browserdata.json`, and add an entry for the new mod
	 - `Name` and `DisplayName` should be the name of the mod (both the same)
	 - `Authors` should be a list of the Town of Salem 2 usernames of the developers. If one of the developers doesn't actually have an account in the game they developed a mod for, ~~what the fu~~ just use their name and it should be fine.
	 - `AuthorIDs` should be a list of the Discord user IDs of the developers. If one of the developers doesn't use Discord, just omit them or something I literally don't even know where this shows in-game
	 - `HarmonyID` should be the Harmony ID of the mod
	 - `Version` should be the version number, considering you're adding a new mod to the repository this is likely just "1.0.0" but it could be something else
	 - `DLLName` should be the name of the DLL that you added to `/mods/`. Not a full path, just the name of the DLL with the file extension
	 - `ThumbnailPath` should be the name of the thumbnail PNG that you added to `/thumbnails/`. Contrary to the name, this is not a full path, just the name of the PNG with the file extension
	 - `ExcludePlatform` I assume is used to exclude Windows/Mac from seeing mods that don't support their operating system, but not only have I not seen a single mod that explicitly can't support another OS playing the game but also I don't even know the format, so just leave it as `""`
	 - `PublishTime` is the Unix timestamp of the time the mod was published or updated, I use https://www.unixtimestamp.com/ to get this
	 - `DownloadCount` is a number that shows next to the download button in the browser menu, you can set it to whatever number you want but you probably shouldn't go too high? you can just use `0` though
	 - `Outdated` determines if the mod is outdated or not, setting it to `true` means it won't load in-game unless the player enables loading outdated mods. Just keep this as `false` for publishing mods, and if a mod breaks you can go back and set it to `true` in an update
	 - `Banned` lets SML know if a mod should be banned from loading, it's there in case a virus gets through. Just keep this as `false`
	 - `Pending` I have absolutely no clue what this does, just keep it as `false`
