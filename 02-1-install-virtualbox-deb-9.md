```$xslt
sudo apt-get -y update
sudo apt-get -y upgrade
```

```$xslt
sudo echo "deb http://download.virtualbox.org/virtualbox/debian stretch contrib" >> /etc/apt/sources.list
```

```$xslt
sudo apt-get install software-properties-common
sudo add-apt-repository "deb http://download.virtualbox.org/virtualbox/debian stretch contrib"
```

```$xslt
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
```

```$xslt
sudo apt-get update
sudo apt-get install virtualbox-6.0

```