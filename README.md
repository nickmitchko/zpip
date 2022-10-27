```
  _________ ___ ____  
 |__  /  _ \_ _|  _ \ 
   / /| |_) | || |_) |  
  / /_|  __/| ||  __/ 
 /____|_|  |___|_|    

  NAME
      zpip, an irispython pip wrapper

  SYNOPSIS
      zpip " [pip command] "

  DESCRIPTION
      zpip can be used like the python pip package but from the
      InterSystems terminal. 
      
      Use zpip just like any other pip command but wrap your 
      command with double-quotes. Usable in terminal and in app
      code.

  EXAMPLES
      
      install 1 package (requests): 
          NS> zpip "install requests"
      
      install multiple packages (requests twilio bs4)
          NS> zpip "install twilio bs4"
      
      install with target directory (numpy)
          NS> zpip "install --target '/usr/irissys/lib/python' numpy"

  LIMITATIONS
      zpip should be run as a %All user, other configurations are
      not in scope.

      zpip can only be used on InterSystem IRIS version >= 2022.1.

      zpip may work on 2021.2, but that version lacks key python
      features.

      zpip makes no guarantees of security. Install packages and run
      pip commands at your own risk!

      In general, irispython pip fails when packages require sudo, root, 
      or admin accessis required to install a package
```

![https://img.shields.io/github/v/release/nickmitchko/zpip](https://img.shields.io/github/v/release/nickmitchko/zpip)

## Install

```cos
%SYS> zpm "install zpip"
// OR
zpm:%SYS> install zpip
```

## Support for pip features

* This is a wrapper around `irispython -m pip`
* Wrapper means that any pip command **should** work
* No guarantees that all pip commands work
