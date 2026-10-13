# shlee1223.github.io

Static files served at <https://shlee1223.github.io/>.

## did:cimd examples

`did-cimd-examples/` holds OAuth Client ID Metadata Documents that serve as resolution examples
for the [did:cimd method](https://github.com/shlee1223/did-method-cimd/blob/main/did-method-cimd.md).

| DID | Document | Keys |
|---|---|---|
| `did:cimd:shlee1223.github.io:did-cimd-examples:client.json` | [client.json](did-cimd-examples/client.json) | referenced through `jwks_uri` ([jwks.json](did-cimd-examples/jwks.json)) |
| `did:cimd:shlee1223.github.io:did-cimd-examples:client-inline.json` | [client-inline.json](did-cimd-examples/client-inline.json) | inline in `jwks` |

The documents contain public keys only. No one holds the private keys, so these clients cannot
authenticate anywhere.

Changing a document's path or its `client_id` changes its DID. The `.nojekyll` file makes GitHub
Pages serve the files as they are.
