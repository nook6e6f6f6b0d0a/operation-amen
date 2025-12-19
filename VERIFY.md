# Verification Procedure (Base64 → Plaintext → SHA-256)

Do NOT hash the Base64. Hash the decoded plaintext.

## Tools (recommended)
- Base64 decode: https://www.base64decode.org/
- SHA-256: https://emn178.github.io/online-tools/sha256.html

## Correct workflow
1) Open `brief.b64` and copy ALL contents.
2) Paste into Base64 decoder → Decode.
3) Copy the FULL decoded plaintext output.
4) Paste into SHA-256 tool (Input: Text) → SHA-256.

## Expected hash
SHA-256(decoded plaintext):
f768f6b0cb5ef109a9e99bfa696d001f439853dc11bda217dbfb0712d7de62e8

## Common failure modes
- Hashing the Base64 output instead of decoded plaintext
- Missing the first/last character when copying
- Extra whitespace/newline added/removed during copy
- Hash output copied with an extra character (hash must be 64 hex chars only)
