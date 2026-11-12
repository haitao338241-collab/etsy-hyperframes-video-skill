# Product video workflow

Use this checklist from intake through handoff. Keep the evidence and creative work inside the video project so a later conversation can continue without guessing.

## Intake and evidence

Create `product-facts.md` with:

- Exact listing URL, listing title, and the date accessed.
- Product identity and materials only as stated by the seller.
- Every selectable variation, its SKU or option mapping, quantity, and what is included.
- Personalization fields, character limits, placement, font/design choices, and any fixed artwork that is not customizable.
- Optional add-ons (such as a gift box), clearly separated from included items.
- Shipping, turnaround, care, and price only if they matter to the requested video; avoid promises that may change.
- A source link or image filename for every fact that appears in the script or visuals.
- Questions and uncertainties. Do not quietly resolve them by borrowing from another listing or an older video.

Use the browser requested by the user (for this user, ego-browser) and follow its current instructions. Prefer visible listing content and normal download controls. Do not defeat access controls. If a page blocks an important fact, use a clearly labeled assumption only when safe; otherwise ask the user for that missing fact and continue independent work.

Build `assets/listing/asset-manifest.csv` (or equivalent) with source filename/URL, selected SKU relevance, image aspect ratio, intended shot, focal point, crop/reframe, and whether the asset is original or generated. Keep original assets. A generated image is a derivative, never the source of truth for product features.

## Story and copy

For a buyer-facing product story, consider these beats in the order useful to a customer:

1. A specific, relatable hook tied to the product's use or gift context.
2. What the item is and why it feels personal or useful.
3. The most important real choices: material/style/design/engraving/packaging, in the listing's actual order and terminology.
4. What the customer needs to enter or select to order correctly.
5. A concise payoff and complete call to action.

Do not force all beats into a short runtime. Prioritize the choices most likely to cause a wrong order. Mention optional items as optional; never imply a bundled set, number of pieces, or default box unless the listing confirms it. Keep the product's variation model specific to this listing's SKU.

For new films longer than roughly 15 seconds, write three clearly different storylines before selecting one when the user has not delegated the creative choice. Save them in `STORYLINES.md`. A choice must change the narrative angle, not just the headline. Then save the selected shot plan and measurable visual decisions in `SPEC.md`: aspect ratio, resolution, fps, duration, palette, title-safe region, narration length, shot order, focal points, transitions, and caption treatment. If the user asks for the finished file or says to proceed without pauses, choose the best direction and continue.

Write `voiceover-script.txt` for the intended speaker and market. Say it aloud if possible. Remove phrases that sound like a product catalog, corporate ad, or AI template. Use natural contractions and a warm opener where appropriate; don't reuse “Hey, guess what?” mechanically. Check that the ending completes its promise and has enough time to land. Save a final narration separately from notes so TTS does not read stage directions.

## Images and art direction

- Inspect source photos at full resolution before placing them. Identify the actual product center, engraving, face of an item, and image labels; do not assume the center of the canvas is the subject.
- Reframe each image individually. Record per-shot focal coordinates or crop decisions; do not reuse a single `object-position` or zoom for every image.
- For generated outpainting or restoration, state what may change (background, missing canvas, resolution/noise) and what must remain pixel-faithful or semantically unchanged (product shape, grain, engraving, text, option chart, quantities, packaging, logo). Compare the output side by side with the listing source.
- Prefer a coherent background, restrained palette, and real photos over decorative filler. Add labels only when they clarify a real option. Avoid recreating tiny listing charts as unreadable overlays; either use a clear crop or reveal options one at a time.
- Design for the smallest intended display. Titles and captions should not overlap a product, baked-in image text, or each other. Maintain a consistent title-safe area and visual rhythm. Review full-frame and phone-size captures.
- Vary motion intentionally: for example, static detail, lateral reveal, crop-to-detail, gentle parallax, comparison, and a held hero frame. Each motion should reveal a feature or guide attention. Do not cycle identical Ken Burns moves by default.

## Voice, music, and captions

- Read the local profile and any supplied TTS manual. Select the exact requested voice by its configured name. If the service is unavailable, report the blocker and use another voice only if the user authorizes a substitute.
- Keep scripts, TTS requests, audio, and renders local to the project unless the user requests a service that uploads them. Do not commit credentials or private model configuration.
- Use music only if it supports the pace and does not mask words. Lower or duck music under narration; leave a deliberate pause before the final line if the script needs it.
- Prefer transcript-based caption timing when a suitable ASR tool is installed. If not, align captions to spoken phrases or sentence boundaries and avoid claiming exact word sync. Check text against the final audio, not just the draft.
- One narrated master is the default. Make silent cutdowns or alternate aspect ratios only when requested or when delivery requirements explicitly require them.

## HyperFrames build and review

Invoke the installed HyperFrames skills and check the current CLI help for version-sensitive options. Keep the root composition small and scenes editable; use registry blocks/components for established effects and inspect their source before adapting.

Before delivery:

1. Run the project's prescribed check (commonly `npm run check` and/or `npx hyperframes check --json`). Resolve errors; explain warnings you intentionally keep.
2. Open a preview. Inspect a beat sheet, all scene transitions, phone-width views, and frames during the important movement (not only static midpoints).
3. Watch/listen to the final MP4 if playback is available. If it isn't, inspect extracted frames and use audio analysis, clearly stating what was and wasn't subjectively reviewed.
4. Check with `ffprobe` or equivalent: container, video codec, width/height, fps, duration, and audio stream. Decode the full file with FFmpeg or an equivalent tool to catch corruption.
5. Review captions against the final speech, check the opening and final hold, and make sure no logo, product detail, caption, or title is cut off.
6. Write `REVIEW.md` with: creative choice; alternatives not selected; checks and visual/audio regions inspected; render metadata; measurements; limitations; and weakest shot with a practical next improvement.

Do not say the video was watched, heard, or fully decoded unless that happened. Separate objective analyzer results from subjective review.

## Handoff

Provide the final path or preview, the target format and duration, and a short note about the verified product angle. Mention only material caveats, such as a listing ambiguity, missing ASR, or a shot that is hard to read on a phone. Do not publish or send the file to a social account unless explicitly requested.
