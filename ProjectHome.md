> The plugin allows web developers create, debug and test [Gaelyk Framework](http://gaelyk.appspot.com) applications using [Netbeans IDE](http://netbeans.org/). **See Wiki's** ChangeList to keep track of information about new versions of the plugin.

# NetBeans App Engine Plugin #

> Allows develop your Java App Engine application, just as you can to develop any other servlet-based web application. With the Google Plugin for NetBeans you can create, test, debug, profile and upload App Engine applications from within NetBeans.

> Plugin .zip archives contain .nbm files.

## Latest Version ##

The latest version of the plugin is in the file named  **nbappengine-7.4.x-gae1.8.x-3.0.0.zip**

### What's New ###

1. **Maven**-based web projects support

2. A menu item **'Change email/password'** added

3. Many internal improvements


## Previous Versions ##

The previous version of the plugin is in the file named  nbappengine-7.3.x-gae1.8.x-2.0.0.zip. can be used for all minor versions of the NetBeans IDE ( 7.3 and 7.3.1 for example).

The latest plugin supports version 2.x of the DataNucleus plugin for App Engine, which corresponds to DataNucleus Access Platform 3.0 and JPA 2.0.

> There are three .zip archives which contain early versions:

  * nbappengine-7.3-gae1.8.x.zip for NetBeans 7.3. Deprecated
  * nbappengine-7.3-gae-1.8.x-1.3.0.zip for NetBeans 7.3. Featured (don't use with NetBeans 7.3.1)
  * nbappengine-7.3.1-gae-1.8.x-1.3.2.zip for NetBeans 7.3.1

# Version 0.8.22 Released #

Few bug fixed.  Provides support for all the commands (including **Debug File( Ctrl+Shift+F5**) for **.groovy** files that are available for **.java** files. New addon module makes it posible to to run, test, compile and debug not only **.groovy** files in a web applications, but also extends J2SE projects with the same capabilities. For more information see sections on this page **_"Groovy and Web Applications Support_** and _**"Groovy and J2SE Applications Support"**_ and also wiki [RunCompileTestDebug](RunCompileTestDebug.md) and [ChangeList](ChangeList.md).

# Version 0.7.14 Released #

To see what's new go to [RunCompileTestDebug](RunCompileTestDebug.md) and [ChangeList](ChangeList.md).

# Features #
  * Create new Gaelyk project with all neccesary configurations. The project is just an extention of a regular Netbeans web project type.
  * Add, edit and save Gaelyk View templates ( .gtpl files ).
  * Add, edit, save Gaelyk controllers, routes and groovlets (Groovy script).
  * Add, edit, debug, test, save **groovy** or/and **java** source files.
  * Support [SiteMesh2](http://www.opensymphony.com/sitemesh/) or  [SiteMesh3](http://www.sitemesh.org/) or both as a web-page's layout systems.
  * **jsp** files may be used without restrictions alongside with Gaelyk proprietary **gtpl** files.
  * Support joint compilation of **grovy** and **java** sources.
  * Support compilation, testing, and debugging  of a **grovy** single file.
  * Build and run Gaelyk applications in the App Engine Development mode using [Google App Engine SDK](http://code.google.com/intl/en/appengine/)
  * Gaelyk Framework may be used together with other Web Frameworks that are Registered in the Netbeans IDE. (Spring, Struts, GWT etc.)

# Installation #
> Now, in order to install **Gaelyk Framework** you must download and install three **nbm** module files:
> Go to the [Download](http://code.google.com/p/nb-gaelyk-plugin/downloads/list) tab and select **nb-groovy-command-actions-0.8.22.nbm**, **nb-groovy-web-plugin-0.8.22.nbm**, and **nb-gaelyk-plugin-0.8.22.nbm** files. In the IDE click **Tools->Plugins**. Select **Downloaded** tab and add **.nbm** files. Then click **Install** button.

**Don't follow this advice:** _You just need to replace groovy-all-1.6.4.jar file with a new one using Netbeans Library Manager. To accomplish this, download   groovy-all v.m=1.7.5 or higher from [here](http://groovy.codehaus.org/Download). Then in the IDE use Tools -> Libraries, choose groovy library, remove groovy-all-1.6.4.jar and add the one you've downloaded._


> Before create your first Gaelyk Project, make sure that the following requirements are met:

  1. Download and install [Netbeans Google App Engine Plugin](http://kenai.com/projects/nbappengine/downloads).
  1. Download Gaelyk jar file [Gaelyk jar](http://gaelyk.appspot.com/download) and place it a directory of your choice. When creating the first Gaelyk project, the plugin will ask you to select the mentioned directory.
  1. Netbeans supports Groovy language out of the box.Download   groovy-all v.m=1.7.5 or higher from [here](http://groovy.codehaus.org/Download). Tnen add **groovy-all-1.7.x.jar** or **groovy-all-1.8.x.jar** into the **Libraries** node of a concrete project.
  1. If you intend to use any version of _SiteMesh Web Page's Layout Framework_ see [SiteMesh-wiki](http://code.google.com/p/nb-gaelyk-plugin/wiki/Sitemesh)

# Groovy and Web Applications Support #

When you have **Gaelyk** installed, you'll automatically get the opportunity to use Groovy for any **Web** application. After creating a web application (not necessarily Gaelyk), right-click the project node, select the "Properties" menu item and in the list of categories click the category "Groovy". Then set the flag "Make Groovy Enabled". Now your web application is ready to use Groovy.

If you don't intend to explore Gaelyk Framework but are going to use Groovy for other web applications you may download and install two nbm modules: **nb-groovy-command-actions-0.8.22.nbm** and **nb-groovy-web-plugin-0.8.22.nbm**.

# Groovy and J2SE Applications Support #

Netbeans IDE supports Groovy out of the box. But the only command that you can use for a .groovy file is "Run File". Starting from 0.8 release you might extend this functionality. All you need to do - is to download and install the two modules: **nb-groovy-command-actions-0.8.22.nbm** and **nb-groovy-j2se-plugin-0.8.22.nbm**. After creating a j2se application, right-click the project node, select the "Properties" menu item and in the list of categories click the category "Groovy Addon". Then set the flag "Make Groovy Addon Enabled". Now your j2ee application can utilize such commands as **"Run File", "Compile File", "Debug File", "Test File", "Debug Test File"**.

