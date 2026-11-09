# TNBS Lab website

A one-page website for the **Translational Neurophysiology & Brain Stimulation (TNBS) Lab** at the Krembil Brain Institute (University Health Network, University of Toronto).

## What's here

- `index.html` is the whole site in one self-contained file (HTML, CSS and JavaScript). The only outside request is to Google Fonts.
- The design is "neural glass": frosted-glass panels over slowly shifting aurora light (amber, violet, teal) that moves to a new arrangement as you scroll from section to section.
- The whole site is set in Barlow (from Google Fonts): bold for headings, with coloured accent words, and regular for body text and labels.
- The hero shows an interactive 3D layer 5 pyramidal neuron in a glass chamber. You can drag it to rotate it, and the button in the chamber's corner resets the view.
  - The chamber is styled as an EEG recording: each cortical layer boundary (L1 to L6, at rat barrel-cortex depths) is a live, scrolling EEG trace with a montage label (FP1–F7, F7–T3, T3–T5, T5–O1, C3–P3), over green chart-paper divisions. The two deepest traces show a sharp transient each time the neuron fires.
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

## Photos and video

All photos come from the lab's current website (torontotnbs.com). They are stored in `assets/` as web-sized WebP files, with a 640 px version for phones where a photo is shown large.

| Folder | What's in it | Where it appears |
|---|---|---|
| `assets/img/logo/` | The TNBS logo and favicons | Nav, footer, browser tab |
| `assets/img/about/` | DBS implantation surgery | About (Fig. 01A) |
| `assets/img/life/` | 20 lab-life photos, 2022–2026, named after their captions | About (Fig. 01B), Facilities (Fig. 04B), and the lab-life filmstrip in Team |
| `assets/img/facilities/` | Fluorescent microscopy, Krembil Discovery Tower | Facilities (Fig. 04A) |
| `assets/img/team/` | Dr. Milosevic's portrait, the team photo and 18 lab-member portraits | Team |
| `assets/img/pubs/` | One figure for each publication | Publications |
| `assets/img/join/` | King's College Circle, University of Toronto | Join the lab |
| `assets/img/funding/` | The funders banner (CIHR's lettering is darkened so it reads on the white card) | Footer |
| `assets/video/` | Poster frame for the video | Inside the operating room |

The video is **Meet Prof. Luka Milosevic: Advancing Brain Stimulation Research** from U of T Biomedical Engineering on YouTube. It shows a local poster frame, and the YouTube player (from youtube-nocookie.com) loads only after someone presses play.

Photos marked as enlargeable open in a photo viewer: the About and Facilities photos, the team photo, King's College Circle and the lab-life filmstrip. Arrow keys step through the photos in the same group.

To update the media:

- **Replace a photo:** save the new image over the old file. Keep the same name and roughly the same shape, or edit the matching `<img>` in `index.html`.
- **Add a lab member:** copy one `<li class="tm">` card in the team list. Change its photo, name, role and one-line focus, and set its `data-group` to `postdoc`, `phd`, `masc` or `ugrad` so the role filter counts it.
- **Add a lab-life photo:** copy one `<li class="film-item">` in the filmstrip.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

The site is static, so any static host works: GitHub Pages (Settings → Pages → deploy from the `main` branch, root folder), Netlify, Vercel or Cloudflare Pages.
