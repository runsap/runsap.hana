# sap-hana-db-restore

Voert een restore uit van een sap hana database.

restore via cli:

`ansible-playbook -i inventory sap-hana-adhoc-restore.yml -e cli_backup_path=/backup/HDS/refresh_s4p/ -e cli_sap_env=s4s` 