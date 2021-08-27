# Zabbix-docker-facil
Instalação fácil do zabbix 5.4 utilizando o docker
Este script em shell, automatiza a instalação do zabbix server utilizando containers.

Pré requesitos:

Docker Engine instalado (disponível em: https://docs.docker.com/engine/install/)
Conhecimentos básicos em Docker (Comandos básicos como: docker run, exec, pull, network)
Contato anterior com o sistema zabbix
Antes de realizar a execução do script é necessário criar um rede em modo bridge, para suportar os containers do zabbix:
docker network create rede-interna --subnet 172.16.0.0/29

Após o dowload do script, devemos executa-lo com permissão de root (admin, no caso do windows):
sudo ./zabbix.docker-postegre.sh

Após execução do comando o docker criará 4 containers, responsável pela execução do módulos do zabbix

Zabbix Server
Zabbix Frontend
Postgres Server
Zabbix Trapper
Agora é possível acessar a interface web do zabbix através do endereço:
localhost/zabbix

Assim temos um servidor zabbix plenamente funcional, ideal para ambiente de hologação e testes. Também sendo possível usar esta abordagem em ambiente menores, com baixa disponibilidade de recursos.
