TriDL backend starter (free Netlify Functions)
================================================

This package preserves the existing TriDL front-end design and adds a Netlify Function that validates public YouTube, TikTok, and Instagram links and tries to fetch public embed metadata.

IMPORTANT:
- This is NOT a video downloader and does not bypass platform restrictions.
- Public metadata lookup may fail for platforms/links that require authentication or restrict oEmbed.
- For YouTube, the official route supports downloading videos you uploaded via YouTube Studio: https://support.google.com/youtube/answer/56100
- For TikTok, use the platform's own Save video option when the creator permits it.
- For Instagram, use Instagram's own download/save features where available, or download your own originals.
- Do not paste platform passwords or private tokens into the website.

ANDROID DEPLOY STEPS
1. Download and unzip tridl-backend-starter.zip on your phone.
2. Open Netlify and sign in: https://app.netlify.com/
3. Important: a folder uploaded to Netlify Drop can be used for manual deploys, but for repeatable function deploys, connect a Git repository.
4. Go to https://github.com/new and create a repository named tridl-site. Set it private or public as you prefer.
5. In GitHub's browser UI, upload the files from this folder, keeping this structure:
   index.html
   netlify/functions/lookup.mjs
6. In Netlify, choose Add new site > Import an existing project, connect GitHub, and select tridl-site.
7. Use the default build settings for this plain HTML project (no build command; publish directory is the repository root). Deploy.
8. To keep your current address, open your existing Netlify site's Site configuration / Build & deploy / Continuous deployment and connect this repository to the EXISTING site, or use the site's deploy settings to link the repo. Do not create a new site unless you want a different URL.
9. After deploy, test the page and paste a public link. The function endpoint is /.netlify/functions/lookup.

If you use a new Netlify site instead, it will have a different netlify.app address unless you change the site's name and that name is available.
