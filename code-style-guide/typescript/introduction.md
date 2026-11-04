# Introduction — TS/JS review instructions

Adapted from Google's [TS/JS Style Guide](https://google.github.io/styleguide/tsguide.html#introduction), source blob `89c4630754647df4b2dc3ebabef33276f6eeece1`. Google and contributors; [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). This adaptation adds application checks, removes presentation wrappers and expands internal links. No Google endorsement is implied.

Read [scope and precedence](README.md) and the [React/Vite applicability profile](react-vite-profile.md) first. The profile's explicit exceptions override the corresponding source rules. Other applicable source rules below retain their original strength. Source examples are illustrative, not additional requirements.

## Application checks

- **TS1.1:** Read the applicability profile before enforcing any source rule.
- **TS1.2:** Preserve must/should/may strength. Examples illustrate rules; incidental example formatting is not mandatory.
- **TS1.3:** For a finding, name the rule, concrete code location, reader cost, proposed change and verification.

## Detailed baseline, including source subsections

The retained source text below supplies the detailed rules, rationale and exceptions. Consult it for the specific pattern under review; do not infer missing constraints from the short checks above.

## Introduction

<a id="terminology-notes"></a>

### Terminology notes

This Style Guide uses [RFC 2119](https://tools.ietf.org/html/rfc2119)
terminology when using the phrases *must*, *must not*, *should*, *should not*,
and *may*. The terms *prefer* and *avoid* correspond to *should* and *should
not*, respectively. Imperative and declarative statements are prescriptive and
correspond to *must*.

<a id="guide-notes"></a>

### Guide notes

All examples given are **non-normative** and serve only to illustrate the
normative language of the style guide. That is, while the examples are in Google
Style, they may not illustrate the *only* stylish way to represent the code.
Optional formatting choices made in examples must not be enforced as rules.

<a id="source-file-basics"></a>
