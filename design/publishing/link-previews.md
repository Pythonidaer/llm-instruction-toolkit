# Website link previews and discovery

Apply this guidance whenever creating or publishing a website. Prepare preview content before deployment and verify the deployed assets afterward. During a focused update, preserve existing preview settings unless the change affects them.

This covers how website links appear outside the website: social shares, browser icons, and search discovery. It does not cover local development previews. Explicit project instructions and audience/privacy requirements take precedence.

## 1. Establish the publication target

- Confirm the final HTTPS origin, deployment subdirectory, intended audience, and pages people will share.
- Use the actual public deployment origin for production metadata, not localhost, a temporary preview host, or another hosted copy.
- For GitHub project Pages, preserve the repository subdirectory in page and image URLs.
- Keep private websites private. Explain that external crawlers may not reach private pages; never broaden access to obtain a thumbnail.
- Use existing branding and page content. Do not invent an author, organization, claim, or affiliation.

## 2. Include metadata in the initial HTML

Give each independently shareable page a descriptive title, concise description, and correct canonical URL. Generate metadata through the framework's server/static facilities or ordinary HTML so crawlers do not depend on client-side JavaScript.

| Purpose | Default implementation |
| --- | --- |
| Page identity | Descriptive `<title>` and `meta name="description"` |
| Canonical destination | Absolute HTTPS `link rel="canonical"` |
| Open Graph | `og:title`, `og:type`, `og:url`, and `og:image` |
| Preview context | `og:description`; site name and locale when appropriate |
| Image details | `og:image:type`, width, height, and meaningful `og:image:alt` |
| Large-image social card | `twitter:card=summary_large_image`, title, description, image, and image alternative text for consumers supporting these tags |
| Browser identity | Favicon; suitable PNG and touch-icon variants when useful |

Keep the canonical URL and Open Graph URL aligned. Use absolute HTTPS image URLs. Override shared defaults when a page has a distinct subject. Avoid duplicate or conflicting tags. Check current platform requirements when a particular destination matters.

## 3. Design an appropriate share image

- Use 1200 × 630px as the project starting size for a landscape share image, not as a universal platform requirement.
- Match the website's typography, palette, subject, and voice. Prefer a purposeful cover over an arbitrary screenshot.
- Use a short title, readable contrast, and generous margins. Inspect it at thumbnail size and consider different crops.
- Keep essential text away from edges. Avoid tiny interface text, irrelevant stock imagery, and misleading badges.
- Export a real PNG or JPEG with sensible compression. A social image should not depend on live font loading or script execution.
- Describe what the image communicates in its alternative text. Match declared dimensions and MIME type to the actual file.
- Reuse an image when the subject is shared; create page-specific variants when they help distinguish destinations.
- Version the image URL when replacing its content if stale caches are a concern. Keep a reproducible source or generation instructions when practical.

## 4. Support search discovery appropriately

- Preserve public/private and indexing decisions. A public URL does not automatically mean the user wants it indexed.
- For a public, indexable website, provide appropriate robots directives and a sitemap of canonical pages when useful. Robots.txt is not access control.
- Let crawlers retrieve the relevant page and image assets. When an informative image belongs in the content, use a real HTML image element and useful alternative text.
- Consider image sitemap entries for relevant images. Do not insert a decorative cover into the reading flow solely to manipulate search results.
- Use structured data only when it accurately describes visible content and an appropriate supported type. Do not invent ratings, authors, dates, or eligibility claims.
- Consider `max-image-preview:large` when large search previews fit the publication intent.
- Keep icons, manifests, and structured data proportional to the website's needs. A web manifest is optional, not a prerequisite for a social thumbnail.

Open Graph share previews, browser icons, and Google Search images are different surfaces. Supplying their inputs does not guarantee indexing, a rich result, a ranking, or a particular thumbnail.

## 5. Verify before and after deployment

Before publishing:

1. Inspect the built HTML for metadata, correct production URLs, and page-specific values.
2. Check image existence, format, dimensions, alternative text, and small-size readability.
3. Check canonical paths, sitemap entries, and icons against the actual hosting layout.

After publishing:

1. Fetch the final pages and images without an authenticated session when they are intended to be public.
2. Confirm successful responses, expected content types, and no accidental sign-in page, missing-file response, or redirect to the wrong host.
3. Inspect metadata in the delivered HTML, not only the JavaScript-updated DOM.
4. Use platform inspectors when available and authorized. Distinguish inspecting a URL from posting or sharing it; publishing a social post requires the user's instruction.
5. Record implementation, deployment, asset checks, and observed platform previews separately. State any verification limits.

For private sites, verify authorized access without exposing the site or its contents to third-party inspectors.

## 6. Handle cached or missing previews

Check public reachability, source metadata, image URLs, and file responses first. If those are correct, a platform may still hold an earlier preview. Use its supported refresh/inspection mechanism or a versioned image URL; do not promise an immediate refresh or require clearing the visitor's browser cache as the default fix.

Useful inspection destinations:

- LinkedIn Post Inspector: https://www.linkedin.com/post-inspector/
- Facebook Sharing Debugger: https://developers.facebook.com/tools/debug/
- Google Rich Results Test: https://search.google.com/test/rich-results

Inspectors may require sign-in. A rich-result test does not verify every ordinary search thumbnail or social preview.

## Integrate into website instructions

When adopting this toolkit in a website, include this rule in the consuming project's existing `AGENTS.md` or equivalent instruction entry point:

> Before deploying this website, apply the LLM Instruction Toolkit's design/publishing/link-previews.md. Prepare appropriate page metadata and share images, preserve the intended audience and indexing policy, and verify the deployed URLs. Report platform-preview verification separately from implementation.

Resolve that reference to an accessible repository URL or maintained local copy in the consuming project. Update an existing instructions file rather than replacing unrelated guidance. Merely storing this Markdown does not activate it in other repositories or install a skill.

## Sources and scope

Original project guidance informed by the technical-writing website rollout. The 1200 × 630px default, workflow, integration wording, and review checklist are project choices, not universal specifications.

Primary references reviewed October 27, 2026:

- Open Graph protocol and image properties: https://ogp.me/
- Google image discovery and presentation guidance: https://developers.google.com/search/docs/appearance/google-images

Recheck relevant platform documentation when requirements, hosting, branding, or publication intent change.
