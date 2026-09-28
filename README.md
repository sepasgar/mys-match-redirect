# mys-match-redirect

Serves the old domain **mys-match.com** (GitHub Pages) and sends every visitor to **https://www.mysmatch.com**, keeping the path.

The only real content is `.well-known/`: installed app builds verify event deep links against mys-match.com, and iOS/Android do not follow redirects for those files, so they must keep being served here byte-for-byte. Keep them in sync with the main site repo (sepasgar/mys-match-website). Do not delete this repo while any app build still claims mys-match.com.

**Every page of the main site has a real redirect page here** (e.g. `privacy-policy/index.html`) so it answers HTTP 200. The `404.html` catch-all also redirects, but with a 404 status — which store policy checkers and crawlers read as a broken link (Google Play rejected the privacy-policy and account-deletion URLs because of it, Sept 2026). When a page is added to the main site, add its redirect page here too.
