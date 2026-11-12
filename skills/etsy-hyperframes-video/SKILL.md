---
name: etsy-hyperframes-video
description: "Create polished, fact-checked Etsy product videos with listing research, product-specific copy, image preparation, voiceover, and HyperFrames production and review. Use when turning an Etsy listing or supplied product photos into a finished narrated video."
---

# Etsy HyperFrames Video

Use this skill for the full path from an Etsy product page to a reviewed video deliverable. Keep the real product and listing choices accurate; make the writing conversational; direct the visuals with clear focal points and varied motion; inspect the encoded video before delivery.

## Before starting

1. Read `references/production-workflow.md` and, if present, `references/local-profile.local.md`. The local profile sets private machine paths, TTS voice, and delivery defaults. Never copy it into a public skill package.
2. Follow the user's current request and any project `AGENTS.md`. Inspect the existing project before editing it. For a new video, invoke `$hyperframes` and `$hyperframes-cli`; use `$hyperframes-registry`, `$media-use`, and `$ego-browser` when those skills are available. Follow their current command and media guidance instead of relying on remembered flags.
3. Use a user-selected location. If there is no location preference, use the machine's documented project default or ask only if the location changes where files are stored. Keep research notes, downloads, generated assets, project source, renders, and caches together under the chosen project root.

## Production sequence

1. **Verify the product.** Open the exact listing in a logged-in browser when available. Read its title, description, variation selectors, quantity, personalization instructions, SKU or option structure, shipping/contents wording, and all relevant images. Record verified facts with source URLs and access date in `product-facts.md`. Match each image to the selected SKU. Flag ambiguities; never transfer one listing's options or bundle logic to another.
2. **Plan a story that helps a buyer choose.** Identify the strongest real benefit and the choices a buyer needs to understand. For a new film over roughly 15 seconds, draft three genuinely different story directions in `STORYLINES.md` and a shot-by-shot `SPEC.md` when the user has not asked for no stops. If the user says to make the video, use your judgment and proceed with the strongest direction. Use a channel-appropriate aspect ratio; default to one narrated vertical social master when the destination is social and no format is specified. Do not make extra silent or platform variants unless requested.
3. **Write and check the narration.** Start naturally, as a person would speak to a potential buyer. Explain the real choices in a useful order, use plain spoken phrasing, and end with a complete thought and a natural invitation to act. Avoid generic claims, unsupported durability/material/shipping promises, inflated language, repetitive feature lists, and an abrupt cutoff. Match the listing's audience language. Save the approved copy to `voiceover-script.txt`; read it aloud or estimate speech timing before producing audio.
4. **Prepare product images faithfully.** Download only listing images available through the normal browser flow or use images supplied by the user. Keep an asset manifest mapping source URL, original filename, SKU/relevance, crop, focal point, and any generated derivative. Preserve the actual product, engraving, option chart, colors, quantity, and packaging. Image generation may extend an edge, repair resolution, or create supporting atmosphere; explicitly protect all product-defining details and inspect the result against its source. Never invent variant artwork, text, product contents, logos, or measurements.
5. **Direct the edit.** Choose a visual system that fits the product. Give every shot a clear product focal point, protect titles/captions from the image and one another, keep text inside mobile-safe areas, and vary shot scale, composition, and motion for a reason. Avoid repeating the same push-in on every photo, covering listing labels, oversized empty bars, unbalanced letterboxing, and decorative movement that distracts from the item. Use the HyperFrames registry before hand-building named visual effects.
6. **Make voice, captions, and sound.** Use the voice and TTS route from the local profile, or the user's requested provider. Never place private voice models, service URLs, credentials, or local machine details in a shared skill. Keep music under speech and let the narration breathe. Use ASR for caption alignment when available; otherwise align phrases to the script and label timing as phrase-level, not word-level. Do not provide a separate silent edit unless asked.
7. **Build and review in HyperFrames.** Keep the project editable. Run the project's check command and clear errors; inspect warnings rather than ignoring them. Open a preview, review the beat sheet, each scene seam, phone-size frames, and the most important focal-point moves. After rendering, inspect the actual encoded output, verify dimensions, frame rate, duration, audio streams, and decode integrity. Measure audio when tools allow. Record creative decisions, checks, limitations, and any remaining weak shot in `REVIEW.md`.
8. **Deliver without publishing.** Save the final file where the user asked. Summarize the chosen story, format, and meaningful limitations. Uploading to Etsy, Facebook, or another service is a separate action; do it only when the user explicitly asks.

## Finish criteria

- Every product claim and shown option is traceable to the exact listing/SKU or user-supplied facts.
- The spoken script sounds natural, covers the buyer's key decision, and has a satisfying opening and ending.
- The product is legible on a phone; titles, captions, and important image details do not collide.
- Motion varies across shots and supports the story; no unintended blank bands or awkward crops dominate the frame.
- The project passes the available HyperFrames checks, and the delivered render has been visually and technically inspected.
- The review file clearly distinguishes measured results from subjective listening or visual judgment that was not performed.
