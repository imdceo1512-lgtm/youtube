# OAuth Branding and free site setup

The app is External. Google requires homepage and privacy-policy links for an External app in production; its Cloud branding guide also lists the Terms of Service field. Use real public pages on a domain that can be verified. Do not enter a placeholder URL.

## Public pages prepared for you

The three files in the site folder are:
- site/index.html — app homepage
- site/privacy.html — Google data and retention policy
- site/terms.html — usage terms

Publish only these files. Never upload the whole T:\YouTubeAutopilot folder, the secrets folder, OAuth JSON, tokens, or channel data.

## Free static hosting option

GitHub Pages is available on GitHub Free for public repositories. If you have a GitHub account, create a public repository named YOUR-USERNAME.github.io and put the three HTML files at the repository root. Enable Pages for the repository. The expected links are:

- https://YOUR-USERNAME.github.io/
- https://YOUR-USERNAME.github.io/privacy.html
- https://YOUR-USERNAME.github.io/terms.html

Then add https://YOUR-USERNAME.github.io/ to Google Search Console as a URL-prefix property. Use the HTML-file verification option: download Google's unique verification file, place that exact file in the repository root, commit it, then click Verify in Search Console. After verification, add the verified host to Authorized domains in Google Auth Platform. If Google will not verify or accept the GitHub Pages host, stop there; do not use an unrelated or invented domain.

## Finish Google Auth Platform

1. Branding: set the app name to Local Creator Publisher. Choose a support email you monitor; Google displays it on the authorization consent screen. It is separate from the public YouTube channel page. Add the developer contact email for Google project notices.
2. In App Domain, enter the live homepage, privacy policy, and terms links above. Save.
3. Audience: set Publishing status to In production and click Publish app.
4. Google may show an unverified-app warning when you grant the YouTube scopes. A personal-use app can generally remain unverified for fewer than 100 users, but you must read the warning and authorize only your own project.

If you keep the app in Testing, Google says authorizations for these YouTube scopes expire after seven days, which would interrupt daily automation.
