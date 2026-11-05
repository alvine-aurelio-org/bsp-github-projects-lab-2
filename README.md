# GitHub Projects — Lab 2: plan and complete sprint work

All participation uses the GitHub website in your browser.

## Step 1 — Set up your sprint workspace

**Time: 18 minutes · Topic: a private workspace, two work issues and sprint commitment**

### Welcome

- **Who is this for?** Project managers, product owners, team leads and developers, either continuing the full workshop or choosing only Lab 2.
- **What will you learn?** Sprint planning, native issue dependencies, browser-based file editing, PR traceability, completion automation and carry-over.
- **What will you build?** A Sprint 1 plan and a real, one-file checklist PR, with unfinished verification retained for Sprint 2.
- **How long?** Optional standalone: **45 minutes** (18 + 7 + 12 + 8). Full-workshop continuation: **35 minutes** (8 + 7 + 12 + 8), because the workspace already exists.
- **Prerequisites:** your own GitHub account, a browser, permission to create a private repository and private Project, and access to native issue dependencies and pull requests. No instructor account, personal access token or App is needed.

### Start here — choose one path

- **Attending all three labs?** Stay in your existing private [Lab 1](https://github.com/alvine-aurelio-org/bsp-github-projects-lab-1) copy, the **same Mona exercise issue and same Project**. Follow Mona's Lab 2 comments there for the **35-minute continuation**, not this standalone setup. Keep your five existing work issues; do not duplicate them. **No other copy is needed.**
- **Optional standalone: practising only Lab 2?** On this Lab 2 source, select **[Use this template](https://github.com/alvine-aurelio-org/bsp-github-projects-lab-2/generate) → Create a new repository**, choose yourself as owner, select **Private**, and create the copy. Use **one private repository and one private Project** for this chosen lab; you do not need three copies. **Already in your private copy? Skip the template button.**
- In that private copy, open **Issues → Mona's GitHub Projects Lab 2 — start here**. Mona creates **only one exercise issue**, never the work issues. If it has not appeared, open **Actions → Mona — guided laboratory → Run workflow → main** once, then recheck Issues. Do not start a second exercise. All later instructions, answers and check feedback stay in this **same Mona exercise issue**; always post a **new comment**, not an edited answer or a PR comment. Public source repositories are inert: do not answer or run the exercise there.

**Why:** an iteration is a timebox, unlike a repository milestone's release grouping. One private workspace keeps delivery work and evidence together.

**How:** create the Project and two native work issues yourself through the browser, then plan the same two issues in Sprint 1.

**Do — standalone setup, after your private copy and Mona exercise exist:**

1. Open your profile → **Your projects → New project → Table**. Name the Project, keep its visibility **Private** in Project settings, and use the **same owner as your repository**. Name the table **Backlog**. In your private repository, open **Projects → Link a project** and select it.
2. In your private repository's **Issues → New issue**, create **only two work issues**, using only the **Exact issue title** column below for their titles. Create both yourself **after Mona's exercise was opened**, keep both **open**, and add each to your Project using its **Projects** sidebar. These are native repository issues, not draft Project rows. Do not add Mona's exercise issue to the Project.

   | Work role      | Exact issue title                                   | Effort | Assignees  | Status      | Sprint   |
   | -------------- | --------------------------------------------------- | -----: | ---------- | ----------- | -------- |
   | Implementation | [Workshop] Publish the service release checklist    |      3 | Yourself   | In progress | Sprint 1 |
   | Verification   | [Workshop] Verify the release checklist in Sprint 2 |      2 | Unassigned | Todo        | Sprint 1 |

3. In Backlog, use the column-header **+ → New field** to create **Effort**, type **Number**, and enter **3** and **2** as above. Assign implementation to yourself, leave verification **unassigned**, and set their **Status** values to **In progress** and **Todo** respectively.
4. Create **Sprint**, type **Iteration**, starting this week with a **one-week** duration. In **… → Settings → Sprint**, name the first two consecutive, non-overlapping one-week iterations **Sprint 1** and **Sprint 2**. Reuse correctly typed fields rather than adding duplicates.
5. Put **both issues in Sprint 1**. In view settings, choose **Group by → Sprint**, set **Field sum → Effort**, and **Save** the view. Check Sprint 1 totals **5**; this is relative size, not available working hours.

**Expected result:** one private Project linked to your private repository, exactly two manually created work issues, and a saved Sprint 1 group with total Effort **5**.

![GitHub Projects field-creation and iteration-settings entry points](assets/screenshots/lab-2-step-1.png)

_Navigation reference: this inherited overview does not show every setup dialog. Follow the controls above. [Image sources and modifications](assets/screenshots/SOURCES.md)._

**Complete in the same Mona exercise:** Open your Project, copy the URL from the address bar, and paste only that link as a new comment below. Do not add a command, label or explanation.

**MIXED EVIDENCE:** Mona checks and binds the two native work issues; your Project setup is self-confirmed.

## Step 2 — Show a native dependency

**Time: 7 minutes · Topic: blockers and delivery sequencing**

**Why:** a native dependency expresses sequencing. A body link, checkbox, label or custom Project field is not the native relationship, and a dependency does not enforce a merge gate.

**How:** use the verification issue's native Relationships menu, not a written link.

**Do:**

- Open your **verification issue #{{ISSUE_verification}}**, not implementation. In its sidebar, open **Relationships → … → Mark as blocked by** (sometimes **Add blocked by**).
- Search for or paste the URL of your **implementation issue #{{ISSUE_implementation}}** and select it. Mona's step comment supplies your actual registered numbers.
- Confirm verification shows **Blocked by → implementation**. Open implementation and inspect the reciprocal **Blocking → verification** relationship. Both issues must belong to your existing private repository; do not reverse the direction.

**Expected result:** verification is natively blocked by implementation, without duplicating either task.

![Real GitHub issue-sidebar orientation for finding Relationships](assets/screenshots/lab-2-step-2.png)

_Navigation reference: this issue overview locates the sidebar; it does not display an expanded Relationships menu. Use the text above. [Image sources and modifications](assets/screenshots/SOURCES.md)._

**Complete in the same Mona exercise:**

```text
/check 2-2
```

**REPOSITORY-VERIFIED:** Mona reads GitHub's native issue-dependency endpoint. A body link or `/done 2-2` cannot pass. An unavailable or failed API check is not a pass.

## Step 3 — Create a linked pull request

**Time: 12 minutes · Topic: browser editing, a one-file change and native issue linkage**

**Why:** a branch isolates the change; a PR lets you inspect it and link delivery to the real implementation issue. This solo activity is self-inspection, **not independent review or self-approval**.

**How:** change only **work/release-checklist.md** and create its PR through GitHub's browser controls in your private repository.

**Do:**

1. Open **Code**, select **main** in the **branch dropdown**, then create the branch **workshop/release-checklist from main**. Confirm that work branch is selected before editing; do not edit main.
2. With the work branch still selected, open **work → release-checklist.md**, select the **pencil → Edit this file**, and change only the first checklist item to this exact line. Leave the second checkbox **unchecked**:

```markdown
- [x] Publish the service release checklist
```

3. Select **Commit changes**. In the dialog, choose **Commit directly to the workshop/release-checklist branch**, not main, and confirm. Do not change any other file or Mona's saved progress.
4. Select **Compare & pull request**. Set **base: main**, **compare: workshop/release-checklist**, and title **Publish the service release checklist**. Use the closing line below in the body. Mona's step comment fills in the actual implementation issue number; when reading the source guide, use your own implementation number instead of unresolved braces:

```text
Closes #{{ISSUE_implementation}}
```

5. Create the PR and confirm its **Development** relationship points to implementation. Inspect **Files changed**: only the checklist file may differ. **Keep the PR open until Mona confirms Step 2-3 passed and posts Step 4.** Do not close implementation manually or change the checked PR head after it passes.

**Expected result:** an open PR, from the exact work branch into main in your own repository, with the single checked line and a native closing relationship to the actual implementation issue.

![Issue Development and Compare and pull request navigation entry points](assets/screenshots/lab-2-step-3.png)

_Navigation reference: this inherited overview locates PR entry points, not every browser file-editing control. [Image sources and modifications](assets/screenshots/SOURCES.md)._

**Complete in the same Mona exercise:** replace **YOUR_PR_NUMBER** with this PR's actual number, not an issue number.

```text
/check 2-3 #YOUR_PR_NUMBER
```

**REPOSITORY-VERIFIED:** Mona checks author, same-repository head/base, exact branch, the native closing relationship, the only changed file and the required checked line. It does not award independent review or approval.

## Step 4 — Complete and carry over

**Time: 8 minutes · Topic: merge traceability, built-in automation and unfinished work**

**Why:** merging a closing PR into the default branch closes its issue. A Project workflow can separately set Status to Done; unfinished verification must remain visible.

**How:** enable the Project's completion workflow, inspect the checked PR, and merge through the browser only after its quality checks pass.

**Do:**

- Only after Mona's Step 2-3 pass, open your Project **… → Workflows** and enable **Item closed → Status: Done**. Return to the same PR, inspect **Files changed**, and wait for the required **content verification and test checks** to pass. Do not alter the checked head.
- Select **Merge pull request → Confirm merge**, or the permitted squash option, into **main**. No approval is required in the personal sandbox; this is **not independent review or self-approval**. Respect inherited organizational protections rather than disabling them.
- Confirm implementation closed as completed and its Project item becomes **Done**. Keep implementation in **Sprint 1**. Keep verification **open**, move only its Sprint value to **Sprint 2**, and save any view changes.

**Expected result:** implementation issue → work branch → PR → merge → closed issue, plus a Done Project item. Verification remains open in Sprint 2. Issue state and Project Status are separate values.

![Pull request merge controls and the Project board completion entry point](assets/screenshots/lab-2-step-4.png)

_Navigation reference: the overview shows entry points, not proof of your own merge or carry-over. Use your actual Sprint field. [Image sources and modifications](assets/screenshots/SOURCES.md)._

**Complete in the same Mona exercise:** use the same actual PR number checked in Step 3.

```text
/check 2-4 #YOUR_PR_NUMBER
```

**MIXED EVIDENCE:** Mona verifies the same checked PR/head, merge, issue closure and open verification. You self-confirm Project Done and Sprint 2 carry-over. It closes only this standalone exercise issue, not verification.

## Troubleshooting and evidence FAQ

- **Which path should I use?** All-three-lab attendees follow the existing Lab 1 Mona comments without another copy or repeated setup. Standalone learners use only this Lab 2 template and its single exercise. `/status` and `/help` are safe in the active private exercise.
- **What does the first link prove?** Mona finds the two native issues by exact title, checks their actual IDs, learner authorship, creation after the exercise and open state, then binds those IDs. Your Project's existence, private visibility, access, repository link, membership, fields and totals are **self-confirmed**. Mona uses **no Projects API**; pasting a link does not prove a UI action occurred.
- **No Mona in my copy:** confirm the repository is private, not itself a template, and uses main. Inspect its Actions result and existing Issues before running the start workflow once. Do not create another exercise, edit bot progress or post in a public source.
- **Missing Sprint controls:** check the field is Iteration, use Project settings and save the view. A Project permission or feature limitation is not completed work; do not self-confirm it.
- **Dependency check fails:** use the verification issue's native Relationships menu, select implementation in the same repository and retry `/check 2-2`. A written issue link is insufficient; API failures earn no progress.
- **Work branch already exists:** inspect that branch and any existing PR in the browser. Preserve your work and resume only if the base and one-file change are correct; do not edit main or delete work to bypass a check.
- **PR check fails:** keep the PR open, use the actual PR and implementation numbers, exact branch and one-file diff, correct the displayed problem, and submit a fresh check. Do not merge before Step 2-3 passes or alter its head afterward.
- **A reviewer is required:** that managed environment has an extra prerequisite. Respect the policy and obtain its authorized review; do not call author self-inspection an approval or disable protections.
- **Done did not update:** inspect Item closed automation and the Project card yourself. A successful repository check is not evidence that Mona read a Project field.

## Safety and evidence

Use synthetic training tasks only, never real BSP data or original BSP documents. Keep exports and account screenshots private. Browser sign-in and the built-in repository workflow token are sufficient; no participant secret, instructor provisioning or deployed service is needed. Offline author checks validate publication content, not a live Project or an independently reviewed assessment.

## Author verification

**Maintainers only:** [package.json](package.json) defines the dependency-free Node test and [content verification](tools/verify-content.mjs) scripts; CI uses **Node 24**. Checks require the four real PNGs, resolved local links, schema-v3 metadata and matching immutable runtime pins. Unresolved pins are a publication blocker. These offline checks are not learner instructions or a live UI rehearsal.

## License and acknowledgements

Workshop text and code: [MIT](LICENSE). Reused GitHub Docs screenshot material is separately [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); see [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) and [image sources](assets/screenshots/SOURCES.md). Inspired by [GitHub Skills](https://skills.github.com/), but independently authored, not an official GitHub Skills course and not endorsed by GitHub or BSP. [Security and privacy](SECURITY.md).
