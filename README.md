# Coastline Exotics Car Rental

Website for Coastline Exotics, exotic, luxury and family car rental in Los Angeles and Orange County, California.

It's a static site: one `index.html` and an `images/` folder. No build step.

## Put it online

**GitHub Pages (free):** in this repo go to **Settings → Pages**, set **Source** to "Deploy from a branch", choose `main` and `/ (root)`, and save. The site appears at `https://novin101.github.io/coastline/` within a minute or two. You can add your own domain on the same page.

**Netlify or Vercel:** import this repo; there's nothing to configure.

## Edit the fleet

The cars are listed near the bottom of `index.html` in the `FLEET` list:

```js
{ id:"es350", make:"Lexus", model:"ES 350", year:"2025", tag:"Luxury sedan",
  line:"Quiet, smooth, made for the 405.",
  specs:["V6","Sedan","5 seats"], pos:"50% 56%", photo:"images/es350.webp" },
```

- To add a car, copy one entry, give it a new `id`, and put its photo in `images/`.
- `feature:true` makes a car full width at the top of the fleet.
- `pos` moves the photo inside its frame (horizontal %, vertical %).
- Leave `photo` empty to show a "Photo coming soon" placeholder.

The inquiry form dropdown and the footer fleet list update automatically.

## Inquiry form

The form checks the visitor's details, then sends the inquiry through Formspree (form `xljgywkl`) to the email on your Formspree account. The endpoint is set in `index.html` as `FORMSPREE`. If a submission fails, the visitor sees an error with a direct link to coastlineexoticsca@gmail.com. A hidden `_gotcha` field catches spam bots.
