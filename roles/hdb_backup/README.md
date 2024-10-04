sap-hana-db-backup
==================

Introduction
------------
Creates a sap hana database backup on the filesystem.

Example
-------
Example task to create a backup on filesystem:

```
- include_role:
    name: sap-hana-db-backup
    vars:
        secure_connection: true
        backup_location: "/backup/{{ hdb_db | upper }}"
        backup_name: "{{ cli_backup_name | default(hdb_db ~ '_' ~ lookup('pipe', 'date +\"%Y-%m-%d_%H%M%S\"')) }}"
        hdb_db: S4S
        hdb_sid: HDB
```

Give the backup a special name:

`ansible-playbook -i inventory ansible/sap-hana-adhoc-backup.yml -e cli_backup_name=refresh_s4p`