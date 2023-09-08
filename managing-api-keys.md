---
section: "Developer Guides"
sortOrder: 1
label: "Managing API Keys"
pageName: "managing-api-keys"
---
# Managing API Keys

API keys serve as access tokens, granting users the ability to utilize
Stateless's resources, such as blockchain node servers. They do not
authenticate individual API requests, but they play an essential role in
ensuring that users have the necessary permissions to access the services they
need. Proper management of these keys is vital for the seamless operation of
Stateless interactions.

## Generating API Keys

To manage resources to enable sending requests, an API key needs to be
generated to associate with your account:

1. [Log in](https://app.stateless.solutions) to your Stateless account
2. Navigate to the ‘API Keys’ table on the ‘Account’ page
3. Click on 'Create API Key'
4. Label your key for easy identification
5. Save the generated key in a secure location

Please note that Stateless will not display your API keys after their initial
generation, and once they are revoked, they cannot be reused.

## Best Practices for Managing API Keys

Keeping API keys secure is one of our primary goals. It's crucial to handle
your API keys securely. Never embed API keys directly into your codebase or
share them in any form. Here are a few best practices to consider:

- **Secure Storage:** API keys are sensitive and should be securely stored, not
  exposed in publicly accessible areas such as GitHub, client-side code, etc.
- **Rotation:** Regularly rotating API keys can reduce the impact if a key is
  compromised.
- **Limited Scope:** If available, scope API keys to specific tasks or access
  levels to minimize potential damage if they are compromised.
- **Delete Unnecessary Keys:** API keys that are no longer in use should be
  deleted to minimize potential exposure.
- **Monitor Usage:** Regularly check the usage of your API keys to detect any
  abnormal activities (and we’ll do the same!)
