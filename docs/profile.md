# User Profile
|          Endpoint          |                             Description                            |  Access Rights  |
|----------------------------|--------------------------------------------------------------------|-----------------|
|       GET /api/profile     |    Retrieves the current user's profile and modules information    |      User       |
|    GET /api/profile/user   |          Retrieves the current user's profile information          |      User       |
|  GET /api/profile/modules  |            Retrieves all modules the current user is in            |      User       |

## `GET /api/profile`
Retrieves the current user's profile and modules information.

### Parameters required
| Request Property |  Name  |           Description           |
|------------------|--------|---------------------------------|
|     req.user     |  User  |  Available after user logs in.  |

### Example response
```json
{
  "canEdit": true,
  "name": "User",
  "avatar": "/uploads/E123456/avatar",
  "nusOpenId": "E123456",
  "year": 2,
  "id":87,
  "modules": [{
                "name": "qweq",
                "role": "Admin",
                "contributionTypes": ["weqwe","wew","eqw"],
                "code": "weqeqwe",
                "id": 129
              },
              {
                "name": "test",
                "role": "Admin",
                "contributionTypes": ["test"],
                "code": "test",
                "id": 121
              }],
  "lastLoggedIn": 1470033863980,
  "superAdmin":true
}
```

## `GET /api/profile/user`
Retrieves the current user's profile information.

### Parameters required
| Request Property |  Name  |           Description           |
|------------------|--------|---------------------------------|
|     req.user     |  User  |  Available after user logs in.  |

### Example response
```json
{ 
  "year": 2,
  "nusOpenId": "E123456",
  "canEdit": true,
  "name": "User",
  "lastLoggedIn": 1469442573896,
  "avatar": "/uploads/E123456/avatar",
  "superAdmin": true,
  "id": 87
}
```

## `GET /api/profile/modules`
Retrieves all the modules (and the role of the user in the module) the current user is in.

### Parameters required
| Request Property |  Name  |           Description           |
|------------------|--------|---------------------------------|
|     req.user     |  User  |  Available after user logs in.  |

### Example response
```json
[{
  "name": "qweq",
  "role": "Admin",
  "contributionTypes": ["weqwe","wew","eqw"],
  "code": "weqeqwe",
  "id": 129
 },
 {
  "name": "test",
  "role": "Admin",
  "contributionTypes":["test"],
  "code": "test",
  "id": 121
}]
```