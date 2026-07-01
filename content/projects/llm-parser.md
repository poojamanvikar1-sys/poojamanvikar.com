---
title: LLM Conversation Parser
---
**What**

I'm currently running a short-term pilot to measure a mechanism of an AI Safety concept.

To test this, I run the same conditions across multiple products(ChatGPT, Claude & Gemini), context lengths, and memory settings, and score each conversation against a fixed marker set that I created. The scoring itself is manual and intentional. But getting from a raw transcript to a scoreable, structured row in Google sheets is a lengthy, manual process I wanted to avoid. So I built a general-purpose parser for it. My research study is its first real use case.

**Why is it tedious to do manually**

The study design captures conversations across three products, two context lengths (short/long), two memory states (on/off) and calibration runs. That's at least 12+ runs where I need to take the raw conversations, convert them to the appropriate rows & columns, making sure they are aligned to manually mark them consistently across products & instances.

Doing this by hand worked for the first two and soon it became too tedious for me where I spent about 2+ hours on making sure to check if I mislabeled, dropped a row or forget to paste the data to the right column. The scoring part of my pilot needs to be manual, not this step.

**What I built** 
- A Python parser (`transcript_to_sheet.py`) that reads the raw transcript that I copy into a .txt file and label the turns from me and AI responses.
- A `CLAUDE.md` file that Claude Code reads automatically, so I don't re-explain the workflow every session.

Usage is one command: `python3 transcript_to_sheet.py FILENAME.txt --runid <ID> --product <NAME> --model "<VERSION>" --context <short|long> --memory <on|off>`

If I don't supply all five inputs, Claude Code asks for the missing ones before running instead of guessing. Each run produces `FILENAME.score.csv` (paired rows for scoring) and `FILENAME.runlog.csv`(this keeps the running list of all the runs across the products & lengths/memory conditions I have chosen).

**The guardrails I set**

The instruction file scope includes:

- The parser should be doing data entry only(converting my raw conversation into right rows & columns). It never fills/touches the rest of the evaluation columns. 
- It shouldn't assume labels. If a transcript file I created isn't already labeled `Me:` / `AI:`, the tool stops and tells me to label it first, rather than guessing who said what.
- It self checks the output. After each run, it reports how many paired rows landed in the score CSV (not the raw turn count, which is a different and not useful to my pilot), confirms both files were written, and flags anything that looks wrong.

The point of this tool is to stop me from producing bad raw data given the significant portion of my pilot is manual. It's a small tool. But the reason it's useful is because the tool has exactly one job, it does that job the same way every time that helps me capture data across products, scenarios & context.