## `ern cauldron del jsapiimpls`

#### Description

* Remove one or more JS API implementation(s) from a given non-released native application version in a Cauldron  
* Generate and publish a new Container version—so that the native applications can use the new Container version to access the new JS API implementation(s) that was/were added  
**Note** The `ern cauldron del jsapiimpls <jsapiimpls..>` command can remove (from the native application version container) all native dependencies that are only used by the removed MiniApps. The `ern cauldron del jsapiimpls <jsapiimpls..>` command does not do native dependency cleanup.

#### Syntax

`ern cauldron del jsapiimpls <jsapiimpls..>`  

**Arguments**

`<jsapiimpls..>`

* One or more package path to JS API implementation(s) (delimited by spaces) to remove from a native application version in the Cauldron.

**Options**  

`--containerVersion/-v <version>`

* Specify a version for the new container  
* **Default**  Incremental patch number of the current container version  
Example: If the current container version is 1.2.3 and a version is not included in the command, the new container version will be 1.2.4.  

`--descriptor/-d <descriptor>`

* Remove the JS API implementation(s) from a given target native application version in the Cauldron matching the provided native application descriptor  
* You can only pass a complete native application descriptor as the native dependencies removed using this command target only a specific single native application version.  
**Default**  Lists all non-released native application versions from the Cauldron and prompts you to choose one.  

`--resetCache`\

* Indicates whether to reset the React Native cache prior to bundling
* **Default** false

#### Remarks

* You don't need to provide a version for the JS API implementation(s) when using the `ern cauldron del jsapiimpls <jsapiimpls..>` command. The version is ignored because only one version of a given JS API implementation can be present in a container at any given time.  
