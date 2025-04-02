```py
import functools

In [47]: user = {"username":"jose", "access_level": "guest"}

In [48]: def make_secure(access_level):
           def decorator(func):
    ...:     @functools.wraps(func)
    ...:     def secure_function(*args, **kwargs):
    ...:         if user["access_level"] == access_level:
    ...:             return func(*args, **kwargs)
    ...:         else:
    ...:             return f"No admin permissions for {user["username"]}."
    ...:      return secure_function
           return decorator 

In [49]: @make_secure("admin")
    ...: def get_admin_password(panel):
             return "1234"

          @make_secure("guest")
          def get_dashboard_password():
            return "user: user_password"

print(get_admin_password())
```
