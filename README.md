modplax
=======

Middleware that installs, integrates, and manages web servers, application
servers, database servers, and more.

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

    Download the installer file for your platform: https://github.com/tars9/modplax/releases/

        e.g., modplax-X.X.X.X-windows-x64.zip

2. Run the installer.

    [comment]: <> (Deploy the compressed files of the installer so that the)
    [comment]: <> (antivirus does not block the installer.)
    [comment]: <> (e.g., Windows Defender SmartScreen.)
    Unzip the downloaded archive and run the installer.

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
`http://localhost:<port>`, `http://127.0.0.1:<port>` or
`http://localhost:<port>` in the address bar (e.g., http://localhost:20080).

<img src="https://github.com/tars9/modplax/blob/master/docs/images/web/itworks.png" width="600">

Use command-line parameters to install Modplax
----------------------------------------------

All options you specify in the Modplax installer GUI can be specified as
command-line parameters.

To install using command line parameters, run the Modplax installer from the
"Command Prompt".

Open the "Command Prompt":

    Press Windows Key + R, type "cmd" into the Run dialog, and press Enter.

Run the following command:

    cd /d "<installer location>"
    modplax-<version>-<platform>.exe [option ...]

> Note: Modplax supports silent install. Silent install mode does not display
  any interactive interface. To install in silent mode, run the installer with
  the "/S" ("silent") option.

### **Usage of the Modplax installer:**

[comment]: <> (Last modified date that copied the usage of the installer: 2019-09-27)
```
☘ SYNOPSIS
    modplax-<version>-<platform>.exe [option ...]

☘ OPTIONS
    -v
        This command will create a verbose log which offers a lot of
        information about the installation.

    /NCRC (uppercase)
        Disables the CRC check.

    /S (uppercase)
        Runs the installer in silent mode.

    /?
        Display help.

♞ CUSTOM INSTALLATION OPTIONS
    --install_dir=<val> - Installation directory.

    --components=<all | [val | "val, val..."]>
        Specify the components to install. The default is "all".
        e.g., --components="apache, nodejs"

        The following components are available for this option:

          all, ant , apache, heidisql, java, mariadb, nodejs, php, ror,
          tomcat

    --apache_domain_name=<val> - The domain name of the Apache
        HTTP Server.

    --apache_http_port=<val> - The port of the Apache HTTP Server.

    --apache_svc_switch=<true | false> - A switch for installing the HTTP
        server as a service.

    --tomcat_http_port=<val> - The HTTP port of the Apache Tomcat.

    --tomcat_shutdown.port=<val> - The shutdown port of the Apache
        Tomcat.

    --tomcat_ajp_connector_port=<val> - The AJP connector port of the
        Apache Tomcat.

    --tomcat_ssl_redirect_port=<val> - The SSL redirect port of the
        Apache Tomcat.

    --tomcat_svc_switch=<true | false> - A switch for installing the
        Apache Tomcat as a service.

    --ror_http_port=<val> - The HTTP port of the Ruby on Rails.

    --ror_svc_switch=<true | false> - A switch for installing the Ruby on
        Rails as a service.

    --nodejs_http_port=<val> - The HTTP port of the Node.js.

    --nodejs_svc_switch=<true | false> - A switch for installing the
        Node.js as a service.

    --mariadb_data_dir=<val> - Location of the database storage.

    --mariadb_set_root_password=<val> - Modify password for
        database user "root".

    --mariadb_port=<val> - The port of the MariaDB.

    --mariadb_svc_switch=<true | false> - A switch for installing the
        MariaDB as a service.

    --create_desktop_icon=<true | false> - If true, create the desktop
        icons.

    --create_smprograms_icon=<true | false> - If true, create the start
        menu folder.

    --run_at_logon_switch=<true | false> - Run TARS 9 Modplax Agent
        at user logon.
```

Use command-line parameters to uninstall Modplax
------------------------------------------------

All options you specify in the Modplax uninstall GUI can be specified as
command-line parameters.

> Note: The Modplax uninstaller "Uninstall.exe" is located in the installation
  directory.

To uninstall using command line parameters, run the Modplax uninstaller
(Uninstall.exe) from the "Command Prompt".

Open the "Command Prompt":

    Press Windows Key + R, type "cmd" into the Run dialog, and press Enter.

Run the following command:

    cd /d "<installed directory>"
    Uninstall.exe [option ...]

> Note: Modplax supports silent uninstall. Silent uninstall mode does not
  display any interactive interface. To uninstall in silent mode, run the
  uninstaller with the "/S" ("silent") option.

### **Usage of the Modplax uninstaller:**

[comment]: <> (Last modified date that copied the usage of the uninstaller: 2019-09-27)
```
☘ SYNOPSIS
    Uninstall.exe [option ...]

☘ OPTIONS
    -v
        This command will create a verbose log which offers a lot of
        information about the installation.

    /NCRC (uppercase)
        Disables the CRC check.

    /S (uppercase)
        Runs the uninstaller in silent mode.

    /?
        Display help.

♞ CUSTOM INSTALLATION OPTIONS
    --un_files_completely_removes=<true | false> - A switch that completely
        removes the TARS 9 Modplax.

    --un_files_data_files=<true | false> - A switch that removes the data
        files in the installation directory.
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

Change the settings of the installed servers
--------------------------------------------

Modplax provides a setup tool that allows you to change the settings of servers
even after installation.

To change the settings of the installed servers, run the setup tool from the
"Command Prompt".

Open the "Command Prompt":

    Press Windows Key + R, type "cmd" into the Run dialog, and press Enter.

Run the following command:

    cd /d "<installed directory>\setup"
    setup [command ...] [option ...]

To display help information for the setup tool, enter the following command:

    setup -h

> Note: The setup tool is located in the "setup" directory of the installation
  directory.

[comment]: <> (Last modified date that copied the usage of the setup tool: 2019-10-08)
```
NAME
    setup - Set up the environment of the Modplax.

SYNOPSIS
    setup [command] [option ...]

DESCRIPTION
    Set up the environment of the Modplax.

COMMANDS
    setup
        Configure the installed products (default).

    install
        Install Application Platform Module (APM) and configure the installed
        products.

    update
        Update Application Platform Module (APM).

    restore
        Restore the configuration to run the installed products.

OPTIONS
    --trg_arch=<x64 | x86>
        Specify the processor architecture of the package to install. Defaults
        to current processor architecture.

    --install_dir=<val>
        Installation directory to be set in the configuration files. The default
        is the directory where the current package is installed.

        Specify this option if you have moved installed packages to another
        location.

    --installed_dir=<val>
        Use it when the install directory to set up and the directory where the
        installed package exists are different. The default is the directory
        where the current package is installed.

    --apm_list=<all | all-s | [val | "val, val..."]>
        Specify the APMs. The default is "all-s". This option is only used with
        the "install" and "update" command.
        e.g., setup install --apm_list="apache, nodejs"

        The following values are available for this option:

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

        By default, Update overwrites existing modules with newer versions of
        the files. For the following modules, if the module already exists
        during the update, the module is removed and installed:

          ant, heidisql, java, jreext, php

    --apache_domain_name=<val>
        The domain name of the Apache HTTP Server.

    --apache_http_port=<val>
        The port of the Apache HTTP Server.

    --tomcat_http_port=<val>
        The HTTP port of the Apache Tomcat.

    --tomcat_shutdown_port=<val>
        The shutdown port of the Apache Tomcat.

    --tomcat_ajp_connector_port=<val>
        The AJP connector port of the Apache Tomcat.

    --tomcat_ssl_redirect_port=<val>
        The SSL redirect port of the Apache Tomcat.

    --ror_http_port=<val>
        The HTTP port of the Ruby on Rails.

    --nodejs_http_port=<val>
        The HTTP port of the Node.js.

    --mariadb_data_dir=<val>
        Location of the database storage. This option allows you to set the data
        path for the database.

        CAUTION: If you set up using this option after installation, the
        database files will not be moved to the new path. Move the database
        files manually.

    --mariadb_port=<val>
        The port of the MariaDB.

    -y, --assumeyes
        Assume yes; assume that the answer to any question which would be asked
        is yes.

    --create_desktop_icon=<true | false>
        If true, create the desktop icons.

    --create_smprograms_icon=<true | false>
        If true, create the start menu folder.

    -h
        Display this help and exit.

EXAMPLES
    Install Application Platform Module (APM) and configure the installed
    products.
        setup install [option ...]

    Update Application Platform Module (APM).
        setup update [option ...]

    Set the domain name and port of the Apache HTTP Server.
        setup --apache_domain_name=localhost --apache_http_port=20080

    Set the HTTP port, shutdown port, AJP connector port, and SSL Redirect port
    of the Apache Tomcat.
        setup --tomcat_http_port=28080 --tomcat_shutdown_port=28005
            --tomcat_ajp_connector_port=28009 --tomcat_ssl_redirect_port=28443

    Set the HTTP port of the Ruby on Rails.
        setup --ror_http_port=23000

    Set the HTTP port of the Node.js.
        setup --nodejs_http_port=23001

    Set the port of the MariaDB.
        setup --mariadb_port=23306

    If you moved the installed package to another location, reconfigure the
    installation directory.
        setup --install_dir="C:\Program Files\Modplax-new"

ADVANCED USAGE
    If the installation directory to set up and the directory where the
    installed package exists are different, specify the directory of the
    installed package using the --installed_dir option.
        setup [command] --installed_dir="C:\Program Files\Modplax-external"
            [option ...]

        setup --trg_arch=x64
            --installed_dir="C:\Program Files\Modplax-external"
            --apache_http_port="20080"
            --tomcat_http_port="28080"
            --tomcat_shutdown_port="28005"
            --tomcat_ajp_connector_port="28009"
            --tomcat_ssl_redirect_port="28443"
            --ror_http_port="23000"
            --nodejs_http_port="23001"
            --mariadb_port="23306"
            --create_desktop_icon="true"
            --create_smprograms_icon="true"
            -y

    Change the database storage location.
        setup --mariadb_data_dir="C:\Program Files\Modplax\mariadb-data-new"

        CAUTION: If you set up using this option after installation, the
        database files will not be moved to the new path. Move the database
        files manually.

    Revert to the previous settings.
        setup restore

    Revert to the previous settings in the specified backup directory.
        setup restore --backup_dir="backup/yyyyMMdd.HHmmss.SSS"
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

* Apache Ant 1.9.11
* Apache HTTP Server 2.4.17
* Apache Tomcat 8.0.26
* HeidiSQL 10.1.0.5578
* JRE 8u60
* MariaDB 10.3.15
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
