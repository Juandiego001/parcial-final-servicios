# parcial-final-servicios
Contenido de archivos y scripts que contienen el parcial final del curso de servicios telemáticos con Oscar Mondragon.

# Link del repo del cliente
https://github.com/Juandiego001/cliente-api-parcial-servicios

<h1>Scripts</h1>
<h2>Firewall</h2>
<pre>
<code>
    systemctl status NetworkManager
    systemctl stop NetworkManager
    systemctl disable NetworkManager
    systemctl status firewalld
    systemctl start firewalld
    firewall-cmd --zone=public --add-masquerade
    firewall-cmd --zone=internal --add-masquerade
    firewall-cmd --zone=public --add-masquerade --permanent
    firewall-cmd --zone=internal --add-masquerade --permanent
    firewall-cmd --zone=public --add-forward-port=port=80:proto=tcp:toport=8080:toaddr=192.168.50.2
    firewall-cmd --zone=public --add-forward-port=port=80:proto=tcp:toport=8080:toaddr=192.168.50.2 --permanent
</code>
</pre>


<h2>Streama</h2>
<pre>
<code>
    yum install wget
    sudo yum install openjdk-8-jre
    wget https://github.com/dularion/streama/releases/download/v1.6.1/streama-1.6.1.war
    mkdir /home/vagrant/streama
    mv streama-1.6.1.war /home/vagrant/streama
    cd /home/vagrant/streama
    chmod +x streama-1.6.1.war
    java -jar streama-1.6.1.war
</code>
</pre>