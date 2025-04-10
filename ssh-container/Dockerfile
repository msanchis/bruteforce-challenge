FROM ubuntu:22.04

# Actualizar e instalar openssh-server, sudo y vim
RUN apt-get update && apt-get install -y openssh-server sudo vim zip netcat

# Crear directorio para llaves SSH
RUN mkdir /var/run/sshd

# Configurar para permitir conexiones SSH con contraseña
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -i 's/#PasswordAuthentication yes/PasswordAuthentication yes/' /etc/ssh/sshd_config

# Crear y configurar el banner SSH con pista sobre el usuario
RUN echo "********************************************" > /etc/issue.net
RUN echo "* CTF Challenge Server                    *" >> /etc/issue.net
RUN echo "* Hint: User starts with 'a' and ends     *" >> /etc/issue.net
RUN echo "* with 'r'. Only 3 letters. Try to guess! *" >> /etc/issue.net
RUN echo "********************************************" >> /etc/issue.net
RUN echo "Banner /etc/issue.net" >> /etc/ssh/sshd_config

# Crear usuario y establecer contraseña
RUN useradd -m -s /bin/bash abr
RUN echo "abr:qwerty" | chpasswd
RUN echo "root:p@ssw0rd" | chpasswd

# Agregar el usuario al grupo sudo
RUN usermod -aG sudo abr

# Configurar sudo para permitir a abr ejecutar vim sin contraseña
RUN echo "abr ALL=(ALL) NOPASSWD: /usr/bin/vim" >> /etc/sudoers

# Crear archivo user.txt en el home del usuario abr
RUN echo "CTF_ABR{BruT3_F0rc3_F0R_C4m3_1N}" > /home/abr/user.txt
RUN chown abr:abr /home/abr/user.txt
RUN chmod 644 /home/abr/user.txt

RUN echo "password1" > /root/passwords && \
    echo "p4ssw0rd" >> /root/passwords && \
    echo "letmein" >> /root/passwords && \
    echo "123456" >> /root/passwords && \
    echo "qwerty" >> /root/passwords && \
    echo "admin" >> /root/passwords && \
    echo "welcome" >> /root/passwords && \
    echo "monkey" >> /root/passwords && \
    echo "dragon" >> /root/passwords && \
    echo "football" >> /root/passwords && \
    echo "iloveyou" >> /root/passwords && \
    echo "starwars" >> /root/passwords && \
    echo "123123" >> /root/passwords && \
    echo "whatever" >> /root/passwords && \
    echo "trustno1" >> /root/passwords && \
    echo "passw0rd" >> /root/passwords && \
    echo "letme1n" >> /root/passwords && \
    echo "admin123" >> /root/passwords && \
    echo "654321" >> /root/passwords && \
    echo "superman" >> /root/passwords && \
    echo "batman" >> /root/passwords && \
    echo "secret123" >> /root/passwords && \
    echo "masterkey" >> /root/passwords && \
    echo "ninja" >> /root/passwords && \
    echo "welcome1" >> /root/passwords && \
    echo "rootroot" >> /root/passwords && \
    echo "zaq12wsx" >> /root/passwords && \
    echo "baseball" >> /root/passwords && \
    echo "shadow" >> /root/passwords && \
    echo "sunshine" >> /root/passwords && \
    echo "password123" >> /root/passwords && \
    echo "charlie" >> /root/passwords && \
    echo "donald" >> /root/passwords && \
    echo "michael" >> /root/passwords && \
    echo "jordan23" >> /root/passwords && \
    echo "cheese" >> /root/passwords && \
    echo "pepperoni" >> /root/passwords && \
    echo "pokemon" >> /root/passwords && \
    echo "1234abcd" >> /root/passwords && \
    echo "1q2w3e4r" >> /root/passwords && \
    echo "asdfgh" >> /root/passwords && \
    echo "qazwsx" >> /root/passwords && \
    echo "pass1234" >> /root/passwords && \
    echo "keyboard" >> /root/passwords && \
    echo "hottie" >> /root/passwords && \
    echo "killer" >> /root/passwords && \
    echo "thunder" >> /root/passwords && \
    echo "trustme" >> /root/passwords && \
    echo "matrix" >> /root/passwords && \
    echo "freedom" >> /root/passwords && \
    echo "computer" >> /root/passwords && \
    echo "internet" >> /root/passwords && \
    echo "access" >> /root/passwords && \
    echo "wizard" >> /root/passwords && \
    echo "gandalf" >> /root/passwords && \
    echo "frodo" >> /root/passwords && \
    echo "sauron" >> /root/passwords && \
    echo "mordor" >> /root/passwords && \
    echo "middleearth" >> /root/passwords && \
    echo "yoda" >> /root/passwords && \
    echo "vader" >> /root/passwords && \
    echo "skywalker" >> /root/passwords && \
    echo "rebellion" >> /root/passwords && \
    echo "empire" >> /root/passwords && \
    echo "deathstar" >> /root/passwords && \
    echo "lightsaber" >> /root/passwords && \
    echo "hanSolo" >> /root/passwords && \
    echo "chewie" >> /root/passwords && \
    echo "wookie" >> /root/passwords && \
    echo "enterprise" >> /root/passwords && \
    echo "kirk" >> /root/passwords && \
    echo "spock" >> /root/passwords && \
    echo "picard" >> /root/passwords && \
    echo "data" >> /root/passwords && \
    echo "borg" >> /root/passwords && \
    echo "qcontinuum" >> /root/passwords && \
    echo "warpdrive" >> /root/passwords && \
    echo "stardust" >> /root/passwords && \
    echo "trekfan" >> /root/passwords && \
    echo "42isanswer" >> /root/passwords && \
    echo "deepthought" >> /root/passwords && \
    echo "arthur" >> /root/passwords && \
    echo "zaphod" >> /root/passwords && \
    echo "marvin" >> /root/passwords && \
    echo "trillian" >> /root/passwords && \
    echo "galaxyquest" >> /root/passwords && \
    echo "alien" >> /root/passwords && \
    echo "predator" >> /root/passwords && \
    echo "matrixreloaded" >> /root/passwords && \
    echo "neo" >> /root/passwords && \
    echo "morpheus" >> /root/passwords && \
    echo "trinity" >> /root/passwords && \
    echo "smith" >> /root/passwords && \
    echo "johnwick" >> /root/passwords && \
    echo "keanu" >> /root/passwords && \
    echo "bulletproof" >> /root/passwords && \
    echo "h4ck3r" >> /root/passwords && \
    echo "backdoor" >> /root/passwords && \
    echo "1337h4x" >> /root/passwords && \
    echo "cyberpunk" >> /root/passwords && \
    echo "ctfhunter" >> /root/passwords && \
    echo "xssxss" >> /root/passwords && \
    echo "buffer0ver" >> /root/passwords && \
    echo "injection" >> /root/passwords && \
    echo "secre7" >> /root/passwords && \
    echo "p@ssw0rd" >> /root/passwords

RUN zip -e -P 'p@ssw0rd' /tmp/backup.zip /root/passwords
RUN chown abr:abr /tmp/backup.zip

# Crear archivo root.txt en el directorio de root
RUN echo "CTF_ABR{N3w_W4y_T0_G3t_Pr1V1l3g3s}" > /root/root.txt
RUN chmod 600 /root/root.txt

# Puerto SSH
EXPOSE 22

# Iniciar el servicio SSH
CMD ["/usr/sbin/sshd", "-D"]
