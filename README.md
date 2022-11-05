# API Document

API Driven Development (c)

```
/// details
name: "Example API";
summary: "Example API Document by Invoke";
icon: "https://user-images.githubusercontent.com/21020331/145628046-ca19dbdf-2935-49fe-934c-a171219566cc.png";

/// communication information
mode invoke {
  url: "http://localhost/invoke";
}

mode jsonRpc {
  url: "http://localhost/json-rpc";
}

/// sections
section "Guide" {
  markdown "Get Started" `
    # Get Started
    ...
  `

  markdown "Rate limits" `
    # Rate limits
    ...
  `
}

section "Methods" {
  saveUser;
}

section "Types" {
  UserInput;
  UserResult;
}

enum Role: "basic" | "editor" | "admin";

/// types
UserData {
  name: string;
  email: string;
  role: Role;
}

UserInput : UserData {
}

UserResult : UserData {
  id: int64;
}

/// methods
saveUser(id: int64, user: UserInput): UserResult;
```

```javascript
import api from 'api-document';

const call = api`
mode invoke {
  url: "http://localhost/invoke";
}

dec2hex(dec: int64): string;
`;

const hex = await call('dec2hex', { dec: 99 });
console.log(hex);
```
