# Deployment

## Where it is now

The site deploys from the GitHub repository ashakbari/firstnationscourt (branch main, root folder) to GitHub Pages at:

https://ashakbari.github.io/firstnationscourt/

To publish a change: edit the files, commit, and push to main. Pages rebuilds by itself within a minute or two. No build step exists; what is in the repository is what is served.

## Moving to firstnationscourt.ca

Two good options once the domain is bought. Either way, after the domain is live, do the "after the domain" steps at the bottom.

### Option A, stay on GitHub Pages (simplest, free)

1. Buy firstnationscourt.ca at any registrar.
2. In the repository on github.com: Settings, then Pages, then Custom domain. Enter firstnationscourt.ca and save. This commits a CNAME file.
3. At the registrar, add these DNS records:
   - Four A records for the apex (@): 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - A CNAME record for www pointing to ashakbari.github.io
4. Back in Settings, Pages: wait for the DNS check to pass, then turn on "Enforce HTTPS".

### Option B, Kinsta Static Site Hosting (the original plan)

1. Sign up at kinsta.com and open MyKinsta.
2. Add service, then Static site. Connect the GitHub account and pick ashakbari/firstnationscourt.
3. Settings: branch main, build command left empty, publish directory left as the repository root. Deploy.
4. In the static site's Domains tab, add firstnationscourt.ca and follow the DNS records Kinsta shows (a CNAME to their endpoint). SSL is issued automatically once DNS propagates.
5. Check Kinsta's current docs if the screens look different; this was written August 2026.

## After the domain is live

1. In sitemap.xml, replace every https://ashakbari.github.io/firstnationscourt/ with https://firstnationscourt.ca/
2. In robots.txt, update the Sitemap line the same way.
3. Commit and push.
4. Work through LAUNCH-CHECKLIST.md (phone spot-checks, court list re-verification, author note, images).
