**R E F E R E N C E G U I D E  ·  B O T H Q U E U E S** 

# **Account Hydration** 

Every Honeybee task runs against a synthetic Google account pre-loaded with a persona's mail, files and calendar. This is how you create that account once, and how you reset it before every run. 

#### **CONTENTS** 

1. What hydration is, and why it matters 
2. Before you begin 
3. First-time setup 
4. Resetting between runs 
5. Proving which account you used 
6. Universes 
7. Troubleshooting 

## **1. What hydration is, and why it matters** 

##### **WHO NEEDS THIS GUIDE** 

- **Honeybee SxS, Aspirational** — **yes.** You reset before every run, and twice on a base task. Read this before your first one. 

- **Honeybee SxS, Traffic** — **no reset.** There is no universe behind the item, so there is nothing to hydrate and nothing to restore. You **_do_** still sign into the demo account the task assigns you, because that is what carries the paid Gemini subscription — but you never reset it, and you will not find pre-loaded emails, files or events in it for that item. 

- **Prompt and Rubrics, Type 2 (Aspirational)** — **yes.** Your universe lives in a hydrated account and the simplified trajectory runs against it. 

- **Prompt and Rubrics, Type 1 (Traffic)** — **no. None of this applies.** 

**The dividing line is the task type, not the queue.** Hydration exists to put a universe in front of a model. Aspirational tasks have a universe; Traffic tasks do not, in either queue. 

A Traffic task has **no universe and no persona**, so there is nothing to hydrate and nothing to reset. In Prompt and Rubrics it also has no assigned account and no model run, so the setup and reset links play no part in that flow at all. **If you work only on Traffic tasks in Prompt and Rubrics, you can skip this guide entirely**; on Traffic tasks in SxS you need only the account setup in section 3, never the reset. 

##### **WHICH UNIVERSE DO I HYDRATE FROM?** 

You never choose. **On an Aspirational task the universe is named in the task requirements**, and you hydrate and reset that one. **On a Traffic task there is no universe to name** — the prompt is standalone and must not depend on a specific file, mailbox or calendar. If a Traffic prompt asks for something out of a universe, **report the task and skip it** rather than picking an environment yourself. Hydrating an arbitrary universe produces a run the item's rubric cannot score. 

Honeybee tasks are not run against mock data. They run against a **real Google account** — real Gmail, real Drive, real Calendar — that has been filled with the synthetic life of a fictional persona: their emails, their documents, their meetings. Filling that account is called **hydration**. Emptying it back to how it started is called a **reset** or **rehydration**. 

You create **one Gmail address** and keep it for the whole project. Everything after that is done through one of two links, and picking the wrong one is the most common setup mistake. 

|**Situation**|**Which link**|**What happens**|
|---|---|---|
|**Your very first account**|[`/setup`](https://synthetic-account-hydration.outlier.ai/setup)|Connects your new Gmail address and hydrates it<br>with your assigned universe.|
|**A different persona or universe**|[`/setup`](https://synthetic-account-hydration.outlier.ai/setup)|Same address, new universe selected from the<br>dropdown. **Do not create a second Gmail**<br>**account.**|
|**Same persona, new task**|[`/reset`](https://synthetic-account-hydration.outlier.ai/reset)|Wipes everything created since hydration and<br>returns the account to its baseline.|
|**Same persona, next model run**|[`/reset`](https://synthetic-account-hydration.outlier.ai/reset)|The same wipe, between the two models of a base<br>task.|



Put simply: **`/setup` changes** **_whose life_ is in the account.** **`/reset` puts that same life back to how it started.** The setup link is rare — first account, then only on a persona or universe change. The reset link is constant. 

##### **WHY THE RESET IS NOT OPTIONAL** 

The models in this project take real actions. They create calendar events, save Drive files and leave Gmail drafts. Those changes persist after the run ends. 

So if you run a second model without resetting first, it starts in a world the first model already rearranged — reading drafts it never wrote, seeing events it never created. **The two runs are then measuring different environments, and the comparison between them is worthless.** No amount of careful grading afterwards can repair it, because the damage is in the data, not in the judgement. 

##### **RESET BEFORE, NEVER AFTER** 

Reset **_before_** a run, not after one. Everything the model produced during a run is evidence you still need — files to upload, drafts to check, events to verify against your rubric grading. Resetting while a task is still open destroys your own evidence. 

## **2. Before you begin** 

### **Create a fresh Gmail address — once** 

Do not reuse a personal account, and do not reuse an account from another project. Hydration writes a large amount of synthetic data into whatever account you point it at, and the reset wipes changes back to that baseline — neither is something you want happening to a real inbox. 

Name the new address after **your first universe persona's first name**, plus any convention of your own: 

`PersonaFirstName.YourOwnConvention@gmail.com`<br>
For example: `nadia.honeybee23@gmail.com` 

##### **ONE ADDRESS, REUSED FOR EVERY PERSONA** 

This address stays with you for the whole project. **When you move to a different persona or universe, you keep the same Gmail account** and re-run <u>`/setup`</u> with the new universe selected. Do not create a second address, and do not ask for a new one. 

A consequence worth knowing up front: **the persona name in your address will stop matching the persona you are working on.** That is expected and is not a problem to fix. The name is a label from your first setup, not a live indicator — the universe dropdown is what determines whose data is actually in the account. 

### **Know which universe you are on** 

**Where a task needs a particular universe, that universe is named in the task's own requirements.** Work from what the task tells you rather than choosing one yourself, and ask your QM only if the task does not name one. 

You select it from a dropdown during setup, and the choice determines the entire contents of the account — the persona, their job, their contacts, their files. Hydrating the wrong universe means every entity you later reference in a prompt belongs to somebody else's task. 

Check this again **every time you are moved to a new persona or universe**, because that is the moment you return to the setup link. Between those moves, the universe does not change and the reset link is all you need. 

### **Be signed in to Outlier** 

Open the setup link in a browser that is **already logged in to outlier.ai**. The hydrator authenticates through that session. 

## **3. Setup — first time, and on every universe change** 

Budget about ten minutes, most of it waiting. You run this flow **once to create your account, and again each time you are moved to a different persona or universe** — same Gmail address, different selection in the dropdown. Between those moves you never come back here; you use the reset link instead. 

###### **Step 1** 

### **Open the setup page and enter your details** 

Go to `synthetic-account-hydration.outlier.ai/setup`. Choose your assigned universe from the **Task workspace** dropdown, type the fresh Gmail address you created, and click **Continue with Google**. 


![](images/Hydration/Hydration.pdf-0005-03.png)


**Enter the exact address you created.** Google will ask you to confirm this precise account on the next screen — if you mistype it here, the flow fails rather than hydrating the wrong inbox. 

###### **Step 2** 

### **Click through the "hasn't verified this app" warning** 

You may see a red warning screen. **This is expected** — the hydrator is an internal tool and is not a published Google app. It is not a sign that something has gone wrong. 

Click **Advanced** at the bottom left, then **Go to outlier.ai (unsafe)**. 

![](images/Hydration/Hydration.pdf-0006-x47.png)

**The warning as it first appears.** The **_Advanced_** link is easy to miss — it is small, grey, and bottom-left, well away from the blue button. 

![](images/Hydration/Hydration.pdf-0007-x51.png)

**After clicking Advanced.** Click **_Go to outlier.ai (unsafe)_** to continue. If you do not see this screen at all, skip ahead — some accounts go straight to permissions. 

###### **Step 3** 

### **Grant all three permissions** 

Tick **Select all** and continue. The hydrator needs Gmail, Drive and Calendar because it writes the persona's data into all three, and the reset later has to clear all three. 


![](images/Hydration/Hydration.pdf-0008-03.png)


**All three boxes must be ticked.** Granting only some of them produces an account that hydrates partially — usually mail but no Drive files — which is confusing to diagnose later, because the account looks populated at first glance. 

##### **ON THE PASSWORD QUESTION** 

The hydrator never asks for or stores your Google password. Authentication happens on Google's own screens, and Google shows you the permission list before you approve it. If anything ever asks you to type a Google password into an Outlier page, stop and raise it in the War Room. 

###### **Step 4** 

### **Wait for hydration to finish** 

You land on a progress screen. **Hydration can take up to five minutes.** Open the new Gmail account in another tab and watch: mail, Drive items and calendar entries appear progressively as it runs. 


![](images/Hydration/Hydration.pdf-0009-03.png)


**The account is populating.** The address shown under **_Use this exact Google account_** is the one being hydrated — worth a last check that it matches the one you meant. 

**Do not start a task until the account genuinely looks lived-in.** A persona whose Drive is still empty will not support a grounded prompt, and any item you build on a half-hydrated account will reference entities that are not there. 

## **4. Resetting between runs** 

This is the part you do over and over. It is much shorter than setup. 

###### **Step 1** 

### **Open the reset page and pick your account** 

Go to `synthetic-account-hydration.outlier.ai/reset` and find your address in the **Connected account** dropdown. If it is not listed, select **My account is not listed** and type it in manually. 

Tick the box acknowledging that changes made after hydration will be removed, then click **Restore baseline**. 


![](images/Hydration/Hydration.pdf-0010-04.png)


**The account dropdown, open.** The acknowledgement checkbox is not a formality — restoring genuinely deletes everything created since hydration, including anything you still need. 

###### **Step 2** 

### **Wait for the green confirmation** 

Progress updates appear as it runs. **Wait for "Your workspace is restored" before you open a chat.** During busy periods you may sit in a queue for a while — that is normal, and starting early means running your model against a half-reset environment. 


![](images/Hydration/Hydration.pdf-0011-03.png)


**This green box is the go signal.** Anything before it is not finished, however complete the account may look in another tab. 

### **When to reset** 

|**Moment**|**Reset?**|**Why**|
|---|---|---|
|Before starting a new **Aspirational**<br>task|**Yes**|The previous task left its own changes behind.|
|Before the first model's run<br>**Aspirational**|**Yes**|This is the baseline both models must start from.|
|Before the second model's run<br>**Aspirational base task**|**Yes**|The most commonly skipped reset, and the one that silently<br>invalidates the comparison.|
|Before a Type 2 simplified trajectory|**Yes**|The complexity gate is only meaningful against a clean<br>environment.|
|Moving to a new persona or<br>universe|**Neither**|This one goes through the setup link, not the reset link —<br>same Gmail address, new universe in the dropdown.|
|Midway through a run|**No**|It would destroy the run's own context. Finish, capture your<br>evidence, then reset for the next one.|
|After finishing a run, before<br>uploading files|**No**|You would delete the artifacts you still have to upload and<br>verify.|
|Anywhere on a **Traffic** task, in<br>either queue|**N/A**|No universe, so nothing to restore. In SxS you still run both<br>models on a Traffic task — you just never reset between<br>them, because there is no baseline environment for them to<br>contaminate. In Prompt and Rubrics there is no account or<br>model run at all.|



## **5. Proving which account you used** 

Both queues ask you to **prove on the task** that you ran on the right account. This is not paperwork — a run whose account cannot be verified cannot be trusted, and it can be rejected on that basis alone. 

**I confirm I am logged in with the demo credentials provided above** REQUIRED 

A single checkbox confirming you are signed in as the exact address printed on the step. 

**Upload a screenshot showing you are in the correct Google account** REQUIRED · 1–3 FILES 

The Google account page or the product interface, **with the email address clearly legible**. A crop that hides the address is rejected. 

##### **TAKE THE SCREENSHOT BEFORE THE RUN, NOT AFTER** 

Along with the model-selector screenshot, this is your only evidence of what you actually ran on. Capturing it afterwards is possible but it proves less, and if you have already switched accounts it cannot be reconstructed at all. 

## **6. Universes** 

A **universe** is one persona and the entire synthetic environment attached to them. Your QM assigns yours; you select it in the Task workspace dropdown during setup. 

##### **Coding universes** 

Backend software engineer · Applied ML and data scientist · Indie game designer. 

These three also carry a **backup repository** you fork before starting a code task: 

- Applied ML → `mechlens-backup` 
- Backend → `tidb-backup` 
- Indie Game Designer → `tidewrack-backup` 

Fork the repo, add `-personal-dev` to the end of the name, and **uncheck "Copy the main branch only"** so all branches come across. 

##### **Expert universes** 

Startup founder · Life sciences researcher · Educator and instructional designer · Independent consultant · Creative producer and marketer · Solo operator and owner · Legal and contracts analyst · Independent financial planner · Ghostwriter and nonfiction author · Luxury travel advisor · Residential real estate agent · Student · Property manager · Household manager and parent · Travel and trip planner. 

##### **THE DROPDOWN USES SHORT INTERNAL NAMES** 

The Task workspace dropdown labels universes with compact identifiers such as `creative_producer` rather than the full titles above. Match on the recognisable part of the name, and if two entries look plausible, **confirm with your QM before hydrating** — switching universes afterwards means starting the whole setup again on a fresh address. 

### **Everything you reference must live in your universe** 

This is the rule the entire project rests on. Every file, person, date and event you put in a prompt, a GTFA, a rubric criterion or a steering turn **must actually exist in the hydrated account.** A criterion referencing something that is not there cannot be scored, and an item built on a phantom fails downstream. 

**So explore before you write.** Read the Universe and Environment Context document on the task, then spend real time in Gmail, Drive and Calendar. Make a list of the exact filenames, people and dates you intend to build on, and confirm each one on screen. The most common rejection in the creation queue is a prompt that **_sounds_** grounded — "the Q3 budget deck" — when no such file exists. 

**Never upload or mock an input file.** Everything the model needs is already staged. If a criterion depends on a document, that document lives in the persona's Drive, not in an attachment you added. 

## **7. Troubleshooting** 

|**Problem**|**What to do**|
|---|---|
|The red "Google hasn't verified this app"<br>screen.|Expected. Click **Advanced** → **Go to outlier.ai (unsafe)**.|
|You never saw that warning screen.|Also fine. Some accounts go straight to the permissions screen.|
|Your account is missing from the reset<br>dropdown.|Select **My account is not listed** and type the address manually.|
|Hydration seems stuck.|Give it the full five minutes and watch Gmail in another tab for incoming<br>data. If nothing has arrived after that, raise it in the War Room.|
|The reset is queued for a long time.|Normal under load. Wait for the green confirmation — do not start the<br>run early.|
|Gmail hydrated but Drive is empty.|Permissions were probably granted only in part. Run the setup flow again<br>and tick **Select all**.|
|You hydrated the wrong universe.|Do not build on it. Raise it in the War Room — you will normally need to<br>set up again on a fresh address.|
|You reset mid-task and lost model outputs.|They are gone; the reset is not reversible. Raise it in the War Room rather<br>than reconstructing or re-running quietly.|
|You are unsure which account a<br>screenshot shows.|Retake it with the address clearly visible. An ambiguous screenshot is<br>treated the same as a missing one.|



