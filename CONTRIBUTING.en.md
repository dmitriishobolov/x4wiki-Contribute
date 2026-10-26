# How to contribute

[Русский](CONTRIBUTING.md) · [Read the wiki](https://x4wiki.com/en/) · [Issue forms](https://github.com/dmitriishobolov/x4wiki-Contribute/issues/new/choose)

## Propose a change without Git

1. Sign in to GitHub and open **Issues → New issue**.
2. Choose **New article / addition (EN)** for a new topic or **Article / example
   correction (EN)** for an existing page.
3. Include the wiki page URL or describe the missing topic. Explain what
   should change and provide a small authored code example when useful.
4. List the X4 and mod versions, primary sources and what you actually checked:
   an idea, source reading, an isolated test or a specific in-game scenario.
5. Select **Create**. Follow the issue for discussion and clarification.

Russian and English submissions are welcome. You do not need a translation
to propose a change; the editor reviews both site languages before publishing.

## Example correction

**Page:** `https://x4wiki.com/en/pages/register-event`.

**Problem:** the example could explain the difference between an event name
and its callback arguments, so a reader does not treat it as a universal signature.

**Proposal:** show a short sender example with a source link and explain that
callback arguments depend on that sender.

**Evidence:** source reading only; the proposed example has not been run in game.

This illustrates a useful submission, rather than asserting that the page has this error.

## Submit a Markdown draft with a pull request

1. Fork this repository. In your fork, use **Add file → Create new file**.
2. Create `proposals/ship-hull-example.en.md` with a stable Latin filename.
3. Copy the [English article template](templates/article.en.md) and fill in the
   goal, prerequisites, steps, example, independent result checks and sources.
4. Commit the file, then choose **Contribute → Open pull request**.
5. Fill in the PR template and link any related issue, for example `Related to #12`.

For an existing page, download its Markdown from the wiki, submit your edited
copy under `proposals/`, link the original URL and summarize the changes.
No access to another project or local wiki installation is required.

If you prefer Git:

```sh
git clone https://github.com/YOUR_NAME/x4wiki-Contribute.git
cd x4wiki-Contribute
git switch -c article/ship-hull-example
# Add your completed draft to proposals/.
git add proposals/ship-hull-example.en.md
git commit -m "Propose ship hull example"
git push -u origin article/ship-hull-example
```

Replace `YOUR_NAME` with your GitHub name and clone your own fork. Open a PR
from that branch into `dmitriishobolov/x4wiki-Contribute:main`.

## Technical material

State the execution layer (XML patch, MD, AI, Lua UI, FFI or a custom library),
versions, insertion point, parameter types established by sources and remaining
unknowns. Explain how to independently read the result and cite primary sources.
Keep untested examples marked as examples. Do not submit mods, mod files, internal
documents or complete source files. Provide a small independent example and public
primary sources. Do not submit credentials, personal logs, saves or extracted game files.

## After submission

An editor reviews evidence, reproducibility and scope, discusses questions,
then transfers accepted material to the wiki working copy. Translation, links,
examples and build checks precede publication. The published URL can be added
to the issue or PR once the change is actually live. Issues and PR merges do
not automatically deploy the site.
