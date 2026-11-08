# App pages for Grab It US LLC

Static pages (HTML and CSS only) for Grab It US LLC's apps, served by GitHub
Pages at https://nautica.ky. No build step, trackers, cookies or scripts.
Every page loads only files from this site: fonts included, nothing is
requested from another domain.

| Address | Page | Source |
| - | - | - |
| `/` | List of apps (Ludo Reign, Easy Days, Alert! Cayman, Pearlwake) with links and support emails | New |
| `/ludo-reign/` | Ludo Reign | Copied from grabit.ky/ludo-reign/ |
| `/ludo-reign/support/` | Support | Copied from grabit.ky/ludo-reign/support/ |
| `/ludo-reign/privacy/` | Privacy policy | Copied from grabit.ky/ludo-reign/privacy/ |
| `/ludo-reign/terms/` | Terms of service | Copied from grabit.ky/ludo-reign/terms/ |
| `/ludo-reign/delete-account/` | Delete your account | Copied from grabit.ky/ludo-reign/delete-account/ |
| `/alert-cayman/` | Alert! Cayman | Copied from alert.grabit.ky (`hosting/index.html`) |
| `/alert-cayman/support/` | Support, with account deletion (`#delete`) | Copied from alert.grabit.ky/support |
| `/alert-cayman/privacy/` | Privacy policy | Copied from alert.grabit.ky/privacy |
| `/alert-cayman/terms/` | Terms | Copied from alert.grabit.ky/terms |
| `/easy-days/privacy/` | Privacy policy | From easy-days `docs/RELEASE.md` (reviewed) |
| `/easy-days/terms/` | Terms of service | New, adapted from Ludo Reign's terms; approved by Glen on 7 November 2026 |
| `/404.html` | Page not found | New |

Copied pages are word for word. The only changes are email addresses
(`@grabit.ky` → `@nautica.ky`), links that pointed at grabit.ky pages, the
"last updated" date on Easy Days' privacy policy, and the footer. Each
footer keeps its original links, pointing at their new addresses (Ludo
Reign: Support, Privacy, Terms, Delete account; Alert! Cayman's support
page: Privacy · Terms), with this line beneath them on every page:
"Published by Grab It US LLC · 407 Lincoln Rd, Suite 6H, PMB 1470, Miami
Beach, FL 33139 · *app*@nautica.ky". The pull request that added them shows
a diff of each whole page, footer included, against its source.

Ludo Reign's pages on grabit.ky had a "Grab It" wordmark at the top,
linking to the game's home page. As Glen decided, it isn't copied: each
page instead has a header with the crown icon and "Ludo Reign", linking to
`/ludo-reign/`. The publisher is named in the footer. Each page sits in its own folder
(`privacy/index.html`), so both `/ludo-reign/privacy` and
`/ludo-reign/privacy/` work.

Icons on the home page (144 × 144, shown at 72 px):
- Ludo Reign: the "App icon" tile from its approved crown emblem B
  (ludo-reign `docs/art/crown-emblem-chosen-b.png`), cropped, not redrawn.
- Easy Days: its app icon (design A).
- Alert! Cayman: its app icon.
- Pearlwake: a plain grey placeholder tile. Its repository has no approved
  icon yet; add `assets/icons/pearlwake.png` when it has one. Pearlwake has
  no pages here yet, only its support email.

No `app-ads.txt` yet: Ludo Reign has no real AdMob account. When it does,
add the line AdMob gives, exactly, as `/app-ads.txt`.

## Fonts

The fonts are served from this site, in `assets/fonts/`, as WOFF2 files with
their licences beside them. They are the files the pages loaded from Google
Fonts until 7 November 2026, downloaded on that date from the addresses in
Google Fonts' own stylesheets, Latin character set only (the pages are in
English). The `@font-face` rules are at the top of `assets/ludo-reign.css`
and `alert-cayman/site.css`, with the same weights and character ranges as
Google's.

| File | Font, weights used | Source | Licence | SHA-256 |
| - | - | - | - | - |
| `exo/exo-400-latin.woff2` | Exo 400 (Ludo Reign headings and links) | `fonts.gstatic.com/s/exo/v25/4UaZrEtFpBI4f1ZSIK9d4LjJ4lM3OwRmO3ws9Iq2uA.woff2` | SIL OFL 1.1 (`exo/OFL.txt`) | `7b9d22aabae35fb758f13a707c51e30cd56da2abccff84510154b122191979ec` |
| `manrope/manrope-latin.woff2` | Manrope, variable: 300 and 400 (Ludo Reign text), 500, 700 and 800 (Alert! Cayman) | `fonts.gstatic.com/s/manrope/v23/xn7gYHE41ni1AdIRggexSvfedN4.woff2` | SIL OFL 1.1 (`manrope/OFL.txt`) | `8bd97e6bbbc1f602a8f791530eed1064c9a357d5731bbc76e3fc587fb068728f` |
| `yellowtail/yellowtail-400-latin.woff2` | Yellowtail 400 (the "Cayman" of Alert! Cayman's wordmark) | `fonts.gstatic.com/s/yellowtail/v25/OZpGg_pnoDtINPfRIlLohlvHwWL9f4k.woff2` | **Apache 2.0** (`yellowtail/LICENSE.txt`), not the OFL | `ac99e23948e0d1edcca4772e3c430272b63803b3c722f3a9ed04bb48560e3696` |
| `exo/OFL.txt` | | `github.com/google/fonts`, `ofl/exo/OFL.txt` | | `1159ea72ed1f7e7541cea35a0dece48d2abb0317d7c70f75a482f94932382a77` |
| `manrope/OFL.txt` | | `github.com/google/fonts`, `ofl/manrope/OFL.txt` | | `58172e0c0fac2cda8a37b348164bb55e44b0e69051e557e92b1d3f6910141f7b` |
| `yellowtail/LICENSE.txt` | | `github.com/google/fonts`, `apache/yellowtail/LICENSE.txt` | | `cfc7749b96f63bd31c3c42b5c471bf756814053e847c10f3eb003417bc523d30` |

"→" (used on a few pages) isn't in any of these fonts, on Google Fonts
either, so it shows in the visitor's system font, as before.

**What the original pages loaded:**
- **Ludo Reign on grabit.ky** (WordPress, Twenty Twenty-Five theme): Manrope
  from grabit.ky's own theme folder
  (`/wp-content/themes/twentytwentyfive/assets/fonts/manrope/`), and no
  Google Fonts stylesheet or preconnect. Their styles named Exo for headings
  and links but nothing loaded it, so visitors without Exo installed saw a
  fallback font there. These pages load Exo, as the design intends, so
  their headings and links look slightly different from the grabit.ky
  originals.
- **Alert! Cayman on alert.grabit.ky:** Manrope (500, 700, 800) and
  Yellowtail from Google Fonts, with preconnects to Google's font servers.

## DNS for nautica.ky (Glen, at Bluehost)

nautica.ky's DNS and mail are at Bluehost. **Only two things change: the
apex A record and the `www` CNAME** (plus one new TXT record for GitHub).
Everything else stays exactly as it is.

| Record | Now | After |
| - | - | - |
| `nautica.ky` A | `66.235.200.147` | four records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` |
| `nautica.ky` AAAA | none | four records: `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153` |
| `www.nautica.ky` CNAME | `nautica.ky` | `gebanks19.github.io` |
| `_github-pages-challenge-gebanks19.nautica.ky` TXT | none | the value GitHub shows (step 1) |

**Not touched** (each is its own record, and none depends on the apex A
record): MX `mail.nautica.ky`; the A records for `mail`, `webmail`,
`cpanel`, `whm`, `webdisk`, `autodiscover`, `autoconfig`, `cpcalendars`,
`cpcontacts` and `ftp` (all `162.241.224.200`); SRV `_autodiscover._tcp`;
TXT for SPF, `_dmarc`, `default._domainkey` (DKIM) and
`_cpanel-dcv-test-record`. There is no wildcard record, as GitHub advises.

SPF, DKIM and DMARC already exist; nothing is missing. SPF
(`v=spf1 ip4:162.241.224.200 a mx include:websitewelcome.com ~all`) stays as
it is for now. Its `a` term will then cover GitHub's addresses, which never
send mail; dropping `a` later is a safe tidy-up, since the `ip4` term
already covers Bluehost's mail server.

1. **Verify the domain with GitHub first** (stops anyone else putting a site
   on it). GitHub → your profile picture → Settings → Pages → Add a domain →
   `nautica.ky`. GitHub shows a TXT record. In Bluehost: Domains →
   nautica.ky → DNS → add TXT, host `_github-pages-challenge-gebanks19`,
   value as shown. Back at GitHub, Verify. Keep this record for good.
2. **Turn on Pages.** After the pull request is merged: this repository →
   Settings → Pages → Build and deployment: Deploy from a branch, `main`,
   `/ (root)`. Custom domain: `nautica.ky` (the `CNAME` file already says
   so). Save.
3. **Change the two records** in Bluehost's DNS editor for nautica.ky:
   delete the A record `@` → `66.235.200.147`; add the four A records and
   the four AAAA records above for `@`; edit the `www` CNAME to
   `gebanks19.github.io`. If Bluehost has a CDN, "website security" or
   proxy turned on for nautica.ky (the site currently shows a "Performing
   security verification" page), turn it off for the website, so visitors
   reach GitHub directly.
4. **Tell Claude.** Claude checks with `dig` and `curl`: the records, that
   https://nautica.ky serves these pages with a valid certificate, that
   `www` redirects to `nautica.ky`, and that MX and the mail records are
   unchanged.
5. **Enforce HTTPS.** Once GitHub has issued the certificate (the option can
   take up to 24 hours to appear): Settings → Pages → tick Enforce HTTPS.

## Later: redirecting the old pages (Glen)

Keep the grabit.ky and alert.grabit.ky pages live until every store listing
points to nautica.ky. Then redirect each one permanently (301), never
delete: invitations and shared results already sent link to them.

- **grabit.ky (WordPress at Bluehost).** With a redirect plugin (for example
  Redirection) or in `.htaccess`, add permanent (301) redirects, each with
  and without the trailing slash:

  | Old | New |
  | - | - |
  | `/ludo-reign/` | `https://nautica.ky/ludo-reign/` |
  | `/ludo-reign/support/` | `https://nautica.ky/ludo-reign/support/` |
  | `/ludo-reign/privacy/` | `https://nautica.ky/ludo-reign/privacy/` |
  | `/ludo-reign/terms/` | `https://nautica.ky/ludo-reign/terms/` |
  | `/ludo-reign/delete-account/` | `https://nautica.ky/ludo-reign/delete-account/` |

- **alert.grabit.ky (Firebase Hosting).** Redirect only the public pages
  (`/`, `/privacy`, `/terms`, `/support`) to `https://nautica.ky/alert-cayman/…`
  with permanent redirects in `firebase.json`. Sign-in (`/__/auth/…`) and
  the admin console (`/admin`) stay exactly as they are. Claude prepares
  that change in the alert-cayman repository when the time comes.

## Glen's checklist

**Mail**
- [ ] Forward `easydays@`, `ludoreign@`, `pearlwake@`, `alert@` and `apps@`
      at nautica.ky to the inbox you read.
- [ ] Test each one both ways with Gmail: send to it from Gmail and see it
      arrive; reply from it and see the reply arrive in Gmail, not in spam.
- [ ] Keep the old `@grabit.ky` addresses forwarding to the new ones.

**Easy Days**
- [ ] Update Easy Days' terms ("no purchases and no ads") and privacy
      policy before the banner ad ships.

**AdMob (Ludo Reign)**
- [ ] When AdMob is set up for real: add its `app-ads.txt` line here, and
      confirm AdMob finds it at https://nautica.ky/app-ads.txt **before**
      changing Ludo Reign's store website.

**Play Console and App Store Connect, per live app**
- [ ] Ludo Reign: contact email `ludoreign@nautica.ky`; website
      `https://nautica.ky/ludo-reign/`; privacy policy
      `https://nautica.ky/ludo-reign/privacy/`; Play's **Delete account
      URL** `https://nautica.ky/ludo-reign/delete-account/`.
- [ ] Ludo Reign: Play Console **payments profile website** (now
      `https://grabit.ky/ludo-reign`) → `https://nautica.ky/ludo-reign/`.
- [ ] Alert! Cayman: contact email `alert@nautica.ky`; website
      `https://nautica.ky/alert-cayman/`; privacy policy
      `https://nautica.ky/alert-cayman/privacy/`; Play's **Delete account
      URL** `https://nautica.ky/alert-cayman/support/#delete`; Apple's terms
      link `https://nautica.ky/alert-cayman/terms/`.
- [ ] Easy Days (when its listing is created): contact email
      `easydays@nautica.ky`; website `https://nautica.ky`; privacy policy
      `https://nautica.ky/easy-days/privacy/`.

**Apple**
- [ ] Register `ludoreign@nautica.ky` with Sign in with Apple's private
      email relay: Apple Developer account → Certificates, Identifiers &
      Profiles → Services → Sign in with Apple for Email Communication →
      Configure email sources. Without this, emails to players who hid their
      address (such as account-deletion checks) won't arrive.

**Google sign-in (Ludo Reign's OAuth consent screen)**
- [ ] Verify nautica.ky in Google Search Console with its DNS TXT record
      first; Google only accepts authorised domains you own.
- [ ] Then: add `nautica.ky` as an authorised domain, and change the home,
      privacy and terms links to `https://nautica.ky/ludo-reign/…`.
- [ ] Change the developer contact email to `ludoreign@nautica.ky`. The user
      support email may have to stay a Google account
      (`grabitky345@gmail.com`); that's fine.

**Firebase**
- [ ] Glance at Authentication → Templates for each project. Alert! Cayman
      signs in by phone and Ludo Reign uses its own server, so none should
      be in use; if any are, change their reply-to to the app's
      `@nautica.ky` address.
