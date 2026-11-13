# Privacy Policy — Mail Manager

**Mail Manager — Smart Email Workspace**
Publisher: **Phan Ngọc Thiện**
Effective date: **November 13, 2026**

This Privacy Policy explains how Mail Manager ("the app", "we", "us") handles your information when you install and use the app on Windows. It applies to all versions distributed through the Microsoft Store and through the app's own installer.

---

## Summary

- **Your data stays on your device.** Your email, contacts, files and settings are stored only on your computer, encrypted.
- **We don't run any server that receives your data.** The app talks only to your email providers: Google (Gmail) and Microsoft (Outlook.com / Microsoft 365).
- **No tracking.** No analytics, telemetry, advertising, crash reporting or third-party SDKs that collect data.
- **We never sell, rent or share your data**, and we don't use it to train AI models.
- **You are in control.** You can remove an account, delete local data or revoke access at any time.

---

## 1. Who is responsible for your data

Mail Manager is a desktop application that runs entirely on your computer. The developer does not receive, store or process your email or account data on any server. You (the user) control all data the app stores on your device.

## 2. Information the app accesses

The app accesses information only after you sign in and grant permission, and only to provide the features you use.

### 2.1 Google accounts (Gmail)

Accessed through the official **Gmail API**:

- Your Google account **email address and display name**, to identify the account and fill in the sender name.
- Your **messages and their metadata**: sender, recipients, subject, date, labels, message body and attachments. The app uses them to display, search, organize, send, reply to, forward, label, archive and delete email.
- Your **Gmail labels**, so you can view and move email between labels.

| Google permission (OAuth scope) | Why it is needed |
|---|---|
| `https://www.googleapis.com/auth/gmail.modify` | Read, send, label, archive and move email to Trash. |
| `https://mail.google.com/` (optional) | Requested **only if you turn on** permanent deletion (emptying Trash or auto-deleting Trash after a number of days), because Gmail allows permanent deletion only with this scope. |

### 2.2 Microsoft accounts (Outlook.com, Hotmail, Live, Microsoft 365)

Accessed through the official **Microsoft Graph API**, using Microsoft's sign-in (OAuth 2.0 with PKCE). No password or client secret is stored by the app.

- Your account **email address and display name**.
- Your **messages, folders, categories, flags and attachments**, for the same purposes as above.

| Microsoft permission (delegated) | Why it is needed |
|---|---|
| `openid`, `profile`, `email`, `User.Read` | Identify the signed-in account (email address and display name). |
| `Mail.ReadWrite` | Read and organize email (folders, categories, flags, read state), move email to Deleted Items, and permanently delete email you choose. |
| `Mail.Send` | Send, reply to and forward email you write. |
| `offline_access` | Keep you signed in so the app can sync in the background. |

Organizations can choose to use their own Microsoft Entra ID app registration instead of the app's built-in one. In that case the organization's administrator controls the permissions granted.

### 2.3 Multiple accounts

You can add several Google and Microsoft accounts. Each account's sign-in session and email are kept separately on your device.

### 2.4 Files you open

When you preview an attachment, or open an `.eml` / `.msg` file with Mail Manager, the file is processed **locally on your computer**. This covers Excel, Word, PDF, images and email files. Files are never uploaded to the developer or to any other service.

## 3. Information you create in the app

The following are created by you and stored only on your device:

- signatures and email templates;
- categories and categorization rules;
- workflows / tasks (recipients, steps, schedules, reminders);
- flags and notes;
- a contact list built from your own email;
- statistics;
- app settings (language, theme, sync and notification options).

## 4. How the information is used

Your information is used **only to provide the app's features to you**:

- showing, searching and organizing your mailbox;
- sending the email you write;
- applying the rules you create;
- tracking replies and sending the follow-up reminders and workflow steps that **you** scheduled;
- previewing attachments and exporting email threads (`.eml` / PDF) that **you** request;
- showing desktop notifications about new mail, replies and due items.

We do **not** use your information for advertising, profiling, analytics, selling, or training machine-learning / AI models.

## 5. Where your data is stored and how it is protected

- All data is stored **locally**, in your Windows user profile (`%APPDATA%\Mail Manager`).
- The local database, the sign-in sessions for your Google and Microsoft accounts, and cached attachments are **encrypted with AES-256**. The key is protected by **Windows Data Protection (DPAPI)**, so only your Windows user account on that computer can read it.
- Non-sensitive preferences (such as language and theme) are kept in a separate `settings.json` file that contains no email content or credentials.
- Attachments you open are cached temporarily and deleted automatically after the period you choose in Settings.
- Email content is displayed in an isolated view that blocks scripts. Remote images and links open only after you choose to open them.
- All network traffic to Google and Microsoft uses encrypted **HTTPS**.

## 6. Sharing and disclosure

- The app communicates **only** with Google (Gmail API, Google sign-in) and Microsoft (Microsoft Graph, Microsoft sign-in).
- **No data is sent to the developer** or to any third party.
- We do not sell, rent, trade or otherwise share your information.
- Email you write is delivered to its recipients through your own email provider, exactly as when you send email in any other email client.

## 7. Google API Services User Data Policy

Mail Manager's use and transfer of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the **Limited Use** requirements. The app:

- uses Gmail data only to provide user-facing email features within the app;
- does not transfer Gmail data to others, except as necessary to provide those features (for example, sending email you compose through Google), to comply with law, or with your explicit consent;
- does not use Gmail data for advertising;
- does not allow humans to read Gmail data. The only exceptions are your explicit consent for a specific message (for example, one you send to us for support), security purposes, or legal requirements.

## 8. Your choices and rights

- **Remove an account:** *Settings › Account › Remove*. The account's sign-in session and the email stored on this device for it are deleted from your device.
- **Revoke access** at any time:
  - Google: <https://myaccount.google.com/permissions>
  - Microsoft personal accounts: <https://account.live.com/consent/Manage>
  - Microsoft work or school accounts: <https://myapps.microsoft.com>, or ask your administrator.
- **Delete local data:**
  - *Settings › Storage & data* clears cached email and attachments.
  - Uninstalling the app and deleting the `%APPDATA%\Mail Manager` folder removes everything the app stored.
- **Backups** you export are unencrypted files saved where you choose; keep them safe.
- Deleting data in the app does not delete email from your Gmail or Outlook account, unless you explicitly delete email or empty Trash in the app.

Because the developer holds no copy of your data, requests to access, correct or delete personal data under laws such as the GDPR are handled directly in the app and through your email provider. Contact us if you need help.

## 9. Data retention

Data remains on your device until you delete it, remove the account, or uninstall the app and delete its data folder. The developer retains no data.

## 10. Children

Mail Manager is not directed to children under 13, or the minimum age required in your country, and does not knowingly collect information from them.

## 11. International use

Because all processing happens on your device and with your own email provider, the app itself does not transfer your data across borders. Your email provider's privacy terms apply to the data stored in your Google or Microsoft account.

## 12. Changes to this policy

We may update this policy when the app changes. The updated version will be published at the same address with a new effective date. Significant changes will also be described in the app's release notes.

## 13. Contact

For questions about this policy or your data, contact **Phan Ngọc Thiện** at [thien181996@gmail.com](mailto:thien181996@gmail.com).
