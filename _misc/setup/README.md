# Setup on Windows 

### Setting up the *cocos* command

The *cocos* command is a cross-platform that provides the following support:

* creating a new project
* building a project
* running a project
* deploying a project

which implies that an IDE is not necessary when using the *cocos* command.

**Run setup**

Execute the *setup.py* script to set up the *cocos* command and the paths required for an Android build. NOTE: Configuring for Android plaform is not mandatory and can be done later when deploying on an Android platform.

```sh
C:\Software\Cocos2d-x\cocos2d-x-3.13.1>python setup.py

Setting up cocos2d-x...
->Check environment variable COCOS_CONSOLE_ROOT
  ->Search for environment variable COCOS_CONSOLE_ROOT...
    ->COCOS_CONSOLE_ROOT not found

  ->Add directory "C:\Software\Cocos2d-x\cocos2d-x-3.13.1\tools\cocos2d-console\bin" into PATH succeed!

  -> Add COCOS_CONSOLE_ROOT environment variable...
    ->Added COCOS_CONSOLE_ROOT=C:\Software\Cocos2d-x\cocos2d-x-3.13.1\tools\cocos2d-console\bin

->Check environment variable COCOS_X_ROOT
  ->Search for environment variable COCOS_X_ROOT...
    ->COCOS_X_ROOT not found

  ->Add directory "C:\Software\Cocos2d-x" into PATH succeed!

  -> Add COCOS_X_ROOT environment variable...
    ->Added COCOS_X_ROOT=C:\Software\Cocos2d-x

->Check environment variable COCOS_TEMPLATES_ROOT
  ->Search for environment variable COCOS_TEMPLATES_ROOT...
    ->COCOS_TEMPLATES_ROOT not found

  ->Add directory "C:\Software\Cocos2d-x\cocos2d-x-3.13.1\templates" into PATH succeed!

  -> Add COCOS_TEMPLATES_ROOT environment variable...
    ->Added COCOS_TEMPLATES_ROOT=C:\Software\Cocos2d-x\cocos2d-x-3.13.1\templates

->Configuration for Android platform only, you can also skip and manually edit your environment variables

->Check environment variable NDK_ROOT
  ->Search for environment variable NDK_ROOT...
    ->NDK_ROOT not found

  ->Search for command ndk-build in system...
    ->Command ndk-build not found

  ->Please enter the path of NDK_ROOT (or press Enter to skip):C:\Software\Android NDK\android-ndk-r12b
  -> Add NDK_ROOT environment variable...
    ->Added NDK_ROOT=C:\Software\Android NDK\android-ndk-r12b

->Check environment variable ANDROID_SDK_ROOT
  ->Search for environment variable ANDROID_SDK_ROOT...
    ->ANDROID_SDK_ROOT not found

  ->Search for command android in system...
    ->Command android not found

  ->Please enter the path of ANDROID_SDK_ROOT (or press Enter to skip):C:\Software\Android
  -> Add ANDROID_SDK_ROOT environment variable...
    ->Added ANDROID_SDK_ROOT=C:\Software\Android

->Check environment variable ANT_ROOT
  ->Search for environment variable ANT_ROOT...
    ->ANT_ROOT not found

  ->Search for command ant in system...
    ->Command ant not found

  ->Please enter the path of ANT_ROOT (or press Enter to skip):C:\Software\Apache Ant\apache-ant-1.9.7
    ->Error: "C:\Software\Apache Ant\apache-ant-1.9.7" is not a valid path of ANT_ROOT. Ignoring it.

Please restart the terminal or restart computer to make added system variables take effect
```

Note that there was an error in setting the "ANT_ROOT" environment variable as the path should be set to the "bin" directory, as "C:\Software\Apache Ant\apache-ant-1.9.7\bin", so define the "ANT_ROOT" environment variable. Also, to avoid the issues that could happen with spaces in the path, change the directory name from "Apache Ant" to "Apache-Ant" and update the path in "ANT_ROOT" environment variable to "C:\Software\Apache-Ant\apache-ant-1.9.7\bin".

Verify that the environment variables are added:

![](_misc/Environment%20Variables.PNG)

```sh
C:\Users\droid>cocos
Cocos collects data when the command-line tools are used for development. This data is examined in the aggregate only and is used to continually innovate and improve Cocos products. This data is anonymous and includes, but is not limited to, a unique hardware identifier, version number our software and information on which tools and/or services in Cocos products are being used and how they are being used. We take your privacy seriously and we do not share or sell any of this data. You can opt-out from sharing this data with us, but by sharing you help contribute to growth of Cocos.

Do you agree to sent the data? [Y]es, [N]o
N

C:\Software\Cocos2d-x\cocos2d-x-3.13.1\tools\cocos2d-console\bin\/cocos.py 2.1 - cocos console: A command line tool for Cocos2d-x.

Available commands:
        run              Compiles, deploy and run project on the target.
        gen-libs         Generate prebuilt libs of engine. The libs will be placed in 'prebuilt' folder of the engine root path.
        luacompile       Encrypt and/or compile lua files.
        deploy           Compile and deploy a project to a device/simulator.
        package          Manage package for cocos.
        compile          Compile projects to binary.
        gen-simulator    Generate Cocos Simulator.
        new              Creates a new project.
        jscompile        Compile and/or compress js files.
        gen-templates    Generate templates for Cocos Framework.

Available arguments:
        -h, --help                      Show this help information.
        -v, --version                   Show the version of this command tool.
        --ol ['en', 'zh', 'zh_tr']      Specify the language of output messages.

Example:
        cocos new --help
        cocos run --help
```

```sh
C:\Users\droid>cocos --help

C:\Software\Cocos2d-x\cocos2d-x-3.13.1\tools\cocos2d-console\bin\/cocos.py 2.1 - cocos console: A command line tool for Cocos2d-x.

Available commands:
        run              Compiles, deploy and run project on the target.
        gen-libs         Generate prebuilt libs of engine. The libs will be placed in 'prebuilt' folder of the engine root path.
        luacompile       Encrypt and/or compile lua files.
        deploy           Compile and deploy a project to a device/simulator.
        package          Manage package for cocos.
        compile          Compile projects to binary.
        gen-simulator    Generate Cocos Simulator.
        new              Creates a new project.
        jscompile        Compile and/or compress js files.
        gen-templates    Generate templates for Cocos Framework.

Available arguments:
        -h, --help                      Show this help information.
        -v, --version                   Show the version of this command tool.
        --ol ['en', 'zh', 'zh_tr']      Specify the language of output messages.

Example:
        cocos new --help
        cocos run --help
```

### Setting up for Android

**Downloads**

*Install ADT in Eclipse*

https://marketplace.eclipse.org/content/android-development-tools-eclipse

*Download Android NDK*

https://developer.android.com/ndk/downloads/index.html

*Download Apache Ant*

http://ant.apache.org/bindownload.cgi
