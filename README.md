drozer
======

Mercury is a security assessment framework for the Android platform. It allows you to dynamically interact with the IPC endpoints exported by an application installed on a device.

Mercury is open source software, maintained by MWR InfoSecurity, and can be downloaded from:

    mwr.to/mercury

Mercury provides similar functionality to a number of static analysis tools, such as aapt, but offers far more flexibility by allowing you to interact with these endpoints from the context of an unprivileged application running on the same device. The Android sandbox is designed to restrict the access of an unprivileged application to other applications, and the underlying device, without requesting appropriate permissions. You will be surprised how much access you actually have...


Installing
----------

The drozer agent can be built in Eclipse or using the ant build system.

You need to make some other sources available for building:

  * $ <workspace>/agent => this directory
  * $ <workspace>/jdiesel => cloned from https://github.com/mwrlabs/jdiesel
  * $ <workspace>/mwr-android => cloned from https://github.com/mwrlabs/mwr-android
  * $ <workspace>/mwr-tls => cloned from https://github.com/mwrlabs/mwr-tls

You must also update the Git submodules in jdiesel:

  * `$ cd jdiesel`
  * `$ git submodule init && git submodule update`

Then, either import the projects into Eclipse and build, or run:

  * `$ cd agent`
  * `$ ant debug`

It is recommended to install the drozer agent using adb:

  * `$ adb install bin/agent.apk`


License
-------

drozer is released under a 3-clause BSD License. See LICENSE for full details.


Contacting the Project
----------------------

drozer is Open Source software, made great by contributions from the community.

For full source code, to report bugs, suggest features and contribute patches please see our Github project:

  https://github.com/mwrlabs/drozer

Bug reports, feature requests, comments and questions can be submitted sent to:

  drozer [at] mwrinfosecurity.com

Follow the latest drozer news, follow the project on Twitter:

  @mwrdrozer
