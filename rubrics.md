**R E F E R E N C E G U I D E  ·  H O N E Y B E E P R O M P T A N D R U B R I C S** 

# **Writing Rubrics** 

How to turn "was this any good?" into something two people can answer the same way — and how that applies on this project specifically. The examples throughout are real criteria from submitted work, quoted as written. 

#### **CONTENTS** 

1. What a rubric is 

2. Where the rubric sits in the pipeline 

3. What the rubric measures here 

4. The form every criterion takes 

5. Weights 

6. Work the task before you write 

7. Everything real, nothing invented 

8. What actually goes wrong 

9. Reading the list as a set 

10. A worked example 

11. Difficulty calibration 

12. The pass to run before you submit 

##### **HOW TO USE THIS GUIDE** 

Sections 1 and 4 are the craft — they are true of any rubric anywhere. Everything else is specific to Honeybee: the categories, the weight scale, the difficulty gate and the failures that actually show up in submitted work. The operational steps and field definitions live in **Honeybee Prompt and Rubrics**; this document is the reasoning behind them. 

## **1. What a rubric is** 

A rubric is **a list of checkable facts.** Not a scoring guide, not a set of guidelines, and not a description of what good looks like. It is a list of specific statements about a piece of work, each of which is either true or false when you look at it. 

You write the list **_before_** you see the work. Then applying it becomes bookkeeping rather than judgement: you go down the list, mark each item true or false, and the total tells you how the work did. 

**CRITERION** 

The report includes a section titled "Risks". 

True or false, and everyone who looks will agree. 

###### **NOT ONE** 

The report should be well structured and easy to follow. 

This is a hope. Two readers will not mark it the same way. 

The shift is from **_describing quality_** to **_listing evidence_**. Everything else in this document follows from that one move. 

### **Why bother** 

Ask five people whether a document is good and you get five answers, all defensible. That is fine for an opinion and useless for a measurement. If the same work can score well or badly depending on who happens to look at it, the score is telling you about the reader. 

|**What a rubric buys**|**Meaning**|
|---|---|
|**Repeatability**|The same work gets the same result from anyone who applies the list.|
|**Comparability**|Two pieces of work can be scored against one fixed standard, so comparing them means<br>something. On this project that **_is_** the product.|
|**A record**|When someone disagrees, you can point at the criterion they disagree with instead of<br>arguing about taste.|
|**Speed**|Checking facts is much faster than forming an opinion.|



This is why the wording matters so much. **A criterion that two people read differently reintroduces exactly the problem the rubric exists to remove.** 

### **Binary, never scaled** 

Criteria are binary. The work either meets the criterion or it does not. There is no partial credit on a single line and no five-point scale inside it. The moment a criterion admits "sort of", you are back to asking for a judgement, and two people will land in different places. 

###### **SCALED** 

Rate the clarity of the summary from 1 to 5. 

Every reader picks a different number, and none of them is wrong. 

###### **BINARY** 

The summary is 200 words or fewer. 

One reader, one answer. Count the words. 

###### **BINARY** 

The summary states the recommendation in its first sentence. 

Also one answer. Read the first sentence. 

If you find yourself wanting a scale, you usually have two or three separate binary criteria hiding inside one line. Split them out. 

## **2. Where the rubric sits in the pipeline** 

The work splits across two queues performed by two different people, and this is the single most important fact about how you write. 

|**Stage**|**What happens**|
|---|---|
|**Honeybee Prompt and Rubrics**<br>You are here|You define the intent and an opening prompt, work the task live across several turns on more than one model, fix the target outcome, and write the rubric against it. Your rubric is then independently reviewed.|
|**Honeybee SxS**<br>Someone else|A different contributor reviews the intent, runs each product for 20+ turns, rates the dimensions, scores your rubric against every run, and records a preference.|



##### **THE PERSON APPLYING YOUR RUBRIC HAS NEVER SEEN YOUR REASONING** 

They were not there when you worked the task. They are reading your criteria for the first time, after the conversations are already finished. **A criterion cannot lean on anything that stayed in your head.** If you cannot say where a number came from, neither can they. 

## **3. What the rubric measures here** 

Eight dimensions are assessed per product in the SxS queue. **Only the first is captured by rubric criteria.** The other seven are captured as ratings with written justifications, and you do not write criteria for them. 

|**Dimension**|**How it is captured**|
|---|---|
|**1. Outcome quality**|**Your rubric criteria**, plus a 1–5 rating downstream|
|2. Communication quality|1–5 rating with justification|
|3. Trust and grounding|1–5 rating with justification|
|4. Tool and connector reliability|1–5 rating with justification|
|5. Interaction efficiency|1–5 rating with justification|
|6. Memory and personalization|1–5 rating with justification|
|7. Collaboration quality|1–5 rating with justification|
|8. Safety|**Yes / No** — whether a safety concern occurred|



##### **WHY THE SPLIT EXISTS** 

It is worth understanding rather than memorising. Rubric criteria have to give the same answer on every run. Anything driven by the **_path_** a conversation happened to take — how the model recovered from an error, whether it took initiative, what tone it struck, how many turns it needed — varies from run to run, so a binary criterion about it would be measuring luck. 

**The practical rule: if it is about the state of the delivered work, it belongs in the rubric. If it is about how the model got there, it belongs in a dimension rating.** Error recovery, proactivity and tone are the named examples of what to keep out. 

Three specific forms this takes, all rejected on sight: **the model's reasoning process** ("considers the alternatives before answering"), **the number of turns** ("completes the task within five turns"), and **conversational style** ("maintains a professional tone throughout"). Grade what the model produced, never how it got there. 

### **The six things Outcome quality can be about** 

Every criterion you write sits under one of these six, and you tag it with the one that fits. Use the list as a coverage prompt too: **a rubric that only ever touches one or two of them is probably missing something the task asked for.** 

|**Code**|**Category**|**What it covers**|
|---|---|---|
|**1.1**|**Instruction Following**|Constraints and specifications stated in the prompt are honored, including ones<br>introduced mid-conversation.|
|**1.2**|**Task Completion**|The required state change happened in the environment: email sent, event<br>created, file shared.|
|**1.3**|**Artifact Delivery**|A usable artifact was actually produced, rather than described.|
|**1.4**|**Artifact / Task**<br>**Correctness**|The result is right and well made: logic sound, computations correct, artifact<br>functional.|
|**1.5**|**Artifact Quality**|Visual elements complete and well executed: resolution, legible diagrams and<br>charts, navigable interface, no generation defects.|
|**1.6**|**Visual Appeal**|Tasteful and appealing, adds value for the persona — something they would<br>download or share.|



##### **TWO THAT ARE EASY TO CONFUSE** 

**1.3 Artifact Delivery** is about whether the file exists **_at all_**. **1.5 Artifact Quality** is about how a produced file **_looks_** — distorted images, unreadable charts. Those are different questions, and a file can pass one while failing the other. 

## **4. The form every criterion takes** 

Between **10 and 30 criteria**, every one binary and carrying a weight. Beyond that, five properties are required — and two of them are about wording rather than substance, which is why they get overlooked. 

|**Property**|**What it means here**|**The test you apply**|
|---|---|---|
|**Binary**|Met or not met against the produced<br>output and the transcript. No partial credit<br>inside a line.|Could work satisfy half of it?|
|**Observable**|Checkable from the delivered artifact or<br>action, or from the transcript. Never from<br>the model's reasoning.|Can you point at something that settles<br>it?|
|**Product-independent**|Phrased so it applies to any product's<br>output. No wording that only makes<br>sense for one of them.|Would this read strangely against a<br>different product?|
|**Atomic**|One requirement per criterion.|Does it need an "and" to hold together?|
|**Positive-only**|Written as a must-have that is present,<br>not as the absence of something.|Is it easier to read backwards than<br>forwards?|



Write in **simple present tense, starting with a verb about the work** — **_States… Includes… Reports… Provides… Leaves…_**. That phrasing is not decoration. It forces the observable form, keeps criteria comparable at a glance, and makes bundling obvious, because a bundled criterion needs an "and" to hold it together. 

**GOOD** 

Reports the owner's net distribution as $7,626.60. 

###### **GOOD** 

Leaves the reply to Jordan Lee as an unsent draft. 

###### **BAD** 

The response must calculate the net distribution. 

Not observable as written, and no value to compare against. 

###### **BAD** 

The model should reason carefully about the recipients. 

Judges process rather than output. This belongs nowhere in a rubric. 

### **If the outcome is a file, check the file** 

When the target outcome includes an artifact, the criterion has to verify that the artifact **exists and is functional** — not that the model mentioned it, described it, or explained how to build it. 

###### **BAD** 

Explains how to structure the reconciliation spreadsheet. 

Passes when the model hands back instructions instead of a file. 

###### **GOOD** 

Provides a spreadsheet file with one row per exhibit and the four unmatched items flagged. 

Only an actual working file can satisfy this. 

##### **THIS MAPS TO A KNOWN LOSS PATTERN** 

A model returning step-by-step instructions for building the deliverable instead of generating it — explaining how to construct the spreadsheet rather than producing the spreadsheet — is a specific, tracked failure mode. **A rubric that accepts a description in place of an artifact scores that failure as a pass**, and the comparison loses the very thing it was built to detect. 

## **5. Weights** 

Criteria are binary, but they are not equal. Missing the headline number in a financial summary is not the same kind of failure as leaving a heading in the wrong font. 

The scale is **1 to 3**. It is short on purpose: with only three levels each one has to mean something distinct, and there is nowhere to hide an undecided criterion. 

**Weight by importance to what the run is actually for.** On a seeded (Type 1) item that is the pre-filled **user goal**; on an item you built from scratch (Type 2) there is no user goal field, so it is the target deliverables you wrote. Everything below reads off whichever one your task has. 

|**Weight**|**Name**|**Definition**|
|---|---|---|
|**3**|**Essential**|Core to task fulfilment. Failure here means the user's goal is not completed.|
|**2**|**Important**|A key quality that strongly contributes to task success. The difference between a<br>work-ready, immediately shareable output and one that needs another iteration.|
|**1**|**Minor positive**|A nice-to-have that showcases craft and user delight. The task is still fulfilled and the<br>output still usable without it.|



**Weight 2 carries most of the real signal, so read its definition closely.** It is not "somewhat important". It is the line between an output the persona could send as-is and one they would have to go back and fix. That is a sharp, checkable distinction, and it is the question to ask of every criterion you are tempted to mark 2 or 3. 

**TWO CHECKS ON YOUR WEIGHTING** 

- **The 3 test.** If the work failed this one criterion and everything else passed, would the user's goal be incomplete? If they would still have what they needed, it is not a 3. 

- **The sorted read.** Sort your criteria by weight and read them as a ranked list. If a 1 is obviously more important to this persona than a 2, one of the two is wrong. 

Weight from **how the prompt treats the requirement**, not from what interests you. Something stated explicitly, repeated or emphasised earns a higher weight; something mentioned once in passing does not; and anything the user later withdrew should carry no weight at all. 

**Weight inflation is the common failure.** If most of the list carries the top weight, the weights have stopped distinguishing anything and the total no longer means what it should. 

## **6. Work the task before you write a single criterion** 

The order is fixed, and it is the part of the process most often skipped. **You cannot write a rubric against an imagined result.** 

###### **First** 

**Define the intent and the opening prompt** 

The concrete deliverable a real user would pay for, and the message they would open with. 

###### **Then** 

**Run the task live, across several turns, on more than one model** 

Experiment with the prompt and the responses. You are looking for how the task actually behaves and what a strong final result looks like. 

###### **Then** 

**Fix the target outcome** 

The reference final state a successful result has to reach — a generated artifact, or a final output such as an email draft. **This becomes the anchor for everything scored.** 

###### **Only then** 

**Write the criteria against that target outcome** 

The target outcome is what makes criteria checkable. **_"Reports the net distribution as $7,626.60"_** is only writable because you worked the task and know the number. Skip the live pass and you end up writing **_"calculates the correct net distribution"_**, which nobody downstream can apply. 

##### **TRACEABILITY** 

Every specific value, filename, recipient and date in your rubric should be traceable to the target outcome and GTFA you fixed — and the GTFA itself is written on **both** task types, so this chain holds on Traffic tasks too. **If you cannot say where a number came from, neither can the person scoring it.** 

## **7. Everything real, nothing invented, nothing uploaded** 

The underlying rule is the same on every task: **every specific value in a criterion must be traceable to something on the task, never to something you assumed.** What you trace it **_to_** depends on which kind of task you are on. 

### **Where the values come from** 

**On an Aspirational (Type 2) task, and on every Honeybee SxS task**, they come from the universe. Tasks run against a pre-populated environment for a fictional persona, staged in the same connected accounts a real subscriber uses: Gmail, Calendar, Drive and GitHub. **The environment is real, not mocked.** 

- **Every entity you name must exist in the universe.** Files, people, dates, events. A criterion referencing something that is not in the environment cannot be scored. 

- **Never upload or mock an input file.** Everything the model needs is already staged. If a criterion depends on a document, that document lives in the persona's Drive, not in an attachment you added. 

- **Explore before you write.** Read the environment context and go through Calendar, Gmail and Drive so you know which people, events, files and emails are actually available to reference. 

This is also what keeps a task specific to its persona rather than a generic ask anyone could have written. **A rubric grounded in real staged data is automatically harder to satisfy by accident.** Setup and reset details are in **Account Hydration**. 

**ON A TRAFFIC (TYPE 1) TASK THERE IS NO UNIVERSE — AND NO INPUT ARTIFACTS EITHER** 

Traffic tasks in Prompt and Rubrics have **no assigned universe, no persona, no hydration and no input artifacts**, so none of the exploration above applies and there is nothing to open or verify. 

Instead, the ground truth is exactly three things: **the opening prompt, the user goal and the target deliverables.** Every exact value in a criterion must already appear in one of those three, because there is nowhere else on the task to get a number, a name or a date from. **The failure mode to watch for is a plausible-sounding figure the contributor inferred** — a grader holding only the prompt cannot confirm it, so the criterion is not self-contained and cannot stand. 

## **8. What actually goes wrong** 

Across **297 criteria** that reviewers found to have a problem, the distribution is lopsided. Every example in this section is a real criterion from submitted work, quoted as written. 

|Problem|Count · Share|
|---|---|
|Unjudgeable wording|90 · 30%|
|Punishes right answers|77 · 26%|
|Missing information|44 · 15%|
|Nobody asked for it|36 · 12%|
|States something untrue|35 · 12%|
|Duplicates another|12 · 4%|
|Bundles two things|3 · 1%|

##### **WHERE TO SPEND YOUR REVIEW TIME** 

The shape of that chart is the whole argument. **Bundling and duplication are what people look for when they proofread a rubric, and together they are 5% of the problem.** The two at the top cost the actual work, and both are caught by asking a single question of each line. 

### **Criteria that punish the right answer** 26% · most expensive 

The criterion rewards something the conversation ruled out, or invents a constraint the user never set. **A flawless response fails it.** This is the most expensive shape because it inverts the measurement: the better the work, the worse it scores. 

###### **REAL** 

Provides the file already in the first turn. 

At turn 3 the user said to produce the document only on request. This rewards the opposite of what they asked for, and penalises a model that correctly waited. 

###### **REAL** 

The 3rd floor in the final PDF has 3 bedrooms. 

The user asked for four bedrooms in total and never said how to distribute them. Any valid 2+2 layout fails. 

###### **REAL** 

Asks about colour requirement for epigenetic marks. 

Turn 1 already specified "small colored dots". Asking again is redundant, so this rewards a model for not reading the prompt. 

###### **REAL** 

Reports the name "Cassandra" as the user's name. 

That name appears nowhere in the conversation. The only way to pass is to invent it, so the criterion pays for a hallucination and fails the honest answer. 

That last one is worth sitting with. It is a criterion **_about grounding_** that can only be satisfied by making something up. Criteria written to catch bad behaviour are unusually prone to this, because demanding a specific fact the conversation never established leaves invention as the only route to a pass. 

##### **THE TEST** 

Would a perfect, honest response pass this criterion? **If a correct answer could fail it, the criterion is wrong, not the answer.** 

### **Wording two people cannot apply the same way** 30% · most common 

The criterion turns on a word that carries no observable feature, so the result depends on who is scoring. 

###### **REAL** 

Maintains a reassuring tone in the note. 

Tone has no threshold, and this note also has to deliver bad news. Two readers resolve it differently. 

###### **REAL** 

The report includes few UI screenshots. 

"Few" is not a number, and it is unclear what counts as a screenshot in a text response. 

###### **REAL** 

Ensures End-to-end execution across the tools. 

Which tools, and what counts as end to end? The prompt names none. 

###### **REAL** 

Provides a downloadable file named SKILL.md. 

"Downloadable" is undefined where the model can write to disk. One reader wants a file on disk, another accepts a code block. 

**The fix is always the same move: replace the adjective with the observable feature.** "Reassuring tone" becomes the specific sentence the note has to contain. "Few screenshots" becomes a count. 

But do not over-correct. Informal wording is not the problem, and a criterion that points back at the prompt's own structure is fine — as long as rereading the prompt settles it the same way for anyone. 

##### **THE TEST** 

Would two people, reading only the prompt and this criterion, reach the same verdict on borderline work? If not, **name the feature instead of the quality.** 

### **Criteria that need information nobody has** 15% 

The wording is perfectly precise. The problem is that deciding it requires a fact the task never supplied, so the person scoring would have to go and research it. 

###### **REAL** 

Includes all the 19 TanStack features in the document. 

Nothing in the criterion or the conversation names the 19 features. Which ones count is unknowable. 

###### **REAL** 

Verifies that no ambiguous wording remains after the change. 

"The change" is one of a dozen revisions across the conversation. Which one? 

###### **REAL** 

The response identifies gVisor's license as [[GVISOR_LICENSE]]. 

An unfilled placeholder shipped into the rubric. **Search your criteria for double brackets before you submit.** 

The canonical trio makes the boundary clear: 

- **_"Reports the tax return as $1,000"_** — **fine**, because the value is in the criterion. 

- **_"Includes the tax return"_** — **fine**, because it only checks coverage. 

- **_"Calculates the correct tax return"_** — **not fine**, because the reader does not know the correct figure. 

Before flagging your own work here, reread the whole prompt. **If the fact is stated anywhere in the turns or in the target outcome, the criterion is fine.** Reserve this for facts genuinely absent everywhere. 

### **And four smaller ones** 

Less common, and mostly caught by a single mechanical pass over the finished list. 

###### **UNTRUE · 12%** 

The delivered document contains at least 20,000 words. 

The user asked for **_over_** 20,000. "At least" admits exactly 20,000, so the criterion is looser than the ask. 

###### **UNTRUE · 12%** 

Includes the heading "Lighting Approach" in "brihgt_hollow_historical_illustration_style_spec.pdf". 

Transposed letters in the filename. Applied literally, nothing can pass. **Paste filenames and numbers rather than retyping them**, and check the direction of every threshold against the turn that set it. 

###### **UNASKED · 12%** 

Provides the delivered image saved in the user's Google Drive. 

Across 21 turns the user only ever discussed the visual design of the infographic. Drive was never mentioned. 

###### **DUPLICATE · 4%** 

Places the open chromatin section on the left side of the diagram. 

Another criterion already required open chromatin on the left. Whenever that one passes, this one does too, so one requirement quietly carries double weight. 

###### **BUNDLED · 1%** 

Recommends 8,000–10,000 steps daily with measuring waist circumference every 2 weeks. 

A step count and a measurement schedule are unrelated. Work can satisfy one and miss the other. 

Bundling is rare and easy to over-correct for. **Several details sharing one focus is still atomic**, and splitting a single requirement into fragments manufactures duplicates instead. Aim for one requirement per line, not one clause per line. 

## **9. Reading the list as a set** 

Some faults only exist **_between_** criteria, so a line-by-line review will never find them. When the draft is done, read the whole list in one pass looking for three things. 

|**Fault**|**How to find it**|
|---|---|
|**Contradiction**<br>**fatal**|Two criteria that cannot both be satisfied — one requires an action, another forbids it. Every<br>piece of work then fails at least one of them no matter what it does.|
|**Duplication**|Sort by topic and read adjacent pairs. Ask whether passing the first **_forces_** passing the second.<br>If it does, merge them. A subset relationship is fine: "mentions X and Y" and "does not mention<br>X" are different checks.|
|**Gaps**|Walk the original request and list everything it asked for. Tick each one against the criterion that<br>covers it. **Anything unticked is a hole**, and a missing criterion costs you exactly what a wrong<br>one does.|



##### **DO THE GAP CHECK IN THE RIGHT DIRECTION** 

Work down the **_request_**, not down your criteria. **Reading your own rubric will only ever confirm what you already thought of.** 

## **10. A worked example** 

**The request:** "Pull our Q3 numbers together into something I can send the board on Monday. Keep it short, and flag anything that looks off." 

**First attempt — none of these work** 

**BAD** 

The memo is board-ready. 

Not observable. This is the whole judgement restated as a criterion. 

**BAD** 

The memo is short and well written. 

Bundled, and neither half is checkable. How short, and by whose reading? 

**BAD** 

The response correctly identifies the Q3 anomalies. 

Needs information nobody has. A reader cannot tell which anomalies are the correct ones. 

**Second attempt — same request, checkable** 

###### **GOOD** 

Provides a document of 500 words or fewer. 

"Short" became a number. Count it. 

###### **GOOD** 

Reports Q3 revenue as $4.18M. 

The value is stated in the criterion, so the reader compares rather than researches. 

###### **GOOD** 

States that the September figure is provisional. 

The specific thing that looked off, named. 

###### **GOOD** 

Includes sections titled "Summary", "Q3 performance", and "Risks". 

One focus — structure — so it stays atomic despite naming three headings. 

###### **GOOD** 

Attaches the document as a file rather than pasting it into the reply. 

"Something I can send" made concrete. 

Notice what happened to the vague words. **_Short_** became a word count. **_Anything that looks off_** became the one specific thing that was off. **_Board-ready_** dissolved into structure, length and format. **None of the meaning was lost, and now the list can be applied by anyone.** 

## **11. Difficulty calibration** 

Difficulty is set at authoring, and it is measured by **how much of your own rubric a model satisfies on the simplified run** — the 1–3 turn pass where you dump every deliverable at once and give the model the easiest possible path. That share is the calibration signal. 

##### **THE GATE: AT MOST 40% OF THE AVAILABLE WEIGHT** 

If the simplified run passes more than **40%**, the item is too easy and needs hardening before it goes any further. A high share means the item cannot separate the products, which is the only thing it exists to do. 

**The number is weighted, not a count of criteria.** A real item had 30 criteria whose weights summed to 61; the simplified run passed criteria worth 19, and the viewer reported 31%. Failing a few **3** criteria moves the number far more than failing the same number of **1** criteria. 

Harden by adding constraints, edge cases, cross-referencing, tighter values and formatting, and coordination across more than one artifact. The set is deliberately weighted toward medium and hard, so it has room to separate products instead of everything topping out at the ceiling. 

##### **HARD FOR THE RIGHT REASONS** 

**Difficulty should come from grounding, judgement, connector discipline and multi-step coordination.** Not from trickery, obscurity, or simply piling on volume. A rubric that is hard because it is unfair fails the perfect-response test on every line. 

**And fix the item, not the measurement.** Deleting or weakening criteria to push the number down produces a thin rubric that fails review later. The gate is a signal about your prompt and deliverables, not about your rubric. 

## **12. The pass to run before you submit** 

Rubric creation is independently reviewed, so this is what you run first. Work down the list once, in order. 

### **Line by line** 

- Would a perfect, honest response pass this? (punishes right answers) 

- Would two people reading only the prompt and this line agree on borderline work? (unjudgeable wording) 

- Can it be decided from the prompt, the environment and the delivered work alone? (missing information) 

- Is it about the delivered state rather than how the model got there? (belongs in a rating instead) 

- Does it name only entities that exist in the universe? (ungrounded) 

- One requirement, present tense, positive, product-neutral? (form) 

### **Once, over the whole list** 

- Search the text for `[[` and confirm no placeholder survived. 

- Paste-check every filename, value and threshold against the target outcome — **including the direction of each inequality.** 

- Read it as a set: does any pair contradict, and does any pair always pass together? 

- Walk the prompt's asks and tick each against the criterion covering it. 

- Count: between **10 and 30** criteria, every weight 1, 2 or 3. 

- Sorted by weight, does the order match what matters to this persona? 

- Estimate what the simplified run would pass. **Above 40% and the item goes back for hardening.** 

##### **THE ONE QUESTION, ASKED OF EVERY LINE** 

Could a stranger, holding only the original request and the delivered work, mark this true or false and get the same answer I would? 

The rubric leaves your hands and gets applied by someone who never saw your reasoning. **Everything it needs has to be on the page.** That is the whole craft; the rest is practice. 

