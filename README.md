# hxcpp (NX support?)

This fork of hxcpp has all the modifications needed to compile Haxe for the Nintendo Switch.
[Code taken from an old fork of hxcpp for the Nintendo Switch.](https://github.com/retronx-team/switch-hxcpp)

More work is needed to get a usable executable on the console. perhaps I will do so in a short time, but I'm not really interested in using Haxe on the Nintendo Switch **for now**, I am interested in using Haxe on the Wii U through my [HxCompileU project](https://github.com/Slushi-Github/hxCompileU), which uses [Reflaxe/C++](https://github.com/SomeRanDev/reflaxe.CPP) (an alternative to hxcpp).

-----

[![Build Status](https://dev.azure.com/HaxeFoundation/GitHubPublic/_apis/build/status/HaxeFoundation.hxcpp?branchName=master)](https://dev.azure.com/HaxeFoundation/GitHubPublic/_build/latest?definitionId=3&branchName=master)

hxcpp is the runtime support for the c++ backend of the [haxe](http://haxe.org/) compiler. This contains the headers, libraries and support code required to generate a fully compiled executable from haxe code.


# building the tools

```
REPO=$(pwd)
cd ${REPO}/tools/run
haxe compile.hxml
cd ${REPO}/tools/hxcpp
haxe compile.hxml
cd $REPO
```

# cppia

You first need to build the cppia host.

```
REPO=$(pwd)
cd ${REPO}/project
haxe compile-cppia.hxml
cd $REPO
```

Then you can do `haxelib run hxcpp file.cppia`.
