# SnapSell AI — Product Image Studio

**HackIndia × Cloudinary hackathon prototype | Track: PS-01 — AI Media Pipelines**

SnapSell AI is a lightweight product-image workflow for small online sellers. It uploads an image directly to Cloudinary, shows the source image, creates an optimized delivery URL, and lets the user copy that URL for reuse in a storefront.

## Features

- Responsive, mobile-friendly interface
- JPG, PNG, and WEBP file validation (10 MB limit)
- Direct browser-to-Cloudinary upload using an unsigned upload preset
- Cloudinary asset storage in the `snapsell-products` folder
- Automatic format and quality delivery using `f_auto` and `q_auto`
- Width-limited delivery transformation (`c_limit,w_1200`)
- Original and optimized preview, plus copy/open URL actions

## Tech stack

- HTML, CSS, JavaScript
- Cloudinary Upload API
- Cloudinary image URL transformations

## Setup

1. Create a Cloudinary account: https://cloudinary.com/
2. In the Cloudinary Console, find your **Cloud Name**.
3. Go to **Settings → Upload → Upload presets** and create a preset named `snapsell_unsigned`.
4. Set its **Signing Mode** to **Unsigned**, then save.
5. Open `index.html` in a browser. Enter your cloud name in the form. The preset field is prefilled with `snapsell_unsigned`.
6. Choose a JPG, PNG, or WEBP image and click **Upload & optimize image**.

No API secret is needed or should be added to this frontend project.

## Run locally

You can open `index.html` directly. For a local web server, run this from the project directory:

```bash
python -m http.server 8000
```

Then open http://localhost:8000.

## Deploy with GitHub Pages

1. Create a **public** GitHub repository named `snapsell-ai`.
2. Upload `index.html`, `README.md`, and `LICENSE`.
3. In repository **Settings → Pages**, choose deployment from the `main` branch and `/ (root)`.
4. Save and wait for GitHub Pages to publish the site. Test the published URL.

## Demo video (2–4 minutes)

Suggested recording outline:
1. **Problem (15–25 sec):** sellers need product photos that load efficiently on different devices.
2. **Solution (20–30 sec):** introduce SnapSell AI and its upload-to-delivery workflow.
3. **Live demo (60–100 sec):** upload an example product image, show the original and optimized delivery preview, open the transformed URL, and copy it.
4. **Cloudinary role (20–30 sec):** explain direct upload, cloud storage, and URL transformations using `c_limit,w_1200`, `f_auto`, and `q_auto`.
5. **Limitations / next steps (15–25 sec):** explain that AI tagging, background removal, and moderation are not implemented in this MVP.

Record your actual working app; do not claim a feature that is not present.

## Important scope note

This version demonstrates Cloudinary upload, storage, and optimized delivery. Despite the product name, it does **not** currently implement AI tagging, background removal, moderation, or generative image creation. If the judging rubric requires an AI Skills Pack feature specifically, add and demonstrate a real supported AI feature before claiming full compliance.

## Security

- Never commit your Cloudinary API secret, passwords, or access tokens.
- An unsigned upload preset is intentionally usable from the browser. Configure upload restrictions in Cloudinary, and use a signed server-side upload flow for a production app.
- Do not upload private or sensitive images to a public demo.

## Project structure

```text
snapsell-ai/
├── index.html
├── README.md
├── SUBMISSION_CHECKLIST.md
├── DEMO_SCRIPT.md
└── LICENSE
```

## Credits

Built as a hackathon prototype using Cloudinary's media upload and transformation capabilities.
