sudo apt-get update\
&& sudo apt install python-minimal -y\
&& sudo apt-get install python3-pip -y\
&& sudo apt-get install python-pip -y\
&& pip install paramiko PyYAML jinja2 httplib2 passlib\
&& sudo apt-get install tango-common -y\
&& sudo apt-get -y install vim dnsutils curl\
&& curl -fsSL https://get.docker.com/ | sh || apt-get -y install docker.io\
&& sudo usermod -aG docker $(whoami | awk '{print $1}')\
&& mkdir -p ~/netflix-proxy\
&& cd ~/netflix-proxy\
&& curl -fsSL https://github.com/tycoonge/netflix-proxy/archive/latest.tar.gz | gunzip - | tar x --strip-components=1\
&& ./build.sh
