---
title: Realm import/export
---

#### How to export realm including users

https://simonscholz.dev/tutorials/keycloak-realm-export-import

Inside Docker of Keycloak:

```bash
/opt/keycloak/bin/kc.sh export --dir /opt/keycloak/data/import --users realm_file --realm <realm_name>
```

---

Keycloak realm update: [Link](https://www.keycloak.org/docs/latest/server_admin/index.html#the-admin-cli)

https://rahulroyz.medium.com/update-keycloak-realm-configurations-using-import-feature-on-kubernetes-platform-b1b0ed85f7f7

```bash
> opt/keycloak/bin/kcadm.sh config credentials --server http://localhost:8080 --realm master --user admin
> opt/keycloak/bin/kcadm.sh update realms/<realm_name> -f /opt/keycloak/data/import/realm-export.json
```

Why this is not a proper way? https://www.keycloak.org/server/containers#_importing_a_realm_on_startup

Proper way?
https://docs.expertflow.com/cx/4.3/script-to-upgrade-the-realm-with-users-being-intac
