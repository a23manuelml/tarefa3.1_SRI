## Servidor FTP vsftpd

O obxectivo desta tarefa é instalar o servidor FTP vsftpd nun equipo Ubuntu Server/Debian

Tomaremos a máquina gandalf dos exercicios anteriores.

Instala o paquete vsftpd e configurao da seguinte maneira:   
    
- Actualizamos o sistema

    ![imaxe1](imaxes/solapt0.1.png)

- Instalamos o servizo FTP

    ![imaxe2](imaxes/solapt0.2.png)

1. A mensaxe de benvida debe ser un ASCII Art da personaxe "Gandalf o Gris"

- Creamos un ficheiro onde gardaremos o ASCII Art

    ![imaxe3](imaxes/solapt1.1.png)

- Modificamos o ficheiro /etc/vsftpd.conf co noso banner

    ![imaxe4](imaxes/solapt1.2.png)

2. Habilita o permiso de escritura aos usuarios locais. Cando suban ficheiros, deben perder o permiso de execución para o grupo e para outros.

- Modificamos o ficheiro /etc/vsftpd.conf permitindo escritura e configurando os permisos dos ficheiros

    ![imaxe5](imaxes/solapt2.1.png)
3. Impide o acceso de todos os usuarios locais fora do seu diectorio home permitindo que poidan escribir so no directorio public_html do seu directorio home.

- Modificamos o ficheiro /etc/vsftpd.conf

    ![imaxe6](imaxes/solapt3.1.png)

- Configuramos os permisos para que os usuarios locais só poidan escribir en ~/public_html

    ![imaxe7](imaxes/solapt3.2.png)

4. Habilita o acceso anónimo no directorio /sauron, permitindo subir ficheiros e crear directorios. O propietario de tales ficheiros debe ser o usuario saruman

- Engadimos as opcións no ficheiro de configuración /etc/vsftpd.conf

    ![imaxe8](imaxes/solapt4.1.png)

- Creamos o directorio /sauron e configuramos os permisos

    ![imaxe9](imaxes/solapt4.2.1.png)
    ![imaxe10](imaxes/solapt4.2.2.png)

5. Instala un certificado dixital, para poder encriptar as transferencias. Probao instalando o paquete ftp-ssl nun cliente.

- Xeramos un certificado autofirmado

    ![imaxe11](imaxes/solapt5.1.1.png)
    ![imaxe12](imaxes/solapt5.1.2.png)

- Modificamos o arquivo de configuracion para poder usar SSl

    ![imaxe13](imaxes/solapt5.2.png)

6. Habilita as cuotas de disco dos usuarios, limitandoas a 10 Mb por usuario.

- Activamos as cotas de disco instalando quota:

    ![imaxe14](imaxes/solapt6.1.png)


7. Establece como tempo de inactividade máximo 60 segundos, e de tempo de inactividade nas transferencias 90 segundos.

- Modificamos o arquivo de configuración, quedando da seguinte forma:

    ![imaxe15](imaxes/solapt7.1.png)

8. Non poderán conectarse máis de 4 sesións simultaneas nin máis de 2 por enderezo IP do cliente.

- Modificamos o arquivo de configuración, quedando da seguinte forma:

    ![imaxe16](imaxes/solapt8.1.png)

9. Establece o ficheiro de log, en /var/log/ftp.log

- Modificamos o arquivo de configuración, quedando da seguinte forma:

    ![imaxe17](imaxes/solapt9.1.png)