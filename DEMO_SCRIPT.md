# SnapSell AI — 2–4 Minute Demo Script

Use this as a guide while recording. Speak naturally and show the real app.

## 0:00–0:25 — Problem
"Online sellers need product images that look good and load efficiently across devices. Preparing and sharing optimized images can add extra work, especially for small shops."

## 0:25–0:50 — Solution
"SnapSell AI is a simple product-image studio. It uses Cloudinary to upload and store a product image, then delivers a transformed version through a Cloudinary URL."

## 0:50–2:10 — Live walkthrough
- Show the app.
- Enter your Cloudinary cloud name.
- Select a sample product photo.
- Click **Upload & optimize image**.
- Show the original and optimized delivery preview.
- Click **Open optimized image**.
- Click **Copy URL**.

Say: "The delivery URL uses `c_limit,w_1200` to limit the width, `f_auto` to request an appropriate format, and `q_auto` to request automatic quality optimization."

## 2:10–2:40 — Cloudinary integration
"The browser uploads directly to Cloudinary using an unsigned upload preset. Cloudinary stores the asset and serves the transformed image through its delivery URL. No API secret is embedded in the frontend."

## 2:40–3:00 — Honest limitations and next steps
"This prototype focuses on upload and optimized delivery. Next, I would extend it with a supported AI media feature such as automatic tagging or background removal, plus batch processing and a product catalog."

Only say that the upload and preview work if you have tested them successfully. Do not claim AI tagging or background removal is implemented.
