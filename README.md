# tlpass-web

> **Pre-alpha: do not store real passwords.** Nothing here has been audited yet, and the app and its data format can still change.

The TLPass web portal, built with React, Vite and TypeScript. It's where you sign up, unlock your vault and manage your passwords in the browser.

All encryption happens in your browser through [`@psi-project-007/tlpass-crypto`](https://github.com/psi-project-007/tlpass-crypto). The portal sends the server only the Auth Hash and encrypted data, never your master password or a key that can decrypt.

## How it fits

| Repository | Role |
| --- | --- |
| tlpass-crypto | The cryptography, published as `@psi-project-007/tlpass-crypto` |
| **tlpass-web** (this one) | The web portal |
| tlpass-api | The API (Go Lambda handlers), which stores only encrypted data |
| tlpass-infra | The AWS infrastructure (CDK in Go) |

## Licence

[AGPL-3.0](LICENSE).

## Security

Please don't report vulnerabilities in public issues. Follow the [security policy](https://github.com/psi-project-007/.github/blob/main/SECURITY.md).
