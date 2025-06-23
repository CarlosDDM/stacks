# Stacks de Containers para monitoramento
## Grafana, Zabbix e Uptime-Kuma (*BETA*)

> [!NOTE]
> Caso queira subir o Grafana e o Zabbix na mesma stack é possivel basta copiar todo o serviço do grafana na stack do zabbix e esse forma mudar a *networks* do grafana para *zabbix-monit*.

> [!NOTE]
> Uptime-Kuma *BETA* o uso desse container em beta acontece devido uma limitação de performace que o sqlite entrega. E a versão beta entrega um novo tipo de conexão com o banco.

> [!TIP]
>   Caso queira usar o Grafana na mesma stack é possivel retirar a porta exposta do postgres, e assim deixar a comunicação somente interna na rede do docker. Dessa forma é possivel usar o DNS quando para apontar o banco e a url do zabbix.O DNS geralmente é o (container_name), BANCO *postgres-zabbix* INTERFACE VISUAL ZABBIX *zabbix-web*. A url de conexão com o Zabbix seria: *http://zabbix-web:8080/api_jsonrpc.php*

> [!TIP]
> Caso necessario utilize o campo *TZ* no environment para colocar a data do seu local. No caso do zabbix é *PHP_TZ*.

> [!IMPORTANT]
> Para fazer o apontamento do uptime-kuma dessa forma basta colocar o nome do container do banco contido na stack que pe *mariadb-uptime* nesse caso. Dessa forma não sera necessario deixar a porta do banco exposta.


