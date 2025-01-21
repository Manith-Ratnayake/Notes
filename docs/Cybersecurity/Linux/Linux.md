
    • ls                                                       
    • pwd                                                  
    • cd          
                                              
    • rm                                                 
    • rmdir 
    • rm -r {dir}
    
    • cp {src} {dest}
    • mv {}  ./Path
    • touch {name}

    • cat  {file}
    • more {file}
    • nano {file}

    • ifconfig 
    • grep {conetnt} {filename}
    • locate {filename}
    
    • uname -i 
    • hostname 
    • uptime
    • sudo apt-get 
    • ip a
    • ip r
    • ip n


    • ping -s 1300 -f {ip address}
    • hping3 -S -V --flood {ip address}
    • hping3 --tracerout -V -1 {domain} 
    • hping3 --traceout -V -p 80  -S -A --baseport 1337 {doamain}
    
    • ptunnel -p {ip address} -lp 8000 -da {ip} -dp  22
    • tcpdump -i any icmp
    • ssh -p 8080 {domain@localhost}
    • grep -Hnri tree | ???
    
    • nmap --source-port {ip}
    • nmap -D RND:10
    • masscan -p80,443,22, {ip} --rate=1000
    • masscan {ip} -p0-65535 --rate=1000 --randomize-hosts
    
    • sl
    • cat /dev/urandom
    • alias ls = "cat /dev/urandom"
    
    • whois {domain}
    • whatweb {domain}
    • curl -i {link}
    
    • gobuster dir -u {domain} -w {wordlist file}
    • apt install seclist
    • apt install wget
    
    • gobuster dns -d {website} -w {wordlist file}
    • apt install sublist3r
    • sublist3r -d {domain}
    
    • wpscan --url {domain} --enumerate -u
    • wpscan --url {domain} --enumerate -t
    • wpscan --url {domain} --enumerate vp,vt --plugins-detection aggressive 
    • wpscan --url {domain} --api-token {api} --enumerate  u 
    
    • amass enum -d {domain}
    • amass enum -passive -d {domain}
    
    • git clone {searchploit url}
    • searchploit wordpress plugings
    • searchploit ssh
    
    • /bin/bash
    • /bin/bash -p
    • /bin/bash
    • sudo chmod +s /bin/bash
    • bash -p
    
    • tcpdump -w capture.pcap -i eth0
    • tcpdump -i eth0 -c 100
    
    • tshark -V -c 1 -i  eth0
    • tshark -Y'http.request.method == "GET" -I eth0
    • timeout 15 tshark -i eth0 -w tshark.pcap
    • tshark -r tshark.pcap -qz endpoints,ip 
    • tshark -r tshark.pcap -qz follow,tcp,ascii7
    • tshark -e ip.src -e ip.dst -e frame.protocols -T fields -r capture.pcap
    
    • ssh networkchuck@{ip}
    • ssh networkchuck@{ip}
    • ssh networkchuck@{ip} 'whoami'
    • ssh -D 1337 -C -q -N root@{ip} 


Managing users

    • sudo adduser {name}
    • cat /etc/passwd
    • sudo cat /etc/shadow
    
    • sudo useradd {name}                                  #Lazy
    • sudo usermod {name} --shell /bin/bash
    • sudo usermod -l {name/s}
    • sudo useradd {name} -m
    • su -
    • sudo visudo
    • sudo userdel {name}
    • sudo groupadd {name}
    • cat /etc/group
    • groups
    • %{groupname} ALL = NOPASSWD:ALL
    • sudo usermod -aG {name}
    • sudo gpasswd -d {name/s}
    • sudo groupdel {name}
    

Linux Package Management


    Ø dpkg - low level
    Ø apt install - high level


    • dpkg -i 
    • sudo apt install pidgen
    • sudo apt edit-sources
    • sudo apt list
    • sudo apt --installed | grep {name}
    • sudo apt search 
    • sudo apt remove
    • sudo apt purge {app}
    • dpkg -l | grep nmap
    • sudo aptitude
    • sudo snap install --classic code
    • git clone {turbolist3r}
    • python turbolist3r.py  -d hackthebox.eu


Daemons

    • ps -aux
    • ps -aux | grep {sublime/ntp}
    • pstree
    • sudo systemctl stop {sshd}
    • sudo systemctl start {sshd}
    • sudo systemctl restart {sshd/ systemd- journald}
    • sudo systemctl reload-or-restart {sshd}
    • sudo systemctl disable {sshd/ntp}                                   #when rebooting
    • sudo systemctl status{sshd}
    • sudo systemctl enable {sshd}
    • sudo systemctl is-active {sshd}
    • sudo systemctl list-units
    • sudo systemctl list-units -t service
    • sudo systemctl list-units | grep {nginx/journal}
    • sudo systemctl list-units --all | grep nginx
    • sudo systemctl list-unit-files | grep nginx
    • sudo systemctl is-enable {sshd}
    • sudo journal ctl -xe


Processors

    • ps
    • ps -u {user} | grep {firefox}
    • pgrep {firefox}
    • kill {id}
    • ps -aux
    • top
    • htop
    • jobs
    • bg {id}
    • ps -ax
    • kill -l
    • sleep 900 &
    • pkill -9 {ping/}

Sever

    • python -m http.server {port}  #if not specified, default
    • php -S 127.0.0.1:8085
    • npx http-server -p  8086
    • systemctl start apache2
    • sudo nano /etc/apache2/ports.conf
        ○ Listen {port number}
    • curl localhost:7600
    • curl -o {website} localhost:8080
        ○ ls
    • curl -I localhost:8080
    • curl -v localhost:8080
    • wget localhost:7600


Shortcuts

    • cd /usr/var/sniffjoke/generic
    • cd ../../..
    • cd -
    • echo $OLDPWD
    • ls -l
    • ls -al
    • ll
    • la
    • alias lumos="ls"
    • nano .bashrc
    • CTRL + A               #begaining
    • CTRL + E                # end
    • CTRL + U               # delete everything before
    • CTRL + Y               # paste everything
    • CTRL + K               # delete everything after
    • ALT + BACKARROW   # Word by word delete
    • CTRL + X + E        # nano edit
    • sudo !!
    • TAB TAB                     
    • sudo tail -f /var/log/auth.log
    • CTRL + R

Files
    
    cat > file.txt
    cat << EOF > {filename} 
    .BAK
    mkdir -p {dir}
    tree
    cp -r {dir/dir/}
    ls {dir}
    rm -rf
    sudo rm -rf --no-preserve-root/
    nano {nameFile}.sh
    
    
    

    
