# Implementation Plan - Ayengee Labs GitHub Pages & Google Play Portal

## Objective
Establish a clean, professional, 100% free developer portal hosted on GitHub Pages (`ayengeelabs.github.io`) that complies with Google Play Console developer verification, store listing, and app privacy policy requirements.

---

## 1. Directory Structure

```text
d:\Projects\Ayengee\
├── index.html                  # Lab portal (Company intro, app showcase)
├── contact.html                # Support, contact & developer verification details
├── 404.html                    # Graceful error page
├── CNAME                       # (Optional) Custom domain pointer if added later
├── apps/
│   ├── telepath.html           # Telepath product landing page
│   ├── fortressfi.html         # FortressFi product landing page
│   └── eduplay.html            # Eduplay Suite landing page
└── privacy/
    ├── telepath.html           # Mandatory Play Console Privacy Policy (Telepath)
    ├── fortressfi.html         # Mandatory Play Console Privacy Policy (FortressFi)
    └── eduplay.html            # Mandatory Play Console Privacy Policy (Eduplay)
```

---

## 2. URL Mapping for Google Play Console

| Field in Google Play Console | Path / URL | Purpose |
| :--- | :--- | :--- |
| **Developer Website** | `https://ayengeelabs.github.io/` | Account verification & developer branding |
| **Store Listing Website (Telepath)** | `https://ayengeelabs.github.io/apps/telepath.html` | Play Store App landing page |
| **Store Listing Website (FortressFi)** | `https://ayengeelabs.github.io/apps/fortressfi.html` | Play Store App landing page |
| **Store Listing Website (Eduplay)** | `https://ayengeelabs.github.io/apps/eduplay.html` | Play Store App landing page |
| **Privacy Policy URL (Telepath)** | `https://ayengeelabs.github.io/privacy/telepath.html` | Policy & programs -> App Content |
| **Privacy Policy URL (FortressFi)** | `https://ayengeelabs.github.io/privacy/fortressfi.html` | Policy & programs -> App Content |
| **Privacy Policy URL (Eduplay)** | `https://ayengeelabs.github.io/privacy/eduplay.html` | Policy & programs -> App Content |
| **Contact / Support URL** | `https://ayengeelabs.github.io/contact.html` | Support email & inquiries |

---

## 3. Phased Execution Steps

### Phase 1: Local Site Architecture & Page Implementation
1. **Homepage (`index.html`)**:
   - Modern dark theme using Tailwind CSS (CDN).
   - Brand header with Ayengee Labs logo styling.
   - Product showcase cards for **Telepath**, **FortressFi**, and **Eduplay**.
   - Footer with copyright and contact navigation.
2. **Contact & Support (`contact.html`)**:
   - Contact form / direct support email link (`mailto:`).
   - FAQ & technical support expectations.
   - Publisher verification information for Play Store compliance.
3. **App Showcase Pages (`apps/*.html`)**:
   - `apps/telepath.html`: Package ID `com.ayengee.telepath`, DAG structuring, local encryption, specs, Play Store badge.
   - `apps/fortressfi.html`: Package ID `com.ayengee.fortressfi`, biometric vault, offline wealth tracker.
   - `apps/eduplay.html`: Package ID `com.ayengee.eduplay`, educational apps suite details.
4. **Dedicated Privacy Policies (`privacy/*.html`)**:
   - Comprehensive GDPR / Play Store compliant privacy policy templates for each app.
   - Disclosure of on-device storage, zero-tracking, optional Google Drive AppData synchronization, and biometric usage.

### Phase 2: Git Initialization & Remote Linking
1. Initialize git in `d:\Projects\Ayengee`.
2. Link to your GitHub repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Ayengee Labs website and Google Play compliance pages"
   git branch -M main
   git remote add origin https://github.com/<your-username-or-org>/ayengeelabs.github.io.git
   git push -u origin main
   ```

### Phase 3: GitHub Pages Configuration
1. Go to repository **Settings** -> **Pages**.
2. Under **Build and deployment**:
   - Source: `Deploy from a branch`
   - Branch: `main` / `/ (root)`
3. Save and wait 1–2 minutes for the site to go live at `https://<org-or-user>.github.io/` or `https://ayengeelabs.github.io`.

### Phase 4: Google Play Console Population
1. **Developer Profile**: Enter Developer Website (`https://ayengeelabs.github.io`).
2. **App Content > Privacy Policy**: Enter corresponding `/privacy/<app>.html`.
3. **Store Presence > Store Settings**: Enter App Product URL `/apps/<app>.html` and support contact details.
