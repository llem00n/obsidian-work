## languages
- app config must feature a section for languages configuration.
```json
{
  ...
  "languages": {
    "en": ["en.commodities.json", "en.json"],
    "es": ["es.json"]
  }
}
```

- *maybe* doing it using translations page
required back-end endpoints:

***GET*** /Translations/list
Example response:
```json
[
  {
    code: "en",
    name: "English"
  }
]
```

***PUT*** /Translations
Example body:
```json
{
  code: "en",
  name: "English",
  translations: "{ ... }"
}
```

***GET*** /Translations/{code}
Example response:
```json
{
  code: "en",
  name: "English",
  translations: "{ ... }"
}
```

---
## forms
- new directive for field labels may be a good idea
- app config must feature forms feature
```json
{
  ...
  "forms": {
    ...
    "master_recipe": {
      ...
      "planned_quantity": {
        "visible": true,
        "required": true
      }
    }
  }
}
```

---
## pages
- need to add a pages section to the app config:
```json
{
  ...
  "pages": {
     "manufacturing_analytics": {
       "work_center_performance_dashboard": {
         "available": true,
         "roles": ["MOM-SUPER-ADMIN"]
       }
     }
  }
}
```

- need to add `fullPath` property to the `data` of the routes
```typescript
{
  ...
  {  
    path: InboundDeliveriesRoutes.AddInboundDelivery,  
    component: AddInboundDeliveryComponent,  
    canActivate: [RolesPermissionsGuard],  
    data: {
      breadcrumb: 'breadcrumbs.add_inbound_delivery', 
      fullPath: [RoutesEnum.Deliveries, DeliveriesRoutes.InboundDeliveries, InboundDeliveriesRoutes.AddInboundDelivery] 
    }  
  },
  ...
}
```
