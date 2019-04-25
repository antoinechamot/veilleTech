## Maven Plugins


# maven-dependency-plugin

 - The go-offline goal is used by CI-Systems to cache dependencies.
 - the go-offline goal suffers from several drawbacks:
	- Multi-Module builds are not supported since the plugin tries to download reactor-dependencies from the remote repository
	- Most parameters simply do not work
	- There is no option to download dynamic dependencies
	=> Go Offline Maven Plugin fixes these drawbacks : https://github.com/qaware/go-offline-maven-plugin

