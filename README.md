### Bye Bye System-Config-*, Hello Web Console

I’m starting to use RHEL 8 and trying to get myself familiar with it. Coming from a UI friendly background and getting started with RHEL was challenging and learning experience. It took me a while to get familiar with terminal and adapt open it every now and then for every single thing.

It was not this simple initially when I started my journey with RHEL, 2 years back however system-config-* tools were a big relief for me as I was afraid to change configuration files manually and figure out different parameters. But now, it has been deprecated in RHEL 8 and replaced by a cool tool called cockpit. I’m surprise to know how friendly and cool it is.

So, let’s get started and get our hands dirty with this cool Web console tool:

- Check if the package is already installed:

~~~
# rpm -qa|grep -I cockpit
~~~

- If it’s not installed, simply run following command to install it:

~~~
# yum install cockpit 
~~~

- Let’s enable the service: 

~~~
# systemctl enable --now cockpit.socket 
~~~

- Open your favourite Brower, chrome in my case and put:

<https://server_name_or_IP:9090> or <https://localhost:9090>

- Sing the self-signed certificate and you would be prompted for username/password:
