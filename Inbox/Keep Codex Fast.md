![[Pasted image 20260502115203.png]]
Codex's app has been super slow for me lately.

at first, I thought the problem was Codex itself.

It wasn’t.

After cleaning things up properly, Codex felt roughly 10X faster. 0 slowness. Before this, I had 8GB of logs built up, and it slowed things down like crazy.

Here’s the 15-point cleanup system, which worked perfectly for me. It won't delete anything.

Copy paste these 15 bullet points when your Codex starts to slow down:

>  it will inspect things first
> back up & archive important files
> and make your Codex blazing fast again.

15 ITEMS TO KEEP CODEX FAST

1. Check what is actually taking space.

Inspect sessions, archived sessions, worktrees, archived worktrees, logs, config, and the local state database.

2. Back up the important files first.

Back up config, global state, session index, state database, memories, skills, plugins, and automations before changing anything.

3. Check if Codex is open.

If Codex is running, only inspect. Apply cleanup after closing it so the local database is not being touched from two places.

4. Find the giant active chats.

Look for the biggest active session files. These are often old conversations that are still treated as active history.

5. Archive old non-pinned chats.

Move chats older than 7-10 days into archived sessions, unless they are pinned or clearly still current.

6. Keep only recent work active.

Your sidebar/history should not be carrying weeks or months old execution threads.

7. Use handoff docs instead of massive chats.

If an old thread matters, turn it into a handoff doc, archive the thread, and resume in a fresh chat from the doc.

8. Normalize weird paths.

On Windows, clean up path mismatches like normal C:\... paths vs extended \\?\C:\... paths.

9. Prune dead config projects.

Remove project paths from config that no longer exist or point to temporary folders.

10. Move stale worktrees.

Don’t keep old Codex worktrees in the hot worktrees folder. Archive them instead of deleting them.

11. Rotate large logs.

Move oversized old logs into an archive folder so Codex can recreate fresh ones.

12. Check heavy background processes.

Look at Node/dev-server processes. Don’t auto-kill them, but close the ones you don’t need.

13. Verify the cleanup.

Afterward, confirm config still parses, the database opens, active session size dropped, archived sessions increased, and no bad paths remain.

14. Turn this into a weekly script.

The cleanup should not be a dramatic one-time rescue mission. Make it repeatable.

15. Make it boring.

Weekly maintenance should back up first, archive old sessions, normalize paths, prune config, move stale worktrees, rotate logs, and give you a report.

The biggest lesson for me: giant chats should not become permanent memory.

Chats are for execution. Handoff docs are for memory. Archives are for history. Fresh threads are for speed.

P.S. Before doing all this, make comprehensive handoff documents for each active chat, too, with prompts prepared for each to reactivate them after. 

This will start new chats from the exact places you left off, but at blazing-fast speed.

Like this, things simply work perfectly.

I even told my Codex to automate these weekly, and it has set it up for every Sunday.

Save this for when you will need it, as Codex app does get heavy as you use it more, especially if you are using many terminals and long sessions a lot.