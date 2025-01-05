# OUTIL DE SUPERVISION : ZABBIX et GRAFANA

Un outil de supervision informatique est un logiciel conçu pour surveiller, analyser et gérer l'infrastructure informatique d'une organisation. Ces outils permettent de :
•	Surveiller en temps réel les différents composants du système informatique, tels que les serveurs, les réseaux, les applications et les bases de données15.
•	Détecter et alerter rapidement sur les anomalies, pannes ou dysfonctionnements potentiels15.
•	Collecter et analyser des données sur les performances et la disponibilité des systèmes4.
•	Générer des rapports et des visualisations pour faciliter la compréhension de l'état du système2.
•	Automatiser certaines tâches de maintenance et de résolution de problèmes
Dans notre cas d’étude le choix se portera sur deux outils incontournables :
•	Zabbix 
•	Grafana
 #                                 INSTALLATION ZABBIX
Choix de notre plateforme : Debian(linux)
Accéder au site de zabbix pour le choix de l’installation approprié selon le système d’exploitation :

https://www.zabbix.com/fr/download?zabbix=7.2&os_distribution=debian&os_version=12&components=server_frontend_agent&db=mysql&ws=apache
  
# Les commandes d’installation zabbix sous debian :

	e/zabbix-release_latest_7.2+debian12_all.deb
	dpkg -i zabbix-release_latest_7.2+debian12_all.deb
	apt update
	apt install zabbix-server-mysql zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts zabbix-agent
	apt install mariadb-server
	mysql_secure_installation
	mysql -uroot -p
	zcat /usr/share/zabbix/sql-scripts/mysql/server.sql.gz | mysql --default-character-set=utf8mb4 -uzabbix -p zabbix
	mysql -uroot -p
	nano /etc/zabbix/zabbix_server.conf
	systemctl restart zabbix-server zabbix-agent apache2
	systemctl enable zabbix-server zabbix-agent apache2
	apt install locales –y
	exit
	apt install locales –y
	sudo apt install locales -y
	apt install locales -y
	dpkg-reconfigure locales
	rboot
	hostname -I 
	192.168.8.12

# Lien par défaut de connexion : (en http sur le port 80 par défaut)

http://192.168.8.12/zabbix/zabbix.php?action=dashboard.view&dashboardid=1 
