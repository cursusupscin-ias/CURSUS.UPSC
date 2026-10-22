# CURSUS UPSC — GitHub Pages package

This package is arranged for the repository root of `cursusupscin-ias/CURSUS.UPSC`.

## Included
- `index.html` — CURSUS UPSC Resource Library homepage
- `assets/` — branding images used by the homepage
- `constitution-companion/index.html` — standalone Constitution Companion

## Publish on GitHub Pages
1. Open the repository `https://github.com/cursusupscin-ias/CURSUS.UPSC`.
2. Choose **Add file → Upload files**.
3. Upload the *contents* of this package (not the enclosing ZIP and not the enclosing folder) so `index.html` appears at the repository root and `assets/` and `constitution-companion/` are beside it.
4. Commit the upload to the `main` branch.
5. Open **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, branch `main`, folder `/(root)`, then **Save**.
6. Wait for the Pages deployment to finish. The expected site URL is `https://cursusupscin-ias.github.io/CURSUS.UPSC/`.

## Important backend notes
- The resource library uses Supabase for its resource records, PDF storage, and Publisher sign-in. This package does not migrate or delete your Supabase data.
- The Supabase URL and publishable client key in the homepage are browser-side settings; do not put a Supabase service-role/secret key in any public HTML file.
- Before relying on Publisher uploads/deletes, verify Supabase Row Level Security and Storage policies restrict write/delete operations to authorized publishers.
- GitHub Pages hosts static files; it is not unlimited storage and does not replace Supabase. Keep PDFs in Supabase unless you intentionally want them public in the repository.
- The existing Netlify site is not changed by this package. Test GitHub Pages first, then decide whether to keep Netlify as a backup.

## Local reference checks
Homepage references `assets/favicon.png`, `assets/logo-icon.png`, and `assets/logo-full-dark.png`; all are included. The Constitution Companion is self-contained and uses an embedded logo image.
