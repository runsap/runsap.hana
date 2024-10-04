sap-hana-db-restore
===================

Introduction
------------
Performs restore of a SAP HANA Database.

Example
-------
Example task to do a restore from from filesystem:

```
- include_role: 
    name: sap-hana-db-backup
    vars: 
        secure_connection: true
        backup_path: "/backup/1234/"
        hdb_db: S4S
        hdb_sid: HDB
```

Restore through cli:

`ansible-playbook -i inventory sap-hana-adhoc-restore.yml -e cli_backup_path=/backup/HDS/refresh_s4p/ -e cli_sap_env=s4s` 