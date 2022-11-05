# API Document

API Driven Development (c)

```
/// types
type UserInput {
  name: string;
  email: string;
}

type UserResult {
  id: int64;
  name: string;
  email: string;
}

/// methods
saveUser(id: int64, user: UserInput): UserResult;

/// sections
section "Guide" {
  markdown "Get Started" {
    # Get Started
    ...
  }

  markdown "Rate limits" {
    # Rate limits
    ...
  }
}

section "Methods" {
  saveUser;
}

section "Types" {
  UserInput;
  UserResult;
}
```
