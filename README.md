# TNBS Lab website

A one-page website for the **Translational Neurophysiology & Brain Stimulation (TNBS) Lab** at the Krembil Brain Institute (University Health Network, University of Toronto).

## What's here

- `index.html` is the whole site in one self-contained file (HTML, CSS and JavaScript). The only outside request is to Google Fonts.
- The design is "neural glass": frosted-glass panels over slowly shifting aurora light (amber, violet, teal) that moves to a new arrangement as you scroll from section to section.
- The hero shows an interactive 3D layer 5 pyramidal neuron in a glass chamber. You can drag it to rotate it, and the button in the chamber's corner resets the view.
  - A cortical layer gauge (L1 to L6) beside the neuron marks the layer boundaries, using rat barrel-cortex depths.
  - A glass oscilloscope shows the simulated single-unit recording and its firing rate.
  - The chamber glows each time the cell fires.
- Each research card has a small live visual:
  - spike, LFP and ECoG traces
  - a charge-balanced DBS pulse train
  - strengthening synapses
  - a 10–20 EEG montage
  - a spectrogram with beta-band bursts
  - optogenetic light with the calcium response
- Other interactive pieces:
  - a glass nav whose highlight slides to the current section, with a scroll-progress line
  - a full-screen glass menu on phones
  - a sliding year filter for publications
  - an orbiting diagram of collaborating disciplines
  - a learning curve for the workshop sessions
  - copy-email
  - a live Toronto clock
- Animations are turned off when the visitor's system asks for reduced motion, and decorative animations pause while their section is off screen.

## Adding the lab's photos and video

The photo and video spots show a "coming soon" placeholder. Each one is marked in `index.html` with an HTML comment such as `<!-- Photo: DBS implantation surgery ... -->`. Put an `<img>` (or a `<video>`) right after that comment, inside the same `<div class="frame">`, and it fills the frame and covers the placeholder:

```html
<img src="images/dbs-surgery.jpg" alt="DBS implantation surgery at Toronto Western Hospital">
```

| Spot | Section |
|---|---|
| DBS implantation surgery | About |
| Operating-room video (`<video src="..." controls playsinline>`) | Inside the operating room |
| Krembil Brain Institute (pictured: Dr. Taufik Valiante) | Facilities |
| CRANIA Neuromodulation Suite | Facilities |
| Portrait of Dr. Luka Milosevic | Team |
| The TNBS team, 2026 | Team |

The team member names and roles marked `[ ]` are still placeholders from the old site's team page.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

The site is static, so any static host works: GitHub Pages (Settings → Pages → deploy from the `main` branch, root folder), Netlify, Vercel or Cloudflare Pages.
