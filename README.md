modplax
=======

TARS 9 Modplax is an integrated server that installs, integrates and manages
Apache HTTP Server, Apache Tomcat, Ruby on Rails, Node.js, PHP and MariaDB.

Table of contents
-----------------

- [Table of contents](#table-of-contents)
- [Features](#features)
- [Supported platforms](#supported-platforms)
- [Installation](#installation)
- [Complete the installation](#complete-the-installation)
- [Use command-line parameters to install Modplax](#use-command-line-parameters-to-install-modplax)
- [Use command-line parameters to uninstall Modplax](#use-command-line-parameters-to-uninstall-modplax)
- [Modplax Agent](#modplax-agent)
- [Customize the settings of installed servers](#customize-the-settings-of-installed-servers)
- [Server management commands](#how-to-use-server-management-commands)
- [Bugs and feature requests](#bugs-and-feature-requests)
- [Using the issue tracker](#using-the-issue-tracker)
- [Versions of included software](#versions-of-included-software)
- [Versioning](#versioning)
- [Creators](#creators)
- [Copyright and license](#copyright-and-license)

Features
--------

<table>
  <thead>
    <tr>
      <th>Feature</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        ⊛ TARS 9 Modplax optionally installs each of the following web servers,
          application servers, and database servers:
        <p></p>
        <ul>
        <li><strong>Apache HTTP Server</strong></li>
        <li><strong>Apache Tomcat</strong></li>
        <li><strong>Ruby on Rails</strong></li>
        <li><strong>Node.js</strong></li>
        <li><strong>PHP</strong></li>
        <li><strong>MariaDB</strong></li>
        </ul>
      </td>
      <td>
        If you are installing Apache Tomcat, the Modplax installer installs the
        JRE in the install directory, so you do not need to install a separate
        JRE.
        <p></p>
        For more information about the software versions, see the
        <a href="https://github.com/tars9/modplax/blob/master/README.md#versions-of-included-software">
        Versions of included software</a>.
      </td>
    </tr>
    <tr>
      <td>
        ⊛ All components that you install are installed under the specified
          installation directory without affecting any other existing software.
      </td>
      <td>
      </td>
    </tr>
    <tr>
      <td>
        ⊛ Customize the settings of installed servers.
      </td>
      <td>
        You can easily change the ports of the servers, the location of the
        database storage, and the installation directory at any time during or
        after installation.
        <p></p>
        For more information, see the
        <a href="https://github.com/tars9/modplax/blob/master/README.md#customize-the-settings-of-installed-servers">
        Customize the settings of installed servers</a>.
      </td>
    </tr>
    <tr>
      <td>
        ⊛ The Modplax installer supports silent install/uninstall. You can also
          specify all installation options in a silent install/uninstall.
      </td>
      <td>
        For more information about silent installation/uninstallation, see the
        following article:
        <p></p>
        <ul>
          <li><a href="https://github.com/tars9/modplax/blob/master/README.md#use-command-line-parameters-to-install-modplax">Use command-line parameters to install Modplax</a></li>
          <li><a href="https://github.com/tars9/modplax/blob/master/README.md#use-command-line-parameters-to-uninstall-modplax">Use command-line parameters to uninstall Modplax</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        ⊛ Automatically integrates application servers with a web server.
      </td>
      <td>
        Integrate Apache Tomcat, Ruby on Rails, Node.js, and PHP with Apache
        HTTP Server.
      </td>
    </tr>
    <tr>
      <td>
        ⊛ Provides a <a href="https://github.com/tars9/modplax/blob/master/README.md#modplax-agent">GUI tool</a>
          to check the status of servers and to start/stop.
      </td>
      <td></td>
    </tr>
    <tr>
      <td>
        ⊛ All servers can be started as services or as regular processes. This
          can be controlled by the <a href="https://github.com/tars9/modplax/blob/master/README.md#server-management-commands">
          Server management commands</a>.
      </td>
      <td></td>
    </tr>
  </tbody>
</table>

Supported platforms
-------------------

* Operating systems
    * Microsoft Windows: Server 2008+, Vista+
    * Linux: Modplax was designed from the beginning to enable Linux support. We
      will support Linux in the near future.

Installation
------------

1. Download the latest release

    [Download the installer file for your platform](https://github.com/tars9/modplax/releases/)

2. Run the installer.

    Follow the prompts to install TARS 9 Modplax. You'll be asked for the
    following information.

    * Language selection

        ![Alt text](https://github.com/tars9/modplax/blob/master/docs/images/mpxinstw/mpxinstw-01-01-language.png "Language selection")

        - Select the installation language.
            > The default installation language is the language that is detected
              by the user's default Windows language.

    * Components

        ![Alt text](https://github.com/tars9/modplax/blob/master/docs/images/mpxinstw/mpxinstw-04-components.png "Components")

        - Select the components to install.

    * Install Location

        ![Alt text](https://github.com/tars9/modplax/blob/master/docs/images/mpxinstw/mpxinstw-05-install_location.png "Install Location")

        - Destination Folder
            > This is where TARS 9 Modplax will be installed.

    * Apache HTTP Server configuration options

        ![Alt text](https://github.com/tars9/modplax/blob/master/docs/images/mpxinstw/mpxinstw-06-01-conf-apache.png "Apache HTTP Server configuration options")

        - Domain name
            > This is a hostname for the server. The value specified in domain
              name must be a valid Domain Name Service (DNS) name that can be
              resolved by the system. The default is "localhost".
              When specifying a self defined domain name, be sure the IP address
              and server name pair are included in the hosts file below:

              C:\Windows\System32\drivers\etc\hosts
        - Port
            > This is a HTTP port.
        - Install Apache HTTP Server as a service
            > This is an option for registering Windows service. This option
              allows application to start automatically at system boot.

    * Apache Tomcat configuration options

        ![Alt text](https://github.com/tars9/modplax/blob/master/docs/images/mpxinstw/mpxinstw-06-02-conf-tomcat.png "Apache Tomcat configuration options")

        - Ports
            > These are the Apache Tomcat ports. Stick with the default unless
              you're running another application on the same ports.
        - Install Apache Tomcat as a service
            > This is an option for registering Windows service. This option
              allows application to start automatically at system boot.

    * Ruby on Rails configuration options

        ![Alt text](https://github.com/tars9/modplax/blob/master/docs/images/mpxinstw/mpxinstw-06-03-conf-ror.png "Ruby on Rails configuration options")

        - Port
            > This is a HTTP port.
        - Install Ruby on Rails as a service
            > This is an option for registering Windows service. This option
              allows application to start automatically at system boot.

    * Node.js configuration options

        ![Alt text](https://github.com/tars9/modplax/blob/master/docs/images/mpxinstw/mpxinstw-06-04-conf-nodejs.png "Node.js configuration options")

        - Port
            > This is a HTTP port.
        - Install Node.js as a service
            > This is an option for registering Windows service. This option
              allows application to start automatically at system boot.

    * MariaDB configuration options

        ![Alt text](https://github.com/tars9/modplax/blob/master/docs/images/mpxinstw/mpxinstw-06-05-conf-mariadb.png "MariaDB configuration options")

        - Data directory
            > This is where MariaDB database files will be stored.
        - Modify password for database user "root"
            > This is a password for database user "root".
        - Port
            > This is a MariaDB port.
        - Install MariaDB as a service
            > This is an option for registering Windows service. This option
              allows application to start automatically at system boot.

    * Additional configuration options

        ![Alt text](https://github.com/tars9/modplax/blob/master/docs/images/mpxinstw/mpxinstw-06-06-conf-additional.png "Additional configuration options")

        - Create the desktop icons for TARS 9 Modplax
            > This option allows to create the desktop icons.
        - Create the start menu folder for TARS 9 Modplax
            > This option allows to create the start menu folder.
        - Run TARS 9 Modplax Agent at user logon
            > This option allows TARS 9 Modplax Agent to start automatically at
              user logon.

Complete the installation
-------------------------

Start your web browser and type localhost, or http://127.0.0.1 or
http://localhost in the address bar. You can test the installed application
server from the Modplax test page.

Note: If you set the HTTP server port to a port other than 80, type
localhost:\<port>, http://127.0.0.1:\<port> or http://localhost:\<port> in the
address bar (e.g., localhost:20080).

<img src="https://github.com/tars9/modplax/blob/master/docs/images/web/itworks.png" width="600">

Use command-line parameters to install Modplax
----------------------------------------------

All options you specify in the Modplax installer GUI can be specified as
command-line parameters.

To install using command-line parameters, run the Modplax installer with the
parameters within the "Command Prompt".

Open the "Command Prompt":

    Press Windows Key + R, type "cmd" into the Run dialog, and press Enter.

> Note: Modplax supports silent install. Silent install mode does not display
  any interactive interface. To install in silent mode, run the installer with
  the "/S" ("silent") option.

### **Usage of the Modplax installer:**

```
SYNOPSIS
    modplax-XX.exe [option ...]

OPTIONS
    -v
        This command will create a verbose log which offers a lot of
        information about the installation.

    /NCRC (uppercase)
        Disables the CRC check.

    /S (uppercase)
        Runs the installer in silent mode.

    /?
        Display help.

CUSTOM INSTALLATION OPTIONS
    -Dinstall.dir=<val>
        Installation directory.

    -Dcomponents=<all | [val | "val, val..."]>
        Specify the components to install. The default is "all".
        e.g., -Dcomponents="apache, nodejs"

        The following components are available for this option:

        all             : All modules.
        ant             : Apache Ant.
        apache          : Apache HTTP Server.
        heidisql        : HeidiSQL.
        java            : Java SE.
        mariadb         : MariaDB.
        nodejs          : Node.js.
        php             : PHP.
        ror             : Ruby on Rails.
        tomcat          : Apache Tomcat.

    -Dapache.domain_name=<val>
        The domain name of the Apache HTTP Server.

    -Dapache.http.port=<val>
        The port of the Apache HTTP Server.

    --apache_svc_switch=<true | false>
        A switch for installing the HTTP server as a service.

    -Dtomcat.http.port=<val>
        The HTTP port of the Apache Tomcat.

    -Dtomcat.shutdown.port=<val>
        The shutdown port of the Apache Tomcat.

    -Dtomcat.ajp.connector.port=<val>
        The AJP connector port of the Apache Tomcat.

    -Dtomcat.ssl.redirect.port=<val>
        The SSL redirect port of the Apache Tomcat.

    --tomcat_svc_switch=<true | false>
        A switch for installing the Apache Tomcat as a service.

    -Dror.http.port=<val>
        The HTTP port of the Ruby on Rails.

    --ror_svc_switch=<true | false>
        A switch for installing the Ruby on Rails as a service.

    -Dnodejs.http.port=<val>
        The HTTP port of the Node.js.

    --nodejs_svc_switch=<true | false>
        A switch for installing the Node.js as a service.

    -Dmariadb.datadir=<val>
        Location of the database storage.

    --mariadb_set_root_password=<val>
        Modify password for database user "root".

    -Dmariadb.port=<val> - The port of the MariaDB.

    --mariadb_svc_switch=<true | false>
        A switch for installing the MariaDB as a service.

    -Dcreate.desktop.icon=<true | false>
        If true, create the desktop icons.

    -Dcreate.smprograms.icon=<true | false>
        If true, create the start menu folder.

    --run_at_logon_switch=<true | false>
        Run TARS 9 Modplax Agent at user logon.
```

Use command-line parameters to uninstall Modplax
------------------------------------------------

All options you specify in the Modplax uninstall GUI can be specified as
command-line parameters.

> Note: The Modplax uninstaller "Uninstall.exe" is located in the installation
  directory.

To uninstall using command-line parameters, run the Modplax uninstall with the
parameters within the "Command Prompt".

Open the "Command Prompt":

    Press Windows Key + R, type "cmd" into the Run dialog, and press Enter.

> Note: Modplax supports silent uninstall. Silent uninstall mode does not
  display any interactive interface. To uninstall in silent mode, run the
  uninstaller with the "/S" ("silent") option.

### **Usage of the Modplax uninstaller:**

```
SYNOPSIS
    Uninstall.exe [option ...]

OPTIONS
    -v
        This command will create a verbose log which offers a lot of
        information about the installation.

    /NCRC (uppercase)
        Disables the CRC check.

    /S (uppercase)
        Runs the uninstaller in silent mode.

    /?
        Display help.

CUSTOM INSTALLATION OPTIONS
    --un_files_completely_removes=<true | false>
        A switch that completely removes the TARS 9 Modplax.

    --un_files_data_files=<true | false>
        A switch that removes the data files in the installation directory.
```

Modplax Agent
-------------

With Modplax Agent, you can easily start, stop and restart each server.

![Alt text](https://github.com/tars9/modplax/blob/master/docs/images/mpxagentw/mpxagentw.png "Modplax Agent")

You can also safely start or stop all servers sequentially. This will start or
stop each server in the following order:

* Start all servers
    > MariaDB → Node.js → Ruby on Rails → Apache Tomcat → Apache HTTP Server

* Stop all servers
    > Apache HTTP Server → Apache Tomcat → Ruby on Rails → Node.js → MariaDB

Customize the settings of installed servers
-------------------------------------------

Modplax provides a "setup" configuration tool that allows you to change the
settings of each component after installation.

> Note: "setup" is located in the setup directory of the installation directory.

```
NAME
    setup - Set up the environment of the Modplax.

SYNOPSIS
    setup [command ...] [option ...]

DESCRIPTION
    Set up the environment of the Modplax.

COMMANDS
    setup
        Configure the installed products (default).

    install
        Install Application Platform Module (APM) and configure the installed
        products.

    reset-inst-path
        Setting up the installation path to the current directory.

    restore
        Restore the configuration to run the installed products.

OPTIONS
    -Dinstall.dir=<val>
        Installation directory.

    -Dinstalled.dir=<val>
        Use it when the install directory (install.dir) to set up and the
        directory where the installed package exists are different. The default
        is the directory where the current package is installed.

    -Dapm=<all | all-s | [val | "val, val..."]>
        Specify installation modules. The default is "all-s". This option is
        only relevant for the "install" command.
        e.g., -Dapm="apache, nodejs"

        The following modules are available for this option:

            all             : All modules.
            all-s           : All modules (silent mode).
            ant             : Apache Ant.
            apache          : Apache HTTP Server.
            heidisql        : HeidiSQL.
            java            : Java SE.
            mariadb         : MariaDB.
            mariadb-data    : MariaDB's default database file.
            nodejs          : Node.js.
            php             : PHP.
            ror             : Ruby on Rails.
            tomcat          : Apache Tomcat.

    -Dapache.domain.name=<val>
        The domain name of the Apache HTTP Server.

    -Dapache.http.port=<val>
        The port of the Apache HTTP Server.

    -Dtomcat.http.port=<val>
        The HTTP port of the Apache Tomcat.

    -Dtomcat.shutdown.port=<val>
        The shutdown port of the Apache Tomcat.

    -Dtomcat.ajp.connector.port=<val>
        The AJP connector port of the Apache Tomcat.

    -Dtomcat.ssl.redirect.port=<val>
        The SSL redirect port of the Apache Tomcat.

    -Dror.http.port=<val>
        The HTTP port of the Ruby on Rails.

    -Dnodejs.http.port=<val>
        The HTTP port of the Node.js.

    -Dmariadb.data.dir=<val>
        Location of the database storage.
        This option allows you to set the path of the database files. Actual
        database files is not moved to a new path, you must manually move
        database files to a new path.

    -Dmariadb.port=<val>
        The port of the MariaDB.

    -Dsilent.mode=<true | false>
        If true, run in silent mode.

    -Dcreate.desktop.icon=<true | false>
        If true, create the desktop icons.

    -Dcreate.smprograms.icon=<true | false>
        If true, create the start menu folder.

    -Dtrg.os=<linux | windows>
        Specify the OS of the package to install. The default is current OS.

    -Dtrg.arch=<x64 | x86>
        Specify the processor architecture of the package to install. Defaults
        to current processor architecture.

    -h
        Display this help and exit.

EXAMPLES
    Set the domain name and port of the Apache HTTP Server.
        setup -Dapache.domain.name=localhost -Dapache.http.port=20080

    Set the HTTP port, shutdown port, AJP connector port, and SSL Redirect port
    of the Apache Tomcat.
        setup -Dtomcat.http.port=28080 -Dtomcat.shutdown.port=28005
            -Dtomcat.ajp.connector.port=28009 -Dtomcat.ssl.redirect.port=28443

    Set the HTTP port of the Ruby on Rails.
        setup -Dror.http.port=23000

    Set the HTTP port of the Node.js.
        setup -Dnodejs.http.port=23001

    Set the port of the MariaDB.
        setup -Dmariadb.port=23306

    Change the installation directory.
        setup -Dinstall.dir="C:\Program Files\Modplax-new"

ADVANCED USAGE
    If the installation directory (install.dir) to set up and the directory
    where the installed package exists are different, specify the directory of
    the installed package using the -Dinstalled.dir option.
        setup -Dinstalled.dir="C:\Program Files\Modplax-new" [option ...]

        setup -Dtrg.os=windows -Dtrg.arch=x64 setup
            -Dinstall.dir="C:\Program Files\Modplax"
            -Dinstalled.dir="C:\Program Files\Modplax-new"
            -Dapache.http.port="20080"
            -Dtomcat.http.port="28080"
            -Dtomcat.shutdown.port="28005"
            -Dtomcat.ajp.connector.port="28009"
            -Dtomcat.ssl.redirect.port="28443"
            -Dror.http.port="23000"
            -Dnodejs.http.port="23001"
            -Dmariadb.port="23306"
            -Dcreate.desktop.icon="true"
            -Dcreate.smprograms.icon="true"
            -Dsilent.mode="true"

        setup -Dtrg.os=windows -Dtrg.arch=x64 install
            -Dinstall.dir="C:\Program Files\Modplax"
            -Dinstalled.dir="C:\Program Files\Modplax-new"
            -Dapache.http.port="20080"

    Change the database storage location.
    This option allows you to set the path of the database files. Actual
    database files is not moved to a new path, you must manually move database
    files to a new path.
        setup -Dmariadb.data.dir="C:\Program Files\Modplax\mariadb-data-new"

    Revert to the previous settings.
        setup restore

    Revert to the previous settings in the specified backup directory.
        setup restore -Dbackup.dir="backup/yyyy-MM-dd.HHmmss.SSS"

    Setting up the installation path to the current directory.
        setup reset-inst-path
```

Server management commands
--------------------------

Modplax provides the following server management tools:

|   Management tool    |                      Description                      |
|----------------------|-------------------------------------------------------|
| apachectl            | Apache HTTP Server control interface.                 |
| tomcatctl            | Apache Tomcat control interface.                      |
| rorctl               | Ruby on Rails control interface.                      |
| nodejsctl            | Node.js control interface.                            |
| mariadbctl           | MariaDB control interface.                            |
| modplaxctl           | Control interface for all TARS 9 Modplax servers.     |

> Note: The server management tools are located in the "bin" directory of the
  installed directory.

Using the above tools, you can start, stop, restart, install service, uninstall
service, and check startup status of each server.

As with the Modplax Agent, You can also safely start or stop all servers
sequentially using "modplaxctl".

For detailed usage, run the server management tool with the "-h" option (e.g.,
apachectl -h).

Bugs and feature requests
-------------------------

Have a bug or a feature request? Please first search for existing and closed
[issues](https://github.com/tars9/modplax/issues). If your problem or idea is
not addressed yet, [please open a new issue](https://github.com/tars9/modplax/issues/new).

Using the issue tracker
-----------------------

The [issue tracker](https://github.com/tars9/modplax/issues) is the preferred
channel for bug reports, features requests and submitting pull requests, but
please respect the following restrictions:

* Please **do not** use the issue tracker for personal support requests.

* Please **do not** derail or troll issues. Keep the discussion on topic and
  respect the opinions of others.

* Please **do not** post comments consisting solely of "+1" or ":thumbsup:".
  Use [GitHub's "reactions" feature](https://github.com/blog/2119-add-reactions-to-pull-requests-issues-and-comments)
  instead. We reserve the right to delete comments which violate this rule.

Versions of included software
-----------------------------

This version of Modplax contains the following software releases:

* Apache Ant 1.9.4
* Apache HTTP Server 2.4.17
* Apache Tomcat 8.0.26
* HeidiSQL 9.3.0.4984
* JRE 8u60
* MariaDB 10.0.21
* Node.js 8.11.2
* PHP 7.2.1
* Ruby 2.4.1

Versioning
----------

TARS 9 software version numbers consist of 4 parts: MAJOR.MINOR.BUILD.PATCH.

MAJOR and MINOR may get updated with any significant TARS 9 software release.
Given a version number MAJOR.MINOR.BUILD.PATCH, increment the:

    1. MAJOR version when you make incompatible API changes.
    2. MINOR version when you add functionality in a backwards-compatible
       manner. When the MAJOR version number is incremented, the MINOR version
       and PATCH version MUST be reset to zero.
    2. BUILD must get updated whenever a release candidate is built from the
       current trunk. The BUILD number is an EVER-INCREASING NUMBER representing
       a point in time of the product trunk
    4. PATCH version when you make backwards-compatible bug fixes. PATCH must
       get updated whenever a release candidate is built from the BUILD branch.
       When a BUILD version number is incremented, the patch version MUST be
       reset to zero.

For instance: 1.1.3.8 -> 1.1.4.0 and 1.2.5.7 -> 2.0.6.0

The BUILD and PATCH numbers together are the canonical representation of what
code is in a given release. The BUILD number is always increasing as the source
code trunk advances, so build 150 is always newer code than build 145. The PATCH
number is always increasing for a given BUILD. Developers and testers generally
refer to an instance of the product as BUILD.PATCH. It is the shortest
unambiguous name for a build.

See [the Releases section of our GitHub project](https://github.com/tars9/modplax/releases)
for changelogs for each release version of Modplax.

Creators
--------

**Dongwoon Kim**

- <dongwoonkm@gmail.com>

Copyright
---------

Copyright (c) TARS 9. All rights reserved.

NOTICE: All information contained herein is, and remains the property of\
TARS Nine ("TARS 9") and its suppliers, if any. The intellectual and\
technical concepts contained herein are proprietary to TARS 9 and its\
suppliers and may be covered by Republic of Korea and Foreign Patents,\
patents in process, and are protected by trade secret or copyright law.\
Dissemination of this information or reproduction of this material is\
strictly forbidden unless prior written permission is obtained from TARS 9.

License
-------

See <a href="https://github.com/tars9/modplax/blob/master/LICENSE_EN.txt">TARS 9 Freeware License</a>.
