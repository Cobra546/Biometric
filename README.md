# 🔐 Biometric Unlock Demo

A small GitHub Pages demo showing how a website can request the device's built-in authenticator through **WebAuthn / Passkeys**.

## What it demonstrates

- Fingerprint authentication on supported devices
- Face/device authentication where the browser exposes a platform authenticator
- WebAuthn registration and authentication prompts
- A simple unlock screen after authentication
- Local credential ID storage for this demo browser

## Run it

Enable **GitHub Pages** for the repository and open the HTTPS Pages URL. WebAuthn requires a secure context (HTTPS; localhost is also allowed for development).

## Important security note

This repository is an educational/demo project. The browser-side demo confirms that the device returned a WebAuthn assertion, but it does **not** perform full server-side signature verification. Do not use this exact implementation to protect real private data or admin panels.

For a production authentication system, the server should issue a fresh challenge, verify the returned WebAuthn assertion and signature, check the origin/RP ID, and maintain the credential record server-side.

WebAuthn/passkeys use cryptographic credentials and the website does not receive the user's fingerprint or face data.
