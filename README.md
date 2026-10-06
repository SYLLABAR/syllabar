# Syllabar Language Center – landing page

A static website, with no build step. Vercel serves the files exactly as they are.

```
index.html          the whole page (layout, text, forms, FAQ, payment step)
assets/logo.png     header and hero logo (also the browser tab icon)
assets/logo-full.svg footer logo
assets/daymara.jpg  team photos
assets/magoma.jpg
assets/kakunga.jpg
vercel.json         small Vercel settings (clean URLs, caching for images)
```

## Deploy on Vercel

**Option A: GitHub (recommended, so later updates deploy automatically)**
1. Create a new repository on github.com, for example `syllabar-site`.
2. Upload everything in this folder to it: drag the files onto **Add file › Upload files** and commit.
3. On vercel.com, click **Add New › Project**, import the repository and click **Deploy**.
   Framework preset: **Other**. Leave the build command empty and the output directory as is.
4. You get a link like `syllabar-site.vercel.app`.

**Option B: Vercel CLI**
```
npm i -g vercel
cd syllabar-site      # this folder
vercel                # first deploy (preview)
vercel --prod         # publish to production
```

## Use your own domain (syllabar.com)
In Vercel, go to **Project › Settings › Domains**, add `syllabar.com` (and `www.syllabar.com`), then add the DNS records
Vercel shows you at your domain registrar.

## Useful links to share
- Registration form: `https://syllabar.com/#register`
- Free trial form:   `https://syllabar.com/#contact`
- FAQ:               `https://syllabar.com/#faq`

## Before going live
- Check the Paybill (522533 / 8133903) and KCB (1355869331) details carefully.
- **M-Pesa prompt:** the button shows the "Check your phone" screen but does not send a real STK push yet.
  That needs a developer to connect Safaricom Daraja (or Pesapal, Paystack, etc.) through a small server function.
  Paybill and bank transfer work today as manual payments.
- **Forms:** "Request my free trial" and "Complete my registration" open the visitor's email app with all the details
  filled in, addressed to info@syllabar.com. To receive submissions without the email app, connect a form service
  such as Formspree, or a Vercel serverless function.
- The refund policy in the FAQ has **[7]** placeholders. Replace them with your real terms (search `[7]` in index.html).

## Editing text later
Open `index.html` in any text editor, find the sentence, change it, save and upload again. With option A, commit on GitHub
and Vercel redeploys within about a minute.
