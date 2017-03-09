# Autodesk® Stingray / Flow Nodes sample plugin
---

This folder contains Stingray Plugin sample showcasing the creation of custom flow nodes inside a engine runtime plugin.

This is a sample plugin that registers flow nodes nodes showcasing how to add flow implementations as a runtime plugin. Don't rely on the implementations do something actually useful, the code is only provieded as a sample.
Some of the nodes have their ui_scopes set so they are not visible in any editor by default ("sample_flow_node" and "profiler"). The "Dragon" category of flow nodes show how you can use custom data fields as input/output to flow nodes.

This plugin has a corresponding editor plugin part which contains the mapping of flow_node_definition file so they can be used in the editor and properly compiled. the flow_node_definition file is not needed to run your compiled project.

### Install prerequisites

-   Git client: <https://git-scm.com/>
-   Ruby 2.0 or later: <http://rubyinstaller.org>.
    -   Rubygems SSL fix (if needed): <http://guides.rubygems.org/ssl-certificate-update>
-   Visual Studio 2015 with Update 3 & Patch KB3165756: <https://www.visualstudio.com/downloads/#visual-studio-professional-2015-with-update-3>

### Set up your library directory

Every revision of the Stingray source code depends on several libraries that are not stored in Git. Instead, our build tools copy these libraries to your computer from a storage location on the Internet.

Before you run a build, you have to specify a location on your computer where you want the build to store and access these libraries.

-   Create an environment variable named `SR_LIB_DIR`. Set its value to an empty directory on your computer where you want the libraries to be copied. Make sure that you have at least 2 GB of space.

### Build

Run the `make.rb` script in the root directory of this repository.

~~~
> ruby make.rb
~~~

Once you've successfully built the flow nodes sample plugin, you can zip the `plugin` folder and **distribute** your plugin. For help getting started with with the Stingray SDK, see the tutorial videos and topics in the [main Stingray SDK Help](http://help.autodesk.com/view/Stingray/ENU/?guid=__sdk_help_introduction_html).

For more details regarding building your own plugins see the stingray-plugin repository: https://github.com/AutodeskGames/stingray-plugin
