# Plugin Integration into source code for Archives Space
This documentation is about the current NYU workflow to add plugins to the ArchivesSpace source code.

Currently, the workflow is as follows:

1. The developer creates a plugin repository
  * The developer adds a file called plugin_info.txt. Here is an [example](https://github.com/NYULibraries/nyu_marcxml_export_plugin/blob/master/plugin_info.txt) from the [nyu_marcxml_export_plugin repository](https://github.com/NYULibraries/nyu_marcxml_export_plugin)
  ```
  AppConfig[:plugins] = ['nyu_marcxml_export_plugin']
  plugin_version:0.1.0
  ```

  * The string in AppConfig[:plugins] is the name of the plugin. It should probably be the name of the repository
  * The plugin version should follow [semantic versioning practices](http://semver.org/).

2. The plugin_info.txt file should be at the root of the repository.

The process of integrating plugins into the ArchivesSpace source code and compiling is then done using puppet and Jenkins. Further documentation on that is upcoming.
