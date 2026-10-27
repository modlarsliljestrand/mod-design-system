# UserChip

Who is signed in: the initials (replaced by the profile photo once it loads), the name, the UPN and a *Logga ut* link, as a glass pill on the hero.

- Show the **UPN** (`fornamn@modgroup.se`), not the mail address: the UPN is the identity every permission and every Power BI RLS rule resolves, and for some people the two strings differ. If the name and the UPN are the same, show the name only.
- Render it `hidden` and reveal it only once the identity is known: `.me[hidden]` keeps an empty chip (a blank circle and *Logga ut*) from showing when the lookup fails.
- Write the name and UPN with `textContent`, never `innerHTML`: they come from a token.
- Paint the initials first (`accent` circle, `blue-1` ExtraBold), then swap in the photo in the image's `onload`, so a person without a photo keeps the initials.
- `.me__role` adds a lime role tag (*Admin*, *Granskare*) before *Logga ut*.
- Contrast: from 1000px up the chip floats into the hero's glow, and there the UPN measures 3.5:1 and *Logga ut* 4.2:1 on the glass (the code's values, kept). Keep both short; add no more small text to the chip.
- The consumer provides the identity (on Container Apps: the Easy Auth principal re-published by nginx as `/me.json`, not `/.auth/me`) and the logout URL (`/.auth/logout`).
