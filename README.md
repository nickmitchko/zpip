```
  _________ ___ ____  
 |__  /  _ \_ _|  _ \ 
   / /| |_) | || |_) |  
  / /_|  __/| ||  __/ 
 /____|_|  |___|_|    

  NAME
      zpip, an irispython pip wrapper
```


![https://img.shields.io/github/v/release/nickmitchko/zpip](https://img.shields.io/github/v/release/nickmitchko/zpip)

---

## Getting Started

```cos
%SYS> zpm "install zpip"
// OR
zpm:%SYS> install zpip
```

## Install Package

```cos
%SYS> zpip "install <package>"
```

## Uninstalling Package

> Note! You must use `uninstall -y` for the command to work correctly.

```
%SYS> zpip "uninstall -y <package>"
```


## Support for pip features

* This is a wrapper around `irispython -m pip`
* Wrapper means that any pip command **should** work
* No guarantees that all pip commands work. User input not supported
  * For example, any interactive command needs `-y` to function. eg;<br> `zpip "uninstall -y <package>"`


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

# DOCKER Support
### Prerequisites   
Make sure you have [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [Docker desktop](https://www.docker.com/products/docker-desktop) installed.    
### Installation    
Clone/git pull the repo into any local directory
```
$ git clone https://github.com/nickmitchko/zpip.git
```
Open the terminal in this directory and run:
```
$ docker-compose build
```
Run IRIS container with your project:
```
$ docker-compose up -d
```
Test from docker console
```
$ docker-compose exec iris1 iris session iris
USER>
```
or using **WebTerminal**
```
http://localhost:42773/terminal/
```