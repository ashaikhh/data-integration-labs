# Lab 4 Task 1: My agent Setup

| Question | Answer |
|---|---|
|Tool, version, model |GitHub Copilot in VS Code, VS Code 1.147.0, Copilot Free. Model: *Copilot Fusion*, which picks a model per request: it chose GPT-6 Luna for my first prompt and MAI Code 2 Flash for the plan.|
|Permission mode at start, how I switched |Agent mode with *Manual permissions*. Even so, it created `hello.txt` without asking. Only after I added `"chat.tools.edits.autoApprove": {"**/*":false}` to my user settings did it ask before writing (*Create file? Allow Once/ Skip*). |
|What it did without asking |Read files: yes (*Read agent-test*). Edit files: yes, until I changed the setting above. Run commands: `git log` ran without asking, since it only reads. |
|See and undo changes |The chat shows each change (*Edited hello.txt +2 -0*), and `git status` lists the new file as untracked. *Undo* in the chat removed it; `git status` was clean again.|
|Fresh session, context, quota |*New Chat* (+) at the top of the chat. Quota: The Copilot icon in the status bar shows *Credits 0% used* after this task (Copilot Free, rests on 1 December) and *Inline Suggestions 4% used*. I did not find a display of how full the context window is. |
|Instruction files |`AGENTS.md`, according to the course's table and the VS Code documentation |
|Training on my data |Copilot Free: GitHub may use prompts for training unless switched off. The setting is *Allow GitHub to use my data for AI model training* on github.com/settings/copilot. I have not changed it yet.|

In plan mode (`/plan Add a script that counts the files in this folder.`), it first listed the folder, asked me two questions (which files to count, and the script name), then showed a three-step plan, I rejected; `git status` stayed clean.

## Why this tool?
I chose GitHub Copilot in VS Code because it is free for students (access and cost) and runs inside VS Code, which I already use for Git (integration). Prompts on the free plan may be used for training, so I switched that off (data protection). It reads `AGENTS.md`, an open standard, so our team can share one instruction file even if we use different tools (team consistency). The free plan has limited quota, so I will check it before the lab (usage limits).
