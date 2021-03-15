# Azure CLI AppRole extension

Adds functionality to add, remove and list app role assignments for service principals (ie. managed identities)

## List existing assignments

```cli
az approle assignment list --service-principal logic_app_user -otable
ApplicationId                         ApplicationName    RoleName              ServicePrincipalDisplayName    ServicePrincipalId
------------------------------------  -----------------  --------------------  -----------------------------  ------------------------------------
fb900fd0-3383-47dc-8a34-f25643f3b69f  Hello World API    Task.World.Update      logic_app_user                 6c3dc441-671e-47b8-ba79-51ad0808dab2
fb900fd0-3383-47dc-8a34-f25643f3b69f  Hello World API    Task.World.Read        logic_app_user                 6c3dc441-671e-47b8-ba79-51ad0808dab2
```

## Add app role assignment

`az approle assignment add --service-principal "36cccbe0-9b58-4f20-833b-1458ae7732d1" --app-id fb900fd0-3383-47dc-8a34-f25643f3b69f --role Task.World.Read`


or by name:

`az approle assignment add --service-principal my_managed_identity --app-id "Hello World API" --role Task.World.Delete`

