# Improved LinkedIn Insight Tag
An optimized (and greatly simplified) LinkedIn Insight tag template that actually works like it should. Includes support for overriding advanced conversion options not well documented by LinkedIn.

## Why use this tag template?

There are numerous issues with the [LinkedIn InsightTag 2.0](https://github.com/linkedin/linkedin-gtm-community-template) template in the gallery. Unfortunately, LinkedIn has not fixed or addressed issues in a timely fashion. 

**This template fixes issues such as:**

- Proper use of a cache key with `injectScript` to prevent issues with duplicate script injection (sometimes at a very high mulititude). See: https://github.com/linkedin/linkedin-gtm-community-template/issues/4 for more details.
- Issues with the tag template not properly calling `data.gtmOnSuccess` which results in the tag showing as "Still Running" inside GTM preview mode even though the tag is no longer running.
- Adds support for setting advanced conversion options available via the `lintrk('track')` options object: `conversion_value`, `conversion_currency`, `conversion_type`, `order_id`, and `event_id`. _**Note**, these options are not publically documented - but were found inside the insights.min.js source code. Use at your discretion!_

Additionally, the template code is greatly simplified by using sandboxed APIs such as `createQueue`, and `createArgumentsQueue` that naturally check if values exist before setting them, whereas the LinkedIn template does a bunch of manual variable checking that is unecessary and makes the template harder to maintain.

**Author(s)**
[@derekcavaliero](https://github.com/derekcavaliero)
