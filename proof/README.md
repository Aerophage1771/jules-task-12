# Proofs

This directory contains the proof of the requested visual review for the GermaineTutoring theme mockup.

## Stills

| State | 1280px Capture | 375px Capture |
| :--- | :--- | :--- |
| **Marketing Site** | `proof/1280/marketing.png` | `proof/375/marketing.png` |
| **Course Portal** | `proof/1280/portal.png` | `proof/375/portal.png` |
| **Blog & Campaign** | `proof/1280/blog.png` | `proof/375/blog.png` |

## Interaction

The interaction showing tab switching and scrolling across the mockup is available at `proof/walkthrough.webm`.

## Notes
All states were captured successfully. The fonts (`Yanone Kaffeesatz` and `Cabin` base64), variables, and structures match the requested "Civic Reasoning Bulletin" theme specifications across all three main views.


## Findings
During testing, some issues were identified on mobile (375px) width:
- Elements in the dashboard (sidebar, grids) collided or overflowed.
- Fixed widths on the course portal sidebar broke the layout on smaller screens.
- Global navigation links overflowed.
- Proof strip collapsed improperly.

**Fixes Applied:**
- Added a responsive media query (`max-width: 768px`) that switches the `.grid-2` and `.grid-3` layouts to a single column (`1fr`).
- Made the sidebar in the Course Portal full width (`100%`) on smaller screens and adjusted its flex-direction to row.
- Modified the `.global-nav` to flow as a column on smaller screens, resolving overlaps.
- Restructured `.proof-strip` for better display at mobile breakpoints (`1fr 1fr` up to 480px, then `1fr`).
