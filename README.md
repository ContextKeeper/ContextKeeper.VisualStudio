# [ContextKeeper: The State-of-the-Art Session Manager for Visual Studio](https://contextkeeper.io)

## **Save and restore** your **complete development context** with a single click 🔥

## **Key Features:**

- **Save open documents**, **files and the tabs layout** with **breakpoints** and **bookmarks** - restore them later and **make context switching less painful**
- **Automagically restore your last context** when **switching** git **branches**
- **Full multi-monitor and DPIs support** for complex windows and the tabs layout
- Preserve your **exact document layout** and **editor state**
- **Simple JSON file** storage for **easy backup** and **portability**

**Reclaim your lost productivity**. ContextKeeper safely **preserves your task's progress** so you can seamlessly **switch between different projects or features** without losing your piece of mind 🧠

Designed with 💖 for developers who need to maintain multiple work contexts throughout their day. Do you know [**the real cost of interruption and context switching**](https://contextkeeper.io/blog/the-real-cost-of-an-interruption-and-context-switching/) and **The Law of Context Density** - "*A larger context naturally emerges with a bigger screen real estate.*"?

## 💡 **ContextKeeper is currently in the Free Beta with [Optional Founders License](#Optional-Founders License), if you will find any issues please [report them](https://github.com/ContextKeeper/ContextKeeper.VisualStudio/issues)**.

Missing the Save All Tabs extension? ContextKeeper is the modern replacement you've been waiting for. 

## 🧙‍♂️ [**Automatically switch contexts** when changing Git branches](#automatic-snapshot-switching-when-changing-branches) and check more detailed [article here](https://contextkeeper.io/blog/automatic-snapshot-switching-when-changing-branches-v1/).

Are you use using Favorite Documents, Workspace Manager or Task Canvas? [Check how much **value ContextKeeper delivers** when **compared to them**.](#how-much-value-contextkeeper-delivers-when-compared-to-others)

Looking for **ARM-compatible build** or **VS 2019/2017/2015 support**? [Download from here](https://contextkeeper.io/downloads).

<video src="https://github.com/ContextKeeper/ContextKeeper.VisualStudio/assets/8102322/630b296a-e103-42c6-aeca-88dbe37867f3" controls autoplay width="1000"></video>

## The supported context is made by:

* logical state
  * your favorites files (non-solution files are also supported)
  * last opened files, order and state including last selected line&column
  * pinned tabs
  * tabs groups
  * [breakpoints](#breakpoints-and-bookmarks)
  * [bookmarks](#bookmarks)
  * [relative paths](#relative-paths)
  
* visual state
  * main IDE window position and size
  * floating windows position and size
  * docked state and horizontal/vertical orientation
  * tabs groups (including horizontal/vertical orientation)
  * [last active and selected tabs](#selected-and-active-documents-in-tab-groups)
  * [full screen (maximized) windows support](#full-screen-windows-support)

**Join the revolution and install it today!** Save at least **3300 minutes/year** = 55 hours = 2.3 days (15 mins x 20 days x 11 months). You need about  15 minutes to fully switch between contexts at the best possible  scenario. 

In worst case scenarios **switching to detailed context could take several hours**, one of the [**real** **horror stories**](https://developercommunity.visualstudio.com/t/vs2017-1552-does-not-restore-open-documents/175923#T-N177842-N178047):

"*Losing this functionality interrupts my workflow beyond imagination. The  opened documents represent a "bookmark" for me and I'm barely able to  pick up work again without them.*

*Every time this happens (...) I am willing to put hours into finding a  solution, because the thought of losing my opened document state once  more after a work session is terrifying. But this time around (...)  nothing of the usual remedies helps (...)* **This has added another 20 Minutes and counting to my two hours put into solving this**."

With ContextKeeper you could **safely store and switch between different programming contexts in seconds 🔥**

**All opened files, pinned tabs, documents positions, editor state and the tabs layout  (horizontal/vertical orientation, docked state and files order)**, **breakpoints and bookmarks** are  preserved in a **simple JSON file** 😍 No more dealing with broken .suo file again. 

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



## Automatic snapshot switching when changing branches

[![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/5YYSqMkrHsJEEcp5W6sa8y?w=800&fit=max)](https://www.youtube.com/watch?v=BlxAoJpBrZ0)

When switching to another git branch ContextKeeper will automatically  remember current branch snapshot and save it to  .contextkeeper/.git-branches folder. Also it will be added to the  "Mental Snapshots" UI list at the very top with <Git Branch>  prefix:



![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/oyuQheTPi2ohmNMqCevUG9?w=800&fit=max)

This is the same process that you could do manually before switching branches but now fully automated for your convenience 🔥. The current  branch snapshot is always [continuously auto-saved](https://contextkeeper.io/blog/continuous-auto-saving-branch-snapshots-and-git-worktree-support/) when you **add**, **remove** or **change** position of any document tab or window (with tabs).

Also a git branch could be changed from CLI, Visual Studio or other  third-party client and ContextKeeper will detect it auto-magically 🧙‍♂️ and restore snapshot for currently selected branch.

## Breakpoints and bookmarks

Generally, when a snapshot is created, **breakpoints** and **bookmarks** are **saved only for the currently open files**. This behavior differs from that of Visual Studio, which remembers all  breakpoints and bookmarks across different sessions for all files.  However, I believe that saving them only for open files is more  practical. I remember countless examples of finding old breakpoints from days before that were no longer relevant because I was working on a  different task.

The second important thing is that **when they are restored for a file**, all **old breakpoints or/and bookmarks are removed if there were any**, but only for that file and nothing else.

### Breakpoints

Standard and conditional breakpoints are currently supported. When breakpoint is disabled it will be still saved to a snapshot with `IsEnabled` property set to `false` and restored in a disabled state later in the Visual Studio. A single conditional expression is supported with two modes `Is true` and `When changed`

![img](https://contextkeeper.io/content/images/2023/03/Breakpoints_JSON.png)

Although the **supported area is probably enough for about 90-95% of use cases**, there are **some limitations**:

- only a single conditional expression,
- no support for Hit Count or Filter expressions,
- no support for Actions, “Remove breakpoint once” hit or “Only enable when the following breakpoint is hit” options.

I will be looking for ways to support excluded areas, starting from “Hit  Count” and combined conditions (e. g. Conditional Expression with Hit  Count). Unfortunately not every breakpoint’s detail is easily exposed  via API but I will be extensively digging in Visual Studio’s internals  to cover more use cases.

### Bookmarks

Bookmarks are stored using line numbers in a similar way to breakpoints.

![img](https://contextkeeper.io/content/images/2023/03/Bookmarks.png)

Visual Studio API for bookmarks is really limited; therefore, currently there is no support for:

- named bookmarks - only the line number is stored but not the bookmark name,
- folders - bookmarks folder structure is not restored.

I hope you will enjoy using new breakpoints & bookmarks support!

## Relative paths

The feature was one of the missing puzzle pieces, that I always wanted to include. Adding support for **relative path** is essential part to allow **sharing your context** between different **dev environments** and also **inside your team**. It will unlock potential to e. g.:

- **switching** between **laptop** and **workstation**
- **faster onboarding** developers to new tasks, taking over responsibilities
- **sharing mental models** of the project across **team members**
- **fixing complex bugs easier**, using targeted mental snapshots 

Every time a new snapshot is created it will include `RelativePath` property for every entry in a `*.ck` file. When a snapshot is restored, relative paths will be used by default. There is still `FilePath` property used, as a **fallback strategy**, for global files. All different types of files are supported including:

- **solution and projects files**
- **"loose" files** (not included in a solution/project) but still part of the folders structure
- **global files** (relative paths cannot be created for them, absolute paths are used)

![RelativePath](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/tva8A8pu5XWBxd7JQ5Xvb9)

## Selected and active documents in tab groups

There can be multiple tab groups opened at once and single document **selected** in each:

![img](https://contextkeeper.io/content/images/2022/11/Selected-tabs-in-groups.jpg)

The state of both selected documents is now preserved using `IsSelected` JSON property.

Additionally, support for the **active** tab was added. When a document has focus while generating the snapshot, it will be tagged internally using `IsActive` property.

![img](https://contextkeeper.io/content/images/2022/11/IsActive--property.png)

## **Create stash snapshot and restore it later**

There are two additional commands in the toolbar. **Stash** and **unstash**. The idea is from git workflow but here it's applied to a current context you're working on. You could **quickly save it (stash)** and switch to something else that needs an **urgent attention**. **After stashing** a snapshot **all tabs will be closed automatically**, similarly how stashing works in git - current context is cleared and ready for a new work.

A stash snapshot is always displayed as a first on the list. Currently only single stash is supported but multiple stashes will be supported in the future.

![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/kgAeeubdKzrWxkpK3CECfv/email?w=250)

A stash has **additional description**, like "<stashed> **2 hours ago**", to get you additional awareness how long it's awaiting to be unstashed. It's really easy to lose track of time, during coding session, and it will act as an **useful reminder** how long your "main" task was **put on hold**. The **stash timestamp** description **is live updated**. If you decide that more meaningful name for stash snapshot is needed, you can simply rename it and it will become a regular snapshot.

### Keyboard shortcuts

You could **assign your favorites keyboard shortcut** combination for stash and unstash commands from the toolbar. There aren't default shortcuts assigned but I found useful to use:

- Ctrl+Shift+S, Ctrl+Shift+S for **s**nasphot **s**tashing
- Ctrl+Shift+S, Ctrl+Shift+U for **s**nasphot **u**nstashing

![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/aw76uizdFeTKB1Rj1T7L96/email)

## Full screen windows support 
There is a support added to remember if windows is maximized during snapshot creation. No more problems with restoring maximized windows, especially during git branch switching 😍 Only maximized windows will have additional property serialized in a snapshot.

![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/s2WTETYNrgrKaZiP5vW8Bj/email?w=300)

## Where the snapshots are stored?

All snapshots are stored in the **.contextkeeper** folder which is created in the same folder where solution file (.sln)  sits. A snapshot is saved using self explanatory JSON format. You could  try changing different bits manually and later checking an impact it has during restoring process.



![img](https://embed.filekitcdn.com/e/ta2FHAgWPvhq7wYzRrVqfZ/aj9BPm1H1e8wRGYwLRqubF/email)

## Git worktree support

The git worktree support, introduced in [v1.3](https://contextkeeper.io/blog/downloads/), allows even [more streamlined context switching](https://stackoverflow.com/a/31951225). If you sometimes clone entire repository when working on a feature I recommend checking [git worktree](https://kickertech.com/git-worktrees-why-would-you-use-it/). Long story short, working tree is like clean, cloned repository but better because:

- repository "cloning" is done instantly - it's a local operation, 
- worktree uses less disk space - there is a single .git folder shared across multiple working trees,
- often more convenient than stashing

## How much value ContextKeeper delivers when compared to others

Below, you'll find a table comparing extensions that work with VS 2022. I've included free extensions, with the exception of Task Canvas, which is a paid one. I've invested several hours testing Favorite Documents, Workspace Manager, and Task Canvas to get a clearer picture of how they all stack up against ContextKeeper.

| Features supported                                           |  ContextKeeper   | Task Canvas |      Favorite Documents      | Workspace Manager |
| ------------------------------------------------------------ | :--------------: | :---------: | :--------------------------: | :---------------: |
| Automatic session switching when changing Git branches       |        ✅         |      ❌      |              ❌               |         ❌         |
| Restores full Visual Studio's original documents state       |        ✅         |      ❌      |              ❌               |         ❌         |
| Tabs order                                                   |        ✅         |      ❌      |              ❌               |    unreliable     |
| Tab groups (including horizontal/vertical orientation)       |        ✅         |      ❌      |              ❌               |    unreliable     |
| Document windows positions & size (including floating windows) |        ✅         |      ❌      |              ❌               |    unreliable     |
| Breakpoints                                                  |        ✅         |      ❌      |              ❌               |         ❌         |
| Bookmarks                                                    |        ✅         |      ❌      |              ❌               |         ❌         |
| Last selected tab for every window                           |        ✅         |      ❌      |              ❌               |    unreliable     |
| Last active tab among all opened                             |        ✅         |      ❌      |              ❌               |    unreliable     |
| Visual Studio independent restore engine                     |        ✅         |  partially  |              ❌               |         ❌         |
| Multiple document windows                                    |        ✅         |      ❌      |              ❌               |    unreliable     |
| Multiple-monitor and DPIs support                            |        ✅         |      ❌      |              ❌               |    unreliable     |
| Relative path (portable sessions between environments)       |        ✅         |   limited   |           limited            |         ❌         |
| Maximized/Normal state for document windows                  |        ✅         |      ❌      |              ❌               |         ❌         |
| Source control ready sessions files (diffable JSON format)   |        ✅         |      ❌      |              ❌               |         ❌         |
| Continuous session auto-save for branch snapshots            |        ✅         |      ❌      |              ❌               |         ❌         |
| One-click append files                                       |        ✅         |      ❌      |              ✅               |         ❌         |
| Pinned files                                                 |        ✅         |      ❌      |              ✅               |    unreliable     |
| One-click session update                                     |        ✅         |      ✅      |        ❌(only adding)        |    unreliable     |
| One-click restore                                            |        ✅         |      ✅      |              ❌               |         ❌         |
| Shareable session's file between teammates                   |        ✅         |      ✅      | ❌(one file for all sessions) |         ❌         |
| Last opened files                                            |        ✅         |      ✅      |              ✅               |    unreliable     |
| Line & column for every file                                 |        ✅         |      ✅      |              ✅               |    unreliable     |
| Non-solution (external) files                                |        ✅         |      ✅      |              ✅               |         ❌         |
| Not based on the (broken) IVsUIShellDocumentWindowMgr        |        ✅         |      ✅      |              ✅               |         ❌         |
| Still in an active development (updates in 2023)             |        ✅         |      ❌      |              ✅               |         ❌         |
| Price                                                        | Free during Beta |     $49     |             Free             |       Free        |



## Task Canvas

I must say, I'm a bit surprised by how Task Canvas, the only paid competitor, performed in the comparison. It was built with a different workflow in mind, which is why it lacks in certain areas. However, it's still quite powerful and presents an interesting concept with its independent task canvas (separate, physical tab). Kudos to Sergey for trying something different. I'll take a closer look to see if there are any elements from this concept that could add additional value to ContextKeeper. What are your thoughts on this?

## Favorite Documents

It appears that the most popular extension is based on the simple VS API - `VsShellUtilities.OpenDocument()`. Unfortunately, it lacks more sophisticated use cases. Nonetheless, it's still better than relying solely on Visual Studio's default state engine and the inherently flawed `.suo` file.

## Workspace Manager

The spiritual successor to the (broken) approach of Save All the Tabs, utilizing the `IVsUIShellDocumentWindowMgr.ReopenDocumentWindows()` API. Unfortunately it is nothing more than wrapper for the default Visual Studio state engine, which which has had persistent, unresolved issues for years. It's unreliable, sometimes functioning properly but often failing. My experience with it has been similar to Save All the Tabs, which I tried  using with mixed success in the past.

**The fail of the Save All the Tabs extension**, to **deliver a stable** and **reliable** restore mechanism, **really push me** to work on the a **truly independent session restore engine**. I distinctly recall my thought process during that time - 

> If it doesn't work, I'll at least give it a shot and try to build it. There's nothing wrong with failing, but if I succeed, it will be a big deal one day! I will try to make it the state-of-the-art session manager that Visual Studio has never had but always deserved.

Later, the context engine has become the heart of ContextKeeper. It was entirely written from scratch, and it is fully independent from Visual Studio session restore API. It is rock solid, and works in VS 2022, including olders versions VS 2019/2017/2015. It has taken thousands of hours and years of work to bring it to a state where it is a true pleasure and an enjoyable experience to use, and to have the session manager that Visual Studio has always deserved. 🚀 Cause there ain't room for more than one King 👑 in this town.

## Optional Founders License

- ***Free Beta***: Currently, all features are available for free during the beta period
- ***Optional License***: [The founder license is available for early adopters](https://contextkeeper.io/license-preorder/) who wish to support development
- ***Future Model***: After the beta (not ETA at this point), basic features will remain free, while more advanced features will require a paid license

## Current limitations

- windows positions are tightly coupled to your (multi) monitor setup, and switching between them is not supported yet (e.g., switching between workstation and laptop with re-adjusted documents size & position to a new resolution). 

  

[The Roadmap](https://contextkeeper.io/blog/roadmap-for-2022/) includes among others:

- [**breakpoints & bookmarks**](https://contextkeeper.io/blog/launching-breakpoints-bookmarks-support/) (*update:* implemented 15th March 2023)
- [**relative paths**](https://contextkeeper.io/blog/relative-paths-support-in-v1-8-and-contextkeeper-mentioned-on-the-jesse-libertys-podcast/) (*update*: implemented, 1st June 2022) and **machine-independent snapshots restore process**
- **storing snapshots outside of the solution folder**
- [**search dialog**](https://contextkeeper.io/blog/search-dialog-v1-71/) (*update*: implemented, 15th April 2022)
