---
title: Keycloak
---

#### What Clients are

- `Account` -> test with opening `http://172.16.6.16:8080/realms/<realm_name>/account/`
- `Account-console` -> test with running this cURL

```bash
curl -v -X GET \
  "http://172.16.6.16:8080/realms/{{realm}}/account/applications" \
  -H "Authorization: Bearer $TOKEN" \
  -H "Accept: application/json"
```

---
