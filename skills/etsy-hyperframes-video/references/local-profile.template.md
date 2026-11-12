# Local profile template

Copy this file to `references/local-profile.local.md` on the user's machine. Keep that private file out of public repositories, shared archives, screenshots, and logs.

Fill in only the settings that the user has explicitly established:

- **Project root:** `</absolute/path/to/video-projects>`
- **Package/cache root:** `</absolute/path/to/cache>`
- **TTS provider:** `<local service or provider name>`
- **Voice/model:** `<exact configured voice name>`
- **Default language and audience:** `<language / market>`
- **Default output:** `<aspect ratio, resolution, fps, and narrated/silent preference>`
- **Delivery folder:** `<path>`
- **Image-generation policy:** `<whether image generation is available and what it may alter>`

Do not store passwords, API tokens, private IP addresses, auth cookies, or endpoints containing secrets in this file. Point to a separate secure user-managed configuration instead. Never assume these values on another machine.
