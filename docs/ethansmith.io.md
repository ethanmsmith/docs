Deploy to GH Pages
Define homepage value in package.json
  "homepage": "http://ethanmsmith.github.io/ethansmith.io"
  "homepage": "http://{username}.github.io/{repository}"
  "homepage": "http://{username}.github.io/" //Custom domain
Add predeploy to scripts
Add deploy property
    "predeploy":"npm run build",
    "deploy":"gh-pages -d build"

Add A names to google domains

Add cname for www subdomain to point to github pages repo
ethanmsmith.github.io.
