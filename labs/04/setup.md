# Lab 4, Task 1: My agent setup

## First session

In a throwaway repository `agent-test` (one commit with a `README.md`), I asked: *What files are in this folder? Do not change anything.* I no longer remember the details, so I repeated the prompt on 24.11.2026 in my lab repository, where it could only read: Copilot Fusion chose MAI Code 2 Flash, and the agent used one tool, *Find files matching `**/*`* (a file search). It listed the files and changed nothing.

## Finding the brakes

| Test | What happened |
|---|---|
| *Create a file hello.txt with the line Hello.* | The agent created `hello.txt` without asking, although *Manual permissions* was selected. `git status` showed it as untracked. I removed it with *Undo* in the chat. After I added `"chat.tools.edits.autoApprove": {"**/*": false}` to my user settings, the agent asked first (*Create file? Allow Once / Skip*). |
| *Run git log.* | It ran the command without asking, because `git log` only reads. |
| `/plan Add a script that counts the files in this folder.` | It listed the folder, asked me two questions (which files to count, and the name of the script) and showed a plan in three steps. I rejected the plan; `git status` stayed clean. |

## What I found out

| Question | Answer |
|---|---|
| Which tool, which version? Which model answered? | GitHub Copilot in VS Code, VS Code 1.147.0, plan Copilot Free. The model is chosen for me (*Copilot Fusion*, the Auto mode): it chose GPT-6 Luna for my first prompt and MAI Code 2 Flash for the plan. |
| In which permission mode did the tool start, and how did I switch? | A new chat opens in *Agent* mode with *Interactive* and *Manual permissions*, shown below the chat input (checked again on 24.11.2026). VS Code keeps the last choice, so I cannot say for sure what it was at the very first start. *Manual permissions* was not enough for file edits: only the setting `"chat.tools.edits.autoApprove": {"**/*": false}` made it ask before writing. |
| What did it do without asking? | Read files: yes. Edit files: yes, until I added the setting. Run commands: `git log` ran without asking, since it only reads. |
| How do I see what it changed, and how do I undo it? | The chat shows each change with its diff (*Edited hello.txt +2 -0*), and `git status` or `git diff` shows it too. *Undo* in the chat (or *Restore Checkpoint*) reverts it. |
| Fresh session, context window, quota | *New Chat* (+) at the top of the chat starts fresh. The Copilot icon in the status bar showed *Credits 0% used* and *Inline Suggestions 4% used* after this task; the quota resets on 1 December. I did not find a display of how full the context window is. |
| Which instruction files does it read? | `AGENTS.md`, according to the course's table and the VS Code documentation. |
| May my prompts and code be used for training? | On Copilot Free, GitHub may use them unless I switch it off. The setting is *Allow GitHub to use my data for AI model training* on github.com/settings/copilot. I switched it off. |

## Why this tool?

I chose GitHub Copilot in VS Code because Copilot Free costs nothing (access and cost) and it runs inside VS Code, which I already use for Git (integration). On the free plan my prompts may be used for training, so I switched that off (data protection). Copilot itself is not open source, but it reads `AGENTS.md`, an open format, so our team can share one instruction file even though my partner used a different model (openness, team consistency). The free plan has a monthly limit, but this task used almost none of it, so it is enough for the lab (usage limits).