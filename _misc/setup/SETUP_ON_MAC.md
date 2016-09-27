# Setting up on OS X

```sh
droid@Yamz:~/Software/Cocos2d-x/Cocos2d-x-3.13.1$ which python
/usr/bin/python
droid@Yamz:~/Software/Cocos2d-x/Cocos2d-x-3.13.1$ python --version
Python 2.7.6
droid@Yamz:~/Software/Cocos2d-x/Cocos2d-x-3.13.1$ ./setup.py

Setting up cocos2d-x...
->Check environment variable COCOS_CONSOLE_ROOT
  ->Search for environment variable COCOS_CONSOLE_ROOT...
    ->COCOS_CONSOLE_ROOT not found

  -> Add COCOS_CONSOLE_ROOT environment variable...
    ->Added COCOS_CONSOLE_ROOT=/Users/droid/Software/Cocos2d-x/Cocos2d-x-3.13.1/tools/cocos2d-console/bin

->Check environment variable COCOS_X_ROOT
  ->Search for environment variable COCOS_X_ROOT...
    ->COCOS_X_ROOT not found

  -> Add COCOS_X_ROOT environment variable...
    ->Added COCOS_X_ROOT=/Users/droid/Software/Cocos2d-x

->Check environment variable COCOS_TEMPLATES_ROOT
  ->Search for environment variable COCOS_TEMPLATES_ROOT...
    ->COCOS_TEMPLATES_ROOT not found

  -> Add COCOS_TEMPLATES_ROOT environment variable...
    ->Added COCOS_TEMPLATES_ROOT=/Users/droid/Software/Cocos2d-x/Cocos2d-x-3.13.1/templates

->Configuration for Android platform only, you can also skip and manually edit "/Users/droid/.bash_profile"

->Check environment variable NDK_ROOT
  ->Search for environment variable NDK_ROOT...
    ->NDK_ROOT not found

  ->Search for command ndk-build in system...
    ->Command ndk-build not found

  ->Please enter the path of NDK_ROOT (or press Enter to skip):/Users/droid/Software/Android-NDK/android-ndk-r12b
  -> Add NDK_ROOT environment variable...
    ->Added NDK_ROOT=/Users/droid/Software/Android-NDK/android-ndk-r12b

->Check environment variable ANDROID_SDK_ROOT
  ->Search for environment variable ANDROID_SDK_ROOT...
    ->ANDROID_SDK_ROOT not found

  ->Search for command android in system...
    ->Command android not found

  ->Please enter the path of ANDROID_SDK_ROOT (or press Enter to skip):/Users/droid/Software/Android
  -> Add ANDROID_SDK_ROOT environment variable...
    ->Added ANDROID_SDK_ROOT=/Users/droid/Software/Android

->Check environment variable ANT_ROOT
  ->Search for environment variable ANT_ROOT...
    ->ANT_ROOT not found

  ->Search for command ant in system...
    ->Command ant not found

  ->Please enter the path of ANT_ROOT (or press Enter to skip):/Users/droid/Software/Apache-Ant/apache-ant-1.9.7/bin
  -> Add ANT_ROOT environment variable...
    ->Added ANT_ROOT=/Users/droid/Software/Apache-Ant/apache-ant-1.9.7/bin


A backup file "/Users/droid/.bash_profile.backup" is created for "/Users/droid/.bash_profile".

Please execute command: "source /Users/droid/.bash_profile" to make added system variables take effect
droid@Yamz:~/Software/Cocos2d-x/Cocos2d-x-3.13.1$ source /Users/droid/.bash_profile
```

Verify that the environment variables are added in *~/.bash_profile*

```sh
droid@Yamz:~/Software/Cocos2d-x/Cocos2d-x-3.13.1$ cat ~/.bash_profile
#export CLICOLOR=1
#export LSCOLORS=GxFxCxDxBxegedabagaced

export PS1="\[\033[36m\]\u\[\033[m\]@\[\033[32m\]\h:\[\033[33;1m\]\w\[\033[m\]\$ "
export CLICOLOR=1
export LSCOLORS=ExFxBxDxCxegedabagacad
alias ls='ls -GFh'

# Add environment variable COCOS_CONSOLE_ROOT for cocos2d-x
export COCOS_CONSOLE_ROOT=/Users/droid/Software/Cocos2d-x/Cocos2d-x-3.13.1/tools/cocos2d-console/bin
export PATH=$COCOS_CONSOLE_ROOT:$PATH

# Add environment variable COCOS_X_ROOT for cocos2d-x
export COCOS_X_ROOT=/Users/droid/Software/Cocos2d-x
export PATH=$COCOS_X_ROOT:$PATH

# Add environment variable COCOS_TEMPLATES_ROOT for cocos2d-x
export COCOS_TEMPLATES_ROOT=/Users/droid/Software/Cocos2d-x/Cocos2d-x-3.13.1/templates
export PATH=$COCOS_TEMPLATES_ROOT:$PATH

# Add environment variable NDK_ROOT for cocos2d-x
export NDK_ROOT=/Users/droid/Software/Android-NDK/android-ndk-r12b
export PATH=$NDK_ROOT:$PATH

# Add environment variable ANDROID_SDK_ROOT for cocos2d-x
export ANDROID_SDK_ROOT=/Users/droid/Software/Android
export PATH=$ANDROID_SDK_ROOT:$PATH
export PATH=$ANDROID_SDK_ROOT/tools:$ANDROID_SDK_ROOT/platform-tools:$PATH

# Add environment variable ANT_ROOT for cocos2d-x
export ANT_ROOT=/Users/droid/Software/Apache-Ant/apache-ant-1.9.7/bin
export PATH=$ANT_ROOT:$PATH
```

### Using the *cocos* command

```sh
droid@Yamz:~$ which cocos
/Users/droid/Software/Cocos2d-x/Cocos2d-x-3.13.1/tools/cocos2d-console/bin/cocos

droid@Yamz:~$ cocos
Cocos collects data when the command-line tools are used for development. This data is examined in the aggregate only and is used to continually innovate and improve Cocos products. This data is anonymous and includes, but is not limited to, a unique hardware identifier, version number our software and information on which tools and/or services in Cocos products are being used and how they are being used. We take your privacy seriously and we do not share or sell any of this data. You can opt-out from sharing this data with us, but by sharing you help contribute to growth of Cocos.

Do you agree to sent the data? [Y]es, [N]o
N

/Users/droid/Software/Cocos2d-x/Cocos2d-x-3.13.1/tools/cocos2d-console/bin/cocos.py 2.1 - cocos console: A command line tool for Cocos2d-x.

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
	-h, --help			Show this help information.
	-v, --version			Show the version of this command tool.
	--ol ['en', 'zh', 'zh_tr']	Specify the language of output messages.

Example:
	cocos new --help
	cocos run --help
  
droid@Yamz:~$ cocos --help

/Users/droid/Software/Cocos2d-x/Cocos2d-x-3.13.1/tools/cocos2d-console/bin/cocos.py 2.1 - cocos console: A command line tool for Cocos2d-x.

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
	-h, --help			Show this help information.
	-v, --version			Show the version of this command tool.
	--ol ['en', 'zh', 'zh_tr']	Specify the language of output messages.

Example:
	cocos new --help
	cocos run --help  
```
