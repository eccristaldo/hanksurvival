# Hank's Survival Workshop

A buildless static website. Upload index.html, privacy.html, terms.html, disclaimer.html, and assets/ together. No install command, framework, server code, or build step is required.

## Deploy to hanksurvival.com

1. Create a static-hosting project and upload this folder's contents as the public root (index.html must be at the root, not inside a second nested folder). Leave the build command empty.
2. Add hanksurvival.com as a custom domain in your host's dashboard.
3. At your DNS provider, use the exact records supplied by your host: typically an A record for the apex (@), or an ALIAS/ANAME/flattened CNAME if the host supports it. Point www using the host-provided CNAME. Do not invent an IP address; use your host's instructions. Preserve unrelated email/DNS records.
4. Enable the host's HTTPS certificate, wait for DNS and certificate provisioning, and redirect HTTP to HTTPS. Choose hanksurvival.com as canonical and redirect www to it if you use www.
5. Open the HTTPS site and each footer link, then test the CTA on a phone and inside the Facebook browser.

## Change the destination

Open index.html and find the inline script. Change only the quoted value of `const HOPLINK` at its top. The script assigns that value directly to the sole CTA link, which uses the same tab. Keep the full URL and parameter order intact. JavaScript must be enabled for this link assignment.

The supplied affiliate link is preserved exactly.

## Avatar and design

assets/hank.jpg is an optimized JPEG made from the supplied Hank portrait. Replace it with your own square portrait using the same filename; it also supplies the favicon and Open Graph image. If the avatar cannot load, the header shows a neutral gray circle and removes the favicon reference.

Lato is the only external page resource, served by Google Fonts with display=swap; system sans-serif is the fallback. The page includes no tracking scripts, popups, autoplay, or cookie banner. Affiliate and educational disclosures appear on the legal pages. Review the generic legal text for your actual business and hosting practices before publication.

The page uses a warm cream background, navy accents, and an antique gold CTA with dark navy text. Food-safety guidance appears in the footer and disclaimer.

## QA

See the accompanying QA report for measured sizes and Lighthouse results. Lighthouse SEO is expected to flag indexing because noindex,nofollow is intentional. Hosting, network latency, caching, and font delivery may change production performance.
