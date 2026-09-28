# mys-match-redirect

Serves the old domain **mys-match.com** (GitHub Pages) and sends every visitor to **https://www.mysmatch.com**, keeping the path.

The only real content is `.well-known/`: installed app builds verify event deep links against mys-match.com, and iOS/Android do not follow redirects for those files, so they must keep being served here byte-for-byte. Keep them in sync with the main site repo (sepasgar/mys-match-website). Do not delete this repo while any app build still claims mys-match.com.
