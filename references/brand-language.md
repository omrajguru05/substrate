# Substrate Brand Language

Substrate should sound clear, calm, capable, and human.

The writing should never need to prove that the company is intelligent, serious, transparent, humane, technically capable, or ambitious. Those qualities should be apparent from the work, the evidence, the decisions we explain, and the way we speak to people.

The work comes first.

This document applies to product copy, website copy, research updates, model releases, technical writing, documentation, pricing, events, social posts, changelogs, status pages, emails, careers pages, press material, investor material, and other public or internal communication written in the Substrate voice.

The same principles apply everywhere, but the amount of personality changes by context. A product interface should be cleaner than a research article. Documentation should be more literal than a launch page. A release announcement can have a stronger headline than an error message.

The underlying voice remains the same.

---

## 1. The voice

Substrate speaks with confidence, but never with theatre.

We state things plainly. We explain technical work without making it sound larger than it is. We do not manufacture excitement around ordinary progress, and we do not make ambitious work vague in an attempt to make it impressive.

Confidence comes from clarity.

Prefer:

> Clinical 1 reads handwritten prescriptions more reliably and handles longer records than the previous model.

Avoid:

> Clinical 1 represents a major leap forward in the future of medical intelligence.

If something is good, explain why.

If something improved, show what changed.

If something is uncertain, say that it is uncertain.

If something does not work, say that it does not work.

Do not turn tone into performance. The writing should not call attention to itself.

---

## 2. Core qualities

### Calm

Substrate should sound composed.

Do not use urgency, exaggerated excitement, dramatic framing, or inflated language to make ordinary work feel consequential.

Avoid:

> This changes everything.

> A new era begins today.

> The future of medicine starts here.

Prefer:

> Clinical 1 is available today.

> We have started testing the model on longer patient records.

> Document processing is currently delayed.

The facts should carry their own weight.

### Confident

State what is known without unnecessary hedging.

Prefer:

> Clinical 1 handles longer records than the previous model.

Avoid:

> We believe Clinical 1 may potentially offer improvements when working with longer records.

Confidence should not become arrogance. It should come from knowing what the evidence supports.

### Straightforward

Get to the point early.

Do not introduce a simple idea with several lines of setup. Do not hide an inconvenient fact behind formal language. Do not make people decode corporate phrasing.

Prefer:

> Document processing is delayed. Uploads are working normally, but results may take longer than usual.

Avoid:

> We are currently experiencing a temporary degradation in certain parts of the document processing experience.

Say what happened.

### Humane

Write for the person using the product.

Most people do not care about internal implementation details unless those details affect what they can do.

Instead of leading with:

> 200K context window.

Say:

> You can give it an entire patient history and ask questions across it.

Instead of:

> 40% lower inference cost.

Say:

> A workload that previously cost about ₹100 now costs about ₹60.

Instead of:

> 120 pages per minute.

Say:

> A 300-page medical record takes about 2½ minutes to process.

The technical specification can still exist. Put the useful meaning first.

### Kind

Kindness should appear in how we explain things.

Do not blame people for errors. Do not make someone feel uninformed because they do not understand a technical term. Do not hide bad news behind cheerful language.

Prefer:

> This device is using a setting the system does not currently support.

Avoid:

> Invalid user configuration.

Prefer:

> We could not read this section reliably. Check the original document before using the result.

Kindness and directness are compatible.

---

## 3. Honesty

Describe the system that exists, not the system we would like people to imagine.

Do not make a claim stronger because stronger wording sounds better.

If results are preliminary, say so.

If the model is uncertain, show the uncertainty.

If performance varies by task, explain where.

If another approach performs better in a specific area, there is no reason to disguise it.

Prefer:

> The model performs well on digitally generated reports but remains less reliable on handwritten prescriptions.

Avoid:

> The model delivers consistently strong performance across clinical documents.

unless the evidence actually supports that statement.

Do not bury limitations at the bottom of a page merely because they make the product sound less impressive.

A limitation that materially affects use belongs near the relevant capability.

---

## 4. Transparency without unnecessary exposure

Transparency does not require publishing everything.

We can keep internal methods, unreleased projects, proprietary systems, security details, research directions, commercial strategy, and other sensitive information private.

The distinction is simple:

We may keep the work private when necessary.

We should not keep material truth from the person using the product.

If a limitation affects reliability, disclose it.

If an outage affects results, disclose it.

If pricing has an important condition, disclose it.

If a model is experimental, say so.

If a feature is not available, do not imply that it is.

Do not compensate for secrecy by becoming vague.

Avoid:

> We use proprietary technology to provide best-in-class results.

Prefer:

> The model combines information across reports, scans, and structured records. We do not publish the internal training method.

The second version is clear about the product without exposing what does not need to be public.

---

## 5. Write for use, not for features

A feature matters because of what it lets someone do.

Prefer:

> Compare several reports and see how a value changed over time.

Avoid:

> Advanced longitudinal analysis.

Prefer:

> Give it a scan and the accompanying report, and it can use information from both.

Avoid:

> Multimodal clinical reasoning.

Prefer:

> Review an entire patient record without opening every document separately.

Avoid:

> Long-context document intelligence.

Prefer:

> It can flag the fields it could not read reliably.

Avoid:

> Confidence-aware extraction pipeline.

Use technical terminology when it is genuinely useful. Do not use it as decoration.

---

## 6. Human-scale numbers

Whenever possible, translate infrastructure metrics into something a person can understand.

Technical numbers are useful, especially for developers and researchers. They should not automatically be the first thing everyone sees.

### Context

Instead of:

> 200K tokens.

Prefer:

> You can give it an entire patient history and ask questions across it.

Then, where useful:

> Maximum context: 200K tokens.

### Cost

Instead of:

> ₹X per million input tokens.

Prefer:

> About ₹18 for a typical 100-page patient record.

Then provide the exact technical pricing underneath.

### Speed

Instead of:

> 120 pages per minute.

Prefer:

> A 300-page record takes about 2½ minutes to process.

### Rate limits

Instead of:

> 500K TPM / 100 RPM.

Prefer:

> You can process roughly 150 standard reports every hour on this plan.

Then provide the exact rate limits for people who need them.

### Efficiency improvements

Instead of:

> 40% lower inference cost.

Prefer:

> A workload that previously cost about ₹100 now costs about ₹60.

If the exact amount varies:

> For our typical workloads, the same task costs about 40% less.

Always make clear what the number represents.

---

## 7. Keep product language clean

Product copy should contain as little noise as possible.

Every word should do at least one of these things:

- explain what something is,
- help someone decide,
- help someone complete an action,
- explain what happened,
- explain what to do next,
- communicate a meaningful limitation.

Avoid decorative labels, filler copy, repeated explanations, fake sophistication, and sentences written only because a section appears to need text.

Prefer:

> Upload report

Avoid:

> Begin your document analysis journey

Prefer:

> Recent reports

Avoid:

> Your clinical intelligence workspace

Prefer:

> No reports yet. Upload a document to begin.

Avoid:

> Your reports will appear here once you begin exploring everything Substrate can do.

If a label can disappear without making the interface harder to understand, remove it.

If a sentence exists only to fill visual space, remove it.

If a heading repeats the paragraph directly below it without adding meaning, remove it.

Whitespace is preferable to filler.

---

## 8. Interface language should be literal

Interfaces should describe what is happening.

### Loading

Use:

> Reading document…

> Extracting clinical information…

> Comparing reports…

> Checking uncertain fields…

> Preparing results…

Avoid:

> Thinking…

> Understanding your health…

> Working its magic…

> Making sense of everything…

Do not make software sound sentient when there is no reason to.

### Errors

Use:

> We could not read this file. Try uploading the original PDF or a clearer scan.

> This document is password protected. Remove the password and upload it again.

> The upload stopped before the file finished sending. Try again.

Avoid:

> Something went wrong.

when we know what went wrong.

### Empty states

Use:

> No reports yet. Upload a document to begin.

> No results found.

> No fields need review.

Avoid:

> Nothing here yet. Your journey starts when you upload your first report.

### Confirmation

Use:

> Report deleted.

> Changes saved.

> Upload complete.

Do not add celebration to routine actions.

Avoid:

> Success! Your report has been successfully deleted.

### Buttons

Buttons should describe the action.

Use:

> Upload report

> Compare reports

> Review fields

> Download PDF

> Delete report

Avoid:

> Get started

> Explore

> Continue

when a more specific action is available.

---

## 9. Uncertainty

Uncertainty is part of the product, particularly in medicine.

Do not hide it. Do not dramatise it either.

Use:

> The model could not determine this value reliably.

> This section may contain an error. Check the original document before using the result.

> The handwriting in this section could not be read with sufficient confidence.

> The report does not contain enough information to determine this reliably.

> The model found two possible readings for this value. Check the original report.

Do not use vague warnings that force the person to guess what is wrong.

Avoid:

> AI can make mistakes.

when we can identify the specific uncertain result.

General warnings still have a place. They should not replace useful local information.

---

## 10. Limitations

Explain limitations with the same confidence as capabilities.

Prefer:

> Clinical 1 performs well on clear reports but still struggles with heavily degraded scans and uncommon handwritten abbreviations.

Do not write limitations apologetically.

Do not bury them in legal language if they matter to normal use.

Do not turn them into marketing.

Avoid:

> While Clinical 1 already delivers impressive results, we are continuously working to make it even better in challenging edge cases.

Prefer:

> Poor scans and uncommon abbreviations remain the largest sources of error.

The second version is more useful.

---

## 11. Evidence before adjectives

Prefer evidence to praise.

Avoid relying on words such as:

- powerful
- advanced
- intelligent
- revolutionary
- groundbreaking
- transformative
- seamless
- cutting-edge
- next-generation
- industry-leading
- unprecedented
- game-changing
- world-class
- state-of-the-art, unless used as a precise technical comparison with evidence
- robust, unless the exact meaning is clear
- effortless
- beautiful, when describing functionality
- innovative, as self-description

Instead of:

> Our most powerful clinical model yet.

Prefer:

> Clinical 2 reads handwriting more reliably, handles longer patient histories, and makes fewer unsupported assumptions than Clinical 1.

Instead of:

> Significantly faster.

Prefer:

> A 300-page record now takes about 2 minutes to process instead of 4.

Instead of:

> More accurate.

Prefer:

> Prescription extraction improved from 78% to 91% on our evaluation set.

Whenever an adjective can be replaced with useful information, replace it.

---

## 12. Research language

Research writing should distinguish clearly between what we know, what we observed, what we infer, and what we are testing.

Use:

> We are developing…

for active work.

> We are testing…

for an experiment.

> We are investigating…

when the answer remains unclear.

> We found…

when there is evidence.

> Our current results suggest…

when the evidence is useful but not sufficient for a strong conclusion.

> Our aim is…

for a longer-term direction.

> In this evaluation…

when a result belongs to a specific test rather than a universal claim.

Do not turn research plans into achievements.

Do not turn early results into conclusions.

Do not generalise beyond the population or dataset that was evaluated.

Prefer:

> On our current evaluation set, the model correctly extracted medication instructions from 91% of prescriptions.

Avoid:

> The model reads prescriptions with 91% accuracy.

unless that broader statement is actually justified.

---

## 13. Research updates

A research update should usually answer:

1. What are we testing?
2. Why does it matter?
3. What have we observed?
4. Where does it still fail?
5. What happens next?

Example:

> We are testing whether a single model can understand information across reports, scans, handwritten notes, and medical images.

> Early results are strongest on digitally generated reports. Handwriting remains considerably less reliable, particularly when scans are damaged or abbreviations are uncommon.

> We will publish the evaluation once testing is complete.

Do not turn every research update into an announcement.

---

## 14. Technical writing

Technical writing should explain the system, not display the writer's technical vocabulary.

A useful structure is:

1. what the problem was,
2. what was happening,
3. why it was happening,
4. what changed,
5. what effect that change had,
6. what limitations remain.

Prefer:

> The model was reading the table correctly, but values were being paired with the wrong reference ranges because the layout parser treated each column independently. We changed the parser to preserve row relationships before extraction.

Avoid:

> We implemented an advanced context-preserving layout intelligence layer to significantly improve structured clinical understanding.

The first version tells us what actually happened.

---

## 15. Product launches

A launch should answer a few basic questions quickly:

- What is it?
- What changed?
- What can someone do with it?
- How well does it work?
- What still needs work?
- What does it cost?
- When is it available?

A good launch does not require ceremonial language.

Example:

> Introducing Clinical 1, our first model designed specifically for clinical documents.

> It reads reports, prescriptions, handwritten notes, and structured medical records, and can use information across them together.

> Compared with our previous system, it handles longer records better, reads handwriting more reliably, and costs less to run.

> On our current prescription evaluation, medication-instruction extraction improved from 78% to 91%.

> Poor scans and uncommon abbreviations remain the largest sources of error.

> Clinical 1 is available today.

Avoid:

> Today marks an important moment for Substrate.

The release itself is the news.

---

## 16. Release writing

Release copy can be slightly more assertive than normal product copy, but it should remain factual.

A useful structure is:

### What it is

> Clinical 1 is our first model designed specifically for clinical documents.

### What changed

> It handles longer records, reads handwriting more reliably, and makes fewer unsupported assumptions when information is missing.

### What that means

> A 300-page patient history can now be processed in about 2 minutes instead of 4.

### Where it still struggles

> Poor scans remain the largest source of extraction errors.

### Availability

> Clinical 1 is available today.

### Optional closing line

> We are looking forward to seeing what you use it for.

Warmth is welcome at the edge of a release. It should not replace useful information.

---

## 17. Headlines

Headlines can be more distilled than body copy.

They can carry slightly more personality, but they should not become vague slogans.

Examples:

> More of the picture.

> Beyond the report.

> A clearer read.

> Made for medicine.

> Better with handwriting.

> More context. Less guesswork.

> From data to context.

> Built to understand.

> See what matters.

> Medicine, understood.

A headline may create interest.

The paragraph beneath it should explain exactly what it means.

Do not make both the headline and the body abstract.

---

## 18. Event titles

Event titles can be concise and slightly suggestive.

Examples:

> More of the picture.

> Beyond the report.

> A clearer read.

> Built to understand.

> See what matters.

> Made for medicine.

Keep the surrounding copy minimal.

Example:

> **More of the picture.**  
> Substrate Event  
> October 14

Or:

> **More of the picture.**  
> Join us on October 14 for a closer look at what we have been working on across models, clinical information, and medical tools.

Do not add copy because an event page has empty space.

Avoid:

> Join us for an exciting look at the future of medical AI.

The event does not need to advertise its own importance.

---

## 19. Website copy

Website copy should establish what Substrate does quickly.

A homepage hero should not require interpretation.

Examples:

> **AI for medicine.**  
> Understand reports, compare clinical information, and work across different medical formats in one place.

Or:

> **Made for medicine.**  
> Models and systems that understand clinical information and work across medical tools.

The rest of the page should become more specific as the person moves downward.

Avoid spending the first screen on philosophy when the visitor still does not know what the company does.

---

## 20. Product pages

Lead with what someone can do.

Example:

> **Clinical 1**  
> Understand reports, prescriptions, handwritten notes, and other clinical documents.

Then:

> Give it a patient record and ask questions across the entire history instead of reviewing every document separately.

Then practical information:

> A typical 100-page record takes about 40 seconds to process and costs about ₹18.

Then technical details for people who need them.

Do not reverse that order by leading with architecture, model size, context limits, token pricing, or internal terminology.

---

## 21. Feature copy

Feature sections should describe actions and outcomes.

Use:

> **Compare reports**  
> See how values changed across multiple tests.

> **Read handwriting**  
> Extract information from prescriptions and handwritten clinical notes.

> **Review uncertainty**  
> Fields the model could not determine reliably are marked for review.

Avoid:

> **Powerful insights**

> **Smarter workflows**

> **Clinical intelligence**

These labels say almost nothing.

---

## 22. Documentation

Documentation should be almost invisible as brand writing.

Be exact.

Use:

> Upload a PDF, image, or structured document.

> Clinical 1 extracts the relevant information and returns it in a common format.

> Fields with low confidence are marked separately.

The reader is there to understand the system and use it.

Do not make them read brand copy first.

Avoid opening documentation with a manifesto.

---

## 23. Developer copy

Developer pages should still explain use before infrastructure.

Prefer:

> **Build with Clinical 1.**

> Send reports, scans, or structured medical records through the API and receive normalised clinical information in return.

> Use it to review documents, compare records, extract values, or build your own clinical workflows.

Then provide:

- endpoints,
- model names,
- rate limits,
- context limits,
- pricing,
- SDK details,
- schema references.

The technical detail matters. The order matters too.

---

## 24. Pricing

Pricing should answer what something will cost in practice.

Lead with a relatable unit when one exists.

Example:

> About ₹18 for a typical 100-page patient record.

Then:

> ₹X per million input tokens  
> ₹Y per million output tokens

If cost depends heavily on usage, say so.

Avoid presenting a single example as a universal price.

Use:

> Most 100-page records cost between ₹15 and ₹22 to process, depending on document density.

when that is more truthful.

---

## 25. Social writing

Social writing should remain recognisably Substrate.

Short does not mean loud.

Examples:

> Clinical 1 is available today. It reads handwriting more reliably, handles longer medical records, and costs less to use.

> A medical model should understand the report, not just extract text from it.

> We are testing models that can understand reports, scans, handwritten notes, and machine outputs together.

> Poor scans remain the largest source of prescription-reading errors in our current evaluation.

Avoid launch clichés, forced excitement, excessive punctuation, slang inserted to appear relatable, and artificial informality.

Do not write differently simply because the platform rewards attention.

---

## 26. Changelogs

Changelogs should tell people exactly what changed.

Use:

> **Better handwriting recognition**  
> Improved extraction of drug names and dosage instructions from prescriptions.

> **Faster long-document processing**  
> Large patient records now take less time to process.

> **Clearer uncertainty**  
> Low-confidence fields are now marked for review instead of being returned as normal values.

Avoid:

> General improvements and bug fixes.

when meaningful changes can be named.

---

## 27. Status and incident communication

Status communication should be factual and current.

During an incident:

> Document processing is delayed.

> Uploads are working normally, but results may take longer than usual. We are investigating the cause.

If the issue becomes clearer:

> Processing is delayed because one of our document-analysis services is not completing jobs normally. Uploads remain available.

When resolved:

> Document processing is back to normal. Files submitted during the incident have been processed.

Do not use euphemisms.

Do not over-apologise.

Do not speculate before the cause is known.

---

## 28. Email

Email should be useful immediately.

Example:

> Your report is ready.

> We found 3 fields that should be reviewed because the model could not read them reliably.

> Open report

Avoid:

> Great news! Your AI-powered report analysis is complete.

For a service issue:

> Processing is taking longer than usual today. Your report is still in the queue and will continue automatically.

Tell the person what happened and whether they need to do anything.

---

## 29. Onboarding

Onboarding should help someone begin.

Use:

> Upload your first report.

> We will extract the clinical information and show anything that needs your attention.

Do not create several screens of explanation before a person can use the product.

Avoid:

> Welcome to the future of clinical intelligence.

Let the product introduce itself through use.

---

## 30. About copy

About copy should describe the work.

Example:

> Substrate Labs works on artificial intelligence for medicine.

> Our current work includes clinical document understanding, models designed for medical tasks, and systems that allow AI to work with medical tools.

> Some of this work is available today. Some remains research.

Avoid using the About page to tell readers that the company is ambitious, innovative, responsible, or visionary.

Describe the work and let them decide.

---

## 31. Careers

Careers copy should be direct and respectful.

Example:

> We are a small team working on AI for medicine.

> We are looking for people across machine learning, medicine, infrastructure, and applied research.

> You do not need to match every requirement below.

Job requirements should distinguish between what is necessary and what is useful.

Avoid cultural theatre.

Do not write:

> We only hire exceptional people.

> We move fast and break boundaries.

> We are looking for 10x builders.

Say what the work requires.

---

## 32. Press descriptions

Press descriptions should be factual.

Example:

> Substrate Labs is an AI company working on models for medicine, clinical information systems, and ways for AI to work with medical equipment.

Do not turn a press description into an advertisement.

The purpose is accurate identification.

---

## 33. Investor communication

Investor material can be more strategic, but it should remain specific.

Example:

> Medical AI still operates across disconnected documents, models, and software systems.

> Substrate is working on models that can understand clinical information across those systems and, over time, interact with the medical tools that produce it.

Then show:

- the product,
- the evidence,
- usage,
- market,
- economics,
- research progress,
- risks,
- what remains unresolved.

Avoid grand category claims unless they are already defensible.

Do not call Substrate "the operating system for healthcare" simply because the phrase sounds large.

---

## 34. Internal updates

Internal writing should be even more direct.

Example:

> Prescription extraction improved this week, particularly for dosage instructions.

> Drug-name recognition remains inconsistent on poor scans, so that is the next area we are testing.

Do not turn internal progress into motivational copy.

The purpose is shared understanding.

---

## 35. Security and privacy

Do not ask people to trust adjectives.

State the actual protections.

Prefer:

> Your files are encrypted in transit and at rest.

> We do not use your clinical data to train our models unless you explicitly allow it.

> Deleted files are removed from active systems within X days.

Avoid:

> Your privacy is our top priority.

A factual statement is stronger.

If a protection has exceptions, explain them.

---

## 36. Warmth

Substrate can be warm.

It should not be sentimental.

A launch may end with:

> We are looking forward to seeing what you use it for.

A research update may end with:

> There is considerably more to test, and we will share what we find.

A product update may simply end after the final useful fact.

Not every piece of writing needs a closing statement.

Do not force warmth into errors, pricing, warnings, technical documentation, or serious medical limitations.

---

## 37. Personality in headlines, precision in body copy

Headlines have more room for compression.

Body copy has less.

A headline may say:

> More of the picture.

The paragraph below should say:

> Clinical 1 can use information across reports, scans, handwritten notes, and structured records instead of processing each source independently.

Do not write:

> More of the picture.

followed by:

> A new way to see medicine differently.

That leaves the reader with two abstractions and no information.

A useful rule:

**Headlines may be distilled. Body copy must be explicit.**

---

## 38. No drama

This is a hard rule.

Do not manufacture drama around technology, research, medicine, engineering, launches, incidents, or internal progress.

Avoid:

> And then everything changed.

> This was the moment it clicked.

> What happened next surprised us.

> Years of medicine. One model.

> The impossible, now possible.

> A new chapter begins.

> We asked a simple question.

> The answer changed how we think about medicine.

If something changed, explain what changed.

If something was surprising, explain the result.

If something matters, show why.

Do not use writing to create importance that the subject does not already have.

---

## 39. No pseudo-copywriting

Avoid language that sounds like copy without communicating anything.

Examples to remove:

> Intelligence, reimagined.

> Built for what comes next.

> Designed around you.

> Where medicine meets possibility.

> A smarter way forward.

> Clarity at every step.

> The future, made practical.

> Your work, elevated.

> Better starts here.

These lines are not automatically wrong because they are short. They are wrong when they could describe almost any company or product.

If a line could be placed on a banking app, cloud platform, fitness product, AI assistant, hospital dashboard, and laptop page without changing a word, it is probably not useful enough.

---

## 40. Avoid filler labels

Do not place labels above sections simply because the design has room for one.

Avoid:

> OUR MISSION

> OUR TECHNOLOGY

> INNOVATION

> THE FUTURE

> POWERED BY AI

> NEXT GENERATION

unless the label communicates something the heading does not.

Prefer a useful heading directly.

Instead of:

> TECHNOLOGY  
> Intelligent document understanding

Use:

> Clinical document understanding

Instead of:

> FEATURES  
> Everything you need

Use the actual feature name.

---

## 41. Sentence construction

Use complete, natural sentences.

Short sentences are welcome when they are genuinely complete and useful.

Do not manufacture rhythm through fragments.

Avoid:

> More context. More intelligence. Better medicine.

Prefer:

> Clinical 1 can use more of the patient record when answering a question.

Fragments may be acceptable for interface labels, headings, event titles, buttons, and concise product metadata.

They should not become the default style of paragraphs.

---

## 42. Punctuation

Use punctuation conventionally.

Avoid excessive exclamation marks.

Do not use punctuation to manufacture excitement.

Avoid em dashes in normal prose. Use commas, parentheses, colons, semicolons, or separate sentences instead.

Do not overuse colons in headings.

Do not add periods to short interface labels unless the design system calls for them.

---

## 43. Vocabulary

Prefer ordinary English.

Use technical language when precision requires it.

Useful words include:

- clear
- reliable
- current
- measured
- available
- tested
- observed
- improved
- reduced
- increased
- uncertain
- preliminary
- specific
- typical
- average
- approximate
- current
- experimental
- practical
- relevant

Words should describe something.

Avoid vocabulary whose main purpose is atmosphere or prestige.

---

## 44. Naming capabilities

Capability names should explain what the capability does.

Prefer:

> Report comparison

> Prescription reading

> Patient history review

> Document extraction

> Clinical search

> Review required

Avoid:

> Intelligence Engine

> Insight Layer

> Cognitive Core

> SmartFlow

> Precision AI

unless the term refers to a real named system that needs an identity.

A feature does not need a brand name simply because it exists.

---

## 45. Calls to action

Calls to action should name the next action.

Use:

> Try Clinical 1

> Read the research

> View pricing

> Upload report

> Compare reports

> Read documentation

> Contact us

Avoid:

> Learn more

when a specific destination can be named.

Avoid:

> Discover

> Explore possibilities

> Start your journey

> Experience Substrate

The action should be obvious before the person clicks.

---

## 46. Comparative claims

When comparing versions, competitors, baselines, or previous systems, state the basis of comparison.

Prefer:

> Clinical 1 extracted medication instructions correctly in 91% of prescriptions in our evaluation, compared with 78% for the previous model.

Avoid:

> Clinical 1 is far more accurate.

If the comparison is limited to a dataset, task, region, document type, or configuration, include that context.

Do not imply universal superiority from a narrow test.

---

## 47. Superlatives

Use superlatives rarely.

Words such as:

- best
- fastest
- most accurate
- safest
- strongest
- leading

require a clear comparison and evidence.

Prefer:

> This is our fastest clinical model.

only if it is true across the relevant models and measurement.

Better still:

> Clinical 1 processes our typical 100-page record about 35% faster than Clinical 0.9.

Specific comparisons are more useful than status claims.

---

## 48. When technical detail belongs first

There are contexts where technical information is the main thing the reader came for.

Examples include:

- API reference,
- model cards,
- benchmark pages,
- research papers,
- technical release notes,
- infrastructure documentation,
- developer pricing,
- safety evaluations.

In those contexts, do not hide technical information behind simplified marketing language.

The rule is not "avoid technical detail."

The rule is "put the reader's actual need first."

A developer looking for rate limits needs rate limits.

A doctor deciding whether a model can process a patient record may need a practical description first.

---

## 49. Model cards

A model card should be compact and useful.

Example:

> **Clinical 1**

> Best for: clinical document understanding, patient-record review, prescription extraction, and cross-document questions.

> Typical 100-page record: about 40 seconds.

> Typical cost: about ₹18.

> Maximum context: 200K tokens.

> Known limitations: poor scans, uncommon handwritten abbreviations, and incomplete source records.

Then provide detailed evaluation, safety, technical, and methodology sections.

Do not open with a paragraph praising the model.

---

## 50. Medical language

Medical writing should be careful without becoming sterile.

Do not use certainty that the evidence does not support.

Distinguish clearly between:

- extracted information,
- model interpretation,
- clinical finding,
- suggestion,
- uncertainty,
- diagnosis,
- recommendation.

Do not imply that a system has made a diagnosis when it has only summarised or classified information.

Do not replace clinical terminology when doing so would change meaning.

Explain unfamiliar terminology when the audience may not know it.

---

## 51. Safety language

Safety copy should tell people what matters.

Use:

> This result should be reviewed before it is used for a clinical decision.

> The model could not verify this value from the source document.

> This output is based on the uploaded records and may be incomplete if relevant information is missing.

Avoid generic safety paragraphs where a specific warning is possible.

Safety language should reduce ambiguity, not merely reduce legal exposure.

---

## 52. What Substrate should never sound like

Substrate should not sound:

- theatrical,
- cinematic,
- self-important,
- evasive,
- over-polished,
- artificially futuristic,
- aggressively technical without reason,
- motivational,
- sentimental,
- startup-generic,
- corporate for the sake of formality,
- casual for the sake of relatability,
- impressed with itself.

The reader should notice the work before the writing.

---

## 53. Common rewrites

### Marketing to useful

Avoid:

> Experience the power of advanced clinical intelligence.

Use:

> Review reports, prescriptions, and patient histories in one place.

### Vague to specific

Avoid:

> Improved performance across complex medical tasks.

Use:

> The model reads prescriptions more reliably and makes fewer extraction errors on long reports.

### Technical to human

Avoid:

> 40% lower inference cost.

Use:

> A typical workload that cost ₹100 before now costs about ₹60.

### Defensive to honest

Avoid:

> Results may occasionally vary in certain edge cases.

Use:

> Poor scans and uncommon abbreviations remain the largest sources of error.

### Corporate to direct

Avoid:

> We are currently investigating reports of degraded performance.

Use:

> Document processing is slower than usual. We are investigating the cause.

### Blaming to helpful

Avoid:

> Invalid file uploaded.

Use:

> We could not read this file. Try the original PDF or a clearer scan.

### Feature to use case

Avoid:

> Long-context reasoning.

Use:

> Ask questions across an entire patient history.

### Praise to evidence

Avoid:

> Our most advanced model yet.

Use:

> Clinical 2 handles longer records and reads handwriting more reliably than Clinical 1.

---

## 54. Final test

Before publishing, ask:

Does this tell the person what they actually need to know?

Could a useful number replace an adjective?

Are we describing the product, or advertising the idea of the product?

Are we saying something because it matters, or because the page felt empty?

Could this be shorter without losing meaning?

Are we making an uncertain claim sound certain?

Are we hiding a relevant limitation?

Are we exposing technical detail that the reader does not need yet?

Would a human-scale example explain this better?

Does the interface describe what is actually happening?

Does the call to action say what happens next?

Could this sentence belong to almost any technology company?

Is there any drama that the facts themselves do not justify?

If the copy disappears and the product becomes harder to understand, keep it.

If the copy disappears and nothing is lost, remove it.
