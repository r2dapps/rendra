# RENDRA — Positioning, Promotion & Growth Plan for AEC

*Prepared 16 November 2026. Market prices come from published 2026 comparisons and vary by source, so confirm them on each vendor's site before quoting them publicly.*

## 1. Honest summary

RENDRA is a **free, private, zero-install SketchUp-to-GLB viewer and presentation studio that runs in the browser**. That is a real and useful niche. It is **not** a replacement for Lumion, D5 Render, Twinmotion or Enscape for hero-quality marketing renders, and positioning it as one would hurt credibility with professionals.

**Where it can win:** quick client previews, sharing a model with people who do not own SketchUp, converting SKP to GLB for web and AR, basic sun studies and measuring, and quick social clips.

**Where it loses today:** photorealism, material and asset libraries, BIM/IFC workflows, sharing links, collaboration, and enterprise trust.

**Recommended positioning:** *"The fastest way to show a SketchUp model to a client. Open it, light it, send it, with nothing to install and nothing uploaded."*

## 2. Specialities today

- **Runs entirely in the browser.** There is no install, no GPU workstation requirement, and it works on a phone or tablet.
- **Privacy by design.** Files are converted on the user's own device. This matters to firms under NDA, and few competitors can claim it.
- **SKP to GLB in one step.** It is useful for web, AR, game engines and Blender pipelines.
- **Lumion-style context in seconds.** The tool provides a 180° solar arc, procedural terrain, roads, traffic, trees, a sky dome, clouds and weather.
- **Director tools.** It has one-click looks, mist, rain and snow, photo capture, WebM film recording, a cinematic tour and a clean-screen mode.
- **Inspection tools.** It offers section planes, x-ray, clay mode, a tape measure, a 2D plan with click-to-focus, an outliner and selection bounding boxes.
- **PWA and offline.** It is installable and works offline after the first load.
- **Price.** It is free, which is a strong hook against paid tools.

## 3. Market context

Real-time rendering for architects is crowded, and the leaders are well funded. Approximate 2026 list prices from published comparisons:

| Tool | Typical entry price | Notes |
| --- | --- | --- |
| Twinmotion | Free under $1M revenue; about $445/seat/year above that | Runs on Mac and Windows |
| D5 Render | Free Community tier; Pro about $360/year | Windows, GPU-hungry |
| Enscape | From about $575/year | Live link to Revit, SketchUp and others |
| Lumion | View about $229/year; Pro about $1,149/year (some sources quote lower) | Strong exteriors and landscapes, high hardware demand |
| V-Ray | From about $515–540/year | Photorealism standard |

**Takeaway:** "free" alone is not a differentiator, because Twinmotion and D5 already have free tiers. RENDRA's difference is **no install, no GPU, no upload, instant sharing**. Lead with that.

## 4. Is it really useful for marketing?

**Yes, for these jobs:**

- A first client look at massing, orientation and sun and shadow, sent as a clip or photo within minutes.
- Social content such as sun-study timelapses, before/after weather looks and turntable clips.
- Pre-sales and real estate teasers where a stylised look is acceptable.
- Student and freelancer portfolios.

**Not yet, for these jobs:**

- Final marketing imagery for premium developments. Clients expect photoreal materials, people, vegetation and glass, which a stylised procedural world cannot deliver.
- Competition boards that need print-resolution stills.
- Regulated deliverables such as BIM coordination and IFC handover.

The honest line for clients is *"concept and review visuals"*, not *"final renders"*.

## 5. Drawbacks of the current page

**Visual quality**

- The world is stylised and low-poly. Materials are basic, with no PBR texture library, no HDRI sky, no ambient occlusion or bloom, and no people, furniture or detailed vegetation.
- Photos are captured at the canvas size, with no 4K or print-resolution export.

**Workflow gaps**

- There is no shareable link or embed, so a client cannot open "your" model without receiving the file.
- There is no IFC or Revit import, no comments or markup, no versions and no accounts.
- SKP support depends on the OpenSKP library. SKP versions, textures, components and very large files need systematic testing.
- Recording is WebM only, which does not play everywhere. MP4 is what marketers expect.

**Technical and maintenance**

- The app is one very large HTML file, with no automated tests and no build step. This makes it risky to extend.
- It loads libraries (three.js, OpenSKP, fonts, Tailwind) from public CDNs. The Tailwind CDN script is not intended for production, and this weakens the "fully offline and private" claim until everything is bundled.
- Performance on phones is untested with heavy models (the loaded GLB in your screenshot had about 616k triangles).

**Business and legal**

- There are no analytics, no feedback loop and no monetisation yet.
- Check the licence and terms of OpenSKP and of every asset or library you ship. Avoid implying any affiliation with SketchUp or Trimble, and use their name only descriptively.
- "Nothing is uploaded" is accurate for the user's model, but state clearly that third-party CDNs are contacted until libraries are self-hosted.

## 6. Improvement roadmap

### Priority 1: do first (1–4 weeks)

1. **Bundle and self-host everything.** Use Vite, compiled Tailwind and local copies of three.js and OpenSKP. This delivers true offline use and a verifiable privacy claim.
2. **Better stills.** Add 2x and 4x export, transparent background and a watermark option.
3. **MP4 export.** Use WebCodecs or ffmpeg.wasm, with fixed 1080p and 4K resolution presets.
4. **Visual upgrade.** Add an HDRI sky, SSAO, soft bloom, depth of field and a proper sun and shadow quality setting.
5. **Real sun study.** Let the user pick a location and date (a SunCalc-style calculation) and export a day timelapse.
6. **Large-model handling.** Add GLB optimisation with meshopt or Draco, instancing, and a low-power mode for phones.
7. **Feedback and analytics.** Use privacy-friendly analytics and a one-click feedback button.

### Priority 2: differentiate (1–3 months)

1. **Share links.** A read-only viewer link or embed so a client opens the model in a browser. This is the strongest feature for AEC marketing and a natural paid feature.
2. **AR and mobile.** Export USDZ and GLB for iOS Quick Look and Android Scene Viewer, with a QR code to view the building at site scale.
3. **Markup and comments.** Pins, screenshots with notes and a review list the client can export as PDF.
4. **Material and asset library.** Add PBR materials, people, cars, furniture and vegetation. Use CC0 assets and track their licences.
5. **Branded presentation mode.** Provide a studio logo, title cards, a lower-third and camera bookmarks (scenes) with animated transitions.
6. **Quantities.** Offer area and volume read-outs, per-material counts and a CSV export.

### Priority 3: grow (3–9 months)

1. **IFC/Revit-via-glTF support** and Rhino or Blender round-trips.
2. **Team plans** with a shared library, brand kits and an admin console.
3. **Cloud rendering** (path-traced stills) as a paid add-on for the "final image" gap.
4. **Plugin or API** so firms can embed the viewer in their own sites and proposals.

## 7. Who to target in AEC

| Segment | Why they care | Pitch |
| --- | --- | --- |
| SketchUp freelancers and small studios | Price sensitive, no GPU workstation, need quick client wins | "Show the design today, not after an overnight render" |
| Interior designers | Need fast visuals for clients on phones | "Send a walkthrough clip from any laptop" |
| Real estate and developers' sales teams | Need teasers for off-plan units | "Shareable 3D preview link" (needs share links) |
| Contractors and estimators | Need to review models without SketchUp | "Open, section and measure with no licence" |
| Students and colleges | Free access and easy sharing for crits | Campus ambassadors and workshop kits |
| Indian and emerging-market studios | Heavy SketchUp use, tight budgets, mobile-first clients | Local-language demos and a WhatsApp-friendly share flow |

## 8. Where to promote

| Channel | What to post | Effort |
| --- | --- | --- |
| **Product Hunt** | A launch with a 30-second demo clip and a clear "no install, no upload" tagline | Medium, one day |
| **Hacker News (Show HN)** | A technical post about running SKP-to-GLB entirely in the browser | Low |
| **Reddit** (r/SketchUp, r/archviz, r/architecture, r/threejs, r/webdev, r/InternetIsBeautiful) | Demos and before/after clips. Read each community's self-promotion rules first | Low, ongoing |
| **SketchUp Community forum and SketchUcation** | Helpful answers to "how do I share my model" with the tool as a solution | Medium |
| **LinkedIn** | Short sun-study clips, "how I sent a client a model in 5 minutes" and founder-story posts. AEC buyers are very active here | Medium, ongoing |
| **YouTube and Shorts / Instagram Reels** | Tutorials such as "SKP to GLB in 10 seconds" and "Golden hour from a phone" | High, high payoff |
| **Behance, ArtStation, CGarchitect** | Portfolio-style showcases made with the tool | Low |
| **Three.js Discourse and showcase** | The technical build log. Developers often become advocates | Low |
| **Sketchfab and glTF communities** | The GLB export workflow | Low |
| **Discord and Telegram/WhatsApp groups** (archviz, SketchUp India, architecture students) | Direct demos and feedback requests | Low |
| **AlternativeTo, SaaSHub, Slant, directories of free design tools** | Listings as an alternative to Lumion, D5 and Twinmotion | Low, one-time |
| **GitHub and Dev.to** | An open-source or source-available repo with the README, plus build-in-public posts | Medium |
| **Colleges and architecture schools** | A free workshop and a student licence | Medium, high trust |
| **AEC newsletters and bloggers** | Short pitches with a demo link. Offer a free exclusive feature walkthrough | Medium |

## 9. A 90-day go-to-market plan

**Days 1–30: make it launch-ready**

- Finish Priority 1 items 1 to 4: self-hosting, better stills, MP4 and the visual upgrade.
- Create a landing page with a 30-second demo, a clear privacy statement and an "open the studio" button.
- Record five demo clips: golden hour, rain look, section cut, tour and a before/after.
- Recruit 10 beta users from SketchUp communities and note what breaks.

**Days 31–60: first public push**

- Launch on Product Hunt and Show HN, and post in the Reddit communities above.
- Publish two YouTube tutorials and weekly LinkedIn clips.
- Ship share links and a QR AR preview.
- Interview 10 architects or designers about their real client-review pain.

**Days 61–90: convert interest into paying customers**

- Introduce a paid tier (see below) and run three paid pilots with small studios.
- Write two case studies with real models and a quote from each studio.
- Offer a campus workshop to one architecture college.

**Metrics to track:** studio opens, files loaded, successful exports, share links created, returning users after 7 days, and demo requests.

## 10. Monetisation ideas

- **Free:** local viewing, GLB export and watermarked 1080p clips.
- **Pro (about $5–12/month, to be tested):** no watermark, 4K stills and MP4, brand kit and share links.
- **Studio (per-seat, to be tested):** team library, hosted client review links, comments and analytics.
- **Services:** custom environments, white-label embeds and training workshops.

Price by testing. Ask early users what they would pay and what they would drop.

## 11. How to attract AEC clients (practical tactics)

1. **Sell a pain, not a feature.** "Clients cannot open my SKP" and "my render takes hours" convert better than "Lumion-style world".
2. **Offer a free pilot on their real model.** Ask for one live project, deliver a shareable preview and a sun-study clip within a day, and collect a quote.
3. **Show before and after.** Use the same model, side by side: raw SketchUp view versus RENDRA golden-hour look.
4. **Be honest about limits.** Say plainly "concept visuals, not final renders". Professionals respect it, and it protects you from bad reviews.
5. **Build proof.** Collect logos, testimonials, short case studies and a public gallery with permission.
6. **Partner.** Work with SketchUp trainers, archviz freelancers and BIM consultants who can recommend it or white-label it.
7. **Be present where AEC people already talk.** LinkedIn comments, SketchUp forums, college crit sessions and local architect associations.
8. **Make it easy to try.** One link, the demo villa preloaded, no sign-up for basic use.

## 12. Content ideas (ready to film or write)

1. "Sun study of any SketchUp model in 60 seconds"
2. "Send a client a 3D model without they installing anything"
3. "Golden hour vs overcast: same house, six looks"
4. "Why your render takes hours, and when it doesn't need to"
5. "SKP to GLB for AR: a QR code on your drawing"
6. "Free tools for architecture students (a checklist)"
7. "Rain, snow and mist for concept presentations"
8. "Building a Lumion-style world in the browser with three.js" (developer audience)

## 13. Risks to manage

- **Expectation risk:** users who expect Lumion quality will leave disappointed. Fix this with honest positioning and the visual roadmap.
- **Dependency risk:** OpenSKP or CDN changes could break loading. Pin versions and self-host.
- **Legal risk:** verify licences, avoid brand confusion with SketchUp, Lumion and others, and add terms and a privacy page.
- **Support risk:** broken files will arrive. Add a clear error message with a one-click "send this file for analysis" option that always asks for consent.
- **Competitor risk:** D5, Twinmotion and Enscape are adding browser, cloud and AI features. Move fast on sharing, AR and simplicity, where small tools can lead.

## 14. Next-step checklist

- [ ] Pick one sharp tagline and one target segment for the first 90 days
- [ ] Self-host all libraries and compile Tailwind
- [ ] Ship MP4 export, 4K stills and a better sky
- [ ] Build the landing page with demo clips
- [ ] Recruit 10 beta users and run 3 pilots
- [ ] Launch on Product Hunt, Show HN and Reddit
- [ ] Start weekly LinkedIn and YouTube Shorts clips
- [ ] Add share links, then introduce the paid tier

*Bottom line: RENDRA is most valuable as the fastest, most private way to preview and share SketchUp work. Win that niche first, then earn the right to compete on render quality.*
