# SiteMesh #

> You can use SiteMesh v.m=2.x.x or SiteMesh v.m=3.xx or both in your Gaelyk application.

> First you need to download the SiteMesh lib. If intend to use SiteMesh-2 go [here](http://www.opensymphony.com/sitemesh/) and for SiteMesh-3 lib go [here](http://www.sitemesh.org/).

> When downloaded place it in the directory of your choice. For example, **c:\sitemesh2** or **c:\sitemesh3** on Windows OS. Now you are ready to use SiteMesh.

> Just right-click your project in an IDE Project Manager then coose **New -> File -> Other**. Select Gaelyk from a list of **Categories**. You now see a list of files where _Gaelyk SiteMesh2 decorator_ and _Gaelyk SiteMesh3 decorator_ are present. Choose any and press **Finish** button. If you selected SiteMesh 2 decorator and a Sitemesh-2 library is not registered in the Library Manager of the IDE, the plugin will ask you to point a directory which contains a sitemesh-2.x.x.jar файл. The same is true when choosing SiteMesh-3 decorator.

## SiteMesh-3 Alpha1 ##

> Unfortunately there is a bug in a current SiteMesh-3 Alpha1 release library. This leads to the fact that a decoration is not applied actually. The bug is fixed in the current trunk of SiteMesh-3. So, you can download it and compile yourself.

> For now I may suggest a small jar library to use as a workaround. If you configer Sitemesh3 filter in the **web.xml** of your project to use a SiteMesh filter class from that library everything will work fine.
  1. Create new Gaelyk project. Add new Sitemesh 3 decorator in order to configer Sitemesh 3.
  1. Download the sitemesh-3-filter-ex.jar файл from [here](http://code.google.com/p/nb-gaelyk-plugin/downloads/detail?name=sitemesh-3-filter-ex.jar&can=2&q=) or go to **Downloads** tab and select the file.
  1. Add jar to the Sitemesh-3 library using IDE Library manager.
  1. Modify the project's web deployment descriptor (web.xml). Now it must looks like:
```
 ........

 <filter>
        <filter-name>sitemesh3</filter-name>
        <!--filter-class>org.sitemesh.config.ConfigurableSiteMeshFilter</filter-class-->
        <filter-class>org.sitemesh.config.SiteMesh3Filter</filter-class>
</filter>
 ........

```