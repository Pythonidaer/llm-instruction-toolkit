# Content design decisions

General AI writing instructions adapted from every Markdown file in [writing decisions](../../writing-decisions/README.md), plus the existing AI content reset. This file includes the decision rules, qualifications, examples, brief template and review guidance; the source files remain unchanged.

You do not need to use or know Mailchimp to apply these instructions. Mailchimp and Google identify where guidance came from; they are not products you must use or brand personalities you must adopt. Apply the general rules to the actual audience and task. Credit sources separately from the decisions themselves.

Read alongside [visual styling](visual-styling.md) and [information architecture](layout-and-information-architecture.md). Work from audience and task toward wording and conventions. Use the sections relevant to the current task; do not add website copy merely to demonstrate a rule.

## Required first response: audience and purpose

When a new session is asked to read or apply these rules for creating or substantially rewriting a website, return to the user before drafting content, designing the interface or implementing the site.

1. Read the supplied context and reuse answers already given. Do not make the user repeat available information.
2. Ask the following unanswered questions in one short message, with no more than three questions:
   - Who is this website for? Include the creator when they will use it, and identify any secondary audiences.
   - What should each audience be able to accomplish, and what is the creator's purpose for building the site?
   - When audience needs compete, which takes priority? Priorities may differ by page.
3. **End the response after asking. Wait for the user's reply. Do not silently assume answers, treat silence as agreement, or start drafting, designing or implementing while waiting.** Reading the repository to understand the request is allowed.
4. If all answers are already available, summarize the audience, purpose and priorities briefly and ask the user to confirm that starting brief. Wait for their reply before proceeding. Do not repeat this checkpoint within the same project once the user has confirmed it, unless the scope or audience materially changes.
5. After the reply, summarize the agreed starting brief, label assumptions about other people's needs, and proceed. A provisional answer or “I'm not sure; let's explore” is enough to begin a reversible exploration; certainty and formal user research are not prerequisites. Revisit the brief as prototypes and feedback sharpen the idea.

The creator is a legitimate audience for a personal learning tool. Distinguish the creator's reason for building from each visitor's reason for using the site. Support multiple audiences deliberately; do not automatically create separate navigation categories for each.

This checkpoint applies to new website work or a substantial content rethink. Do not restart discovery for a narrow maintenance task, a factual explanation, or an edit to these rules themselves. A later explicit user instruction to skip discovery takes precedence.

---

<br>

## Start here

| Layer | Decide | Jump to |
| --- | --- | --- |
| Content decisions | What belongs, where it belongs and what the visitor needs | [Content](#content-decisions) |
| Goals and principles | Intended outcomes and criteria for judging writing | [Goals and principles](#goals-and-principles) |
| Voice | Stable product character | [Voice](#voice) |
| Tone | Delivery for this situation | [Tone](#tone) |
| Grammar | Sentence structure, tense and clear responsibility | [Grammar](#grammar) |
| Mechanics | Numbers, dates, names, capitalization and formatting | [Mechanics](#mechanics) |
| Punctuation | Marks that organize written meaning; part of mechanics | [Punctuation](#punctuation) |
| Project brief | Relevant questions, examples and recorded choices | [Questions and brief](#project-questions-and-brief) |
| Evaluation and maintenance | Understanding, task completion, accuracy and ownership | [Review](#evaluation-and-maintenance) |

For a new project: establish the brief, choose goals and principles, establish voice and tone, draft in the interface, check grammar/mechanics, then test and maintain. Revisit earlier decisions when evidence changes. Overlapping rules apply once; a source heading is not an exclusive category.

---

<br>

## Resolve choices before applying them

<br>

### Priority and scope

- Reuse explicit user instructions and approved project conventions. Preserve factual accuracy, accessibility, required values and identifiers.
- Combine compatible guidance. Do not ask the user to choose an entire publisher when only one convention differs.
- Use the writing advice as general prompting guidance. Choose tone and regional conventions for the actual project. Publisher names are attribution, not profiles to adopt. Google's punctuation guidance is for interface text, not a ban on punctuation throughout articles.
- The existing no-emoji preference and Google's numeral preference at sentence openings are already settled. Do not ask about them again unless the user requests reconsideration.
- Ask only when an unresolved choice affects the current work. Explain the concrete difference with two short examples, name the affected content type, and record the answer in the consuming project's brief. Ask no more than three related questions at once; continue independent work while the affected choice is pending.
- For an actual unresolved contradiction, ask: **“For [specific content type], should I follow Google's [specific convention and example] or Mailchimp's [specific convention and example]?”** Do not invent a source position to fill this template. If neither file specifies the alternative, describe it as a project choice.

<br>

### Decisions to check at the point of use

| Decision | What the files actually say | Ask only if unresolved and relevant |
| --- | --- | --- |
| Fractions in prose | Google gives a general digit preference without an explicit fraction rule; Mailchimp explicitly spells out prose fractions. This is a scope question, not a verified direct contradiction. | “For prose fractions, should I extend the Google numeral preference to `2/3`, or use Mailchimp's `two-thirds` convention?” |
| A label that also introduces a list | Google omits colons after labels; Mailchimp uses colons to introduce lists. Usually the distinction between a UI label and a sentence resolves this. | “For this label above a list, should I use Google's label treatment (`Options`) or Mailchimp's list-introduction treatment (`Options:`)?” |
| Brevity and personality | Google's concise interface guidance and Mailchimp's friendly, appropriate writing can coexist. Neither requires unnecessary words. | If the brief does not resolve the desired delivery: “For these messages, would you prefer a brief Google-style interface treatment or warmer, conversational wording informed by Mailchimp's guidance? Both will preserve the same facts and action.” This is an authored style comparison, not a source contradiction. |

<br>

### Compatible rules: apply together

- Google's omitted periods for standalone UI sentences and Mailchimp's placement of periods inside quotation marks answer different questions: whether a period is needed, then where it belongs.
- Google's goal-first instructions and Mailchimp's main-point-first principle normally support each other.
- Common wording and official product names can coexist: avoid invented jargon while preserving real names and required terminology.
- Present tense for routine behavior does not override accurate past events, historical chronology or exact quotations.
- Do not force a choice between clarity, truth, accessibility and personality. Adapt expression while preserving meaning and consequences.

---

<br>

## Content decisions

<br>

### Reset: Rules

- Page headings name the subject or task; section headings describe their contents; navigation labels identify destinations.
- Avoid automatic editorial, cinematic, metaphorical, or slogan-like phrases. Do not default to “Where X meets Y,” “Less X. More Y,” or “This isn't X. It's Y.”
- Replace interchangeable promotional filler such as “unlock,” “elevate,” “seamless,” “supercharge,” and “next level” with the supported action and concrete result.
- Remove redundant eyebrows, repeated headings, duplicate counts, obvious instructions, and helper copy that explains implementation rather than helping the visitor decide.
- Use consistent terms for the same object. Distinguish save, send, submit, copy, and continue. Button labels should name the actual action and object when needed.
- Explain requirements, limitations, and consequences where they affect a decision. Keep background technical detail in an appropriate disclosure or resource.
- Give feedback that says what changed. Errors identify the problem and a useful recovery action. Loading feedback must reflect actual state; do not invent percentages or artificial waits.
- Do not invent testimonials, customers, statistics, or performance claims. Identify fictional examples and distinguish measured values from estimates.
- Use plain visible sequence numbers: 1, 2, 3. Preserve meaningful formats such as dates, times, and identifiers.
- Give icon-only controls accessible names on the controls themselves. A tooltip alone is insufficient. The menu trigger and close state form a consistent visual pair; this does not remove useful labels elsewhere.
- Keep assistant-to-owner conversation out of public copy. Do not address the creator’s project, requests, notes, or approval history as though visitors share that context. Write for the actual audience; keep authoring rationale in chat or repository documentation. See [the public-copy guidance](../../writing-decisions/best-practices.md#keep-authoring-context-out-of-public-copy).
- Do not default to count-first editorial fragments such as “Eight websites, examined…” when the count and framing add no useful information. Use counts when they serve a task; delete redundant introductions rather than replacing them with another slogan.
- Add personality after meaning is clear. Deliberate expressive writing remains available when it serves the subject.

<br>

### Reset: Avoid these content and tone habits

- Before new website work, follow the [required audience-and-purpose checkpoint](#required-first-response-audience-and-purpose): ask the unanswered questions and wait for the user's reply before drafting or building. Start with a provisional brief and refine it as evidence develops. A stakeholder request for more content alone is not proof of a visitor need; the creator can also be a legitimate user.
- Do not make every project sound like GOV.UK, a promotional landing page or a friendly chatbot. Choose a project profile across all four tone dimensions.
- Do not keep one emotional tone for introductions, errors, confirmations and sensitive situations. Preserve identity while adapting to the task.
- Do not use fabricated urgency, unverifiable reassurance, automatic praise, patronising instructions or jokes that blame the reader.
- Do not assume the reader's feelings or use stock empathy in place of practical help.
- Do not repeat general disclaimers, source explanations or obvious instructions on every slide, card or modal. Place them once at the right level; repeat only when an independent decision needs them.
- Do not achieve brevity by deleting conditions, consequences, accessibility context or recovery steps.
- Do not hide essential information in a disclosure or use vague labels such as “Read more” when a specific destination matters.
- Do not copy facts from an earlier interface state, invent a capability or contradict the status the product actually reports.
- Do not treat tone preference, readability scores, clicks or traffic as proof that readers understand the content.

<br>

### Writing decision layers

| Layer | Question it answers | Example |
| --- | --- | --- |
| Content decisions | What does this person need to know or do? | Explain the upload limit before they choose a file |
| Goals | What should the writing accomplish? | Help someone recover from a failed upload |
| Principles | What qualities guide the writing? | Be clear, useful, concise and respectful |
| Voice | What consistent character should the product communicate? | Knowledgeable and approachable |
| Tone | How should that voice adapt to this situation? | Calm and practical during an error |
| Grammar | How do words form clear sentences? | Choose a tense that accurately describes what happened |
| Mechanics | How do we present written language consistently? | Choose numeral, capitalization and abbreviation conventions |
| Punctuation | How do marks organize meaning? | Decide whether a short interface message needs a period |

Punctuation is usually included under mechanics. Grammar concerns sentence structure; mechanics concerns written conventions. Both can affect meaning.

**These layers overlap.** A publisher's document title does not guarantee that every rule belongs to one category. Google's principles include numeral and punctuation conventions; Mailchimp's mechanics guide also contains broad writing advice. These files retain that overlap for now.

<br>

### Project workflow

#### 1. Establish the reader and task
Use [Project questions](../../writing-decisions/project-questions.md) in small batches. Identify the audience, immediate task, required facts and source of truth.

Use [Content best practices](../../writing-decisions/best-practices.md) to decide what belongs on the page, where it belongs, and which interface states need content. Keep authoring conversations and unnecessary implementation details out of public copy.

#### 2. Choose goals and principles
Read [Mailchimp goals and principles](../../writing-decisions/goals-and-principles/mailchimp-writing-goals-principles.md) for broad communication aims: empower, respect, educate, guide and speak truth.

Read [Google writing principles](../../writing-decisions/goals-and-principles/google-writing-goals-principles.md) for practical interface guidance: essential information, direct wording, concise labels and consistent conventions.

Use these as decision criteria. Do not add text merely to demonstrate every goal.

#### 3. Establish voice and adapt tone
Use [Voice](../../writing-decisions/voice-and-rules/voice/voice.md) for stable identity and [Tone](../../writing-decisions/voice-and-rules/tone/tone.md) for contextual delivery.

[Mailchimp voice and tone](../../writing-decisions/voice-and-rules/mailchimp-tone-voice.md) remains a combined reference pending further separation. Use its general lessons about clarity, warmth and context; choose the actual project's voice independently.

#### 4. Draft in the actual interface
Write headings, labels, instructions, errors and recovery options around the real task. Check what each text element contributes. Keep facts and actions unchanged when comparing tone variants.

#### 5. Check grammar and mechanics
Use [Mailchimp grammar and mechanics](../../writing-decisions/grammar-and-mechanics/mailchimp-grammar-mechanics.md) as a lookup reference for numbers, dates, punctuation, capitalization, names and formatting.

The sentence-opening number rule already follows Google's numeral preference. Preserve explicit project decisions, required identifiers and accurate values. If another conflict appears, resolve it explicitly rather than combining incompatible instructions.

#### 6. Test and revise
Can someone understand what happened and complete the task without coaching? Review wording and layout together. A correctly punctuated sentence can still be unnecessary or unhelpful.

<br>

### Find guidance for your current task

| If you are asking… | Open… |
| --- | --- |
| Does this text belong here? | [Content best practices](../../writing-decisions/best-practices.md) |
| What are we trying to accomplish? | [Mailchimp goals and principles](../../writing-decisions/goals-and-principles/mailchimp-writing-goals-principles.md) |
| How can this interface copy be clearer? | [Google writing principles](../../writing-decisions/goals-and-principles/google-writing-goals-principles.md) |
| What should the product sound like? | [Voice](../../writing-decisions/voice-and-rules/voice/voice.md) |
| How should this particular message feel? | [Tone](../../writing-decisions/voice-and-rules/tone/tone.md) |
| How should this number, date or punctuation mark appear? | [Grammar and mechanics](../../writing-decisions/grammar-and-mechanics/mailchimp-grammar-mechanics.md) |

Select only the references needed for the current task. These files require explicit loading or integration into project instructions; storing them here does not automatically apply them elsewhere.

<br>

### Apply the guidance

1. Identify the audience, task and evidence.
2. Decide what information belongs where and in which format.
3. Choose an initial tone profile and context-specific adjustments.
4. Draft real content in the interface, including non-success states.
5. Test comprehension and task completion, then revise.
6. Assign ownership, sources and review triggers.

Use the [AI content reset](content-design.md) to catch automatic writing habits. Record the chosen tone in the consuming project; do not turn one project's preferences into global toolkit rules.

<br>

### Start with a useful outcome

- Identify what the intended person should be able to decide, understand or do, and how the proposed page supports that purpose. Include the creator's learning or experimentation goals where relevant.
- Use available evidence, including the creator's stated needs and experience. Distinguish confirmed information from assumptions in the discussion or project notes, rather than automatically adding assumption labels to the published interface. Formal research is not a prerequisite for a personal project: start provisionally when evidence is limited, and revisit assumptions through feedback.
- Check existing content before adding more. Improve, combine, relocate or retire material where appropriate.
- Select text, a form, checklist, table, diagram, audio or another format because it helps the task.
- Coordinate content placement and labels with information architecture. Navigation alone is not the content plan.
- Keep required facts, conditions, costs, deadlines, consequences and alternatives near the action they affect.

Content design includes selection, organisation, format, wording and maintenance. It can begin in plain copy, but wording and interface should be revised together.

<br>

### Make content findable and understandable

| Element | Instruction |
| --- | --- |
| Titles | Name the subject or task using recognisable terms. Put distinguishing information early. Avoid keyword stuffing. |
| Summaries | Help someone decide whether the page is relevant. Add information beyond the title; do not repeat it in the opening paragraph. |
| Headings | Describe the contents beneath them. Check whether the headings alone explain the route. |
| Order | Put the answer or next useful action first, followed by supporting detail. Preserve necessary qualifications. |
| Paragraphs | Keep related information together. Prefer direct verbs and familiar words; explain specialist terms. |
| Lists | Use bullets for parallel items and numbers for a required sequence. |
| Links | Describe the destination or action. Indicate important file or navigation consequences where needed. |
| Terminology | Use consistent names, accurate product terms and deliberate conventions for dates, numbers and abbreviations. |
| URLs | Prefer stable, descriptive paths. Plan redirects and ownership before moving published content. |

Shorten without changing meaning: permission, obligation and possibility are different. Keep useful explanations; plain language also serves expert readers.

<br>

### Write for actual interface states

- Name the real action on each control. Distinguish opening, saving, submitting, copying and continuing.
- Provide labels, hints, validation, loading, empty, error, success and recovery messages where relevant.
- State what happened, its effect and the available next step. Explain a cause only when known.
- Match feedback to the actual state. Do not claim something was saved, completed or protected without evidence.
- Show decision-relevant limitations before the person commits. Keep background implementation detail in optional documentation.
- Place a general explanation once where it is useful. Repeat it at independently encountered decision points only when it remains necessary.
- Keep material requirements visible; optional detail may use disclosure. Do not hide essential recovery instructions just to shorten a screen.

A shared disclaimer on every resource slide creates reading work. Prefer one clear course/source explanation, while retaining specific warnings at the links or actions that need them.

<br>

### Keep authoring context out of public copy

Write for the person using the published website, not for the owner discussing its creation with an assistant.

- Do not publish assistant-to-owner messages, implementation handoffs, design rationales, approval history, or references to the authoring conversation as interface copy. Keep those in the conversation or appropriate repository documentation.
- Avoid phrases such as “your project,” “as you requested,” “we added,” or “based on your notes” when they address the creator rather than the actual visitor. Such wording can be appropriate only when the visitor really is the person being addressed and the context is available to them.
- Public readers should not need access to a private conversation to understand the page. Include provenance or attribution only where it serves the reader, using neutral, self-contained wording.
- Do not automatically open with a count followed by a comma and an abstract description, such as “Eight websites, examined through the ideas in your Type Study project.” Counts are useful when they support a task; do not use them as decorative editorial framing or repeat them unnecessarily.
- Prefer deletion when the title and interface already explain the page. Do not replace removed filler with another slogan or redundant summary.

Before publishing, ask: “Who does ‘you’ refer to here? Would a first-time visitor understand this without knowing how the site was made? Does the sentence help that visitor decide or act?”

For the example above, remove the sentence when “Website typography studies” and the gallery already establish the subject. If a summary is genuinely needed, describe the visitor’s task or the contents directly, without mentioning the assistant’s collaboration with the owner.

<br>

### Design for access and different contexts

- Use semantic headings, descriptive links and meaningful control labels, including accessible names for icon-only controls.
- Provide text alternatives for informative visuals and transcripts or other suitable alternatives for audio.
- Do not rely on colour, position or sound alone to communicate meaning.
- Check content in its actual layout, including narrow screens, enlarged text and assistive technology where relevant.
- Plan language versions using audience evidence. Keep terminology consistent and assign responsibility for synchronised updates.
- Do not treat machine translation or an automated accessibility/readability score as proof of understanding.
- For learning content, connect the explanation, example, practice and feedback to a useful learning outcome. A short slide is a delivery choice, not proof that learning occurred.

<br>

### Content structure

Lead with goals, disclose details progressively, keep terminology consistent, and refer to controls by label.

<br>

### Additional project rules for AI-generated websites

These are authored project instructions addressing the requested writing-decisions concerns, separate from the Google adaptation above.

#### Establish the content brief
Identify the intended visitor, their main task, and what they need to know at each point. Resolve material uncertainty with the site owner.

#### Keep production conversation out of published content
- Interpret chat messages as requirements; do not paste them into the interface.
- Keep implementation notes, design rationale, development status, and instructions to the owner in project documentation unless visitors need them.
- Write so a first-time visitor understands the page without seeing the conversation.

#### Require a purpose for every text element
- Add headings, badges, labels, and helper sentences only when they contribute distinct information.
- Remove repetition and commentary describing an obvious layout.
- Preserve accessible control labels, instructions for unfamiliar tasks, and consequences visitors need before acting.

#### Review before delivery
For every text element, identify the visitor question it answers or action it supports. Revise, relocate, or remove text without a useful purpose. Review silently; report material uncertainties separately to the owner.

---

<br>

## Goals and principles

<br>

### Principles

#### Be concise
Use brief, scannable passages with few concepts.

#### Write simply and directly
Focus wording on the current task.

#### Address users clearly
Usually use “you”; use “I” for ownership.

#### Avoid combining first and second person
Keep perspectives consistent within a phrase.

#### Communicate essential details
Omit unnecessary implementation explanations; sometimes omit text.

#### Write for all reading levels
Prefer familiar vocabulary.

#### Industry terms and feature names
Avoid jargon and invented terminology unless necessary.

#### Write in the present tense
Describe routine behavior in present tense; otherwise use simple verb forms.

#### Use numerals
Prefer digits; distinguish mixed numeric meanings with words.

#### Skip unnecessary punctuation
Remove punctuation that adds no clarity.

##### Periods: avoid using periods on
Standalone sentences in labels, hover text, lists, and dialogs.

##### Use periods on
Multiple sentences and sentences preceding links; avoid full-sentence links.

##### Periods in longer text
Punctuate for clarity; maintain consistency throughout the flow.

##### Colons
Omit colons after labels.

<br>

### Writing goals

#### Empower

- Give readers information that helps them understand the product and use it effectively.
- Explain available actions, choices and outcomes so people can make informed decisions.
- Encourage progress through useful guidance rather than pressure or exaggerated praise.

#### Respect

- Treat readers as capable people with limited time and other priorities.
- Consider their situation without assuming their feelings, background or knowledge.
- Be considerate and inclusive. Explain unfamiliar concepts without patronising.
- Communicate with readers rather than directing a sales pitch at them. Keep promotional content relevant and honest.

#### Educate

- Prioritise what readers need to know over what the organisation wants to announce.
- Provide the exact information needed for the immediate task, including relevant requirements and limitations.
- Offer opportunities to learn more without making optional detail a prerequisite for a simple action.
- Explain knowledge the writer takes for granted. Readers do not have access to everything the expert knows.

#### Guide

- Help readers understand where they are, what to do and what comes next.
- Use friendly, specific instructions in a useful sequence.
- Apply this care to educational material and interface tasks, including errors and recovery.
- Supply necessary context without overwhelming the reader.

#### Speak truth

- Describe the product's real role in people's lives and its supported strengths.
- Avoid dramatic storytelling, inflated importance and grandiose promises.
- Verify factual claims and distinguish confirmed behaviour from assumptions.
- Preserve limitations and consequences that affect the reader's decision.

<br>

### Content principles

| Principle | Writing rules | Review question |
| --- | --- | --- |
| Clear | Understand the subject before explaining it. Use simple words and sentences; explain necessary specialist terms. | Can the reader understand the main point and the next action? |
| Useful | Identify the purpose, audience and information need before drafting. Include content because it helps that need. | What purpose does this serve, who will read it and what do they need to know? |
| Friendly | Write naturally and considerately across homepage copy, instructions and system alerts. Allow flexible phrasing when it improves understanding and relatability. | Does this sound like a helpful person speaking to the reader? |
| Appropriate | Adapt tone to the audience, situation, task and stakes while keeping a consistent voice. | Does the delivery fit this particular moment? |

Friendliness does not require jokes, cheerfulness or familiarity in every message. In a failure message, warmth can mean calm wording and a practical recovery action. Flexibility with writing rules must preserve meaning, accuracy and accessibility.

<br>

### Apply the goals and principles

1. Name the reader, their immediate task and the purpose of the content.
2. Identify the facts, conditions and choices they need; check the source of truth.
3. Lead with the information that helps them act or understand.
4. Add the context needed to proceed and an optional route to deeper learning.
5. Adjust tone for the situation using the voice and tone profile.
6. Remove patronising language, irrelevant promotion, dramatic claims and unnecessary detail.
7. Review the result in its actual context. Check whether a reader understands what to do without extra coaching.

A piece of content may serve several goals at once. Use them as review criteria rather than adding a separate paragraph for every goal.

<br>

### Original example

For a failed upload, an appropriate message might be:

> Your file exceeds the 10 MB limit. Choose a smaller file and try again.

Use this wording only when the product has confirmed the cause and the limit is accurate. It explains the issue, respects the reader's time and gives a supported next step without blame or drama. Link to file-reduction guidance if readers need more help.

---

<br>

## Voice

<br>

### Separate voice from tone

Voice is the consistent character of the organisation or product. Tone changes with the reader's task, situation and likely state of mind.

Keep the voice knowledgeable, compassionate, clear and approachable across channels. Adjust formality, humour and energy to suit the moment. Use evidence from the situation; do not claim to know how someone feels.

<br>

### Voice rules

1. **Speak plainly.** Put useful information first. Use familiar words and direct verbs. Remove hype, inflated claims, upsells disguised as help, decorative metaphors and emotional pressure.
2. **Be warm and credible.** Write like an experienced, considerate partner. Take the reader's goals seriously, including small or early-stage projects. Use natural conversation without manufactured intimacy or invented shared experience.
3. **Teach without talking down.** Explain unfamiliar concepts and give practical next steps. Avoid language such as “obviously,” “simply” or “as everyone knows” when it dismisses difficulty.
4. **Translate specialist language.** Replace jargon with plain English where possible. When a technical term matters, explain it on first use and use it consistently. Preserve precision and necessary qualifications.
5. **Encourage through useful guidance.** Help people understand their options and make progress. Make encouragement specific; avoid empty praise, guaranteed outcomes or claims of mastery.
6. **Use restrained, inclusive humour.** Optional humour may be dry, subtle and slightly offbeat. The reader should understand the joke without insider knowledge. Never mock the reader, exclude a group, sound superior or make distress the punchline.
7. **Let clarity decide.** Remove personality that slows comprehension, hides an action or weakens trust. A straightforward sentence is a complete choice.

<br>

### Establish a voice

Voice is the relatively stable identity of the organisation or product. Tone adapts to the purpose, reader and situation. Writing style also includes mechanics such as spelling, punctuation and terminology. Keep these decisions distinct.

Use [Project questions](../../writing-decisions/project-questions.md) to establish the project brief. For tone profiles, qualities and situational adjustments, use [Tone guidance](../../writing-decisions/voice-and-rules/tone/tone.md).

---

<br>

## Tone

<br>

### Adapt tone to context

Start with an informal, respectful, conversational tone. Change it according to the reader's needs, including within the same journey.

| Context | Tone and content rule | Humour |
| --- | --- | --- |
| Introduction or exploration | Be approachable; explain relevance and available choices without over-promising. | Optional and unobtrusive. |
| Learning an unfamiliar task | Be patient and specific; explain terms and steps without assuming prior knowledge. | Only if it supports understanding. |
| Confusion or a request for help | Reduce verbal decoration; answer directly and give an actionable next step. | Usually omit it. |
| Error, interrupted work or possible loss | Explain the known issue, its effect and recovery options calmly. Avoid blame and unsupported reassurance. | Omit it. |
| A verified completion | Confirm what happened, then provide the next useful option. Match enthusiasm to the significance of the result. | Light humour may fit; never force it. |
| Serious or sensitive information | Use measured, precise wording and preserve consequences, conditions and limitations. | Omit it. |

This table operationalises the supplied principles; it is not a quoted Mailchimp taxonomy.

If humour does not come naturally, leave it out. When appropriateness is uncertain, use straightforward wording. Informality never excuses vague instructions, slang or careless claims.

<br>

### Original examples

These examples illustrate the adaptation; they are not Mailchimp copy. Use status claims only when confirmed by the product.

| Avoid | Prefer | Reason |
| --- | --- | --- |
| “Unlock unparalleled audience optimisation.” | “Choose who receives your email.” | Translate jargon into the actual task. |
| “Obviously, just authenticate your domain.” | “Verify that you own this domain. Follow these steps to add the required DNS records.” | Explain unfamiliar work without dismissing its difficulty. |
| “Oops! Your campaign took a little vacation.” | “Your campaign was not sent. Try sending it again.” | State the failure and a supported recovery action without a joke. |
| “Don't leave the name field empty.” | “Enter a name.” | State the required action positively. |
| “You're a marketing genius!” | “Your campaign is scheduled for Tuesday at 10 am.” | Confirm the real outcome without exaggerated praise. |

Adapt examples to actual product behaviour. If retrying is unsafe or unavailable, provide the supported recovery route instead.

<br>

### Establish a tone profile

Choose one initial profile across all four [NN/g dimensions](https://www.nngroup.com/articles/tone-of-voice-dimensions/):

| Dimension | Spectrum |
| --- | --- |
| Formality | Formal to casual |
| Humour | Serious to funny |
| Respectfulness | Respectful to irreverent |
| Enthusiasm | Matter-of-fact to enthusiastic |

These are independent spectrums, not four exclusive tones or a quality ranking. Refine the profile with a few target qualities and qualities to avoid. Use [Project questions](../../writing-decisions/project-questions.md) to make the choices concrete.

Keep facts, conditions and actions unchanged when comparing tone variants. A tone preference never justifies misleading or unusable content.

<br>

### Use tone qualities deliberately

These overlapping qualities are an authored teaching aid from the LMS, not an exhaustive or official GOV.UK taxonomy.

| Quality | Apply it through | Avoid |
| --- | --- | --- |
| Reassuring | Verified status and useful options | Promises of safety or recovery without evidence |
| Authoritative | Accurate, supported guidance | Jargon, condescension and unsupported certainty |
| Instructional | Specific actions in a useful order | Vague directions and missing prerequisites |
| Conversational | Natural, direct wording | Filler, slang that excludes readers and hidden conditions |
| Encouraging | Specific feedback on progress | Empty praise or unsupported claims of mastery |
| Empathetic | Acknowledgement and practical help | Assuming the reader's feelings or manufacturing intimacy |
| Playful | Appropriate lightness in low-stakes situations | Jokes that obscure a task or blame the reader |
| Urgent | Real deadlines and consequences | Invented scarcity or pressure |
| Neutral | Accurate information with restrained emotion | Unhelpful brevity or vague status |
| Celebratory | Proportionate recognition of a real result | Exaggeration and premature success messages |

Respectfulness remains a requirement toward people even when a brand is irreverent about its subject. Do not make every message enthusiastic, humorous or emotionally flat by default.

<br>

### Adapt tone to the situation

| Situation | Consider |
| --- | --- |
| Discovery or introduction | Help the reader recognise relevance; use only the persuasion the project calls for. |
| Instructions | Make the sequence and requirements clear. |
| Errors or interrupted work | Reduce emotional intensity; explain the issue and recovery. |
| Confirmation | State the verified outcome and next step. |
| Learning feedback | Identify what worked and what to try next; distinguish completion from demonstrated understanding. |
| Time-sensitive notices | Name the real deadline, consequence and action. |

These are starting considerations, not mandatory tone presets. Preserve project identity while adapting to context.

---

<br>

## Grammar

<br>

### Abbreviations and acronyms

- Spell out an unfamiliar abbreviation on first mention, then use the short form.
- Include the abbreviation in parentheses when its relationship to the full term is unclear. For clarity, introducing both together is also useful: “Coordinated Universal Time (UTC).”
- Use familiar terms such as API or HTML without expansion when appropriate for the actual audience. Familiarity is audience-dependent.

<br>

### Active voice

- Prefer active voice so readers can identify the actor and action: “Riley updated the account.”
- Use passive voice deliberately when the action or recipient matters more than the actor, or the actor is unknown.
- Words such as “was” and “by” are review clues, not proof of passive voice. Do not mechanically delete them or invent responsibility.

<br>

### Slang and jargon

- Write in plain English.
- Briefly explain a necessary technical term where it appears. A definition should make the concept useful, not replace jargon with more jargon.
- Match explanations to audience knowledge without assuming every reader is an expert.

<br>

### Write positively

State the useful action: “Join the queue to collect your ticket.”

Review wording containing can't, don't or similar negatives for an opportunity to explain what the reader can do. Keep explicit negatives when needed to communicate a failure, restriction, warning or consequence accurately. Positive wording must not disguise a problem.

<br>

### Sentence-level rules

- Prefer active voice so the reader can identify who does what: “We saved your changes.” Avoid passive constructions when they hide responsibility. Never invent an actor merely to make a sentence active.
- Use plain English. Replace slang, unexplained acronyms and business jargon with terms the audience understands.
- Phrase guidance positively by stating the useful action: “Choose a password with at least 12 characters.”
- Retain explicit negatives when accuracy requires them: “Your payment was not processed.” Positive wording must not hide failures, restrictions or consequences.
- Use warmth through clear, considerate wording. Do not add excessive exclamation marks, forced jokes or familiarity.
- Write labels and calls to action literally. Let the reader predict the result before acting.

---

<br>

## Mechanics

<br>

### Basics

1. Write for both careful readers and people who skim. Group related ideas and use descriptive headings and subheadings.
2. Lead with the main point at sentence, paragraph, section and page level.
3. Prefer short, familiar words and manageable sentences. Remove unnecessary modifiers.
4. Be specific. Replace vague claims and filler with useful facts or actions.
5. Apply the same terminology, copy patterns and conventions throughout the content.

<br>

### Capitalization and contractions

- Sentence case capitalizes the first word and proper nouns. Title case capitalizes major words, generally excluding articles, prepositions and conjunctions. Choose the project's convention for each content type consistently; the supplied excerpt describes both without assigning them universally.
- Keep ordinary uses of website, internet, online and email lowercase.
- Present email addresses and website domains in lowercase where accurate. Preserve case-sensitive URL paths, query values and exact identifiers.
- Use natural contractions for an informal, friendly tone. Avoid any contraction that makes a requirement or meaning unclear.

<br>

### Emoji

Mailchimp's supplied guidance permits occasional, deliberate emoji. This toolkit's existing no-emoji preference takes precedence: do not introduce emoji into project content or use text characters as substitute UI icons.

<br>

### Numbers

| Subject | Rule | Example |
| --- | --- | --- |
| Ordinary numbers | Prefer numerals, including at the start of a sentence and for ordinals. Follow [Google’s numeral guidance](../../writing-decisions/goals-and-principles/google-writing-goals-principles.md#use-numerals); use words when needed to distinguish mixed numeric meanings. | “8 people joined, and 12 return tomorrow.”; “3rd place” |
| Established expressions | Preserve conventional spelled-out forms. | first impression; third-party integration; all-in-one |
| Thousands | Use commas in numbers with more than 3 digits. | 999; 1,000; 150,000 |
| Large amounts | Write the full number unless space is constrained; use compact forms consistently when necessary. | 150,000; 150k in a compact chart |
| Fractions | Spell out prose fractions. | two-thirds |
| Decimals | Use decimal points when a fraction would be awkward or obscure precision. | 1.375; 47.2 |
| Percentages | Use the % symbol. | 25% |
| Ranges | Use a hyphen without surrounding spaces. | 20-30 days |
| US currency | Put $ before the amount; omit cents when zero, otherwise show cents. | $20; $19.99 |
| Other currencies | This profile places the symbol before the amount; clarify the currency if ambiguous. Follow the target locale when required. | €20; ¥500 |
| Telephone numbers | Separate number groups with dashes and no spaces; include a country code for international readers. | +1-202-555-0148 |
| Fahrenheit | Use the degree symbol immediately before capital F. | 98°F |

These are prose conventions. Preserve exact values, code, identifiers, measurements and machine-readable formats when conversion would damage meaning.

<br>

### Dates, time and decades

- Generally spell out the weekday and month: “Saturday, January 24.” Abbreviate only where space requires it: “Sat., Jan. 24.” Include a year when needed to avoid ambiguity.
- Use numerals followed by a space and lowercase am or pm: “7 am,” “7:30 pm.” Omit zero minutes on the hour.
- Use an unspaced hyphen for a time span: “7 am-10:30 pm.” Repeat am or pm where needed for clarity.
- Include a time zone for events and other scheduled activity.
- For continental US zones, use ET, CT, MT and PT.
- Spell out international zone names, such as Nepal Standard Time. Use a UTC offset when a zone lacks a set name; give the offset applicable to the event date when needed.
- Mailchimp's ET default reflects its stated Atlanta context. In other projects, use the event's or audience's actual zone; do not impose ET.
- For decades within the past 100 years, shortened forms such as “the 90s” are allowed when the century is clear. Use full forms for older or ambiguous decades: “the 1890s,” “the 1990s.” Reassess the relative 100-year window over time.

Source clarification: the supplied time-span instruction says hyphen, but its example uses an en dash. This profile follows the written instruction and the general numeric-range rule consistently.

<br>

### People, places and things

#### File extensions and filenames

- Refer to a file type in uppercase without a leading period: PDF, GIF, HTML.
- Add a lowercase s for plurals: PDFs, JPGs.
- Prefer lowercase filenames when creating new files: “project-notes.pdf.”
- Preserve the exact case of an existing filename or path. Do not silently change a link target.

Source clarification: the supplied excerpt requests lowercase filenames but includes a mixed-case example. This profile distinguishes new naming conventions from accurate references to existing files.

#### Pronouns

- Use singular they, them and their when gender is unknown or irrelevant.
- Use a person's appropriate pronouns when known.
- Avoid “one” as an impersonal pronoun in this conversational profile.

#### Quotations and personal names

- Use present-tense attribution for quotations in blog posts and similar publications: “says Jordan Lee.”
- Preserve chronology when a historical context requires a different tense.
- Give a person's first and last names on first mention; use their first name afterward when appropriate to the context and unambiguous.
- Do not invent names or personal details to satisfy a copy pattern.

#### Teams, departments and job titles

- Capitalize department and team names, but not the generic words “team” and “department”: “Marketing team,” “Support department.”
- Capitalize an individual title when referring to a specific role under the selected capitalization convention: “Marketing Manager.” Lowercase generic references: “the managers.”
- Avoid calling people ninjas, rockstars or wizards unless the description is literal.

#### Schools

- Use the full official school, college or university name on first mention.
- Use its recognised short name or abbreviation on later mentions. Introduce it clearly where readers might not recognise it.

#### Cities, states and countries

- Spell out city and state names.
- Under the supplied US house style, accompany a US city with its state except for these listed cities:

Atlanta, Baltimore, Boston, Chicago, Cincinnati, Cleveland, Dallas, Denver, Detroit, Honolulu, Houston, Indianapolis, Las Vegas, Los Angeles, Miami, Milwaukee, Minneapolis, New Orleans, New York, Oklahoma City, Philadelphia, Phoenix, Pittsburgh, St. Louis, Salt Lake City, San Antonio, San Diego, San Francisco, Seattle and Washington.

- Treat this as the exception list in the supplied excerpt, not a verified statement of current AP Style. Add location detail whenever the audience needs it for clarity.
- Spell out United States on first mention, then use US. Apply the same pattern to names with common abbreviations, such as United Kingdom (UK) and European Union (EU). The EU is a union, not a country.

#### Websites and URLs

- Capitalize official website and web-publication names; do not italicize them.
- Prefer descriptive linked text where appropriate. When displaying a web address, omit the protocol and www when doing so remains clear.
- Keep the actual link destination complete and accurate. Do not remove meaningful subdomains or alter case-sensitive paths.
- Explicit user preferences for visible full URLs take precedence.

<br>

### Source-specific brand examples

Mailchimp's legal entity, plan names, company voice and product capitalization are examples from the source material, not general AI writing decisions. They do not apply to your projects unless you are actually writing about that company. For any company, verify its current names and preserve official spelling; do not borrow its identity or claims.

<br>

### Writing about other companies

- Follow each company's official spelling and capitalization for itself and its products, such as iPad, YouTube and Yahoo!.
- Use “it” for a company or product in this guide.
- Verify names against an authoritative source when needed; preserve literal brand punctuation.

<br>

### Text formatting

- Italicize titles of long works, such as books, films and albums.
- Use italics sparingly for emphasis.
- For consistent formatting, italicize references to in-app elements and button or navigation labels in instructions. Match the interface's exact wording.
- Do not underline text for decoration or combine italic, bold, capitals and underline for emphasis. Preserve normal visual affordances for actual links.
- Left-align prose in left-to-right content; avoid centered or right-aligned body text.
- This prose rule does not override language direction, numeric table alignment or an approved interface layout.
- Keep one space between sentences.

---

<br>

## Punctuation

<br>

### Punctuation

#### Apostrophes

- Add ’s for a singular possessive, including singular names ending in s: “Alex's notes,” “Chris's notes.”
- Add only an apostrophe for plural possessives ending in s: “the editors' notes.”
- Use apostrophes for omitted letters in contractions. Stylised omissions for humour or emphasis should be rare.
- Use consistent typographic apostrophes in published prose where supported. Preserve literal characters required by code and identifiers.

#### Colons

- Introduce a list with a colon rather than an ellipsis, dash or comma.
- A colon may connect closely related clauses. Capitalize the first word after it when a complete sentence follows.

#### Commas

- Use the serial (Oxford) comma in a list of 3 or more items.
- Check sentence structure and meaning when placing commas. Reading aloud can reveal awkward phrasing, but a breath alone is not a grammatical reason to add a comma.

#### Hyphens and em dashes

- Use an unspaced hyphen to join compound terms where needed or indicate a range: “first-time visitor,” “Monday-Friday.”
- Use a true em dash without surrounding spaces for an aside. Do not substitute a hyphen or double hyphen.
- Keep asides useful and restrained; a new sentence may be clearer.

#### Ellipses

- Use three periods (...) sparingly to show an unfinished thought.
- Do not use ellipses for drama, emphasis, titles or headings.
- Use bracketed ellipses [...] for omitted words in a quotation. Preserve the original meaning and context.

#### Periods and spacing

- Under US punctuation conventions, periods and commas go inside quotation marks.
- Put a period outside parentheses when the parenthetical belongs to a larger sentence. Put it inside for a complete standalone parenthetical sentence.
- Leave exactly one space between sentences.

#### Questions and exclamations

- Place a question mark or exclamation point inside quotation marks when it belongs to the quoted words; otherwise place it outside.
- For parentheses, place the mark according to whether it belongs to the parenthetical or the surrounding sentence.
- Use exclamation points sparingly, never repeated.
- Never use exclamation points in failure messages or alerts. Omit them when uncertain.
- The supplied excerpt gives a blanket instruction to place exclamation points inside quotes; this adaptation uses meaning-based placement for accuracy.

#### Quotation marks

- Use quotation marks for direct quotations, words or letters discussed as terms, and titles of short works such as articles or poems.
- Use single quotation marks inside double quotation marks for a nested quote.
- Keep quoted wording accurate and clearly attributed.

#### Semicolons and ampersands

- Use semicolons sparingly. Prefer simpler sentences; use an em dash only when the relationship warrants an aside.
- Write “and” unless an ampersand is part of an official company or brand name.

---

<br>

## Project questions and brief

<br>

### How to ask

- Reuse answers and approved decisions already available in the project.
- Ask the few questions that affect the next draft, in small batches of no more than three. Do not present this whole document as a required questionnaire.
- Offer short examples or two contrasting drafts when abstract labels are difficult to choose.
- Start with one provisional profile, then adjust using context and reader feedback.
- State assumptions if optional preferences remain unanswered. Do not invent missing facts, permissions or service guarantees.
- Keep the selected project conventions in the consuming project's documentation; do not add every local preference to global rules.

<br>

### Start with the project

Choose the most useful unanswered questions first:

1. Who is this for, and what should they be able to decide, understand or do?
2. Where will they encounter the content: a website, form, application, lesson, email or another channel?
3. What should the experience feel like, and what should it avoid?

Then establish what is already known: audience research, existing copy, the source of truth, brand guidance, terminology and scope. Ask what is uncertain rather than treating assumptions as evidence.

<br>

### Choose an initial tone profile

Choose a position on each spectrum. These form one combined profile; the user does not have to choose only one dimension.

| Dimension | Question |
| --- | --- |
| Formality | More formal, more casual, or somewhere between? |
| Humour | Serious, lightly humorous, or openly funny? |
| Respectfulness | Straightforward and respectful, or irreverent about the subject? |
| Enthusiasm | Restrained and factual, or more enthusiastic? |

Record the choices with concrete wording examples. Do not present the poles as good and bad scores. The framework comes from [NN/g](https://www.nngroup.com/articles/tone-of-voice-dimensions/); these intake questions are an authored application.

If the user needs a starting suggestion, offer serious, conversational, respectful and mostly matter-of-fact wording as a provisional service-writing option. This is not a universal style or an approved project preference until adopted.

<br>

### Refine the profile when useful

| Area | Questions to select from |
| --- | --- |
| Identity | Which two or three qualities should readers notice? Which qualities should they never infer? |
| Examples | Is there existing wording you like? What specifically works about it? |
| Audience | Are readers beginners, specialists or mixed? What terms do they already know? |
| Situation | Are readers exploring, learning, buying, recovering from failure or facing a deadline? What evidence supports that context? |
| Outcomes | Which facts, conditions and next actions must remain clear in every tone variant? |
| Boundaries | Are jokes, slang, exclamation marks, metaphors, praise or emotional language appropriate here? |
| Trust | What claims can we verify? Which uncertainties or limitations affect the reader's decision? |
| Language | Which language, regional spelling and terminology conventions should we use? Are translations needed? |
| Structure | What belongs in the main flow, optional detail or another destination? Does existing content already meet the need? |
| Maintenance | Who owns accuracy, and what changes should trigger a review? |
| Evidence | How will we know readers understand the message and can act on it? |

Target qualities can include reassuring, authoritative, instructional, conversational, encouraging, empathetic, playful, urgent, neutral or celebratory. They can overlap; do not treat that list as a required taxonomy.

Examples of boundaries: precise without sounding superior; approachable without filler; encouraging without claiming mastery. Turn each chosen boundary into an example and a practical check.

<br>

### Agree on contextual adjustments

Ask only about contexts present in the project.

- Does introductory or promotional copy need more energy than task instructions?
- How should the tone change when something fails or the reader risks losing work?
- What should confirmations say about the verified outcome and next step?
- If this is learning content, what should feedback recognise and what should it avoid claiming?
- When is urgency justified by a real deadline?
- Should repeated or frequently encountered messages be quieter than first-time guidance?

Record these as exceptions to the baseline, with facts and actions preserved. A different project scope can justify a different baseline later.

<br>

### Compare drafts instead of debating adjectives

1. Draft a representative message in the provisional profile.
2. Create one alternative that changes a single tone dimension.
3. Keep the underlying information, consequences and action the same.
4. Ask how each sounds, which fits the situation and what the reader would do.
5. Record a provisional choice and test it in the interface.

For an original low-stakes example, compare a brief saved-draft confirmation with a warmer version. Both may claim saving only when the application has confirmed it. For errors, include a real recovery action rather than adding personality to an unhelpful message.

<br>

### Save a short project brief

Use this template in the consuming project:

~~~markdown
# Project content and tone brief

Status: provisional / reviewed
Applies to:
Audience and task:
Evidence and assumptions:
Required facts and source of truth:

Voice qualities:
Tone profile:
- Formality:
- Humour:
- Respectfulness:
- Enthusiasm:

Context adjustments:
- Instructions:
- Errors and recovery:
- Confirmations:
- Other relevant contexts:

Words, claims and approaches to avoid:
Terminology and language conventions:
Preferred example:
Example to avoid:
Content owner and review triggers:
What to test next:
~~~

Not every field must be completed before a small reversible draft. Missing facts that determine correctness need a source or an explicitly marked placeholder.

<br>

### Revisit deliberately

Reconsider the profile when audience, medium, project scope, stakes or research changes. Update the relevant examples and brief rather than silently changing all copy. Keep a useful record of the decision and its reason; avoid duplicating obsolete profiles as simultaneous requirements.

---

<br>

## Evaluation and maintenance

<br>

### Reset: Check

Read headings and actions without the body copy: is the subject and next action understandable? Then remove sentences that could describe almost any unrelated product. Check that shortening has preserved necessary context and qualifications.

<br>

### Evaluate the result

- Use real content in a prototype early; test wording and layout together.
- Ask someone to find an answer or complete a task without coaching.
- Observe misunderstandings before explaining the intended meaning.
- Compare tone variants with the same facts and actions. Ask readers how each sounds and what they would do next.
- Check comprehension, appropriateness and preference separately.
- Use analytics to investigate questions, not as a substitute for research. Clicks, visits, reading time and scores alone do not establish success.
- Record the change, reason and remaining uncertainty. Revise the brief when audience, scope or evidence changes.

<br>

### Maintain content after publication

- Give each important content item an owner, source of truth and review trigger.
- Audit conflicting or duplicate information and coordinate consolidation.
- Review after relevant service, policy, product or language changes, not only on a calendar.
- Explain changes through their effect on the reader: who is affected, when and what to do.
- When a change note is needed, describe the substantive difference rather than saying only that a page was updated.
- Decide whether obsolete material should be replaced, archived, withdrawn or removed. Consider continuing needs, records and redirects.
- Use house style as a lookup reference. Do not impose GOV.UK publishing rules, Mailchimp's personality or one project's tone on every website.

<br>

### Review checklist

1. Can a reader identify the main point by scanning the headings and opening sentences?
2. Are names, terms and abbreviations accurate and consistent?
3. Are numbers, dates, currencies and times unambiguous for the audience?
4. Are punctuation, capitalization and formatting consistent with the selected project conventions?
5. Do links, filenames, quoted wording and interface labels preserve exact required values?
6. Does the wording identify actions and responsibility without hiding failures or conditions?
7. Have project-specific preferences and documented exceptions been preserved?

<br>

### Drafting and review

1. Identify the audience, immediate task, required facts and available next action.
2. Establish the likely context from evidence. Mark uncertain assumptions.
3. Draft in the stable voice, then adjust tone for the situation.
4. Check that terms, actions and consequences are understandable.
5. Remove forced humour, hype, condescension and unsupported claims.
6. Read the copy in its interface and confirm the status and recovery instructions are accurate.
7. Test whether a reader understands what happened and what to do next.

---

<br>

## Source scope and coverage

<br>

### README.md — scope

Use this folder to decide what content belongs in a project, how it should sound, and how to write it consistently. Work from the reader's needs toward sentence-level details. Return to earlier decisions when testing exposes a problem.

<br>

### best-practices.md — scope

Use this file when planning, drafting or reviewing website, application, service or learning content. Start with [Project questions](../../writing-decisions/project-questions.md) to establish a project-specific brief.

This is an original synthesis of the content-design LMS and its source map. It covers content decisions, not a required visual theme, audio voice, software stack or government identity. Existing user instructions and approved project decisions take precedence.

<br>

### Sources and coverage

Reviewed 2026-10-19 against [content-design-lms](https://github.com/Pythonidaer/content-design-lms), its course and source manifest. The pinned snapshot is recorded in [design sources](../sources.md).

The review covers all 26 lesson decks: user needs; scope and formats; drafting; organisation; structure; language; titles; summaries; links; accessibility; translation; URLs; maintenance; retirement; change communication; change notes; style guides; evaluation; voice/tone; tone dimensions; GOV.UK tone; tone testing; the tone reference; orientation; capstone; and source scope.

Primary references:

- [GOV.UK: Understand content design](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/plan-manage-content/understand-content-design/)
- [GOV.UK: Writing to GOV.UK standards](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/)
- [GOV.UK: Use the right tone](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/writing-guidelines/right-tone/)
- [NN/g: Four Dimensions of Tone of Voice](https://www.nngroup.com/articles/tone-of-voice-dimensions/)
- [Mailchimp: Voice and Tone](https://styleguide.mailchimp.com/voice-and-tone/)

This is reusable guidance, not a full reproduction of those sources. The complete A to Z style guides remain lookup references. Adapt publishing conventions to the project.

<br>

### google-writing-goals-principles.md — scope

Source: [Material Design 2 — Writing](https://m2.material.io/design/communication/writing.html).
Condensed adaptation; not an official Google instruction file. Apply to interface copy.

<br>

### mailchimp-writing-goals-principles.md — scope

Use these general writing goals when planning, drafting or reviewing content. Apply it alongside [Content and tone guidance](../../writing-decisions/best-practices.md), [Mailchimp voice and tone](../../writing-decisions/voice-and-rules/mailchimp-tone-voice.md) and [Mailchimp grammar and mechanics](../../writing-decisions/grammar-and-mechanics/mailchimp-grammar-mechanics.md).

These rules adapt the user-supplied “Writing Goals and Principles” excerpt. Apply the principles to the actual product, audience and task; do not claim Mailchimp's identity or business context for another organisation. Explicit user instructions and approved project decisions take precedence.

<br>

### Source and scope

Based on the “Writing Goals and Principles” excerpt supplied by the user from Mailchimp's Content Style Guide. The five goals are empower, respect, educate, guide and speak truth. The four content principles are clear, useful, friendly and appropriate.

The actionable rules, review questions, workflow and example are toolkit applications of those goals and principles. This is an adaptation of the supplied material, not an independently checked account of the current live guide.

<br>

### mailchimp-grammar-mechanics.md — scope

Use this grammar and mechanics reference alongside [Mailchimp voice and tone](../../writing-decisions/voice-and-rules/mailchimp-tone-voice.md) and [Content and tone guidance](../../writing-decisions/best-practices.md) when checking project copy. Grammar and mechanics govern consistent writing conventions; voice and tone govern character and situational delivery.

Adapted from the user-supplied Mailchimp “Grammar and Mechanics” excerpt. This is a reusable reference, to be adapted to the project's language and locale. Explicit user instructions, established project conventions, accessibility and factual accuracy take precedence.

<br>

### Source and adaptation scope

Based on the user-supplied “Grammar and Mechanics” excerpt from [Mailchimp's Content Style Guide](https://styleguide.mailchimp.com/grammar-and-mechanics/). This file adapts the supplied material; it does not assert that the live guide, company details or external style standards were independently checked.

All supplied subject areas are covered. Clarifications address passive-voice detection, audience familiarity, URL and filename case, time-range punctuation, quotation punctuation, locale and time-zone defaults, factual verification, accessible formatting and positive wording. The existing toolkit no-emoji preference overrides the source's permissive emoji rule.

<br>

### project-questions.md — scope

Use this with [Content and tone guidance](../../writing-decisions/best-practices.md). The goal is a usable starting brief that can change as the project develops.

<br>

### mailchimp-tone-voice.md — scope

Use these general voice and tone instructions when drafting project copy. Apply it alongside [Content and tone guidance](../../writing-decisions/best-practices.md) and record the choice using [Project questions](../../writing-decisions/project-questions.md). Existing user instructions and approved project decisions take precedence.

These rules are an authored adaptation of the Mailchimp “Voice and Tone” excerpt supplied by the user. Their source is Mailchimp, but the general advice can guide any project. Choose a voice appropriate to the actual audience and never claim another company's identity or history.

<br>

### Source and scope

Based on the user-supplied excerpt from [Mailchimp: Voice and Tone](https://styleguide.mailchimp.com/voice-and-tone/), adapted on 2026-10-20.

Coverage: stable voice versus situational tone; an experienced and compassionate partner; plain, warm and accessible language; explaining specialist concepts; subtle inclusive humour; clarity before entertainment; active voice; avoiding slang and jargon; and positive phrasing.

The examples, context table, qualifications and review process are toolkit applications of those principles. This file does not reproduce or replace Mailchimp's separate grammar and mechanics guide.

<br>

### tone.md — scope

Moved from [Content and tone guidance](../../writing-decisions/best-practices.md). This is an original synthesis of the content-design LMS; existing user instructions and approved project decisions take precedence.

Use [Voice guidance](../../writing-decisions/voice-and-rules/voice/voice.md) for the distinction between voice, tone and mechanics.

<br>

### Source

The pinned LMS snapshot and provenance are recorded in [design sources](../sources.md).

<br>

### voice.md — scope

Moved from [Content and tone guidance](../../writing-decisions/best-practices.md). This is an original synthesis of the content-design LMS; existing user instructions and approved project decisions take precedence.

<br>

### Source

The pinned LMS snapshot and provenance are recorded in [design sources](../sources.md).

<br>

### Consolidation coverage

The following table records every input file. The source decisions are organized into the categories above; publisher-specific brand examples are summarized separately from the general instructions. Repeated guidance remains traceable and should be applied once, not repeated in published copy. This compilation uses repository adaptations; it does not claim a fresh audit of the publishers’ live sites.

| Input | Included sections |
| --- | --- |
| [design/ai-design-reset/content-design.md](content-design.md) | 3 |
| [writing-decisions/README.md](../../writing-decisions/README.md) | 4 |
| [writing-decisions/best-practices.md](../../writing-decisions/best-practices.md) | 10 |
| [writing-decisions/goals-and-principles/google-writing-goals-principles.md](../../writing-decisions/goals-and-principles/google-writing-goals-principles.md) | 4 |
| [writing-decisions/goals-and-principles/mailchimp-writing-goals-principles.md](../../writing-decisions/goals-and-principles/mailchimp-writing-goals-principles.md) | 6 |
| [writing-decisions/grammar-and-mechanics/mailchimp-grammar-mechanics.md](../../writing-decisions/grammar-and-mechanics/mailchimp-grammar-mechanics.md) | 17 |
| [writing-decisions/project-questions.md](../../writing-decisions/project-questions.md) | 9 |
| [writing-decisions/voice-and-rules/mailchimp-tone-voice.md](../../writing-decisions/voice-and-rules/mailchimp-tone-voice.md) | 8 |
| [writing-decisions/voice-and-rules/tone/tone.md](../../writing-decisions/voice-and-rules/tone/tone.md) | 5 |
| [writing-decisions/voice-and-rules/voice/voice.md](../../writing-decisions/voice-and-rules/voice/voice.md) | 3 |
