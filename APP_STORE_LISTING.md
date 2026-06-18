# GPX Life — App Store Connect Listing Reference

Everything you'll need to fill in when you create the app record in App Store
Connect, organized in the order ASC asks for it. Copy/paste sections directly,
or tweak as needed.

---

## 1. App Information (one-time, app-level)

| Field | Value |
| --- | --- |
| **Name** | `GPX Life` |
| **Subtitle** *(30 char max)* | `Your routes, your library` |
| **Bundle ID** | `life.gpx.app` |
| **SKU** *(your internal id, never shown)* | `gpxlife-ios-001` |
| **Primary Language** | English (U.S.) |
| **Primary Category** | `Health & Fitness` |
| **Secondary Category** | `Navigation` |
| **Content Rights** | "Does not contain, show, or access third-party content" → **Yes** (you own all content; Open-Meteo / OSM are first-party API calls, not embedded third-party content) |

> Alternate categories worth considering:
> - **Primary: Sports**, Secondary: Health & Fitness — if you want to be discovered alongside Strava/Komoot.
> - **Primary: Navigation**, Secondary: Sports — if discovery via "GPX" / "route" search matters more than fitness.
> The first option (Health & Fitness + Navigation) is the safest default.

---

## 2. Pricing and Availability

| Field | Value |
| --- | --- |
| **Price (base app)** | Free |
| **Availability** | All territories |
| **Pre-Order** | Off (recommended for first launch) |
| **Distribute on Apple Vision Pro** | Off (no visionOS support yet) |
| **Distribute on Mac (Designed for iPad)** | Optional — leaving on is harmless |

---

## 3. Version Information (per release; this is v1.0)

### Promotional Text *(170 char max — editable any time without re-review)*
> Free forever for up to 10 routes. Go Pro for unlimited imports, Reverse Route, Auto-Detect Waypoints, and unlimited derived versions per route.

### Description *(4,000 char max)*
```
GPX Life is the Photos app for your GPX routes — a fast, private, iCloud-native library for every run, ride, and hike you've ever recorded.

Drop in a GPX from Mail, Files, Strava, AllTrails, Komoot, Garmin Connect, or any GPX-aware app. GPX Life renders it on Apple Maps with the cleanest detail map iOS can produce, fetches a fresh weather forecast for your start point, and stores it forever in your own iCloud — never on our servers, because we don't have any.

WHY GPX LIFE
• Zero-account, zero-tracking. No sign-up, no login, no analytics. The app has no backend.
• Offline-first. Browse, view, and even import routes without a signal.
• iCloud-native. Optional iCloud sync keeps your library identical across iPhone and iPad. Your data stays inside Apple's perimeter.
• Beautifully native. Real Apple Maps with elevation-aware overlays. No third-party tile farms.
• Open standards. Standard GPX in, standard GPX out. Hand off to any other app at any time.

CORE FEATURES (Free)
• Import unlimited types of GPX file (free tier capped at 10 saved routes)
• Apple Maps + OpenStreetMap rendering
• Open-Meteo weather forecast for the route's start point
• One-tap export to Strava, Komoot, Gaia GPS, CalTopo, Files, Mail, Messages
• Open-in any installed maps app: Apple Maps, Google Maps, OSM
• Long-route handling: separate "Near start" / "Near end" map links
• Configurable share sheet, configurable maps app, configurable long-route threshold

PRO UPGRADE
• Unlimited imported routes (free tier is capped at 10)
• Reverse Route — generate the return trip with one tap
• Auto-Detect Waypoints — turn key turns and intersections into named waypoints
• Unlimited derived versions per original route
• Priority support

PRO PRICING
• Monthly: $2.99
• Yearly: $19.99 (save 44%)
• Lifetime: $49.99 (one-time, never expires)

PRIVACY YOU CAN TRUST
GPX Life has no servers. We don't see your routes, your location, your device, or your purchases. The only data that ever leaves your phone is:
• Weather queries to Open-Meteo (start coordinates only, no identity attached)
• Map tile requests to Apple/OSM (tile coordinates only)
• In-app purchase verification through Apple StoreKit
That's it. Read the full policy at teamv02.com/gpxlife/privacy.html

QUESTIONS OR FEEDBACK?
Email apps@teamvagner.com — we read every message.
```

### Keywords *(100 char max, comma-separated, no spaces between)*
```
gpx,route,running,hiking,cycling,trail,strava,komoot,garmin,offline,icloud,navigation,outdoor
```

> 99 characters. Avoid duplicating words from your title/subtitle (Apple
> already indexes those). Apple specifically forbids competitor brand names
> in some categories — `strava`, `komoot`, `garmin` are typically allowed
> because they're file-format-related search terms, but if review pushes
> back, swap them for: `track,waypoint,explorer,workout,fitness`.

### Support URL *(required)*
```
https://teamv02.com/gpxlife/support.html
```

### Marketing URL *(optional)*
```
https://teamv02.com/gpxlife/
```

### Privacy Policy URL *(required)*
```
https://teamv02.com/gpxlife/privacy.html
```

### Copyright
```
© 2026 Team Vagner
```

### Version Number
```
1.0.0
```

### What's New in This Version
> *(skip for first submission — this field is for updates)*
> For a v1.1 you'd write something like:
> ```
> • Auto-Detect Waypoints now handles longer routes faster.
> • Fixed a crash when importing GPX files with extended <extensions> blocks.
> • Smaller tweaks to the offline UX.
> ```

---

## 4. App Review Information *(seen only by Apple, never publicly)*

| Field | Value |
| --- | --- |
| **Sign-in required** | **No** (the app has no accounts) |
| **Demo Account** | leave blank |
| **Contact First Name** | *(your first name)* |
| **Contact Last Name** | *(your last name)* |
| **Phone Number** | *(your number — Apple may call if review needs clarification)* |
| **Email** | `apps@teamvagner.com` |
| **Notes for Reviewer** | see block below |

### Notes for Reviewer
```
Hi reviewer — thanks for taking the time.

GPX Life has no user accounts and no backend. Everything works without sign-in. To exercise the full app:

1. Tap the "+" on the Library tab and choose any sample GPX file. (If your test device doesn't have one handy, this public sample works: https://www.topografix.com/fells_loop.gpx — save it to Files first, then import.)
2. Tap the imported route to see the map view, weather card, and export sheet.
3. The Settings tab → Upgrade exposes the in-app purchase tiers (Monthly / Yearly / Lifetime). The "Restore Purchases" button is also there.

In-app purchases are wired via StoreKit 2 (expo-iap). Sandbox testers will see real prices from App Store Connect.

There is no third-party tracking SDK, no advertising, no remote content moderation surface, and no user-generated content beyond the user's own GPX files stored locally / in their private iCloud container.

Email apps@teamvagner.com if anything's unclear and we'll respond same-day.
```

### Attachment
> Optional. If review asks for a video walkthrough, a 15-second screen recording showing import → map view → weather card → export sheet is plenty.

---

## 5. App Privacy *(the "nutrition label" questionnaire)*

When ASC asks "Does your app collect data?" the answer is **No**.

If it then asks you to confirm by re-stating each category, here are the
answers — every category should be checked **"Not Collected."**

| Data Type | Answer |
| --- | --- |
| Contact Info | Not Collected |
| Health & Fitness | Not Collected |
| Financial Info | Not Collected |
| Location | Not Collected *(GPX files contain location data, but they live on-device; we never receive them)* |
| Sensitive Info | Not Collected |
| Contacts | Not Collected |
| User Content | Not Collected |
| Browsing History | Not Collected |
| Search History | Not Collected |
| Identifiers | Not Collected |
| Purchases | Not Collected *(Apple processes IAPs; we receive entitlement only)* |
| Usage Data | Not Collected |
| Diagnostics | Not Collected |
| Other Data | Not Collected |

> **Important caveat:** if you ever add crash reporting (Sentry, Firebase
> Crashlytics, even Apple's own Crash Reports if shared with developer), you
> must update this to **"Diagnostics → Crash Data → Not Linked to Identity →
> Not Used for Tracking."** Today, with no crash reporting wired in, "Not
> Collected" is correct.

---

## 6. Age Rating Questionnaire

Answer **No** to every question. The result will be **4+**.

Specifically:
- Cartoon or Fantasy Violence: **None**
- Realistic Violence: **None**
- Sexual Content or Nudity: **None**
- Profanity or Crude Humor: **None**
- Alcohol, Tobacco, or Drug Use: **None**
- Mature/Suggestive Themes: **None**
- Horror/Fear Themes: **None**
- Medical/Treatment Information: **None**
- Gambling: **None**
- Contests: **None**
- Unrestricted Web Access: **No**
- User Generated Content: **No** *(GPX files are user-imported but not shared with other users in-app)*

---

## 7. In-App Purchases

You'll create three IAP records under "Features → In-App Purchases" in ASC.
**Use these exact Product IDs** — they must match what's hardcoded in the app
(`utils/iap.ts` → `PRODUCT_IDS`).

### IAP #1 — Monthly subscription
| Field | Value |
| --- | --- |
| **Type** | Auto-Renewable Subscription |
| **Reference Name** *(internal)* | `Pro Monthly` |
| **Product ID** | `gpxlife_pro_monthly` |
| **Subscription Group** | `gpxlife_pro` *(create new — both subs share this group so users can switch)* |
| **Subscription Duration** | 1 Month |
| **Price** | Tier 3 ($2.99 USD) |
| **Display Name** *(localized)* | `GPX Life Pro — Monthly` |
| **Description** *(localized)* | `Unlimited imported routes, Reverse Route, Auto-Detect Waypoints, and unlimited derived versions per route. Billed monthly, cancel any time.` |

### IAP #2 — Yearly subscription
| Field | Value |
| --- | --- |
| **Type** | Auto-Renewable Subscription |
| **Reference Name** | `Pro Yearly` |
| **Product ID** | `gpxlife_pro_yearly` |
| **Subscription Group** | `gpxlife_pro` *(same group as monthly)* |
| **Subscription Duration** | 1 Year |
| **Price** | Tier 20 ($19.99 USD) |
| **Display Name** | `GPX Life Pro — Yearly` |
| **Description** | `Unlimited imported routes, Reverse Route, Auto-Detect Waypoints, and unlimited derived versions per route. Best value — saves 44% vs monthly. Billed yearly, cancel any time.` |

### IAP #3 — Lifetime
| Field | Value |
| --- | --- |
| **Type** | Non-Consumable |
| **Reference Name** | `Pro Lifetime` |
| **Product ID** | `gpxlife_pro_lifetime` |
| **Price** | Tier 50 ($49.99 USD) |
| **Display Name** | `GPX Life Pro — Lifetime` |
| **Description** | `One-time purchase. Unlocks every Pro feature forever, on any iPhone or iPad signed into your Apple ID. No subscription, no renewals.` |

### Subscription Group Localized Display Name
For the `gpxlife_pro` group:
- **Reference Name:** `GPX Life Pro`
- **Display Name (English):** `GPX Life Pro`

### Required for subscriptions only — Review Notes
```
GPX Life Pro unlocks three features that are gated in the free tier:
1. Imports beyond the 10-route free limit (free users see a "Free Tier Limit" alert on the Import tab once they reach 10 routes)
2. Reverse Route — button in the GPX TOOLS section of any route detail screen. Free users see a "Pro Feature" alert on tap.
3. Auto-Detect Waypoints — also in GPX TOOLS. Free users see the same "Pro Feature" alert on tap.

Both Pro alerts have a "See Pro" button that deep-links to Settings → paywall sheet for purchase.

Reviewers can verify the upgrade flow via Settings → "Upgrade to Pro" or by tapping either Pro-gated tool on a route detail screen.
```

### Required for subscriptions only — Localized Promotional Image *(optional)*
1024×1024 PNG, no text, no Apple trademarks. Skip for v1.0 if you don't have one ready.

---

## 8. Screenshots Required

You only need to upload one size; ASC scales it for the rest.

| Device | Required size (px) | Notes |
| --- | --- | --- |
| **iPhone 6.9" (15/16 Pro Max)** | 1290 × 2796 | **Required.** Most important — shown on iPhone Pro listings. |
| **iPhone 6.5" (Plus / 11/12/13/14 Pro Max)** | 1242 × 2688 *or* 1284 × 2778 | **Required if you don't upload 6.9".** ASC will accept just one of these. |
| iPad 13" / iPad Pro 12.9" | 2064 × 2752 | Optional unless you check "Available on iPad." |

Upload **3–10 screenshots**. Recommended set:
1. Library view (hero shot — show 5–6 routes)
2. Route detail with map + weather card
3. Reverse Route / Auto-Detect Waypoints in action (Pro features)
4. Export sheet open (shows third-party app integration)
5. Settings → Pro upgrade screen (shows the three pricing tiers)
6. Empty / first-launch state (optional, gives reviewers context)

> Pro tip: use the iOS Simulator's "Save Screen" (Cmd+S) at the iPhone 16 Pro Max preset — it generates the exact 1290×2796 size automatically.

### App Preview Video *(optional)*
15–30 seconds, no narration required. ASC accepts up to 3 per device size. Skip for v1.0 unless you already have one.

---

## 9. App Icon Requirements

| Spec | Value |
| --- | --- |
| **Format** | PNG, no transparency, no rounded corners (Apple rounds them) |
| **Size** | 1024 × 1024 |
| **Color profile** | sRGB or Display P3 |
| **Path in repo** | `artifacts/gpx-hub/assets/images/icon.png` *(already exists)* |

> ASC will reject icons with alpha channels. If yours has one, flatten it on
> a solid background before upload.

---

## 10. Export Compliance / Encryption

When ASC asks "Does your app use encryption?":

> **Answer: Yes** — but tick "Your app uses encryption that is exempt from
> export compliance documentation."

Reason: GPX Life only uses HTTPS (Apple-provided URLSession) and Apple's own
StoreKit, both of which fall under the standard exemption for apps that "make
calls over HTTPS for non-encryption purposes." No custom crypto.

In `app.json` you can set this so ASC stops asking:
```json
"ios": {
  "infoPlist": {
    "ITSAppUsesNonExemptEncryption": false
  }
}
```

> *(If you want me to add this to your `app.json`, just say the word.)*

---

## 11. Submission Checklist

- [ ] App Store Connect app record created with bundle `life.gpx.app`
- [ ] Three IAP records created (monthly / yearly / lifetime) with the exact Product IDs above
- [ ] Subscription group `gpxlife_pro` created with monthly + yearly inside it
- [ ] At least one Sandbox Tester account created (Users and Access → Sandbox Testers)
- [ ] Screenshots uploaded (3+ for iPhone 6.9")
- [ ] Privacy Policy URL is live and reachable
- [ ] Support URL is live and reachable
- [ ] Demo flow tested on a custom dev build with a Sandbox account
- [ ] App icon uploaded (1024×1024, no alpha)
- [ ] Age rating answered (all "None" → 4+)
- [ ] App Privacy questionnaire answered ("Not Collected" everywhere)
- [ ] Export compliance set ("Uses encryption — Exempt")
- [ ] Submit for Review

---

## 12. Things you'll be asked at submission time

These are common review questions. Pre-answers:

> **"Why do you need access to Files / Document Picker?"**
> Users import GPX route files from their device. The app reads the file, parses it, and stores it in its own sandbox. No other file access.

> **"Why do you need network access?"**
> (1) Apple Maps / OSM tile loading. (2) Open-Meteo public weather API. (3) Apple StoreKit for in-app purchases. No other network calls.

> **"Do you use any third-party SDKs?"**
> Open-source libraries only (Expo, React Native, react-native-maps, expo-iap, AsyncStorage). No tracking SDKs, no analytics SDKs, no ad SDKs.

> **"Where does user data go?"**
> Locally on device, and optionally in the user's own private iCloud container. We do not operate any backend.
