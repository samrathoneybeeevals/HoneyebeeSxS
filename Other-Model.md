# Gemini App/AI Studio Mini-Guidelines

For tasks that use Gemini App and Google’s AI Studio 

## **Module 1: Gemini App** 

### **Step 1 — Open the model picker** 

Open the Gemini App and go to the model selection menu. 

### **Step 2 — Select the model** 

Navigate to **Pro Release Testing → Model Beetle**. 


![](images/Other-Model/Other-Model.pdf-0001-06.png)


### **Quick check** 

Before starting any test, confirm that **Model Beetle** is shown as the active model. 

## **Module 2: AI Studio** 

Go to AI studio: https://aistudio.google.com/prompts/new_chat 

### **Step 1 — Open model selection** 

In AI Studio, look at the **top right** of the screen and open the **Model selection** panel. 

### **Step 2 — Find the confidential models** 

Click **Confidential**, then select **Gemini 4 Argon EAP**. 


![](images/Other-Model/Other-Model.pdf-0002-08.png)


### **Step 3 — Apply the run settings** 

Set each option in the settings panel exactly as shown below. 

|**Setting**|**Value**|**What it means**|
|---|---|---|
|Model|**Gemini 4**<br>**Argon EAP**|The early-access model we are testing|
|Thinking Level|**High**|The model reasons more deeply before answering|
|Structured outputs|**Off**|Responses come back as normal text, not forced<br>into a format like JSON|
|Code Execution|**Off**|The model cannot run code during its response|
|Function Calling|**Off**|The model cannot call external tools or functions|
|Grounding with<br>Google Search|**ON** ✅|The model can search Google to support its<br>answers with current information|
|URL Context|**Off**|The model will not read content from links you<br>paste in|
|Media resolution|**Default**|Leave unchanged|
|Output length|**32768 tokens**|Maximum length of a response|



## **Common mistakes** 

- **Using the wrong model.** Default models are often pre-selected; always check the model name before you begin. 

- **Forgetting Grounding.** It is the only toggle that should be on, and it is easy to miss. 

- **Settings resetting.** AI Studio settings can revert when you start a new chat or session. Re-check the panel each time. 

- **Not finding the model.** If you can't see **Confidential** or **Gemini 4 Argon EAP**, your account may not have access yet. Reach out to the team lead. 

## **Saving Trajectories in AI Studio** 

#### **Saving and sharing your chat** 

1. When you're done, **save the chat**. 

2. Open Google Drive and **check that the file is there**. 

3. Right-click the file and choose **Share**. 

4. Under General access, change it to **Anyone with the link**. This removes access restrictions so reviewers can open it without requesting permission. 

5. Copy the link and share it. 

6. **Make sure Temporary chat is disabled.** 
