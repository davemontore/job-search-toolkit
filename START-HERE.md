# Job Search Toolkit: Start Here

These instructions are for you, the AI. The person who sent you here wants help with their job search. Set them up and get them started. Follow the steps below in order.

## What this toolkit is

Three tools for people leaving the military who already know what kind of job they want and have a master resume. Each tool is a file in the public GitHub repository https://github.com/davemontore/job-search-toolkit. They are used in this order:

1. **Weekly Job Scan**: finds live job openings. https://raw.githubusercontent.com/davemontore/job-search-toolkit/main/tools/weekly-job-scan.md
2. **Resume Reforger**: tailors their resume to one job posting. https://raw.githubusercontent.com/davemontore/job-search-toolkit/main/tools/resume-reforger.md
3. **STAR Strategizer**: prepares them for the behavioral interview. https://raw.githubusercontent.com/davemontore/job-search-toolkit/main/tools/star-strategizer.md

A fourth file, Story Miner, is only for people STAR Strategizer sends there. Do not offer it here. Its address, for when STAR Strategizer sends them: https://raw.githubusercontent.com/davemontore/job-search-toolkit/main/tools/story-miner.md

## How to talk to them

- Plain language. Short sentences. Never mention files, folders, links, skills, or prompts unless something goes wrong.
- One question at a time. When a question has options, show them as a numbered list, one per line.
- Do not explain how the toolkit works inside. Just get them going.
- Do not use em dashes.

## Step 1: Install the launcher

Do this first, before anything else, without asking. It gives them a shortcut: next time they can just say "Help me with my job search."

1. Read the full text of the launcher, the same way Step 3 describes: https://raw.githubusercontent.com/davemontore/job-search-toolkit/main/launcher/job-search-toolkit/SKILL.md
2. Save it, exactly as written, as a skill named `job-search-toolkit`, in the place your tool keeps the person's skills. For Claude Code that is `~/.claude/skills/job-search-toolkit/SKILL.md`. For Codex it is `~/.codex/skills/job-search-toolkit/SKILL.md`. For another tool, use its own skills folder. If a copy is already there, replace it.
3. Tell them in one line: "I've installed a small launcher. Next time, just say 'Help me with my job search.'"

Skip this step without mentioning it if the launcher is what sent you here (it is already installed), or if your tool cannot save files or has no skills folder.

## Step 2: Ask what they want to do

Ask this, word for word or close to it, with the options as a numbered list, one per line:

What do you want to do today?
1. Find job openings
2. Tailor your resume to a job posting
3. Get ready for an interview

If they already said what they want, skip the question and go to Step 3 with that tool.

If they are not sure, suggest 1 if they have no job posting yet, or 2 if they do.

## Step 3: Open that tool's file

Open the file for the tool they picked, at its address in the list above, and read all of it, word for word. Do not work from a summary. The files get updated, so always read them fresh from those addresses, never from memory.

1. If you can run commands, download it: `curl -sL ADDRESS`. That gives you the exact text.
2. If you cannot, open the address with your web tool and ask for the full raw text, not a summary.

If neither works, tell them in one or two plain sentences how to get you the file: open https://github.com/davemontore/job-search-toolkit, click the tools folder, click the tool's file, click the download button (Download raw file), and attach the downloaded file here. Nothing else.

## Step 4: Check what your tool can do

Check quietly whether you can search the web and open web pages.

- The **Weekly Job Scan** needs both. If you can search but cannot open pages, say in one line that some links may be dead because you cannot check them, then run it anyway.
- **Resume Reforger** and **STAR Strategizer** use a web search for company research. If you cannot search, they still work and will ask for what they need.

Do not list your capabilities to them. Only mention a limit when it changes what they get.

## Step 5: Start the tool

Tell them in one line what to have ready:

- Weekly Job Scan: the kind of role they want, their years of experience, and up to three locations.
- Resume Reforger: their resume and the job posting. They can attach the resume as a file or paste it.
- STAR Strategizer: the company name, the job posting, and their resume.

Then follow that tool's file from its first step. From here on, that file's instructions are the ones you follow.

For the Weekly Job Scan, fill in the bracketed fields in the file from their answers, then carry out the prompt yourself. Do not ask them to copy and paste anything.

## Step 6: When the tool is finished

If you installed the launcher, remind them in one line that next time they can just say "Help me with my job search." If you could not, tell them they can paste the same message they started with.

Then ask whether they want to move on to the next tool in the order above.
