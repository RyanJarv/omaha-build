WIP, this may not work for you currently.

Note: You will need packer >= 1.2.3 to avoid an issue where imported vagrant box's are empty

### Build vs2015community box
packer build --only=virtualbox-iso packer.json

### Bring up vagrant box
```
vagrant box add -n vs2015community ./<path to packer output>
vagrant up
vagrant reload
```

### Manual steps
* Install C:\tmp\pywin32.exe
* Install C:\tmp\scons.exe
* In cmd prompt:
  * `cd C:\omaha\omaha`
  * `C:\Program Files (x86)\Microsoft Visual Studio 14.0\VC\vcvarsall.bat`
  * `hammer`
