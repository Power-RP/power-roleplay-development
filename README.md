PowerRP Development Board — Bug Reporting Guide
==============================================

Purpose
-------

This GitHub repository is the official PowerRP Development Board for bug reports and implementation requests. The fastest way for our developers to help you is for you to submit a clean, detailed issue that follows the template.

This guide explains:
1. How to submit a bug report through GitHub Issues
2. What “good” bug reports look like
3. The exact workflow our team follows after you submit
4. How we communicate updates, fixes, and closures


Where to Report Bugs
--------------------

All bug reports must be submitted through the GitHub “Issues” tab for this repository.

Do not report bugs in Discord chats and expect them to be tracked long-term.
Discord is good for quick questions, but Issues are where bugs get logged, assigned, tested, and resolved.


Step-by-Step: How to Report a Bug
---------------------------------

1. Open the repository page in your browser.

2. Click the “Issues” tab at the top of the repository.

3. Before creating a new issue, search to see if it already exists.
   Type keywords related to the bug (resource name, error message, feature name, UI page name, etc.).
   If an issue already exists, do not make a duplicate.
   Instead, open the existing issue and add a comment with anything new you can provide (more details, logs, reproduction steps, screenshots, and whether it still happens).

4. Click “New issue”.

5. Select the appropriate issue template.
   This repository uses templates to ensure every report contains the required information.

6. Fill out the template completely.
   Do not remove sections from the template.
   If you do not know a field, write “Unknown” instead of deleting it.

7. Submit the issue.


How to Write a High-Quality Bug Report
--------------------------------------

A good bug report answers four questions clearly:
1. What happened?
2. What did you expect to happen?
3. How can we reproduce it?
4. What evidence proves it?

When your report is detailed, it gets triaged and fixed much faster.

What to Include (Follow the Template Exactly)
---------------------------------------------

1. Clear title
   Your title should describe the bug in one line.
   Good example: “Garage menu freezes when opening at Legion Square with ox_inventory enabled”
   Bad example: “Help” or “Bug”

2. Description of the problem
   Explain what you were doing and what went wrong.
   Keep it factual and specific.

3. Expected behavior vs actual behavior
   Expected behavior: what should happen if the system works correctly
   Actual behavior: what happened instead

4. Steps to reproduce (most important section)
   Provide a numbered sequence that someone else can follow exactly.
   Example:
   1. Join the server and spawn as a civilian
   2. Walk to X location
   3. Open the radial menu
   4. Select “Garage”
   5. Observe the freeze after clicking “Take Out Vehicle”

   If we cannot reproduce it, we cannot reliably fix it.

5. Frequency and scope
   Tell us how often it happens:
   Happens every time
   Happens sometimes
   Happened once

   Also tell us who it affects:
   Only you
   Your group
   Random players
   Everyone

6. Evidence (screenshots, clips, logs)
   The best evidence is:
   Server console errors
   Client F8 console errors
   txAdmin logs
   Screenshots of the issue
   Short video clips showing the steps and result

   If there is an error message, paste it exactly as shown.
   If there are logs, include the relevant section, not only “it errors”.

7. Environment details
   Include anything that can change behavior, such as:
   Resource name involved
   Any recent changes you know about (new update, new script, new config)
   Your job/role in-game if relevant
   Location/zone in-game if relevant
   Time it occurred (approximate)
   Whether it happens after a restart only, or anytime


Common Reasons Issues Get Delayed
---------------------------------

1. Missing steps to reproduce
   “It’s broken” is not actionable without a reproduction path.

2. No logs or proof
   Many issues look the same from the outside.
   Logs tell us which part actually failed.

3. Duplicates
   If the issue already exists, the team will close duplicates to keep tracking clean.

4. Mixing multiple bugs into one issue
   One issue should cover one bug.
   If you have multiple different bugs, submit separate issues so each can be tracked, assigned, and tested properly.


What Happens After You Submit an Issue
--------------------------------------

Once you submit, it enters our workflow. Here is the full process so you know what to expect.

Stage 1: Intake and initial triage
----------------------------------

A developer or staff member reviews your issue to confirm:
1. The report follows the template
2. The bug description makes sense
3. Steps to reproduce exist
4. Evidence is included if needed

Possible outcomes at this stage:
1. Accepted for investigation
   We understand the issue and will proceed to reproduce it.

2. Request for more information
   If something is missing, we will comment asking for specific details.
   Example: “Please provide F8 log output after reproducing” or “Which resource version are you on?”

3. Marked as duplicate
   We will close it and link the original issue so everything stays tracked in one place.

4. Not a bug / intended behavior
   If it matches intended behavior or a known rule, we may close it with an explanation.

Stage 2: Reproduction and verification
--------------------------------------

We attempt to reproduce the bug using your steps.
If we reproduce it, the issue is confirmed.

If we cannot reproduce it, we will ask for:
1. More precise steps
2. A video clip showing exact steps
3. Additional logs
4. Additional context (job, location, time, what happened right before, etc.)

If we still cannot reproduce after reasonable attempts, the issue may be closed as “Cannot reproduce”.
If it happens again later, you can reopen or create a new issue with better evidence.

Stage 3: Priority and severity assignment
-----------------------------------------

Confirmed issues are prioritized based on impact.

High priority examples:
1. Server crashes or severe performance degradation
2. Exploits or dupes
3. Bugs affecting many players or key systems (economy, inventory, jobs, PD/EMS core loops)
4. Data loss (items, money, vehicles, properties)

Lower priority examples:
1. Cosmetic issues
2. Minor UI alignment issues
3. Rare edge cases with very low impact
4. Quality-of-life improvements (these may be moved to feature requests)

Stage 4: Work begins (fix or change)
------------------------------------

If the issue is approved for fixing:
1. A developer investigates the root cause
2. A fix is implemented
3. The fix is tested in a controlled environment
4. If safe, it is prepared for deployment

Depending on the type of issue, you may see:
1. A request to test on your side
2. A note that it will be included in a future patch
3. A question about expected behavior to confirm intended design

Stage 5: Resolution outcomes (what you’ll see on the issue)
-----------------------------------------------------------

When work is complete, one of these will happen:

1. Fixed
   We implemented a fix and confirmed it works in testing.
   The issue will be closed with a note describing the fix and, when applicable, when it will be live.

2. Closed as duplicate
   Your issue was already reported.
   We will link the original issue.

3. Closed as not a bug / intended behavior
   The system is working as designed.
   We will explain why and what to do instead (when applicable).

4. Closed as cannot reproduce
   We could not reproduce the bug with the information provided.
   If you can reproduce again, reopen the issue or post new evidence.

5. Won’t fix / out of scope
   This is rare, but sometimes a “fix” would cause bigger problems than it solves, or it conflicts with design direction.
   If so, we will explain the reasoning.

6. Needs more information
   The issue stays open, but we are waiting on your requested details.
   If no response is provided after a reasonable period, it may be closed to keep the board clean.


How We Will Respond (What You Should Expect)
--------------------------------------------

We respond in the issue thread so it stays tracked and searchable.

Typical responses include:
1. Confirmation that we reproduced the issue
2. Questions requesting missing details
3. Updates on status changes (triaged, investigating, fixed, deployed)
4. A closing message describing the outcome

Response timing can vary based on:
1. Severity and priority
2. Developer workload
3. Whether the bug is reproducible
4. Whether it requires deep testing or touches sensitive systems


How You Can Help Us Fix It Faster
---------------------------------

1. Follow the template with complete details
2. Provide exact reproduction steps
3. Include logs and clips
4. Mention recent changes (did this start after an update?)
5. Keep one issue per bug
6. Reply quickly if we request more information


Good Example vs Bad Example
---------------------------

Bad report:
“Inventory is broken. Fix it.”

Good report:
Title: “ox_inventory: stash search crashes client when opening gang stash at Legion”
Description: “When opening the gang stash at Legion, the stash UI loads then freezes.”
Expected: “Stash UI opens and I can move items.”
Actual: “UI freezes and client becomes unresponsive.”
Steps:
1. Join server
2. Go to Legion gang stash
3. Press E to open stash
4. Type any letter in the search box
5. Observe freeze
Evidence: “F8 error: [paste here]”
Frequency: “Every time”
Scope: “Happens to multiple gang members”
Notes: “Started after the last update”


Final Notes
-----------

If you want something changed or added (not a bug), submit it as an implementation request in Issues as well, but be clear it is a feature request, not a bug.

Thank you for keeping reports clean and detailed.
When issues are written well, fixes ship faster and everyone wins.
