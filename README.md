# API Document

API Driven Development (c)

```
/// details
name "Example API";
summary "Example API Document by Invoke";
icon "https://user-images.githubusercontent.com/21020331/145628046-ca19dbdf-2935-49fe-934c-a171219566cc.png";

/// execution information
execution http {
  url "http://localhost/invoke";
}

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
