## XiaomiToolV2 Fork for Linux

This is  a fork of the source code of the Xiaomi modding tool XiaomiTool V2 (www.xiaomitool.com).

**This tool is especially useful for unlocking the bootloader of Xiaomi devices from Linux.**

  - The original repo is abandoned and it needed a small correction to make it run on linux.
  - The modifications are mainly based on the original [issue 23](https://github.com/francescotescari/XiaoMiToolV2/issues/23).

### Prepare your phone before proceeding to an Unlocking

Check this [wiki](https://github.com/tkapias/XiaoMiToolV2/wiki/Unlock-Bootloader-on-any-Xiaomi-Phones).

### Building and Running 

Debian based linux:

```
sudo apt install git
git clone https://github.com/tkapias/XiaoMiToolV2.git
cd XiaoMiToolV2
```

You need the Java JDK v11.0.8, the version provided by your distro is probably higher.

```
wget -v -O openjdk-11.0.8.tar.gz https://builds.openlogic.com/downloadJDK/openlogic-openjdk/11.0.8%2B10/openlogic-openjdk-11.0.8%2B10-linux-x64.tar.gz
tar xvf openjdk-11.0.8.tar.gz && mv openlogic-openjdk-11.0.8+10-linux-x64/ openjdk-11.0.8
JAVA_HOME=$(pwd)/openjdk-11.0.8 ./gradlew build
JAVA_HOME=$(pwd)/openjdk-11.0.8 ./gradlew run
```
To use the tool you just need to select the correct Region and to log in to your Xiaomi account when asked.
