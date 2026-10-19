# TNBS Lab website

A one-page website for the **Translational Neurophysiology & Brain Stimulation (TNBS) Lab** at the Krembil Brain Institute (University Health Network, University of Toronto).

## What's here

- `index.html` is the whole site in one self-contained file (HTML, CSS and JavaScript). The only outside request is to Google Fonts.
- The hero has an interactive, simulated 3D neuron (you can drag to rotate it) and a live spike trace.
- The page has a scroll-progress bar, a nav that highlights the current section, filters for publications by year, and a copy-email button.
- Animations are turned off when the visitor's system asks for reduced motion.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

The site is static, so any static host works: GitHub Pages (Settings → Pages → deploy from the `main` branch, root folder), Netlify, Vercel or Cloudflare Pages.
