# althyr pivatto — website

## Files

- `index.html` — homepage
- `credits.html` — stage credits
- `audio.html` — dubbing, translation, voice direction
- `teaching.html` — workshops (coming soon) + past teaching
- `contact.html` — contact form
- `style.css` — all shared styles
- `images/` — put your poster images here

## Image files needed

Rename your 3 poster images exactly as follows and place them in the `images/` folder:

- `images/frankenstein.jpg` — Frankenstein: Fragments of War poster
- `images/river.jpg` — Where the River Meets the Sea poster
- `images/demons.jpg` — Demons poster

The site will show a placeholder if an image is missing, so the rest of the page still looks fine.

## Deploying to GitHub Pages

1. Go to github.com and sign in as `althyr`
2. Create a new repository — name it exactly: `althyr.github.io`
3. Upload all these files (drag and drop onto the repository page)
4. Go to Settings > Pages > set Source to "main" branch
5. Your site will be live at: https://althyr.github.io

## Connecting your custom domain (althyrpivatto.com)

Once the GitHub Pages site is live:

1. In your GitHub repo, go to Settings > Pages > Custom domain
2. Type: `althyrpivatto.com` and save
3. GitHub will create a file called `CNAME` automatically

Then log in to GoDaddy:
4. Go to DNS settings for althyrpivatto.com
5. Delete any existing A records
6. Add these 4 new A records (Type: A, Name: @, TTL: 600):
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153
7. Add a CNAME record: Name: `www`, Value: `althyr.github.io`

DNS changes take up to 24 hours but usually under an hour.

## Contact form

The contact form currently shows a success message but doesn't actually send email.
To make it send real emails, the easiest free option is Formspree:
1. Go to formspree.io and create a free account
2. Create a new form — you'll get a form endpoint URL
3. In contact.html, change the <form> tag to:
   <form action="https://formspree.io/f/YOUR_ID" method="POST">
   and remove the onsubmit handler and the JS at the bottom.

## Updating content

All content is plain HTML — just open the file in any text editor and change the text.
No database, no CMS, no login required.
