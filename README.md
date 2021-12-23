# Laravel API with Auths

This repo contains basic auth system using Scantum, JWT and Passport.

# Steps

- Sanctum
- JWT
- Passport

# Basic Usages

Basic usages on managing auth tokens.

# Creating tokens

```php
// sanctum
$token = auth()->user()->createToken('access_token')->plainTextToken;
// jwt
$token = auth()->attempt($validatedUser);
// passport 
$token = auth()->user()->createToken('access_token')->accessToken;
```

# Revoking Tokens

Auth tokens will be expired.

```php
auth()->user()->tokens()->delete();
```

## Deleting Tokens

Auth tokens will be deleted from the Database.
```php
// Sanctum and Passport
auth()->user()->tokens()->delete();
// JWT
auth()->user()->logout()
```