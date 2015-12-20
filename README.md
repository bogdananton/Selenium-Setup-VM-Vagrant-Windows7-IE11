## Build from Github and run

```bash
# clone repo
git clone https://github.com/bogdananton/Selenium-Setup-VM-Win7-IE11.git
cd Selenium-Setup-VM-Win7-IE11

# start instance
vagrant up
# then install VirtualBox Guest Additions 5.0 and reboot

# provision
# method 1 (vagrant provision)
# running "vagrant provision" will fail (@todo fix) 

# method 2 (vagrant ssh then use powershell). follow steps from http://asciinema.org/a/6dzvtvw7u6pknr65cenlg07tk 
vagrant ssh
copy \\VBOXSVR\vagrant\bootstrap.ps1 c:\bootstrap.ps1
powershell -NonInteractive -File c:\bootstrap.ps1

# method 3 (manually)
# access via GUI, go to "\\VBOXSVR\vagrant" and run "bootstrap.ps1" using PowerShell

# create a startup task to start Selenium at boot (should run "php c:\Selenium-Setup\selenium-setup start")


```

----

The box was created by running:<br/>
`vagrant package --base selenium-setup-windows7_x64-ie11 --output selenium-setup-windows7_x64-ie11`

----

Once started, the provision shouldn't require babysitting, as seen in http://asciinema.org/a/6dzvtvw7u6pknr65cenlg07tk


## Run already build image

```
vagrant init bogdananton/Selenium-Setup-VM-Win7-IE11
vagrant up
```

----

Check to see that the process is running; start it by running "c:\tools\php\php.exe c:\Selenium-Setup\selenium-setup start".

Open "http://localhost:4444/wd/hub" to check if the server is accessible. Change port to 4446 if accessing from outside.

----

Disk space requirements:
 - base box: 4.6GB
 - running instance: 11GB

----

## Browsers

* Opera 34.0.2036.25 stable (December 6, 2015)
* Chrome 47.0.2526.105 m (December 15, 2015)
* Firefox 43.0.1 (December 18, 2015)
* Internet Explorer 11.0.9600.17843 (December 19, 2015)
