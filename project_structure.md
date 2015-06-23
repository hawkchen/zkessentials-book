Source Code
===========

All source codes used in this book are available on
[github](https://github.com/zkoss/zkessentials). As our example
application has 3 different configurations, our source code is divided
into 3 branches:
[**master**](https://github.com/zkoss/zkessentials/tree/master),
[**chapter9**](https://github.com/zkoss/zkessentials/tree/chapter9), and
[**chapter10**](https://github.com/zkoss/zkessentials/tree/chapter10).

![ center](Tutorial-ch2-3branches.png  " center")

The **master** branch contains examples from chapter 3 to chapter 8. The
**chapter9** branch has examples integrated with Spring and the
**chapter10** branch contains examples which integrate with Spring and
use JPA to persist data into a database.

![ center](Tutorial-ch2-download-zip.png  " center")

You can click the "ZIP" icon to download the current selected branch as
a zip file.

Run Example Application
=======================

After you download the source code, you will find it is a Maven[^1]
project with jetty plugin configured. Therefore, if you have Maven, you
can run the example application with a simple command[^2] (The maven we
use is **3.0.3**). Navigate to the root folder of your downloaded source
code, say it's "zkessentials" and type the command:

**mvn jetty:run**

Then visit the URL *<http://localhost:8080/essentials/>*, and you should
see the screen below.

![ center | 500px](Tutorial-ch2-index.png  " center | 500px")

Project Structure
=================

The 2 images below show the project structure of the example
application. It's Maven default project structure, and all main source
codes are under `src/main`. The left image shows the Java source code is
under `src/main/java` and the right one shows the web application
content is under `src/main/webapp`.

<div  style="width:630px;margin-left:auto;margin-right:auto;">
![ 389px](Tutorial-ch2-project-structure-java.png  "fig: 389px") ![
229px](Tutorial-ch2-project-structure-webapp.png  "fig: 229px")

</div>
<div style="text-align:center;">
**Project Structure: Java(left) and Webapp(right)**

</div>
We name the source code packages according to each chapter and each
package contains the classes used in the example of that chapter. Some
common classes are separated to an independent package as they are used
in multiple chapters. The classes under `org.zkoss.essentials.entity.*`
are entity class. We also define some business interfaces under
`org.zkoss.essentials.service.*` and different chapters have different
implementations.

For ZUL pages, we put them in an independent folder for each chapter
under `src/main/webapp/`. Under "WEB-INF" folder, **web.xml** contains
minimal configuration to run ZK and for its detail please refer to [ ZK
Installation Guide \\ Create and Run Your First ZK Application
Manually](ZK Installation Guide/Quick Start/Create and Run Your First ZK Application Manually "wikilink").
The "zk.xml" is optional configuration descriptor of ZK. Provide this
file if you need to configure ZK differently from the default behavior.
Refer to [ZK Configuration
Reference/zk.xml](ZK Configuration Reference/zk.xml "wikilink") for more
detail.

References
==========

<references/>

[^1]: [Apache Maven](http://maven.apache.org/)

[^2]: [Start jetty in
    Maven](http://docs.codehaus.org/display/JETTY/Maven+Jetty+Plugin)