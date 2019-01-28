# Update Owncloud

sudo wget -nv https://download.owncloud.org/download/repositories/production/Ubuntu_16.04/Release.key -O Release.key

sudo  apt-key add - < Release.key

Run the following shell commands as root to add the repository and install from there.

sudo su
echo 'deb http://download.owncloud.org/download/repositories/production/Ubuntu_16.04/ /' > /etc/apt/sources.list.d/owncloud.list


sudo apt update && sudo apt upgrade

-->> fa gli aggiornamenti ma non aggiorna Owncloud 

Dopo aggiornamento di tutto owncloud funziona ma non si è aggiornato (versione 9.1.6)
Certbot sembra funzionare si è aggiornato alla versione 0.28 e dovrebbe rinnovare il certificato senza problemi

sudo apt autoremove  --> leggere cosa rimuove!!  //non l'ho fatto

per forzare aggiornamento pacchetto owncloud è necessario fare 

sudo apt-get dist-upgrade


cd /var/www/owncloud
sudo -u www-data php occ upgrade  //dovrebbe aggiornare a Owncloud 10.0.10


sudo do-release-upgrade  → per avviare aggiornamento della versione di ubuntu


dopo riavvia owncloud non si raggiunge

sudo service apache2 status
sudo service ufw status

a2dismod php7.0 a2enmod php7.2
sudo apt install php7.2-xml


So I changed in file /etc/apache2/sites-available/000-default.conf e 000-default-le-ssl.conf  the following:

DocumentRoot /var/www/html
to
DocumentRoot /var/www


sudo apt install -->
php-mbstring  php-intl  php-zip  php-gd  php-curl //php-ldap


/etc/apache2/apache2.conf

AllowOverride None
to:
AllowOverride All

su tutte le voci che compaiono


sudo apt autoremove  -->> leggere cosa rimuove!!!!

Personalizzazioni estetiche

Privacy Policy