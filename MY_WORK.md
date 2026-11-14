# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | [Abdullah Ahmed Alwahabie] |
| **Student ID** | [445050041] |
| **University Email** | 445050041@std.psau.edu.sa |
| **GitHub Username** | [AbdullahAlwahabi445050041] |
| **Repository Link** | [[Paste your repository link here](https://github.com/AbdullahAlwahabi445050041/OS-Assignment3--abdullah-alwahabi/edit/main/MY_WORK.md)] |
 
---

## 🎥 Video Link

**Video Link**: [Paste your video link here]

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

**Entry 1 - [November 9, 2026, 5:15 PM]**
* **What I did:** Forked the repo, set my student ID, and ran the starter code.
* **Details:** Changed `studentID` to `445050041` on line 304 and saved the broken output.
* **Challenges:** Multiple CPUs picked the same process and caused `IllegalThreadStateException`.
* **Solution:** Checked `ReadyQueue.poll()` and saw `RaceWindow.pause()` causing a race condition.
* **Time spent:** 40 minutes
---

**Entry 2 - [November 10, 2026, 7:00 PM]**
* **What I did:** Implemented Feature 1 (`ReentrantLock` in `ReadyQueue`).
* **Details:** Added `lock` to protect `add()`, `poll()`, `processOf()`, and `snapshot()` using `try/finally`.
* **Challenges:** I was not sure if `unlock()` works when `return` is inside the `try` block.
* **Solution:** Tested the code and confirmed `finally` always runs before returning.
* **Time spent:** 45 minutes

---

**Entry 3 - [November 11, 2026, 6:30 PM]**
* **What I did:** Implemented Feature 2 (locks in `SharedStats`).
* **Details:** Added `lock1`, `lock2`, and `lock3` to protect the three counters and their getters.
* **Challenges:** I forgot to lock the getter methods at first.
* **Solution:** Added locks to all three getters so reads are also thread-safe.
* **Time spent:** 50 minutes

---

**Entry 4 - [November 13, 2026, 8:15 PM]**
* **What I did:** Implemented Feature 3 (`Semaphore` in `ReadyQueue` and `CpuWorker`).
* **Details:** Added `Semaphore sem = new Semaphore(0)`, called `release()` in `add()`, and `acquire()` in `CpuWorker`.
* **Challenges:** The program hung at the end because one CPU stayed blocked on `sem.acquire()`.
* **Solution:** Added `readyQueue.sem.release(SharedStats.totalCPUs)` when all processes finish to wake up blocked CPUs.
* **Time spent:** 1 hour

---

**Entry 5 - [November 14, 2026, 4:00 PM]**
* **What I did:** Tested the code 5 times and wrote `MY_WORK.md`.
* **Details:** Verified all 4 checks pass with `0` busy-wait polls and answered all questions.
* **Challenges:** Writing clear explanations for deadlock and lock granularity.
* **Solution:** Reviewed the Chapter 5 lecture slides and linked them to my code.
* **Time spent:** 1 hour

---

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

* **Total time spent on assignment:** 4 hours 
* **Most challenging part:** Waking up the sleeping CPUs at the end of Feature 3 so the program terminates cleanly.
* **Most interesting learning:** Seeing how `RaceWindow.pause()` exposes race conditions every time.
* **What I would do differently next time:** Plan the semaphore shutdown logic before writing the code.

---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

[In this assignment, I learned how race conditions happen when multiple threads change shared data at the same time. In the starter code, updating counters and polling from the queue failed because threads interrupted each other during `RaceWindow.pause()`. I learned how to protect critical sections using `ReentrantLock` to guarantee mutual exclusion. I also learned that we must always put `unlock()` inside a `finally` block so the lock is released even if an error happens. Finally, I learned how a counting `Semaphore` puts threads to sleep when the queue is empty instead of wasting CPU time with busy waiting.]

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

[The hardest part for me was Feature 3, especially stopping the CPUs cleanly at the end of the simulation. Replacing the `Thread.sleep(20)` loop with `readyQueue.sem.acquire()` was easy at first. However, when the last process finished, my program froze and the watchdog stopped it. I realized that one CPU was still sleeping inside `sem.acquire()` waiting for a process that would never come. To fix this, the last CPU had to call `sem.release(SharedStats.totalCPUs)` to wake up all sleeping CPUs so they could exit the `while` loop.]

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

[I overcame these challenges by working step by step and testing after every small change. First, I read the `README.md` file and the `TODO` comments in the code very carefully. When the starter code crashed, I read the console output to see which method caused the error. When the program got stuck in Feature 3, I traced the `CpuWorker` loop and saw why the thread was still blocked. Running the program 5 times after each feature helped me make sure my synchronization worked every time.]

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

[Synchronization is used in many real-world systems that handle multiple users at the same time. For example, bank apps use mutex locks during money transfers so two transactions do not corrupt an account balance, just like we protected `SharedStats`. Ticket booking websites use locks so two customers cannot buy the exact same seat at the same time, similar to `ReadyQueue.poll()`. Web servers and databases use counting semaphores to limit how many users can connect at once. Print queues also use semaphores so the printer sleeps until a new document is added.]

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

[In my starter run (Student ID `445050041`), `Context switches` expected `31` but observed `19`, `Completed processes` expected `14` but observed `10`, and `Total service time` expected `98971` but observed `65410`. A lost update happens when `CPU-1` reads `contextSwitchCount` (say `10`) into `tmp` and pauses at `RaceWindow.pause()`, and at the same moment `CPU-2` also reads `10` into its `tmp` before `CPU-1` writes `11`. Both CPUs then write `10 + 1 = 11`, so one increment is lost. On a real machine without `RaceWindow`, the OS scheduler can still preempt a thread between reading a variable into a CPU register and writing it back to memory, which is very hard to detect because that timing window is only a few nanoseconds wide..]

Verification block of the **original starter**:
```
[Context switches (quanta executed)     expected 31       observed 19       ✘ MISMATCH
Completed processes                    expected 14       observed 10       ✘ MISMATCH
Total service time (ms)                expected 98971    observed 65410    ✘ MISMATCH
Busy-waiting polls (must be 0)         expected 0        observed 8        ✘ MISMATCH]
```

Verification block of **my final version**:
```
[Context switches (quanta executed)     expected 31       observed 31       ✔
Completed processes                    expected 14       observed 14       ✔
Total service time (ms)                expected 98971    observed 98971    ✔
Busy-waiting polls (must be 0)         expected 0        observed 0        ✔]
```

**Explanation of the timeline:**
[1. `contextSwitchCount` is `10`.
2. `CPU-1` reads `tmp = 10`, then pauses at `RaceWindow.pause()`.
3. `CPU-2` reads `tmp = 10` at the same time, then pauses.
4. `CPU-1` wakes up and writes `contextSwitchCount = 11`.
5. `CPU-2` wakes up and writes `contextSwitchCount = 11` (one update is lost).]

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

[In `SharedStats`, I used three separate locks (`lock1`, `lock2`, `lock3`—one lock per variable) because the three counters are independent, allowing threads to update different counters at the same time (better concurrency), with the small trade-off of creating three lock objects instead of one. The `ReadyQueue` has its own separate `lock` so queue operations do not block threads that are only updating statistics in `SharedStats`. My code ensures **mutual exclusion** because only one thread can hold a lock at a time, and **progress** is guaranteed because locks are always unlocked in `finally` blocks. However, a default `ReentrantLock` is not fair, so **bounded waiting** is not strictly guaranteed if one thread keeps grabbing the lock first.]

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| `ReadyQueue`: `list` & `map` in `add()`, `poll()`, `processOf()`, `snapshot()` | `lock` | Stops CPUs from picking the same process or crashing during queue iteration. |
| `SharedStats.contextSwitchCount` in `incrementContextSwitch()` & `getContextSwitchCount()` | `lock1` | Prevents lost updates and dirty reads on the context switch counter. |
| `SharedStats.completedProcessCount` in `incrementCompletedProcess()` & `getCompletedProcessCount()` | `lock2` | Protects the completed counter so CPUs know when all 14 processes are done. |
| `SharedStats.totalServiceTime` in `addServiceTime()` & `getTotalServiceTime()` | `lock3` | Prevents lost additions when multiple CPUs add service time concurrently. |


## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

[In the starter code, when the queue was empty, CPUs kept checking `poll()` and sleeping for 20ms in a loop (causing `8` busy-waiting polls in my run), which wastes CPU time. My semaphore `sem` counts the number of processes waiting in `ReadyQueue`; its initial value is `0` because the queue starts empty, and after the `14` initial `add()` calls in `main`, its value becomes `14`. When the queue is empty, `sem.acquire()` blocks the CPU thread until a process is added. When the last process finishes, the CPU calls `sem.release(SharedStats.totalCPUs)` to wake up the other sleeping CPU; otherwise, it would stay blocked forever and trigger the watchdog.]

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

**Classical problem and roles**:
[NThis is the **Producer-Consumer Problem**. The `main` thread is the initial **producer** (adding 14 processes), and the `CpuWorker` threads are both **consumers** (taking processes with `poll()`) and **producers** (re-adding unfinished processes with `add()`).]

**Semaphores for a bounded queue (name and initial value)**:
[For capacity `K`, we need 3 semaphores: `mutex = 1` (protects the queue), `empty = K` (counts free slots), and `full = 0` (counts ready processes)..]

**Deadlock scenario and prevention**:
[If a CPU locked `mutex` (`lock.lock()`) **before** calling `full.acquire()` (`sem.acquire()`) on an empty queue, it would sleep while holding the lock, blocking any other CPU from calling `add()` to release the semaphore. We prevent this deadlock by breaking the **Hold and Wait** condition: always call `sem.acquire()` before locking `lock`.]

## Summary

**Key concepts I understood through these questions:**
1. How race conditions cause lost updates during read-modify-write steps.
2. Using `ReentrantLock` with `try/finally` and choosing one lock per variable.
3. Using a counting `Semaphore` to block threads instead of busy waiting.

**Concepts I need to study more:**
1. Deadlock avoidance methods in operating systems.
2. Fair locks and condition variables in Java.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
**Repository**
- [x] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [x] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [x] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [x] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [x] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [x] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [x] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [x] **The four verification lines are ✔ in 5 consecutive runs**
- [x] Every lock is released in a `finally` block
- [x] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [x] Each feature has clear comments

**Commits**
- [x] **At least 4 meaningful commits, ideally 7 or more**
- [x] **One commit per feature**
- [x] Commits are spread over **different dates** (not all in the last hour)
- [x] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [x] Full name and student ID filled in at the top
- [x] Development log has **5+ entries** on different dates
- [x] Reflection: 4 questions, 5-7 sentences each
- [x] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [x] No `[...]` placeholders left
- [x] No section headers deleted

**Video**
- [ ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [ ] Submit **only** the link to your public GitHub repository
> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
