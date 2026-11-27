# Yoga & Fitness Classes

**Live demo:** https://yoga-fitness-classes.vercel.app  
**Repository:** https://github.com/sarveshkamdi7-collab/yoga-fitness-classes

![Yoga class hero image used on the home page](yogaimg1.webp)

A static, multi-page website for a yoga and fitness group. It presents yoga benefits, guided pose demonstrations, a weekly timetable, enrollment and contact forms, certifications, and embedded fitness sheets. The site is built with plain HTML and CSS, uses Bootstrap 5 from a CDN, and has no backend or build step.

## Highlights

- Nine linked HTML pages with a shared navigation bar on most pages.
- Local image assets and one local Padmasana demonstration video.
- Bootstrap 5.3 components loaded from jsDelivr.
- Embedded Google Sheets for the fitness tracker and diet plan.
- Deployed as a static site on Vercel, with `/` rewritten to `yogafitness.html`.
- No JavaScript source files, package manager, database, or server-side code.

## Pages

| File | Purpose |
| --- | --- |
| `yogafitness.html` | Home page with hero section and yoga, meditation, and diet benefits. |
| `login.html` | Login form UI with a local background image. |
| `live.html` | Pose demonstrations for Padmasana, Vrikshasana, and Uttanasana. |
| `schedule.html` | Weekly class timetable and embedded fitness diet sheet. |
| `aboutus.html` | Group introduction, mission, and reasons to join. |
| `contactus.html` | Contact form and contact details. |
| `enroll.html` | Enrollment form UI. |
| `cert.html` | Instructor certification cards. |
| `fit.html` | Embedded fitness progress tracker. |

## Run locally

No installation or build step is required.

Open `yogafitness.html` directly in a browser, or serve the folder locally:

```powershell
cd "E:\html css projects\mini_project_yogaclasses"
py -m http.server 8000
```

Then visit:

```text
http://localhost:8000/yogafitness.html
```

Use `python -m http.server 8000` if `py` is not available. Internet access is needed for Bootstrap CDN files and the two Google Sheets embeds.

## Media inventory and image descriptions

| Asset | Type | Used in | Description / accessible text |
| --- | --- | --- | --- |
| `yogaimg1.webp` | Image | `yogafitness.html` | Hero image on the landing page. HTML alt text: `yoga`. Also linked as a full-size image. |
| `yoga.webp` | Image | `style.css` | Yoga-themed CSS hero background defined for `.yogaimg`; no HTML alt text because it is a background image. |
| `yogaimg2.jpg` | Image | `yogafitness.html` | Benefit card for yoga, placed with the “Benefits of Yoga” section. HTML alt text: `yoga benefits`. |
| `meditation.jpg` | Image | `yogafitness.html` | Benefit card for meditation, placed with the “Benefits of meditation” section. HTML alt text: `meditation benefits`. |
| `diet.jpg` | Image | `yogafitness.html` | Benefit card for diet, placed with the “Benefits of diet” section. HTML alt text: `diet benefits`. |
| `yoga_group.webp` | Image | `aboutus.html` | Group photo used beside the “Why Join Us?” list. HTML alt text: `Yoga group`. |
| `padmasanaimage.webp` | Image | `live.html` | Padmasana pose reference shown with the figure caption `Padmasana`. HTML alt text: `padmasana`. |
| `padmasanavideo.mp4` | Video | `live.html` | Local MP4 demonstration for the Padmasana pose, shown with playback controls. No captions or transcript are provided. |
| `vrik.jfif` | Image | `live.html` | Vrikshasana, or Tree Pose, reference shown with the figure caption `vrikasna`. HTML alt text: `vrikasna`. |
| `ut.jfif` | Image | `live.html` | Uttanasana, or standing forward bend, reference in the pose description section. HTML alt text: `uttanasana`. |
| `yogacert1.webp` | Image | `cert.html` | Certificate sample in the “National yoga Certified center” card. HTML alt text: `Sample Certificate`. |
| `yogacert2.jfif` | Image | `cert.html` | Certificate sample in the “Fitness Trainer Certification” card. HTML alt text: `Sample Certificate`. |
| `loginbg.jpeg` | Image | `style.css`, `login.html` | CSS background image for the login page; no HTML alt text because it is a background image. |

## Deployment

The production site is hosted at https://yoga-fitness-classes.vercel.app. The `vercel.json` rewrites the root path to `yogafitness.html`, so visitors land on the home page without seeing the file name.

To redeploy from a local copy:

```powershell
npx vercel@latest --prod
```

## Notes

- Login, contact, and enrollment forms are front-end demos only; they do not authenticate users or submit/store data.
- The two embedded sheets require network access and appropriate sharing permissions.
- The custom CSS uses large fixed widths, so the layout is best viewed on wide desktop screens.
- `style2.css` is reserved for contact-page styling and is currently empty.

## License

Released under the MIT License. See `LICENSE`.
