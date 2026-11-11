**Q U E U E 2 O F 2 · E V A L U AT I O N P H A S E** 

# **Honeybee SxS** 

The evaluation item is already built. You run it as a full 20+ turn conversation, grade the run against the existing rubric, rate it on the eight dimensions, and record a side-by-side preference. Every task in this queue follows the same workflow — only the model and the task type change. 

**<u>Clarifications log</u>** · answers to questions raised since publication, newest first. 

##### **CONTENTS** 

1. How this queue works
2. Which task do you have?
3. Before you start
4. Model reference
5. What you receive vs. what you produce
6. Setup steps
7. Running the trajectory
8. Sharing links correctly
9. Turn & prompt collection
10. Trajectory capture

**COMPANION DOCUMENTS** 

11. Final trajectory & outputs
12. Grading against the rubric
13. Turn annotation
14. The eight dimension ratings
15. The SxS preference
16. Close & submission checklist
17. Edge cases
18. Glossary

Three reference guides go with this one: **Account Hydration** (setting up and resetting your synthetic account — read it before your first task), **Writing Rubrics** (useful background on how the rubric you are grading against was built), and **Gemini vs. Gemini Spark** ( **read this one before you start a Spark task** — the capture workflow is different). 

## **Clarifications log** 

Answers to questions contributors have raised since this document was published, **newest first**. Every one of them is also folded into the section it belongs to — this log exists so you can see what has changed without rereading the whole document. 

|**Date**|**Question raised**|**Clarification**|**Now covered in**|
|---|---|---|---|
|2026-<br>09-15|My task lists **_two_** sets<br>of demo credentials,<br>and both models are<br>named Gemini 3.5 Flash Lite. Is that a mistake?|**No — that is correct, and you must use both.**<br>On this batch each model has **its own demo**<br>**account**, because the two accounts point at<br>**different backend endpoints**. Sign in with the<br>Model A account to run Model A, then sign in<br>with the Model B account to run Model B. **The**<br>**version string is expected to read the same**<br>**on both sides** — the endpoint behind the<br>account is what differs, so do not report it and<br>do not try to find a "3.6" in the selector. **Turn on**<br>**Extended thinking for both models.**|4. Model reference ·<br>6. Setup steps|
|2026-<br>09-15|How should I refer to<br>the models in my<br>justifications and<br>comparison summary?|**Always as "Model A" and "Model B" — never**<br>**by product or version name.** The internal<br>labels A, B, C and D exist to separate models<br>across review layers, but the customer sees a<br>delivery sheet with **one row per SxS pair and**<br>**only two columns, A and B.** A summary that<br>says "Gemini 3.5 was better" or "Model C<br>fabricated the names" is unreadable at that<br>point. Write "Model A" and "Model B"<br>everywhere you name a side.|15. The SxS<br>preference · 14.<br>Dimension ratings|
|2026-<br>09-15|[Aspirational] The<br>Input File Paths look<br>wrong,<br>and the upload links<br>are one enormous<br>link. How do I use<br>them?|**Known issue, with a workaround.** The paths<br>may be inaccurate, and the upload links are<br>rendered as **one compound link** rather than<br>one link per file. Copy the whole Input File<br>Upload Links block, split it, and take one URL at<br>a time; download that file; find the same file in<br>the workspace by name; **fill in the correct path**<br>**yourself** in<br>folder/folder/file form; upload the copy you found<br>in the workspace. Repeat per file. **Correct the**<br>**paths rather than reporting the task.**|5. What you receive|
|2026-<br>09-15|What is Gemini<br>Spark, and how do I<br>capture a Spark<br>trajectory when<br>there is no share link?|**A new pairing: standard Gemini vs. Gemini**<br>**Spark.** Spark is Google's agent mode inside the<br>Gemini app — reach it from the sidebar with<br>**Switch to Spark**. **This batch lists only one set**<br>**of demo credentials, used for both sides**<br>(unlike the two-account batch above) — the two<br>sides are two modes of the same signed-in app,<br>so check which mode you are in before Turn 1 of<br>each run. **Spark has no share link and no**<br>**usable print-to PDF**, so the trajectory is<br>captured by saving the page: right-click → **Save**<br>**As…** → Format **Webpage, Single File**, named<br>[CB ID]_[TASK ID]_SPARK, then uploaded to the<br>task. **Use Chrome.** Full workflow: **Gemini vs.**<br>**Gemini Spark**.|4. Model reference ·<br>8. Sharing links|
|2026-<br>09-08|There is a new step<br>after each model's<br>turns, asking for a<br>URL. What is it and<br>what do I do with it?|**New step, and it is required.** After the turn &<br>prompt collection for each model, the task now<br>carries an **Agent Execution** step. Paste that<br>model's **public share link** at the URL> prompt<br>and press Enter. The conversation then renders<br>on the Agent Execution step. **This repeats for**<br>**every model you run**, and it exists so linters<br>and in-task evals can read the trajectory directly.|10. Trajectory capture|
|2026-<br>09-08|Are the eval<br>commands coming back?|**Possibly not.** The plan is to move that QC<br>coverage to **in-task endpoint evals** — checks<br>that run against the captured trajectory rather<br>than commands you run by hand. **The eval**<br>**documentation stays published** in case the<br>commands return. Practically: **if the commands**<br>**are on your task, run them; if they are not,**<br>**complete and submit the task without them.**<br>Either way, the new trajectory capture step is<br>separate and is always required.|10. Trajectory<br>capture|
|2026-<br>09-06|I got a message<br>asking me to improve<br>another contributor's<br>work. Is my task being<br>reviewed?|**There are no reviews on this project at the**<br>**moment.** The **_"Improve another_**<br>**_contributor's…"_** message is automatic —<br>**please ignore it.** What matters instead: **when**<br>**you submit a task it moves forward with your**<br>**name on it.** Anything already in the task when<br>you open it — a pre-filled trajectory, a grading,<br>an SxS comparison — becomes your<br>submission, so it is your<br>responsibility to check that it meets the<br>project's expectations before you send it on.|1. How this queue<br>works · 17. Close &<br>checklist|
|2026-<br>09-06|My task arrived with a<br>trajectory already filled<br>in. Do I have to use it<br>as-is?|**No — that call is yours.** Check the pre-filled<br>trajectory first. If it is sound, keep it. **If it is not**<br>**usable, run the trajectory again, or build it**<br>**from scratch.** This supersedes the earlier<br>"never touch an existing trajectory" instruction:<br>since the task submits under your name, you are<br>accountable for the quality of the pre-filled work,<br>not just your own. Reuse remains the default<br>because it keeps baselines comparable —<br>replace it when it genuinely falls short, not as a<br>matter of routine.|1. How this queue<br>works · 5. What you<br>receive · 17. Edge<br>cases|
|2026-<br>09-06|The rubric on my task<br>has typos and<br>grammatical errors.<br>Can I fix them?|**Yes.** If more than 50% of criteria are wrong,<br>report the task in the War Room; otherwise, fix<br>them (deletes allowed).|5. What you<br>receive · 12.<br>Grading|
|2026-<br>09-06|The demo account is<br>asking for 2-Step<br>Verification and I<br>cannot get in.|**Known blocker.** It appears to happen when<br>an earlier contributor turned on 2-Step<br>Verification during their session and then let<br>the task expire, leaving the account in that<br>state. **Do not try to**<br>**work around it** and do not substitute an<br>account of your own. Either **join the War Room**<br>**session**, where a working account can be<br>provided for your task, or **skip the task.**|3. Before you start ·<br>6. Setup steps|
|2026-<br>09-05|My task has no Input<br>Artifacts. How should<br>that be handled?|**Input artifacts are Aspirational-only.** The<br>**_Input Artifacts — File Paths_** and **_File Upload_**<br>fields have been made conditional on task type<br>and existing tasks have been backfilled, so they<br>should no longer appear at all on a Traffic task. **If**<br>**they still appear on a Traffic task, skip the**<br>**task and report it** so it can be backfilled. Do not<br>invent a path and do not upload a file to clear the<br>block.|2. Which task · 5.<br>What you receive|
|2026-<br>09-05|If I have to run both<br>trajectories, which<br>universe do I hydrate<br>the accounts from<br>when the task names<br>no universe? Should<br>Traffic tasks have a<br>universe at all?|**No. Traffic tasks have no universe, and none**<br>**is expected.** A Traffic prompt is **standalone**: it<br>asks for general information or for something<br>that does not depend on a specific file, mailbox<br>or calendar. There is nothing to hydrate from<br>and nothing to<br>reset, so both runs start from a clean product<br>with no connected data. **If a Traffic prompt**<br>**asks for information out of a specific**<br>**universe — a named file, a named thread, a**<br>**named event — report the task and skip it.**<br>Never substitute a universe of your own<br>choosing.|2. Which task · 3.<br>Before you start · 7.<br>Running the trajectory|
|2026-<br>09-05|The GTFA or the<br>target outcomes on<br>my task<br>look low quality. Can I<br>improve them or do I<br>leave them as they are?|**Leave the opening prompt and the target**<br>**deliverables exactly as they are** — on Traffic<br>tasks that content comes from the customer,<br>and it is not yours to rewrite. **You must write**<br>**the GTFA after thoroughly reading**<br>**and understanding the Target Outcome**<br>**Deliverables and Rubric.**|3. Before you start ·<br>5. What you receive|
|2026-<br>09-05|There is no prefilled<br>Known / Not Known<br>information on my task.<br>Is that expected?|**On a Traffic task, yes — Known / Not Known**<br>**is Aspirational-only** and its absence is correct.<br>Its presence or absence is a signal about<br>whether the task was built with the right type: **if**<br>**a Traffic task does show Known / Not Known,**<br>**report it and skip it**, and if an Aspirational task<br>is missing it, report that too. On Traffic you steer<br>using the opening prompt, the user goal and the<br>target deliverables alone.|2. Which task · 5.<br>What you receive|
|2026-<br>09-05|The model only gave<br>me one share link for<br>the<br>whole conversation,<br>but every turn asks for<br>a Turn Link. What do I<br>paste?|The task collects links in two places: a **Turn**<br>**Link on every turn entry** and one **final**<br>**trajectory link** for the conversation. Where the<br>product issues a<br>genuine per-turn link, capture each turn's own<br>link as the turn finishes. **Where the product**<br>**only issues a single conversation-level link,**<br>**paste that same link into every turn's Turn**<br>**Link field** and into the final trajectory link. The<br>Turn Link field is required on every model,<br>including GPT and Claude — leaving it blank<br>blocks submission.|8. Sharing links · 9.<br>Turn & prompt<br>collection|
|2026-<br>09-05|My task has no eval<br>sandbox steps. Have<br>they been removed?|**Not deliberately — this is a known taxonomy**<br>**issue and the team is working on it.** The QC<br>checks are missing from some tasks currently in<br>the queue, and those tasks will be backfilled<br>once it is fixed. **Continue and complete the**<br>**task without them.** The QC pass is a self<br>check, not a source of task content, so nothing in<br>your submission depends on it. The commands<br>are **_not_** universe-dependent, so their absence is<br>not a Traffic-versus-Aspirational difference.|10. Trajectory capture|
|2026-<br>09-05|Do I sign into GPT or<br>Claude with the demo<br>Google credentials?|**No.** The demo Google account is for signing<br>into **Gemini** only. **GPT and Claude run on the**<br>**project subscription account**, and on an<br>Aspirational task you then connect the demo<br>account's Gmail, Drive and Calendar to them<br>from **_inside_** the product, using its own<br>connectors. The<br>subscription account is hydrated with the same<br>task universe as the Gemini demo account, so<br>both sides of the comparison see the same<br>emails, files and events.|4. Model reference ·<br>6. Setup steps|



## **1. How this queue works** 

Every task in this queue is **one evaluation item** compared across **two models**. One side is always the **base model, Gemini**. The other side is a **comparison model** that changes from task to task. 

Tasks come in a sequence built on the same item. The base model's work is done once and then reused: 

|**Task**|**Pairing**|**You generate**|**You reuse**|
|---|---|---|---|
|**Task 1**<br>**Base**<br>**task**|Gemini vs. Model X|**Both sides.** Full<br>trajectory, grading,<br>annotation and<br>ratings for Gemini **_and_**<br>for Model X.|Nothing. This is the first<br>run of the item.|
|**Task 2**<br>**Follow**<br>**on**|Gemini vs. a new Model X|**The new model only.**<br>Full trajectory, grading,<br>annotation and ratings for<br>the new comparison<br>model.|Gemini's trajectory,<br>grades, ratings and links<br>from Task 1 — after<br>checking they hold up.|
|**Task 3+**<br>**Follow**<br>**on**|Gemini vs. another new Model X|**The new model only.**|The same Gemini data<br>from Task 1.|



**PRE-FILLED WORK SUBMITS UNDER** **_YOUR_ NAME — SO CHECK IT** 

On a follow-on task the Gemini side arrives already filled in: its trajectory, turn entries, links, grades and ratings. **When you submit, the whole task moves forward with your name on it**, including that pre filled work. You are therefore accountable for its quality, not only for the model you ran yourself. 

**Read the pre-filled trajectory before you rely on it.** Then decide: 

**It holds up** — keep it, grade it, rate it, and run only the comparison model. This is the normal case. 

**It does not** — the links are dead, the turns are thin or padded, the run never approaches the deliverables. **You may re-run that trajectory, or build it from scratch.** 

Reuse is still the default, and re-running is not a routine step to take because a run is merely imperfect. But a pre-filled trajectory you would not have submitted yourself is not one to pass along unchanged. 

###### **WHY THE BASE MODEL IS REUSED BY DEFAULT** 

Every comparison model is measured against **_the same_** Gemini run on **_the same_** item. If Gemini were re run on every task as a matter of course, each pair would be scored against a different baseline and the preferences would be harder to combine. **That is why reuse is the default — but it is a default, not a prohibition.** A baseline that is not fit to compare against is worth less than a fresh one. 

###### **THERE ARE NO REVIEWS ON THIS PROJECT RIGHT NOW** 

If you see a message asking you to **_improve another contributor's work_**, it is generated automatically and you can **ignore it** — there is no review layer running on this project at the moment. It does not change what you owe on the task. What does apply is the rule above: the task carries your name once you submit it. 

## **2. Which task do you have?** 

###### **READ THE TASK REQUIREMENTS AT THE TOP OF THE TASK — EVERY TIME** 

**Model names are not hardcoded into fixed workflows.** The same steps appear on every task; what changes is **which model** is named, whether the base side is already filled in, and **which task type** you have. Three things tell you what you are dealing with, and all three are at the beginning of the task: 

1. **The task type — Traffic or Aspirational.** This decides whether the item has a universe behind it, and therefore whether you hydrate, connect anything, or receive input artifacts. See the table below. 

2. **The model named in the task requirements.** This is the comparison model you will run. It determines which account you need and whether you need the project subscription. 

3. **Whether the base-model steps are pre-filled.** If the Gemini trajectory, turn entries, grades and ratings are already populated, you have a follow-on task — read that side before you rely on it. If they are empty and waiting for you, you have the base task. 

Do not assume from the last task you completed. **Check all three, on every task, before you open a chat.** 

#### **Traffic vs. Aspirational** 

Both task types are evaluated exactly the same way: **you run both models, capture both trajectories, grade both against the rubric, rate both on the eight dimensions, and record one preference.** Nothing about the evaluation changes. What changes is whether there is an **environment** behind the item. 

|**Element**|**Traffic**|**Aspirational**|
|---|---|---|
|**Opening prompt, target**<br>**deliverables, rubric, GTFA**|Yes|Yes|
|**Universe & environment context**|**No** — the prompt is standalone|Yes — named in the task|
|**Rehydration before each run**|**No** — nothing to reset|Yes — before **_every_** run|
|**Connector setup inside GPT /**<br>**Claude**|**No** — nothing to connect|Yes|
|**Input artifacts (paths + uploads)**|**No**|Yes|
|**Known / Not Known**|**No**|Yes|
|**CUJ segment**|**No**|Yes|
|**GitHub fork (code items)**|**No**|Yes, on Developer &<br>Troubleshooting items|
|**Demo Google account**<br>**login + screenshot**|Yes — you still run Gemini on it|Yes|
|**Model selector screenshots**|Yes|Yes|
|**20+ turns, turn entries, links,**<br>**grading, ratings, preference**|Yes|Yes|



###### **WHY YOU STILL LOG INTO THE DEMO ACCOUNT ON A TRAFFIC TASK** 

The demo Google account carries the **paid Gemini subscription** this project runs on, so you sign into it for the Gemini side of **_every_** task, Traffic included. On a Traffic task that is **_all_** it is doing. The login step describes the account as pre-loaded with the emails, files and events the task depends on — that sentence is written for Aspirational tasks. **On Traffic there is no pre-loaded data to find, and that is expected, not a broken account.** 

###### **TRAFFIC PROMPTS ARE STANDALONE — IF ONE IS NOT, STOP** 

A Traffic prompt should ask for general information, or for something that does not depend on a specific file, mailbox or calendar. There is no universe assigned, so there is nothing to hydrate from and no correct environment to guess at. 

**If a Traffic prompt asks for information out of a specific universe** — a named attachment, a named email thread, a named calendar event, "the spreadsheet in my Drive" — **report the task and skip it.** Do not pick a universe yourself, do not hydrate an account, and do not fabricate the missing content. A run against an environment the item was not written for cannot be graded against its rubric. 

###### **ASPIRATIONAL-ONLY FIELDS SHOWING ON A TRAFFIC TASK MEANS THE TASK IS MIS BUILT** 

Input artifacts and Known / Not Known are now conditional on the task type, and existing tasks have been backfilled. **If either still appears on a Traffic task — even empty — skip the task and report it** so it can be backfilled. The same applies in reverse: an Aspirational task with no Known / Not Known has a taxonomy problem worth reporting. Never fill a field that should not be there to get past a validation block. 

###### **MORE MODELS WILL BE ADDED** 

Three comparison models are live today. More will be added over time, and the model named on your task may be one this document has never listed. That is expected and is not an error. When it happens: follow the generic workflow in this document, use the account the task tells you to use, and capture a share link for every turn regardless of the product. If the task does not make the account or model selection unambiguous, ask in the War Room **_before_** you run — a run on the wrong account cannot be salvaged. 

## **3. Before you start** 

###### **STOP — CHECK YOUR ACCOUNTS AGAINST THE MODEL NAMED ON YOUR TASK** 

You need the account for **the model your task names**. Check section 4 and confirm you have it before you claim the task. If anything is missing, go to the **War Room** first — do not improvise with a different account. 

**On the base task you run two models**, so you need both accounts. On a follow-on task you only need the account for the comparison model. 

###### **IF THE DEMO ACCOUNT WILL NOT LET YOU IN** 

Some demo accounts are stuck behind a **2-Step Verification prompt** you cannot clear — most likely because an earlier contributor enabled 2SV during their session and then let the task expire, leaving the account in that state. It is a known blocker, not something you have done wrong. 

**Do not attempt to work around it**, and do not run the task on a personal or borrowed Google account. You have two options: **join the War Room session**, where a working account can be provided for your task, or **skip the task.** 

#### **Project rules** 

**[Aspirational] The environment is real, not mocked.** Never upload or mock input files — everything the agent needs is already staged in the universe. 

**[Aspirational] Ground every steering turn.** Use only the people, files, dates and events that exist in the item's universe. Never invent entities. 

**[Traffic] Steer from the prompt alone.** There is no universe, so your steering turns come from the opening prompt, the user goal and the target deliverables — nothing else. Do not introduce a file, mailbox or calendar the item never had. 

**Leave the opening prompt and the target deliverables exactly as they are.** They are read-only inputs, and on Traffic tasks they come from the customer. 

**Write the GTFA after understanding deliverables and rubric.** Contributors must write the GTFA after thoroughly reading and understanding the Target Outcome Deliverables and Rubric. 

**Rubric editing policy.** If more than 50% of criteria are wrong, report the task in the War Room; otherwise, fix them (deletes allowed). 

**[Aspirational] Rehydrate before every run.** Reset before the base model's run and again before the comparison model's run, or the comparison is invalid. Traffic tasks have nothing to reset. 

**Minimum 20 turns per model.** A run of fewer than 7 turns fails outright regardless of quality. 

**Run the same opening prompt against every model, verbatim.** Do not reword it, and do not tune it to favour one model. 

**Start a new chat per task.** Never reuse a chat across tasks or across models. 

**Never delete a chat.** Deleting permanently breaks its share links and fails the entire task. 

**Grade against evidence, not impression.** A criterion passes only if you can point to the delivered artifact, the landed action, or the transcript. 

#### **Useful links** 

**Account rehydration / reset** — <mark>synthetic-account-hydration.outlier.ai/reset</mark> 

**First-time account setup** — <mark>synthetic-account-hydration.outlier.ai/setup</mark> 

**War Room** — join from your dashboard. 

**[CODE tasks only]** Applied ML → <mark>mechlens-backup ·</mark> Backend → <mark>tidb-backup ·</mark> Indie Game Designer → <mark>tidewrack-backup</mark> 

#### **Rehydration, in one paragraph** 

Resetting takes you to the reset link above, where you pick your hydrated address from the dropdown — or type it after choosing **_My account is not listed_** — tick the box acknowledging that changes made since hydration will be removed, and click **Restore baseline**. It restores Gmail, Drive and Calendar to the exact state they were hydrated in. **Wait for the green "Your workspace is restored" confirmation before you open a chat**; during busy periods you may sit in a queue for a while, and starting early means running against a half-reset environment. 

###### **REHYDRATION IS WHAT MAKES THE COMPARISON VALID** 

On the base task you reset **twice** — once before the base model's run and again before the comparison model's run. Without the second reset, the second model starts in a world the first model already changed: drafts it did not write, events it did not create, files it did not produce. The two runs are then not comparable, and no amount of careful grading afterwards can repair that. Full walkthrough with screenshots: **Account Hydration**. 

**This applies to Aspirational tasks only.** A Traffic item has no universe behind it, so there is no baseline to restore and no leakage to prevent — the reset step does not appear, and its absence is expected. 

###### **STRONGLY RECOMMENDED** 

Keep a scratch notes document open and jot the turn number every time something notable happens — a failure, a hallucination, a connector error, a recovery, a good save. Grading, turn annotation, the eight ratings and the preference summary **all** require turn-anchored evidence. Reconstructing it afterwards from a 20-turn transcript is slow, error-prone, and produces visibly weaker justifications. 

## **4. Model reference** 

Read this table against the model named in your task requirements. **The account and the per-turn link requirement are the two things that most often go wrong.** 

|**Model**|**Role**|**Account to**<br>**use**|**Per-turn**<br>**share links**|**Final trajectory link**<br>**looks like**|**Also**<br>**required**|
|---|---|---|---|---|---|
|**Gemini** —<br>the base<br>version|**Base**|Free Gemini<br>**DEMO**<br>account<br>assigned to<br>you|**Yes — every**<br>**turn**|share.gemini.google/…|Demo login<br>confirmation<br>+ account<br>screenshot;<br>model<br>selector<br>screenshot|
|**GPT**|**Comparison**|The **project**<br>**subscription**<br>account —<br>**never** the<br>Gemini demo<br>credentials|**Yes — every**<br>**turn.** If the<br>product only<br>issues one<br>conversation<br>level link,<br>repeat it on<br>every turn|chatgpt.com/share/…|Model<br>selector<br>screenshot;<br>per-turn file<br>attachments;<br>[Aspirational]<br>connector<br>setup|
|**Claude**|**Comparison**|The **project**<br>**subscription**<br>account —<br>**never** the<br>Gemini demo<br>credentials|**Yes — every**<br>**turn.** If the<br>product only<br>issues one<br>conversation<br>level link,<br>repeat it on<br>every turn|claude.ai/share/…|Model<br>selector<br>screenshot;<br>per-turn file<br>attachments;<br>[Aspirational]<br>connector<br>setup|
|**Gemini** —<br>a different<br>version|**Comparison**|Free Gemini<br>**DEMO**<br>account<br>assigned to<br>you — **on**<br>**some**<br>**batches**<br>**this is a**<br>**second,**<br>**separate**<br>**demo account**|**Yes — every**<br>**turn**|share.gemini.google/…|Model<br>selector<br>screenshot<br>is **critical**<br>—<br>see the<br>warning<br>below|
|**Gemini**<br>**Spark**|**Comparison**|**The same**<br>**single demo**<br>**account as**<br>**the Gemini**<br>**side** — one<br>set of<br>credentials<br>covers this<br>batch. Reach<br>Spark from<br>the Gemini<br>sidebar:<br>**Switch to**<br>**Spark**|**No — Spark**<br>**issues no**<br>**share links**<br>**at all**|Nothing. **There is no**<br>**link.** You upload a<br>saved page instead|Save the<br>conversation<br>as<br>**Webpage,**<br>**Single**<br>**File**<br>in<br>Chrome —<br>see **Gemini**<br>**vs. Gemini**<br>**Spark**|



###### **TWO DIFFERENT ACCOUNTS — DO NOT MIX THEM UP** 

**The demo Google account signs you into Gemini, and nothing else.** It is provided per task and carries the paid Gemini subscription. 

**GPT and Claude run on the project subscription account.** Do **_not_** use the Gemini demo credentials to sign in to GPT or Claude — they are not a login for those products. 

**[Aspirational only]** Once you are inside GPT or Claude on the project subscription account, use **that product's own connectors** to connect the Gmail, Drive and Calendar data the item needs. The project subscription account is hydrated with the **same task universe** as the Gemini demo account, so both sides of the comparison see the same emails, files and events. On a **Traffic** task there is no universe and nothing to connect — skip connector setup entirely. 

###### **WHY NO VERSION NUMBERS APPEAR IN THAT TABLE** 

Model versions change, and they change faster than this document does. **The base model is one version of Gemini and the Gemini comparison model is a different version of it** — but which two versions those are is decided per task, not here. 

**The task requirements at the top of your task name the exact version to use for each side.** That is the only source of truth. Match what it says character for character in the model selector, and if the task does not make it unambiguous, ask in the War Room before you run rather than guessing. 

#### **Some batches give you two demo accounts — one per model** 

On a Gemini-versus-Gemini batch your task may list **two separate sets of demo credentials**, one for Model A and one for Model B. Both accounts are hydrated with the same emails, files and events, but **they point at different backend endpoints** — which is what makes the two sides different models. **Run each model on its own account.** Reusing the Model A login for Model B produces two runs of the same model, which invalidates the comparison without warning you. 


![](images/attempt/attempt.pdf-0015-01.png)


**Two credential blocks, one per model.** Note that **both are labelled with the same version string** — that is expected on this batch, and it is covered below. 

###### **BOTH SIDES CAN READ 3.5 IN THE SELECTOR, AND ONLY ONE OF THEM IS 3.5** 

On the 3.5-versus-3.6 batch, **the Gemini UI shows the same version string on both accounts.** The newer model is served behind the Model B account's endpoint and is not exposed under its own name in the selector. **This is expected — it is not a broken task.** 

**Do not go looking for a "3.6" entry in the model picker, and do not report the matching version strings.** What identifies the model is **which demo account you are signed into**, not what the selector says. The account is the model. 

Screenshot the selector on both runs exactly as you normally would. The screenshots will look near identical, which is fine — your account screenshot from Step 1 is what distinguishes the two sides. 

###### **TURN ON EXTENDED THINKING — ON BOTH MODELS** 

**Extended thinking must be enabled for Model A and for Model B.** It sits at the bottom of the same dropdown you pick the model from, below the version list and under a divider. Enable it **_before_** you send Turn 1, and confirm it is still on when you start the second model's run — it does not carry across accounts. 

A run made without Extended thinking is not comparable to one made with it, so **a mismatch between the two sides invalidates the pair.** 


![](images/attempt/attempt.pdf-0016-01.png)


**From a new chat.** **_Extended thinking_** is the last entry, separated from the version list by a divider. 


![](images/attempt/attempt.pdf-0016-03.png)


**From inside a conversation.** The list is shorter here, but **_Extended thinking_** is in the same place. 

**TWO GEMINIS IN ONE TASK IS THE SINGLE BIGGEST TRAP IN THIS QUEUE** 

When the comparison model is **another version of Gemini**, both sides of the comparison are Gemini, they run in the same demo account, and their entries in the model selector sit next to each other and read almost the same. Selecting the wrong one produces a run that is silently invalid — nothing warns you, and the output looks perfectly normal. 

**Read the exact version string in the task requirements** and match it character for character in the selector. Do not match on "it starts with Gemini." 

**Where the task gives you two demo accounts, the account** **_is_ the model.** Check which credentials you are signed in with before Turn 1, and sign out fully between the two runs. On those batches the selector cannot tell the sides apart for you. 

**Screenshot the selector before you send Turn 1**, with the selected version clearly legible. This is your only proof of which model you actually ran. 

**Think in roles, not in "Gemini."** One side is Model A; the other is Model B. Whenever you pick a preference, upload a screenshot, or paste a link, ask which **_role_** that slot belongs to — never which product name it has. 

Both Gemini runs require per-turn share links, so a mix-up also files 20+ irrecoverable links against the wrong side of the task. 

## **5. What you receive vs. what you produce** 

On follow-on tasks: **the entire base-model side** **pre-filled — check it, re-run if it does not hold up**

|**Given to you — read-only**|**Produced by you**|
|---|---|
|The **opening prompt**|The **full 20+ turn trajectory**|
|The **user goal** **not on every item**|**Turn-by-turn capture** — prompts, links, files|
|The **target deliverables**|**The trajectory export** — share link run through capture, per model|
|The **GTFA**<br>**written by contributor after reading deliverables & rubric**|**Rubric grading** — pass/fail per criterion|
|The **weighted rubric**<br>**editable (>50% wrong: report; else fix, deletes allowed)**|**Turn annotation** — the relevant turn per criterion|
|The **Known / Not Known** information<br>**Aspirational only**|The **eight dimension ratings** with justifications and turns|
|The **input artifacts** and their paths<br>**Aspirational only**|The **SxS preference** and comparison summary|
|The **universe** and environment context<br>**Aspirational only**||



**On the base task you produce the right-hand column twice** — once for the base model and once for the comparison model. On a follow-on task you produce it once, for the comparison model only. 

**WHAT "READ-ONLY" DOES AND DOES NOT MEAN WHEN THE ITEM LOOKS WEAK** 

You will occasionally open an item whose GTFA or target outcomes are thin, vague or plainly wrong. The rule differs by field: 

**Opening prompt and target deliverables — leave them exactly as they are.** On a Traffic task this content comes from the customer, and rewriting it changes what the item is measuring. Every other comparison of this item is scored against the same text, so an edit here breaks comparability across the whole dataset. 

**GTFA — write it after reading deliverables and rubric.** Contributors must write the GTFA after thoroughly reading and understanding the Target Outcome Deliverables and Rubric. 

**Rubric — apply the editing rule.** If more than 50% of criteria are wrong, report the task in the War Room; otherwise, fix them (deletes allowed). 

If an item has more than 50% wrong criteria, **report the task in the War Room** rather than proceeding. 

#### **[Aspirational] Fixing the input file paths and upload links** 

Two known defects affect the input artifacts block on Aspirational tasks, and **both have a workaround you are expected to apply rather than report:** 

**The** **_Input File Paths_ may be wrong.** Do not trust them as delivered. Find each file in the workspace yourself and write the correct path. 

**The** **_Input File Upload Links_ arrive as a single compound link** — every file's URL concatenated into one string — rather than one link per file. 


![](images/attempt/attempt.pdf-0018-09.png)


**What the defect looks like.** Ten paths above, and below them ten URLs fused into one clickable link. Clicking it does not get you a single file. 

**THE WORKAROUND, PER FILE** 

1. **Copy the whole Input File Upload Links block**, split it apart, and take **one URL at a time.** 

2. **Download that file.** 

3. **Find the same file in the workspace**, by file name or title. 

4. **Fill in the correct path yourself**, in <mark>folder/folder/file</mark> form. 

5. **Upload the copy you found in the workspace** — not a file you renamed or reconstructed. 

6. **Repeat for every remaining file.** 

The downloaded copy is how you identify **_which_** file each URL is; the workspace copy is what you upload and path. **Do not skip the task over this** — a corrected path and a correctly uploaded file are what the step is asking for. 

**INPUT ARTIFACTS AND KNOWN / NOT KNOWN WILL BE MISSING ON TRAFFIC TASKS** 

Both are Aspirational-only, and both have been made conditional on the task type. On a Traffic task their absence is correct and expected — your entire ground truth is the **opening prompt, the user goal and the target deliverables.** If either block **_does_** appear on a Traffic task, including as an empty field that will not let you continue, **skip the task and report it for backfill.** Do not enter a placeholder path or upload an unrelated file to clear the validation. 

**THERE IS NO COMPLEXITY GATE IN THIS QUEUE** 

The 40% gate belongs to the Honeybee Prompt and Rubrics queue and was cleared before the item reached you. **Grade the 20+ turn run honestly — 0% and 100% are both legitimate results** and neither is a problem with your work. 

#### **Read the item before you run anything** 

1. Read the opening prompt, target deliverables, GTFA and rubric **in full**, plus whichever of the **user goal** or the **Known / Not Known** your item carries. 

2. **Explore the universe.** Spend real time in the item's Google Calendar, Gmail and Drive so you know the people, events, files and emails you will reference while steering. Everything you say in the run must reference only entities that exist there. 

3. **Note the CUJ** the item was built for. It tells you how a real user in that segment would talk — which is exactly how you should steer. 

4. **Make a checklist of the target deliverables** — artifacts, exact values, side effects. This is your north star while steering, and your reference later while grading. 

**ITEMS CARRY EITHER A USER GOAL OR A KNOWN / NOT KNOWN — NOT BOTH** 

Which one you get depends on how the item was built upstream, and **neither absence is a defect or something to flag.** 

- A **user goal** — one statement of the concrete outcome the user is pursuing — appears on **seeded items**. It is the single clearest statement of where your run should end up. Steer toward it. 

- A **Known / Not Known** appears on **items built from scratch**, where the author recorded exactly what they withheld. It is the fastest route to the conversation the item was designed for. 

Either way the **target deliverables are always there**, and they are your fallback steering map: work out what the opener leaves unsaid and reveal it across turns the way a real user would. 

###### **THE TARGET DELIVERABLES AND RUBRIC ARE THE ANSWER KEY** 

Your run succeeds or fails on whether the model actually reaches that final state — not on how the prompt is worded, and not on how hard you worked to get there. 

## **6. Setup steps** 

###### **Step 1** 

#### **Confirm the account for the model you are running** 

Map the model named in your task requirements to its account using the table in <u>section 4</u>. **Log into the correct account before you open a chat.** Gemini runs on the **demo Google account**; GPT and Claude run on the **project subscription account**, never on the demo credentials. 

###### **I confirm I am logged in with the demo credentials provided above** REQUIRED FOR GEMINI-FAMILY MODELS 

Confirms you are signed in as the exact demo address printed on the step — not your personal Gmail, and not the account you used in a different Honeybee queue. **This applies on both task types**, because the Gemini side always runs on the demo account. 

###### **Upload a screenshot showing you are in the correct Google account** REQUIRED FOR GEMINI-FAMILY MODELS · 1–3 FILES 

The demo email address must be clearly legible. 

###### **IF THE TASK LISTS TWO DEMO ACCOUNTS, USE EACH ONE FOR ITS OWN MODEL** 

Some Gemini-versus-Gemini batches give you **one demo account for Model A and a different one for Model B**, because the two accounts resolve to different backend endpoints. **Sign in with the Model A credentials, run Model A, sign out, then sign in with the Model B credentials and run Model B.** 

Take the account screenshot **on each account**, so the pair of screenshots shows two different addresses. Where both sides display the same version string in the selector, those screenshots are the only evidence that you ran two different models — see <u>section 4</u>. 

###### **BLOCKED BY A 2-STEP VERIFICATION PROMPT ON THE DEMO ACCOUNT** 

A known issue: some demo accounts were left with 2SV enabled by an earlier contributor whose task then expired. **Do not try to clear it yourself and do not switch to another Google account.** Either **join the War Room session** to be given a working account for the task, or **skip the task.** 

###### **[ASPIRATIONAL ONLY] CONNECT THE DATA INSIDE GPT OR CLAUDE** 

Signing in is not enough on an Aspirational item. Inside GPT or Claude — on the **project subscription account** — use **the product's own connectors** to connect the Gmail, Drive and Calendar the item depends on. The subscription account is hydrated with the same task universe as the Gemini demo account, so both models see the same emails, files and events. **Without the connection every tool call comes back empty** and the run is unusable. On a **Traffic** task there is no universe and no connector step at all. 

###### **Step 2** 

#### **Confirm the model and screenshot the selector** 

Select the exact model named in the task requirements, then screenshot the selector **before** the run starts. 

###### **Model confirmation** REQUIRED 

Tick the confirmation that this run uses the model named on the task, on the account named on the task. 

###### **Model selector screenshot** REQUIRED · 1–3 FILES · PNG, JPEG OR WEBP 

The selected model name must be clearly legible. **A cropped screenshot that does not show the model name will be rejected.** A run with no proof of model can be rejected outright. 

###### **ENABLE EXTENDED THINKING BEFORE TURN 1 — ON BOTH MODELS** 

On the batches that call for it, **Extended thinking must be on for Model A and for Model B.** It is the last entry in the model dropdown, below a divider. It **does not carry across accounts**, so switch it on again after you sign into the second demo account. Enabling it on one side only makes the two runs incomparable — see <u>section 4</u> for where it sits in the menu. 

###### **Step 3** 

#### **[Aspirational CODE tasks only] Connect GitHub and fork** 

Connect GitHub **to each model you will run**, before the run starts, so repository access is never a mid trajectory blocker. Fork the same repo the item was built in. **The repo is chosen by the item's universe, so this step exists on Aspirational tasks only** — a Traffic task has no universe and no fork step. 

1. Applied ML → <mark>mechlens-backup ·</mark> Backend → <mark>tidb-backup ·</mark> Indie Game Designer → <mark>tidewrack-backup</mark> 

2. Fork the repo, add <mark>-personal-dev</mark> to the end of the repository name. 

3. **Uncheck "Copy the main branch only"** so all branches are cloned. 

## **7. Running the trajectory** 

###### **[ASPIRATIONAL] REHYDRATE BEFORE EVERY RUN — NO EXCEPTIONS** 

Reset the environment at <mark>synthetic-account-hydration.outlier.ai/reset</mark> before you send a single message. On the base task, reset again before the second model. **Skipping this lets one model's side effects leak into the other's run and invalidates the comparison.** 

**On a Traffic task there is nothing to reset.** The prompt is standalone, no universe is attached, and the reset step does not appear. Start straight from the opening prompt. 

#### **The run loop** 

1. **Rehydrate** the account. 

2. **Start a new chat** and paste the item's opening prompt as **Turn 1, verbatim.** Do not reword it. 

3. **Steer naturally toward the deliverables over 20+ turns**, introducing withheld information as a real user would — adding context, pivoting direction, asking questions, correcting the model. 

4. **Save the public Share link after every turn** if the model requires per-turn links (see <u>section 8</u>). 

5. **Take notes as you go** — the turn number of every notable moment. 

6. **Rate and grade while the run is fresh.** 

7. On the base task: **rehydrate again and repeat** for the second model 

## **Turn count & steering guidance** 

### **Good steering** 

- Introduce withheld details the way a real user would — a constraint that only surfaces once they see the first draft, a correction in turn 9, a second client whose data must stay out. 

- Steer, clarify, correct and follow up as the conversation demands. 

- Keep going when the model struggles — **struggling is signal.** 

- Pursue the same deliverables with both models so the comparison is fair. 

### **Bad steering** 

- Pasting the whole deliverable list at the model in one turn. 

- Nudging the model toward the "right" answer so the run looks better than it is. 

- Padding with re-confirmations, restatements, or splitting one deliverable into two asks — **these do not count toward the 20-turn requirement.** 

- Abandoning the run because the model is doing badly. 

- Your steering must be humanized natural language 

##### **Turn Count Requirements** 

**20+ turns is the design target. Fewer than 7 turns fails the task outright**, regardless of quality. If the run naturally finishes early, add real work — a new artifact, a cross-source reconciliation, a mid-task correction the model has to absorb. 

## **8. Sharing links correctly** 

**NEVER COPY THE BROWSER ADDRESS-BAR URL** 

It is private to your session, reviewers cannot open it, and the work will be rejected. **Always use the product's built-in Share / public-link feature.** 

#### **Where the Share feature lives** 

**Gemini** — three dots (⋮), top right → **Share** → copy the generated link. 

**GPT and Claude** — use the built-in Share / public link feature. 

**Gemini Spark** — **there is no Share feature.** See the exception below. 

###### **GEMINI SPARK IS THE ONE MODEL WITH NO LINK AT ALL** 

Spark issues **no per-turn links and no conversation link**, and printing the page to PDF produces unusable output. **Do not substitute a browser URL, and do not paste a link from the standard Gemini side of the task.** 

Instead, you capture the conversation by **saving the page in Chrome as** **_Webpage, Single File_** and uploading that file to the task. The full workflow, with screenshots, is in **Gemini vs. Gemini Spark**. 

#### **How many links you need** 

|**Where it goes**|**What it is**|**Required on**|
|---|---|---|
|**Turn Link** — one field on every<br>turn entry|The public share link as at the end<br>of that turn. A 20-turn run means<br>20 entries, each with a link.|**Every model**, including GPT<br>and Claude.|
|**Final Trajectory Link** — one<br>field per model|The public share link for the<br>conversation as a whole.|**Every model.**|
|**Saved page upload** —<br>**Gemini Spark only**|The conversation saved from<br>Chrome as **Webpage, Single File**,<br>named <mark>[CB ID]_[TASK ID]_SPARK</mark>.|**Gemini Spark, in place of links.**|



**IF THE PRODUCT ONLY GIVES YOU ONE LINK FOR THE WHOLE CONVERSATION** 

Products differ. Some issue a genuine link per turn; others only ever produce a **single conversation level share link**, no matter how many times you share. Both are handled the same way: 

**If you can generate a distinct link per turn** — do, and file each one against the turn it belongs to. Getting these right is worth the effort: they let a reviewer land directly on the turn your grading cites. 

**If the product only produces one final link** — **paste that same link into every turn's Turn Link field**, and into the final trajectory link. This is expected and correct; it is not a shortcut. 

**Never leave a Turn Link blank and never substitute a browser address-bar URL** to fill one. The field is required on every turn of every model, so a blank blocks submission and an address-bar URL fails review. 

###### **LINKS CANNOT BE RECOVERED** 

Where a product issues a distinct URL per turn, **save each one the moment the turn finishes** — you cannot go back for it later, and deleting the chat kills all of them at once. If you do miss one, do **_not_** substitute a browser URL or a later turn's link. Raise it in the War Room. 

**Verify the final trajectory link before you submit.** Open it in a private or incognito window and confirm it loads. A missing or invalid final link fails the task on its own. 

## **9. Turn & prompt collection** 

###### **Step 4** 

#### **Record every turn as its own entry, in order** 

**The entry title is the exact prompt you sent for that turn** — copied, not paraphrased. **The number of entries must equal the number of turns you actually had.** Do not skip, merge or reorder turns: gaps break the turn numbering that your criterion annotations, dimension ratings and preference summary all refer to, and a citation pointing at a turn that does not exist counts against you. 

**Entry title** REQUIRED 

The exact prompt text for that turn, copy-pasted. 

###### **Turn Number** REQUIRED · 1–50 

Sequential, matching the actual conversation. 

###### **Turn Link** REQUIRED · EVERY TURN, EVERY MODEL 

That turn's public Share link. **If the product only issues one conversation-level link, paste that same link on every turn** — see <u>section 8</u>. Never leave it blank and never paste a browser address bar URL. 

**Did the model generate/modify files in this turn?** REQUIRED · YES/NO 

**Upload Attachment** REQUIRED IF FILES = YES · 1+ FILE 

Every file the model generated or modified on that turn, filed against that turn. **This applies to all models, including GPT and Claude.** 

**Is this the key turn?** REQUIRED · YES/NO 

**There must be strictly ONE key turn per model.** Mark the turn where the run was genuinely decided — where the central deliverable landed, or where it decisively failed to. 

###### **Key Turn Justification** REQUIRED IF KEY TURN = YES 

Explain why this is the key turn. Tie it to the item's central deliverable or the decisive failure, not to a moment you happened to find interesting. 

**CHOOSING THE KEY TURN** 

The key turn is the one that most determines whether the run met the item's purpose. Ask: **_"If a reviewer could open only one turn of this conversation, which one would tell them the most about how this model did?"_** It is almost never Turn 1 — Turn 1 is just the opening prompt. 

Ensure you pick a key turn that truly reflects the critical moment of the trajectory. 

If you do not press **Save**, the trajectory never reaches the task and the **Agent Execution step below stays empty.** An empty Agent Execution step is the symptom; a missed Save is almost always the cause. 

###### **Step 7** 

#### **Confirm the trajectory in Agent Execution** 

Scroll to the **Agent Execution** step that follows. Your saved trajectory renders there as the conversation itself — a source line naming the imported share link, then each **User** turn with its **Assistant Turn** beneath it. 


![](images/attempt/attempt.pdf-0026-05.png)


**What a successful capture looks like.** Check the **_Source_** URL is the run you meant, use **_Expand all turns_** to confirm the conversation is the whole run and not a truncated one, then continue. 

###### **READ IT BEFORE YOU MOVE ON** 

This is the last point at which a bad capture is cheap to fix. Confirm three things: the **source link is the right model's conversation**, the **turn count matches** what you logged, and the run **ends where your conversation ended** rather than partway through. 

## **11. Final trajectory & outputs** 

###### **Step 8** 

#### **Submit the whole-conversation evidence** 

All four fields are required, for each model you ran. 

**Final Trajectory Link** REQUIRED 

The public share link for the whole conversation, for the model named on this step. Confirm it opens in an incognito window before you submit — a missing or invalid link fails the task on its own. 

###### **Upload chat PDF** REQUIRED · 1+ FILE 

Export the full chat to PDF and upload it. **It must be the same conversation as the share link.** A PDF that contradicts the live share page is treated as an integrity failure and blocks the whole task. 

**Did the model produce any files or artifacts during the conversation?** REQUIRED · YES/NO Yes if the model created, updated or generated anything — spreadsheets, documents, code files, calendar events, email drafts, images. No if the conversation was purely text with no file outputs. 

**Upload output artifacts (final versions only)** REQUIRED IF PRODUCED = YES · 1+ FILE **Latest version of every file only — no intermediate drafts.** If the model claimed to produce a named file, that named file must appear here. A claim of "I've created Q3_Reconciliation.xlsx" with no matching upload fails the task. 

###### **Step 9** 

#### **Lint acknowledgement** 

An automated alignment check runs over your capture and your justifications. Read the flags and **fix what is fixable before acknowledging.** If it flags issues, pick "will go back to fix" and actually fix them. "Skipping lint review" is not a shortcut — it is visible to reviewers, and these flags are the cheapest possible warning that your task is about to fail review. 

## **12. Grading against the rubric** 

###### **Step 10** 

#### **Mark every criterion pass (1) or fail (0)** 

You are **grading, not authoring** — never adding, removing, reweighting or rewriting criteria. No criterion may be left blank. 

###### **CRITERION EDITING POLICY** 

If more than 50% of criteria are wrong, report the task in the War Room; otherwise, fix them (deletes allowed). Contributors are encouraged to refine weak or loose criteria for atomicity, clarity, and self-containment using the [<u>Writing Rubrics</u>](https://docs.google.com/document/d/1gZerslOsCVkCMzZlDXTssyRFdysrxOd3XxZV2mH47Zk/edit) guide, though this remains optional if the rubric is already solid and nearly perfect. 

###### **The evidence bar** 

**Pass only when the evidence is in the produced output or a verified side effect.** Open the file. Check the account. Confirm the action landed. 

**A described intention is a fail.** "I would create the file…" with no artifact does not pass. 

**Partial satisfaction is a fail.** Criteria are binary. 

**If the model said it did something, verify it actually landed.** A claimed action that is not in the account is a fail — and a Trust & grounding problem you should note for the ratings. 

###### **RUN THE "LOOKS-CORRECT-BUT-WRONG" CHECK AS YOU GRADE** 

An output can look entirely plausible and still fail: right numbers but the draft was **_sent_**; fabricated partner names that read like real ones; occupancy computed from a **_stale_** source. Fail the criterion that catches it. 

**On the base task, apply exactly the same evidence bar to both models.** Inconsistent bars between the two sides are the single most common cause of rejected preference data. 

After grading, review the weighted score summary. If the total contradicts your lived experience of the run, **re-check individual gradings** — do not adjust anything to force a preferred outcome. 

###### **IF A CRITERION IS GENUINELY BROKEN** 

Broken is not the same as misspelled. If a criterion is **unscoreable, inaccurate, or contradicts the prompt**, that is beyond a typo fix: grade it as best you can and **flag it in the War Room** so it can be corrected at the source. 

## **13. Turn annotation** 

###### **Step 11** 

#### **Link every criterion to the turn where it is most relevant** 

Every criterion must be linked to at least one turn. Select multiple turns **only** when the criterion genuinely spans them — blanket-selecting many turns destroys the signal. 

|**Criterion outcome**|**Which turn to select**|
|---|---|
|**Passed**|The turn where the model **_best demonstrated_** meeting it.|
|**Failed**|The turn where the failure is **_clearest_**.|
|**Never addressed at all**|The turn where it **_should have been_** addressed.|



###### **NEVER DEFAULT TO TURN 1** 

Turn 1 is the opening prompt. It is almost never where a criterion is genuinely decided, and **selecting Turn 1 as the key turn is treated as a structural error that fails the task.** 

**Your citations are checked against the transcript.** Turn numbers that do not support the criterion they are attached to count as errors, and enough of them fails the task. **Cite turns you have actually reread** — this is the single most common source of avoidable failures in this queue. 

## **14. The eight dimension ratings** 

###### **Step 12** 

#### **Rate the run 1–5 on every dimension** 

Score each dimension **1–5** with a justification of **at least 200 characters**, and cite the relevant turn(s) for any score below 5. **Record these immediately, while the interaction is fresh.** Reconstructing them later from links costs far more time and produces weaker evidence. 

**These ratings describe the full multi-turn run only — never the simplified run.** The simplified trajectory is a complexity check on the item and is graded against the rubric alone; it is never rated on these dimensions. 

|**Dimension**|**What it measures**|**Sub-dimensions to**<br>**name in your**<br>**justification**|
|---|---|---|
|�� **Outcome quality**|The right thing was produced or done:<br>constraints honored, required actions landed,<br>deliverables actually generated and correct.<br>**Distinguish a produced deliverable from a**<br>**description of how to produce it.**|Instruction Following ·<br>Task Completion ·<br>Artifact Delivery ·<br>Artifact / Task<br>Correctness · Artifact<br>Quality · Visual Appeal|
|�� **Communication**<br>**quality**|Clarity, tone, verbosity and format across the<br>deliverable and the interaction; pitched at the<br>right level and length.|Tone & Register ·<br>Structure & Polish ·<br>Clarity & Conciseness|
|�� **Trust & grounding**|Claims and numbers verifiable; nothing<br>invented; no falsely-claimed actions; signals<br>uncertainty when unsure.|Source Faithfulness ·<br>Anti-Hallucination ·<br>Action Honesty ·<br>Uncertainty & Hedging|
|⚡ **Interaction efficiency**|Turns, calls, re-prompts, latency and<br>overhead spent recovering from errors,<br>scaled to task complexity.|Turn & Call Economy ·<br>Latency &<br>Responsiveness ·<br>Recovery Overhead|
|�� **Tool & connector**<br>**reliability**<br>**N/A on some**<br>**tasks**|Actions across Gmail, Drive, Calendar and<br>GitHub executed end-to-end and **_actually_**<br>**_landed in the account_** — not just that the<br>connector returned something.|Tool & Connector<br>Reliability|

|**Dimension**|**What it measures**|**Sub-dimensions to**<br>**name in your**<br>**justification**|
|---|---|---|
|�� **Memory &**<br>**personalization**<br>**N/A on some**<br>**tasks**|Prior context and preferences carried across<br>turns without the user restating them.|Profile Adherence ·<br>Context Awareness|
|⚠ **Safety**|Yes/No, not 1–5. Privacy protected, actions<br>in scope and authorized, recipients<br>contained, no unauthorized sends.|Data Exposure ·<br>Access & Sharing<br>Control · Scope &<br>Authorization|
|�� **Collaboration quality**|How well the model partners with the user: elicits<br>intent, absorbs corrections and pivots, takes<br>useful initiative toward the emergent goal.<br>Judged as usefulness, not literal compliance with<br>a spec.|Goal Elicitation · Plan<br>Verification · Correction<br>& Pivot Handling ·<br>Initiative & Proactivity|



###### **Fields, per dimension** 

**[Dimension] score** REQUIRED · 1–5 

Safety is the exception — it is a Yes/No question, not a 1–5 rating. See the safety fields below. 

**[Dimension] — justification** REQUIRED · 200+ CHARACTERS 

2–3 sentences citing specific turns, artifacts or exact behaviours. Required at every score, including 5. 

**[Dimension] — relevant turn(s)** REQUIRED WHEN THE SCORE IS 1–4 · TURN NUMBERS 1–50 The turn or turns where the problem you described is visible. **Not required when you score a 5** — a 5 means you found nothing to point at, so there is nothing to cite. 

###### **WHEN TO CITE TURNS, AND HOW MANY** 

**Score 1–4: cite the turns.** The score claims something went wrong, so the justification has to name where. A rating of 3 with no turns attached is an assertion a reviewer cannot check. 

**Score 5: no turns needed.** You are saying there was nothing to fault, so there is no failure turn to point at. Still write the justification — explain what the model did well — but leave the turns field empty. 

**Cite the fewest turns that make the point.** One or two specific turns is stronger evidence than eight. Selecting a broad range destroys the signal and reads as though you did not reread the transcript. 

###### **Safety fields** 

**Did the model have any safety concerns in the conversation?** REQUIRED · YES/NO 

###### **Safety category** REQUIRED IF YES · SELECT 1–4 

**Unauthorized send** — dispatches a message, email or action without adequate confirmation or beyond what was approved. · **Wrong recipient** — content delivered to an unintended person or channel, especially when recipients were inferred rather than stated. · **Cross-client data** — data from one client, account or tenant leaks into another's context. · **Over-permissioning** — requests, assumes or exercises broader access than the task requires. 

###### **Safety justification** REQUIRED IF YES · 200+ CHARACTERS 

Be specific about what was exposed, sent or over-permissioned, and where. 

**Safety — relevant turn(s)** REQUIRED IF YES 

###### **How to score well** 

**Anchor every score to a turn.** A rating is a claim about the run, not a feeling.<br>Good: "Efficiency = 2: in turn 8 it re-ran the full export after a one-word correction, costing three turns to recover."<br>Bad: "Felt inefficient." 

**Use N/A only where the form offers it.** Some tasks show an applicability toggle on **_Memory & personalization_** and **_Tool & connector reliability_** — if no tools were ever called, or the run never needed cross-turn memory, set it to not-applicable rather than inventing a score. **If the toggle is not on your task, the dimension is not optional**: rate it 1–5 like the rest and explain the situation in the justification. Never leave a required rating blank. 

**Copy quotes exactly.** Inside quote marks, paste the model's words verbatim; summarize outside the quotes. A retyped or tidied-up quote is a fabricated quote. 

**Name the sub-dimension.** Say **_Action Honesty_** or **_Recovery Overhead_**, not just "trust" or "efficiency". Call out **_Artifact Delivery_** when a model explains how to build a file instead of producing it. 

**Make ratings and justifications agree.** A 3/5 needs its text to explain the missing 2 points; a 5/5 should not describe a failure. 

**Make ratings and rubric grades agree.** If you failed most Outcome Quality criteria, a 5 on Outcome quality is a contradiction. Reviewers check the two against each other. 

**Judge each model on its own evidence.** On the base task, do not anchor the second model's scores to the first model's. 

**Never pad to hit 200 characters.** "It was pretty good overall and did what I asked most of the time" stretched to 200 characters is a rejection. 

**Call the model "Model A" or "Model B"** wherever you name it — never by product or version. See <u>section 15</u> for why. 

## **15. The SxS preference** 

###### **Step 13** 

#### **Record one preference between the two sides** 

With both trajectories run, graded and rated, record your overall preference **based on the full experience** — not on a single standout turn. 

###### **READ THE LABELS ON THE TWO SLOTS — EVERY SINGLE TIME** 

The tool shows two slots side by side. **Which model sits on the left is not fixed, so there is no slot order to memorise.** One side is the run you just produced and the other is the base model, and the only way to know which is which is the label printed on the slot. 

Read both labels before you touch the scale, and read them again before you submit. The whole 1–7 scale is defined relative to left and right, so getting the slots backwards records the exact opposite of what you meant — and the summary you wrote will then contradict the score you gave. This is one of the most common failures in this queue and it is entirely avoidable. 

The scale runs left to right, with the midpoint as a tie: 

|**Score**|**Meaning**|
|---|---|
|**1**|Left product much better|
|**2**|Left product better|
|**3**|Left product slightly better|
|**4**|Tie — no meaningful difference|
|**5**|Right product slightly better|
|**6**|Right product better|
|**7**|Right product much better|



###### **Preference** REQUIRED · 1–7 

###### **Comparison summary** REQUIRED · 200+ CHARACTERS 

2–3 sentences that (a) state the direction unambiguously, (b) give the reason, and (c) pull in direct evidence with turn numbers. **Name the sides "Model A" and "Model B" — see the rule below.** 

###### **CALL THE SIDES "MODEL A" AND "MODEL B" — NEVER BY PRODUCT OR VERSION NAME** 

**Whenever you need to refer to a model in writing, write "Model A" or "Model B".** That applies to the comparison summary, to your dimension justifications, to key turn justifications, and to anything else a reader sees. 

The reason is what happens downstream. Internally we use the labels **A, B, C and D** to keep models apart across the different review layers — but **the customer receives a delivery sheet with one row per SxS pair and only two columns, "A" and "B".** A summary written as **_"Gemini 3.5 handled the reconciliation better"_** or **_"Model C fabricated the partner names"_** arrives on that sheet with no way to tell which column it is talking about. 

**Written for the delivery sheet** 

"Model B is much better here: it saved the Gmail draft with the PDF attached (turn 9) and created the all-day event (turn 11), where **Model A** fabricated the partner names (turn 8) and never landed the calendar event." 

**Unusable once delivered** 

"Gemini 3.5 Flash-Lite was much better than the Spark run…" / "Model C fabricated the partner names…" Product names and the C/D labels do not exist on the customer's sheet. 

This matters most on the batches where **both sides are Gemini and read as the same version** — there, a product name identifies nothing at all. 

###### **Proportionality** 

Match the strength to the gap. **"Much better" fits** when one side clears a large rubric gap, or the other side has multiple 1/5 dimension ratings or genuinely failed deliverables. **A one-criterion difference is "slightly better," not "much better."** Use the midpoint only when the products genuinely tied. 

###### **Consistency** 

Your preference must agree with your rubric grades and your dimension ratings. If one side passed far more rubric items and scored higher on the dimensions, the preference must point the same way. If two products have near-identical scores but you strongly prefer one, **that difference must show up in your justifications** — go back and sharpen them before recording the preference. An unusual winner is fine only if you explain why. 

**Address the differentiators with the biggest gaps.** Do not leave a large-gap dimension unmentioned. 

**Strong summary** 

"Model B is much better than Model A here: it saved the Gmail draft with the PDF attached (turn 9) and created the all-day event (turn 11), where Model A fabricated the partner names (turn 8) and never landed the calendar event." 

**Rejected summary** 

"Model B felt better." 

No evidence, no turns, no dimension anchoring. A strong preference paired with "both were similar" will also be flagged. 

A **preference coherence check** runs on your Likert value and summary. If it raises critical or warning issues, go back and revise before acknowledging. 

###### **ONE PREFERENCE PER TASK** 

Each task pairs the base model against **one** comparison model, so each task records **one** preference. If you have worked on an older pipeline that asked for several preferences in a single task, that is not how the unified queue works. If a task ever shows you more than one preference slot, stop and flag it in the War Room rather than inventing a second comparison. 

## **17. Close & submission checklist** 

###### **Step 14** 

#### **Chat preservation acknowledgement** 

Required to submit. Tick the acknowledgement confirming that you will not delete any chat and that doing so fails the entire task. This covers **every** chat used in the task, on both sides. 

**BEFORE YOU SUBMIT** 

Correct account and correct model, with a legible pre-run selector screenshot. **Where the task lists two demo accounts, each model was run on its own account**, with a screenshot of each. 

**Extended thinking enabled on both models**, where the batch calls for it. 

**[Aspirational]** Environment rehydrated before **_each_** run, and connectors set up inside GPT or Claude. 

Opening prompt pasted verbatim as Turn 1, unmodified. 

20+ turns, with no padding turns counted toward the total. 

Every turn logged with its exact prompt as the entry title, in order, with no gaps. 

A Turn Link filled on **_every_** turn of **_every_** model — a distinct per-turn link where the product issues one, otherwise the single conversation link repeated. 

Per-turn attachments filed for every turn where the model generated or modified files. 

Exactly **one** key turn marked per model, with a justification, and it is **not** Turn 1. 

**Trajectory captured for** **_every_ model** — share link pasted, **Capture Files** and **Save** both pressed, and the conversation actually visible on the Agent Execution step. 

Final trajectory link opens in an incognito window. 

Chat PDF matches the live share page. 

Final output files uploaded — latest versions only, and every named file the model claimed. 

Every rubric criterion graded and turn-annotated. 

Every dimension rated with a 200+ character justification; turns cited on every score of 1–4; N/A used only where the form offers it. 

Safety answered, with category, justification and turns if flagged Yes. 

Preference recorded with an evidence-backed summary, consistent with the grades and ratings. 

**Every written reference to a model says "Model A" or "Model B"** — no product names, no version strings, no C/D labels. 

**[Aspirational]** Input file paths corrected by hand and each input file uploaded from the workspace. 

Lint and coherence flags actually addressed, not skipped. 

**On a follow-on task: the pre-filled side was actually read**, and either stands up to scrutiny or has been re-run. It goes out under your name. 

**No chat deleted.** 

#### **Checks that fail a task outright** 

No matter how good the rest of the work is: 

Final trajectory link missing, or not a valid public share page. 

Fewer than 7 turns. 

A named file claimed in the response with no matching upload. 

Turn 1 selected as the key turn. 

An uploaded PDF that contradicts the live share page, or a duplicate submission. 

A deleted chat, or a deleted trajectory — including a pre-filled one. If a pre-filled trajectory does not hold up, **re-run it**; never delete it. 

Everything else is graded by degree: rubric-grade accuracy, the accuracy of your turn citations, the quality and evidence of your justifications, and whether your grades, ratings and preference agree with each other. 

## **18. Edge cases** 

|**Situation**|**What to do**|
|---|---|
|Your Traffic task has no universe, no<br>hydration step, no input artifacts and<br>no Known / Not Known.|**Expected.** All four are Aspirational-only. Run the item from<br>the opening prompt, the user goal and the target<br>deliverables.|
|A Traffic task **_does_** show input artifacts or<br>Known / Not Known — even as empty<br>fields you cannot get past.|**Skip the task and report it** so it can be backfilled. Do not enter<br>a placeholder path or upload an unrelated file to clear the<br>validation.|
|[Aspirational] The input file paths look<br>wrong, or the upload links are one long<br>compound link.|**Known defect with a workaround — apply it rather than**<br>**reporting.** Split the compound link, download one file at a time, find<br>it in the workspace, write the correct <mark>folder/folder/file</mark> path yourself,<br>and upload the workspace copy. See <u>section 5</u>.|
|The task lists two sets of demo<br>credentials and both models show the<br>same version string.|**Expected on that batch.** The two accounts point at different<br>backend endpoints, so **the account is the model.** Run each model<br>on its own account and do not hunt for a different version in the<br>selector.|
|You cannot find "Extended thinking" in<br>the model dropdown.|It is the last entry, below a divider under the version list. It is<br>per account, so enable it again after switching to the second<br>demo account.|
|Your comparison model is **Gemini Spark**<br>and there is no Share option anywhere.|**Expected — Spark issues no share links.** Capture the<br>conversation with Chrome's **Save As… → Webpage, Single File**<br>and upload the saved file. Full workflow in **Gemini vs. Gemini**<br>**Spark**.|



|**Situation**|**What to do**|
|---|---|
|A Traffic prompt asks for something out of<br>a specific universe — a named file, thread<br>or event.|**Report the task and skip it.** Traffic prompts must be standalone.<br>Do not choose a universe yourself, hydrate an account, or invent<br>the missing content.|
|An Aspirational task has no Known /<br>Not Known.|Report it — the task was likely built with the wrong type. Do not<br>write the split yourself.|
|Your task has no eval sandbox steps<br>(<mark>/trajectory</mark>, <mark>/grading</mark>,<br><mark>/dimensions</mark>, <mark>/sxs</mark>).|**Expected.** They are missing from most tasks and may not be re<br>added — that coverage is moving to in-task endpoint evals.<br>Complete and submit the task without them. **This does not excuse**<br>**the trajectory capture sandbox**, which is a different step.|
|The Agent Execution step is empty after<br>you ran the capture sandbox.|You almost certainly clicked **Capture Files** but not **Save**. Go back<br>to the sandbox, capture and save again.|
|The capture sandbox reports a different<br>turn count from the one you logged, or the<br>export fails.|Wrong link, or a browser URL instead of a share link. Type <mark>paste</mark><br><mark>url</mark> in the terminal and re-run with the correct public share link.|
|You skipped the <mark>URL></mark> prompt with Ctrl-C<br>and moved on.|Nothing was exported. Return to the sandbox step, type <mark>paste-url</mark>,<br>and complete the capture before submitting.|
|The GTFA or target outcomes look<br>low quality.|Leave the prompt and target deliverables exactly as they are —<br>that content comes from the customer. **You may correct the GTFA**<br>if you can make it more accurate, but never edit it to match a<br>model's output.|
|The model only produced one share link<br>for the whole conversation.|Paste that same link into every turn's Turn Link field and into the<br>final trajectory link. This is expected on products that do not issue<br>per-turn links.|
|The product refuses or stalls early.|Keep going and capture it. A refusal is real evidence — grade<br>the affected criteria as fails and annotate the turn where it<br>happened.|
|A connector errors or times out mid-run.|Keep going and recover naturally. Record it under Tool &<br>connector reliability and Recovery Overhead, with turns.|
|The run naturally finishes before 20 turns.|Add real work — a new artifact, a cross-source reconciliation, a<br>mid task correction. Do not pad with re-confirmations; they do not<br>count.|
|The run produced no outputs at all.|Record that honestly and grade accordingly. It is a legitimate result<br>for a hard item.|
|The model sends an email or shares a<br>file when it should have drafted.|Fail the relevant criterion and flag it under Safety (unauthorized<br>send) with the turn number.|
|The model claims it did something<br>you cannot verify in the account.|Fail the criterion and call it out under Trust & grounding<br>(Action Honesty) with the turn.|



|**Situation**|**What to do**|
|---|---|
|No tools were called, or no<br>cross-turn memory was needed.|If the task shows an applicability toggle for that dimension, set it<br>to not-applicable. If it does not, rate 1–5 and say so in the<br>justification.|
|You need outside knowledge — an<br>API, a library, a debugging technique.|Allowed. Only universe-specific entities (people, files, dates,<br>events, emails, calendar items) must stay grounded.|
|A pre-filled trajectory looks weak, or its link<br>is broken.|**Your call, and your name on it.** Keep it if it holds up; otherwise **re**<br>**run it or build it from scratch.** Never delete it, and raise anything<br>you are unsure about in the War Room.|
|You are asked to "improve another<br>contributor's" work.|**Ignore it** — the message is automatic and there are no reviews on<br>this project at the moment.|
|A rubric criterion has a typo or a<br>grammatical error.|**Correct it**, keeping the criterion's core intent and wording. Do<br>not reword it wholesale, change its weight, or add or remove<br>criteria.|
|A rubric criterion is genuinely<br>unscoreable, inaccurate, or contradicts<br>the prompt.|Beyond a typo fix. Grade it as best you can and flag it in the<br>War Room.|
|The demo account is stuck on a<br>2-Step Verification prompt.|Known blocker, left behind by an expired task. **Join the War**<br>**Room session** to be given a working account, or **skip the task.**<br>Never substitute an account of your own.|
|You forgot a turn's share link.|It cannot be recovered. Save every subsequent link and flag it in<br>the War Room rather than substituting a browser URL.|
|You accidentally deleted a chat.|Raise it in the War Room immediately — the links are<br>permanently dead and the task cannot be reviewed as-is.|
|You realise mid-run you selected the<br>wrong model or account.|Stop. The run cannot be salvaged. Rehydrate and start again on the<br>correct model, and raise it in the War Room if the task is already<br>partly filled.|



## **19. Common mistakes** 

Selecting the wrong model when both sides are Gemini. 

Running a model on the wrong account — the custom model on a paid account, or the demo model on a personal Gmail. 

Running both models on the Model A demo account when the task supplied two, producing two runs of the same model. 

Reporting the matching version strings on a two-account batch as a broken task, or hunting the selector for a version that is not exposed there. 

Enabling Extended thinking on the first model and forgetting it after switching accounts. 

Trying to sign into GPT or Claude with the Gemini demo credentials. 

Treating a missing universe, hydration step or input artifact on a Traffic task as a bug, or hunting for a universe to hydrate from. 

Filling an Aspirational-only field that should not be on a Traffic task — a placeholder file path, a recycled screenshot — to get past a validation block, instead of skipping and reporting. 

Rewriting the opening prompt or the target deliverables because they look weak. The GTFA may be written and the rubric for typos, grammar, or structural defects (such as atomicity and self-containment) — nothing else. 

Rewording a rubric criterion, or changing what it measures, under cover of "fixing a typo". 

Rewording the opening prompt instead of pasting it verbatim. 

Skipping rehydration between the two runs on an Aspirational task. 

Copying browser address-bar URLs instead of using Share. 

Leaving Turn Link blank on GPT or Claude, instead of repeating the single conversation link on every turn. 

Collecting links only at the end instead of after every turn. 

Fewer turn entries than actual turns, or entries retitled instead of quoting the exact prompt. 

Padding turns by re-confirming or restating. 

Steering by dumping the deliverables in one turn, or nudging the model toward the answer. 

Marking more than one key turn, or defaulting the key turn to Turn 1. 

Passing a criterion on a described intention rather than a produced artifact. 

Applying a different evidence bar to the two models. 

Justifications under 200 characters, or padded to 200 without citing evidence. 

Naming a model by product or version — or by its C/D label — in a justification or comparison summary, instead of "Model A" and "Model B". 

Retyping a quote instead of pasting it verbatim. 

Uploading intermediate drafts in the final-outputs field. 

Claiming a named file that is not uploaded. 

Ratings that contradict the rubric grades. 

A preference that contradicts the grades and ratings, or leaves a large-gap dimension unaddressed. 

Getting the SxS slots backwards. 

Submitting a pre-filled trajectory you never actually read, on the assumption that someone else owns it. 

Re-running a perfectly usable pre-filled trajectory out of habit, instead of reusing the baseline. Clicking "skipping lint review" to get past a real flag. 

Capturing the trajectory but never pressing **Save**, leaving the Agent Execution step empty. Pasting the wrong model's share link into the capture sandbox, so one model's trajectory is filed twice. 

Skipping the capture sandbox because "the sandbox steps are optional" — that applies to the eval sandbox commands, not to trajectory capture. 

Running a sandbox command and never pressing Snapshot and Save, so the result never reaches the task. 

Typing <mark>/grading</mark> without a product letter, or running two products in one command. Deleting or tidying up chats after submitting. 

## **20. Glossary** 

|**Term**|**Meaning**|
|---|---|
|**Item**|The finished evaluation unit from the Prompt and Rubrics queue: opening prompt ·<br>target deliverables · GTFA · weighted rubric, plus a user goal on seeded items or a<br>Known / Not Known on items built from scratch. Read-only here, except that the GTFA<br>may be corrected for accuracy and the rubric for typos.|
|**Traffic task**|An item built from real customer traffic. **Standalone: no universe, no hydration,**<br>**no connectors, no input artifacts, no Known / Not Known, no CUJ.** You still run<br>both models and score them exactly as on any other task.|
|**Aspirational task**|An item built inside a universe. Carries environment context, input artifacts, Known /<br>Not Known and a CUJ, and requires hydration before every run plus connector setup<br>inside GPT or Claude.|
|**Universe**|The synthetic Gmail, Drive and Calendar environment an Aspirational item was<br>written against. Named in the task requirements — never chosen by you.|
|**User goal**|The concrete outcome the user is pursuing across the conversation. Present on<br>seeded items; steer toward it.|
|**Base model**|Gemini. One side of every comparison, run once and reused across the task sequence.|
|**Comparison model**|The other side of the comparison. Changes from task to task; named in your<br>task requirements.|
|**Base task**|The first task on an item. You run and score both sides.|
|**Follow-on task**|A later task on the same item, arriving with the base-model side pre-filled. You run<br>and score the comparison model, and you check the pre-filled side — it submits<br>under your name, and you may re-run it if it does not hold up.|
|**Trajectory**|The full multi-turn conversation between you and one model, from the opening prompt<br>to the final deliverable.|
|**Turn**|One prompt from you plus the model's reply. Each turn needs its own entry, its<br>attachments, and a Turn Link — a distinct per-turn share link where the product<br>issues one, otherwise the conversation's single share link repeated.|
|**Key turn**|The single turn per model where the run was genuinely decided. Exactly one per<br>model. Never Turn 1.|



|**Term**|**Meaning**|
|---|---|
|**Public share link**|A link created with the product's Share feature that anyone can open — not the session<br>private browser URL. **Gemini Spark has none**; its trajectory is captured as a saved<br>page instead.|
|**Model A / Model B**|The two sides of the comparison, and **the only names to use in writing.** The<br>customer's delivery sheet has one row per pair with columns "A" and "B" only.|
|**Gemini Spark**|Google's agent mode inside the Gemini app, reached from the sidebar via **Switch to**<br>**Spark**. Runs on the **same** demo account as the standard Gemini side, and produces<br>no share link.|
|**Extended thinking**|A Gemini dropdown setting, below the version list. Where a batch requires it, it must be<br>on for **both** models, and it does not carry across accounts.|
|**Artifact**|Any file output produced by a run (PDF, image, CSV, patch), or a final written output<br>such as an email draft.|
|**Trajectory capture**|The per-model sandbox step where you paste the share link and the conversation is<br>exported to <mark>trajectory.json</mark>. Requires **Capture Files** then **Save**. Feeds the linters and<br>in-task evals.|
|**Agent Execution**|The step directly after each capture sandbox, where the exported conversation<br>renders turn by turn. Empty here means the capture did not save.|
|**In-task endpoint eval**|An automated check that runs against the captured trajectory inside the task,<br>replacing the hand-run eval sandbox commands.|
|**Rehydration / reset**|Restoring the account and universe to their original baseline before a run.|
|**Pointwise rating**|Rating one model on its own merits, independent of the other.|
|**Preference**|The single 1–7 judgment of which model did better overall.|
|**SxS**|Side-by-side — a recorded preference between the two trajectories on one item.|
|**CUJ**|Critical User Journey — the customer segment the item exercises.|



