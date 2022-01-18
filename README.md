# Fur Affinity Badge

Create badges for FurAffinity users using the Shields.io API.

## User Badge

To create a user badge, use the `/badge/{site}/{username}` route.

For example: `https://furry-badges.herokuapp.com/badge/user/FurAffinity/FlameOfFurious`
-> [![](https://furry-badges.herokuapp.com/badge/user/FurAffinity/FlameOfFurious)](https://furry-badges.herokuapp.com/badge/user/FurAffinity/FlameOfFurious)

Colors and logos change depending on the site used. Logos and colors are provided for the following websites:

| Site         | Site Code            | Logo                                                                                                                                                                                             |
|:-------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Generic paw  | `paw`                | [![](https://furry-badges.herokuapp.com/badge/user/Paw/Logo)](https://furry-badges.herokuapp.com/badge/user/Paw/Logo)                                                                            |
| Fur Affinity | `furaffinity` / `fa` | [![](https://furry-badges.herokuapp.com/badge/user/FurAffinity/Logo) ![](https://furry-badges.herokuapp.com/badge/user/FA/Logo)](https://furry-badges.herokuapp.com/badge/user/FurAffinity/Logo) |
| Weasyl       | `weasyl`             | [![](https://furry-badges.herokuapp.com/badge/user/Weasyl/Logo)](https://furry-badges.herokuapp.com/badge/user/FA/Logo)                                                                          |

_Note_: logos are matched case-insensitively, but the label on the badge will respect the site used in the link.<br/>
_Note_: using the `label` query parameter does not override the log and color.

The route supports all [Shields.io style parameters](https://shields.io/#styles) except for `message` (it's used by the
backend for the username).

The badge can be embedded in Markdown, reStructuredText, AsciiDoc, HTML, etc. like all Shields.io badges.

## JSON Endpoint

The `/badge/endpoint/{site}/{username}` route is used as endpoint for the Shields.io API.
