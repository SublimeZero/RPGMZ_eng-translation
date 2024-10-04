# Class: StorageManager

A static class that manages game save data.

The local file functionality uses the Node.js fs module.<br />
For saving in the web, the library [localforage](https://localforage.github.io/localForage/) is used instead of directly using localStorage.

In MV, `savefileID` was used, but in MZ it has been changed to a filename.<br />
Additionally, saving is now done with zip compression rather than directly as a JSON string.<br />
The library [pako](https://github.com/nodeca/pako) is used for zip compression and decompression.

Changes were made in versions 1.1.0 and 1.2.0.

---

### Properties

| Identifier              | Type                | Description                      |
|-------------------------|---------------------|----------------------------------|
| `_forageKeys`           | [Array](Array.md)   | [static] Array of forage keys   |
| `_forageKeysUpdated`    | Boolean             | [static] Whether the forage keys are updated |

---

### Methods

#### (static) exists (saveName) → {Boolean}
Checks if the specified save file exists.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) fileDirectoryPath () → {String}
**@MZ** Returns the path to the save file directory.

---

#### (static) filePath (saveName) → {String}
**@MZ** Returns the path with extension (.rmmzsave) for the specified save file.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) forageExists (saveName) → {Boolean}
**@MZ** Checks if the specified save file exists in forage.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) forageKey (saveName) → {String}
**@MZ** Generates and returns a forage key.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) forageKeysUpdated () → {Boolean}
**@MZ** Checks if the forage keys are updated.

---

#### (static) forageTestKey () → {String}
**@MZ** Returns a test forage key.

---

#### (static) fsMkdir (path)
**@MZ** Creates a directory using fs.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `path`    | [String](String.md)| Directory path            |

---

#### (static) fsReadFile (path) → {String}
**@MZ** Reads and returns a file using fs.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `path`    | [String](String.md)| File path                 |

---

#### (static) fsRename (oldPath, newPath)
**@MZ** Renames a file using fs.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `oldPath` | [String](String.md)| Old file path             |
| `newPath` | [String](String.md)| New file path             |

---

#### (static) fsWriteFile (path, data)
**@MZ** Writes data to a file using fs.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `path`    | [String](String.md)| File path                 |
| `data`    | [String](String.md)| Data                      |

---

#### (static) fsUnlink (path)
**@MZ** Unlinks a file using fs.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `path`    | [String](String.md)| File path                 |

---

#### (static) isLocalMode () → {Boolean}
Checks if in local mode.

---

#### (static) loadObject (saveName) → {Object}
**@MZ** Loads the specified save file and returns an object.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) loadZip (saveName) → {Zip}
**@MZ** Loads the specified save file and returns it.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) loadFromLocalFile (saveName) → {Zip}
Loads the specified save file from local and returns it.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) loadFromForage (saveName) → {Zip}
**@MZ** Loads the specified save file from local and returns it.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) localFileExists (saveName) → {Boolean}
Checks if the specified save file exists locally.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) jsonToObject (json) → {Object}
**@MZ** Converts the specified JSON string into an object and returns it.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `json`    | [String](String.md)| JSON string               |

---

#### (static) jsonToZip (json) → {Zip}
**@MZ** Converts the specified JSON string into zip format data and returns it.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `json`    | [String](String.md)| JSON string               |

---

#### (static) objectToJson (object) → {String}
**@MZ** Converts the specified object into a JSON string and returns it.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `object`  | Object            | Object to save            |

---

#### (static) remove (saveName) → {Boolean}
Deletes the specified save file and returns the result.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) removeForage (saveName) → {Boolean}
**@MZ** Deletes the specified save file from forage and returns the result.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) removeLocalFile (saveName)
Deletes the specified save file from local.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |

---

#### (static) saveObject (saveName, object)
**@MZ** Saves the specified save file with a JSON string.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |
| `object`  | Object            | Object to save            |

---

#### (static) saveToForage (saveName, zip)
**@MZ** Saves the zip format data to the specified save file.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |
| `zip`     | Zip               | Zip format data of JSON string |

---

#### (static) saveZip (saveName, zip)
**@MZ** Saves the specified save file with a JSON string.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [String](String.md)| Save file name            |
| `zip`     | Zip               | Zip format data of JSON string |

---

#### (static) saveToLocalFile (saveName, zip)
Saves the specified save file locally with a JSON string.

##### Arguments

| Name      | Type              | Description               |
|-----------|-------------------|---------------------------|
| `saveName`| [Number](Number.md)| Save file ID              |
| `zip`     | Zip               | Zip format data of JSON string |

---

#### (static) updateForageKeys ()
**@MZ** Updates the forage keys.

---

#### (static) zipToJson (zip) → {String}
**@MZ** Converts the specified zip format data into a JSON string and returns it.

##### Arguments

| Name | Type | Description         |
|------|------|---------------------|
| `zip`| Zip  | Zip format data     |

---

### Deprecated MV Methods

[static] backup (savefileId), backupExists (savefileId), cleanBackup (savefileId), load (savefileId), loadFromLocalBackupFile (savefileId), loadFromWebStorage (savefileId), loadFromWebStorageBackup (savefileId), localFileBackupExists (savefileId), localFileDirectoryPath (), localFilePath (savefileId), removeWebStorage (savefileId), restoreBackup (savefileId), save (savefileId, json), saveToWebStorage (savefileId, json), webStorageBackupExists (savefileId), webStorageExists (savefileId), webStorageKey (savefileId)
