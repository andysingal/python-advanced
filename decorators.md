```py
import functools

In [47]: user = {"username":"jose", "access_level": "guest"}

In [48]: def make_secure(func):
    ...:     @functools.wraps(func)
    ...:     def secure_function():
    ...:         if user["access_level"] == "admin":
    ...:             return func()
    ...:         else:
    ...:             return f"No admin permissions for {user["username"]}."
    ...: 

In [49]: @make_secure
    ...: def get_admin_password():
    ...:     return "1234"

print(get_admin_password())
```
