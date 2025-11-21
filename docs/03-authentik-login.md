---
title: How to Login with Authentik to Wiki.js
description: SSO authentication setup for Wiki.js using Authentik
published: true
date: 2025-10-28T11:59:42.752Z
tags: [authentik, sso, authentication, wikijs]
editor: markdown
---

# How to Login with Authentik to Wiki.js

> **Official Sources:**
> - [Authentik Documentation](https://docs.goauthentik.io)
> - [Wiki.js Authentication](https://docs.requarks.io/auth)

**Authentik** is an open-source identity provider (IdP) that enables Single Sign-On (SSO) for Wiki.js and other applications.

## What is SSO (Single Sign-On)?

**Single Sign-On** allows you to log in once and access multiple applications without re-entering credentials.

**Benefits:**
- One password for all services
- Centralized access management
- Enhanced security with 2FA
- Automatic session management

## Prerequisites

Before you begin:

- ✅ Active GitHub account ([Register here](02-github-registration))
- ✅ Invitation email from Wiki.js administrator
- ✅ Access to Authentik instance (provided by admin)

## Step-by-Step Login Process

### 1. Navigate to Wiki.js

Open your browser and go to your Wiki.js instance:
- Example: `https://wiki.example.com`
- Or: `http://localhost:3000` (local development)

### 2. Click "Login" Button

Look for the login button (usually top-right corner).

### 3. Select "Authentik" Provider

You'll see login options:
- **Local Account** (username/password)
- **Authentik** (recommended)
- GitHub OAuth (if configured)

Click **"Login with Authentik"**

### 4. Authentik Authentication

You'll be redirected to Authentik login page.

**First-Time Users:**
1. Enter your email address
2. Check email for magic link (passwordless)
3. Click link to verify identity

**OR** (if password is configured):
1. Enter username/email
2. Enter password
3. Complete 2FA if enabled

### 5. Grant Permissions

Authentik will show what Wiki.js wants to access:
- **Profile information** (name, email)
- **Groups/roles** (for permissions)

Click **"Authorize"**

### 6. Redirected to Wiki.js

You're now logged in! You should see:
- Your username (top-right)
- Edit buttons (if you have permissions)
- Admin panel (if you're an administrator)

## Troubleshooting

### "Access Denied" Error

**Possible Causes:**
1. Your account is not approved by administrator
2. You're not in the required Authentik group
3. OAuth configuration is incorrect

**Solution:** Contact your Wiki.js administrator.

### Redirect Loop

**Symptoms:** Keeps redirecting between Authentik and Wiki.js

**Solutions:**
1. Clear browser cookies
2. Try incognito/private mode
3. Check with administrator for configuration issues

### "Invalid State Parameter"

**Cause:** Session expired during authentication

**Solution:** Start login process again from Wiki.js

### Email Not Received (Magic Link)

1. Check spam/junk folder
2. Verify email address is correct
3. Request administrator to resend invitation
4. Try different email provider (some block automated emails)

## Security Best Practices

### Enable Two-Factor Authentication (2FA)

Authentik supports multiple 2FA methods:
- **TOTP** (Google Authenticator, Authy)
- **WebAuthn** (YubiKey, TouchID)
- **Duo Security**

**Setup Guide:** [Authentik 2FA Documentation](https://docs.goauthentik.io/docs/flow/stages/authenticator/)

### Use Strong Password

If not using passwordless:
- Minimum 15 characters
- Mix uppercase, lowercase, numbers, symbols
- Use password manager

### Review Active Sessions

Periodically check logged-in devices:
1. Authentik Dashboard
2. Settings → Sessions
3. Revoke unknown sessions

## Managing Your Account

### Update Profile Information

1. Click your avatar (top-right)
2. Go to **"Profile Settings"**
3. Update name, email, or avatar
4. Save changes

### Change Password

1. Authentik Dashboard
2. Settings → Password
3. Enter current password
4. Enter new password (twice)
5. Confirm

### Logout

**From Wiki.js:**
- Click avatar → "Logout"

**From All Sessions:**
- Authentik Dashboard → Logout (revokes all tokens)

## Administrator Setup (Reference)

**For Wiki.js Admins:**

Authentik OAuth Application configuration:

```yaml
Client ID: wikijs
Client Secret: <generate-secure-secret>
Redirect URIs: https://wiki.example.com/login/authentik/callback
Authorization URL: https://auth.example.com/application/o/authorize/
Token URL: https://auth.example.com/application/o/token/
User Info URL: https://auth.example.com/application/o/userinfo/
Scopes: openid profile email
```

**Full Setup Guide:** [Wiki.js Authentik Configuration](40-wikijs-basics#authentik-setup)

## Official Resources

- **Authentik Docs:** https://docs.goauthentik.io
- **Authentik GitHub:** https://github.com/goauthentik/authentik
- **Wiki.js Auth Docs:** https://docs.requarks.io/auth
- **OAuth 2.0 Spec:** https://oauth.net/2/

---

**Fact Check:**
- ✅ Authentik documentation URL verified (2025-10-28)
- ✅ OAuth flow description based on [RFC 6749](https://datatracker.ietf.org/doc/html/rfc6749)
- ✅ Wiki.js authentication methods from [official docs](https://docs.requarks.io/auth)
- ✅ SSO benefits sourced from [NIST Digital Identity Guidelines](https://pages.nist.gov/800-63-3/)

**Last Updated:** 2025-10-28
**Author:** dcversus

---

**Next:** [PRP Overview](10-prp-overview) →
