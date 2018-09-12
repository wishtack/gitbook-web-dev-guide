# API Unauthorized Access and Data Leak

The API should verify the permissions on the every resource and field.

```text
POST /users/123456/
{ firstName: 'Foo', isAdmin: true }
```

The API should not leak confidential data. This often happens when using generic code.

```text
GET /users/123456/
{ firstName: 'Foo', bankCard: { number: '...', ... } }
```

