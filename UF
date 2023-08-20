splunk universal forwarder installation

Step-1 : Become root user
1.Login as "root" user using below command
```bash
sudo su 
```
Step-2 : Create new user (splunk), directories & permissions

2.Create user & group

```bash
useradd splunk
groupadd splunk
```
3.Create directory

```bash
mkdir /opt/splunkforwarder
```

4.Change the ownership of the created directory to the new user **"splunk"** (hereafter will be called as splunk user)

```bash
chown -R splunk:splunk /opt/splunkforwarder/
```


5.Verify the ownership of the directory
```bash
ll /opt/splunkforwarder
```

6.Install **"wget"**
```bash
yum install wget
```

Step-3 : Splunk Enterprise Installation

7.Switch to splunk user 

```bash
sudo su - splunk
```

8.Navigate to splunk user home directory

```bash
cd /home/splunk
```

9.Download Splunk Universal Forwarder (Based on the version you want, you can get this command from [https://www.splunk.com/en_us/download/splunk-enterprise/thank-you-enterprise.html](https://www.splunk.com/en_us/download/universal-forwarder/thank-you-universalforwarder.html))

```bash
wget -O splunkforwarder-9.1.0.1-77f73c9edb85-Linux-x86_64.tgz "https://download.splunk.com/products/universalforwarder/releases/9.1.0.1/linux/splunkforwarder-9.1.0.1-77f73c9edb85-Linux-x86_64.tgz"
```

10.Extract the tar package

```bash
tar -xvf splunkforwarder-9.1.0.1-77f73c9edb85-Linux-x86_64.tgz -C /opt/
```

11.Navigate to Splunk bin directory

```bash
cd /opt/splunkforwarder/bin
```

12.Start the Splunk with accepting license & setting the default username (admin) passing the passowrd (Pa55word)

```bash
./splunk start --accept-license --no-prompt --answer-yes --seed-passwd Pa55word
```

**Note:** In above step installer will ask you to create username and password, please keep these credentials safe (These are the admin credentials which you will use to Manage Splunk)

At this point, universal Forwarder is installed in your linux server

Step-4: Configure Splunk to run at boot time

13.Exit from splunk user & sign in as **root** user

``` bash
exit
sudo su 
```

14.Enable boot start

``` bash
/opt/splunkforwarder/bin/splunk enable boot-start -user splunk
```
