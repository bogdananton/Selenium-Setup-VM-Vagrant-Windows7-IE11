# Install and run

## Using Github

```bash
git clone https://github.com/bogdananton/Selenium-Setup-VM-Win7-IE11.git
cd Selenium-Setup-VM-Win7-IE11
vagrant up --provision
```

Then access via GUI, go to "\\\\VBOXSVR\vagrant" and run "bootstrap.ps1" using PowerShell (or _fix the provision call in Vagrantfile_).

## Using Vagrant boxes

```
vagrant init bogdananton/Selenium-Setup-VM-Win7-IE11
vagrant up
```

Optional: map your host port to the guest's 4444
Access: http://{guest-IP}:4444/wd/hub
