# [ContextKeeper for Visual Studio](https://contextkeeper.io)

Your favorite files and contexts under your fingertips. Safely store and switch between **documents sets**  in seconds using **simple JSON files** 🔥  ContextKeeper is a modern replacement for Save All Tabs extension.

[**Automatically switch contexts** when changing Git branches](https://contextkeeper.io/blog/automatic-snapshot-switching-when-changing-branches-v1/).

Looking for **ARM-compatible build** or **VS 2019/2017/2015 support**? [Download from here](https://contextkeeper.io/downloads).

### The context is made by:

* logical state
  * your favorites files (non-solution files are also supported)
  * last opened files, order and state including last selected line&column
  * pinned tabs
  * tabs groups
  * breakpoints
  * bookmarks

* visual state
  * main IDE window position and size
  * floating windows position and size
  * docked state and horizontal/vertical orientation
  * tabs groups (including horizontal/vertical orientation)
  * last active and selected tabs

**Join the revolution and install it today!** Save at least **3300 minutes/year** = 55 hours = 2.3 days (15 mins x 20 days x 11 months). You need about  15 minutes to fully switch between contexts at the best possible  scenario. 

In worst case scenarios **switching to detailed context could take several hours**, one of the [**real** **horror stories**](https://developercommunity.visualstudio.com/t/vs2017-1552-does-not-restore-open-documents/175923#T-N177842-N178047):

"*Losing this functionality interrupts my workflow beyond imagination. The  opened documents represent a "bookmark" for me and I'm barely able to  pick up work again without them.*

*Every time this happens (...) I am willing to put hours into finding a  solution, because the thought of losing my opened document state once  more after a work session is terrifying. But this time around (...)  nothing of the usual remedies helps (...)* **This has added another 20 Minutes and counting to my two hours put into solving this**."

With ContextKeeper you could **safely store and switch between different programming contexts in seconds 🔥**

**All opened files, pinned tabs, documents positions and state  (horizontal/vertical orientation, docked state and files order)** are  preserved in a **simple JSON file** 😍 No more dealing with broken .suo file again. 

After installing VSIX package you could access your latest Mental Snapshots by navigating to 

## View -> Other Windows -> Mental Snapshots



![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/27hKCBytTdc6vJLjEuzPuX/email) 

By default tool window will open next to **Solution Explorer**

![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/pCodzPVj8AFjJrJ5nmoiDA/email) Tool 

You could create a new snapshot using **Create Snapshot** button

![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/hLLWTq2itByEq5hZPaQjMi)

and restore them quickly using few commands from **right-click context menu**

![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/bUbWPtYLCdWtkiYcbJKpEP/email) 



- **Full Restore** - restores all files including windows state&position, pinned tabs and current line&column for every file,
- **Append Files** - adds all files from a selected snapshot to the current active window,
- **Restore Files** - closes all tabs and restores a snapshot in the same way as Append Files,
- **Update** - update selected snapshot using current visual&logical state



## ✨Automatic snapshot switching when changing branches

[![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/5YYSqMkrHsJEEcp5W6sa8y?w=800&fit=max)](https://www.youtube.com/watch?v=BlxAoJpBrZ0)

When switching to another git branch ContextKeeper will automatically  remember current branch snapshot and save it to  .contextkeeper/.git-branches folder. Also it will be added to the  "Mental Snapshots" UI list at the very top with <Git Branch>  prefix:



![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/oyuQheTPi2ohmNMqCevUG9?w=800&fit=max)

This is the same process that you could do manually before switching branches but now fully automated for your convenience 🔥. The current  branch snapshot is always [continuously auto-saved](https://contextkeeper.io/blog/continuous-auto-saving-branch-snapshots-and-git-worktree-support/) when you **add**, **remove** or **change** position of any document tab or window (with tabs).

Also a git branch could be changed from CLI, Visual Studio or other  third-party client and ContextKeeper will detect it auto-magically 🧙‍♂️ and restore snapshot for currently selected branch.



## Where the snapshots are stored?

All snapshots are stored in the **.contextkeeper** folder which is created in the same folder where solution file (.sln)  sits. A snapshot is saved using self explanatory JSON format. You could  try changing different bits manually and later checking an impact it has during restoring process.



![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/aj9BPm1H1e8wRGYwLRqubF/email)

## Git worktree support

The git worktree support, introduced in [v1.3](https://contextkeeper.io/blog/downloads/), allows even [more streamlined context switching](https://stackoverflow.com/a/31951225). If you sometimes clone entire repository when working on a feature I recommend checking [git worktree](https://kickertech.com/git-worktrees-why-would-you-use-it/). Long story short, working tree is like clean, cloned repository but better because:

- repository "cloning" is done instantly - it's a local operation, 
- worktree uses less disk space - there is a single .git folder shared across multiple working trees,
- often more convenient than stashing



## Current limitations

- windows  positions are tightly coupled to your (multi) monitor setup and  switching between them are not supported yet (e. g. switching between  workstation and laptop). 

  



[The Roadmap](https://contextkeeper.io/blog/roadmap-for-2022/) includes among others:

- [**breakpoints & bookmarks**](https://contextkeeper.io/blog/launching-breakpoints-bookmarks-support/) (*update:* implemented 15th March 2023)
- [**relative paths**](https://contextkeeper.io/blog/relative-paths-support-in-v1-8-and-contextkeeper-mentioned-on-the-jesse-libertys-podcast/) (*update*: implemented, 1st June 2022) and **machine-independent snapshots restore process**
- **storing snapshots outside of the solution folder**
- [**search dialog**](https://contextkeeper.io/blog/search-dialog-v1-71/) (*update*: implemented, 15th April 2022)