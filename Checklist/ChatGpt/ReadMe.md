https://chatgpt.com/share/68dd7971-34fc-800e-ad2c-2b0a5d975612
Skip to content
Chat history

You said:
I am making a godot asset lib for the store.

Help me check all the files and step to be validated 
ChatGPT said:
Here’s a checklist + recommended steps you can use to validate your Godot AssetLib submission. (You can send me your file structure / files later and I’ll help you check them.)

🛠 Checklist for Godot AssetLib Submission
Based on the official docs: Submitting to the Asset Library 
Godot Engine Documentation

Requirements (must-have)
Asset works

It must run / function properly in the target Godot version(s) you claim.

No broken scenes, missing scripts, missing resources, etc.

.gitignore

Include a .gitignore file to exclude redundant files (e.g. build outputs, user-specific files).

Don’t include large generated files that can be re-generated.

No essential submodules

If you use git submodules, they must not be essential — GitHub’s ZIP export doesn’t include submodules by default.

If the submodule is essential, the asset won't work when users download via AssetLib.

License file

Repository must include a license file named LICENSE or LICENSE.md.

Include the full license text and a copyright notice (years and copyright holder).

The license chosen in the submission must match the content in the repo.

If your asset is a plugin/addon, also place a copy of the license inside the plugin folder (so users always have it). (Recommended) 
Godot Engine Documentation

Proper name & English description

Asset name should be descriptive and unique.

Use proper English (capitalization, full sentences) for description.

You may include other languages, but English version must exist.

Include features, usage, version compatibility, etc. 
Godot Engine Documentation

Icon URL

Must provide a direct link to the icon (PNG or JPG).

If hosted on GitHub, the link must use raw.githubusercontent.com/... not github.com/.

Icon must be square (1:1 aspect ratio), minimum 128×128 pixels. 
Godot Engine Documentation
+1

Submission Form Fields to Validate
When filling the AssetLib submission, check:

Asset Name

Category (Addons, Tools, Templates, etc.)

Godot version / minimum version

Asset version (your versioning scheme)

Repository host (GitHub, GitLab, etc.)

Repository URL (not .git clone, but browsable URL)

Issues URL (if using separate issue tracker)

Download commit / tag / URL

Icon URL (direct link)

License (choose matching license)

Description (English, full sentences, explain features)

Previews (images or YouTube videos) — you can include up to 3 previews

Thumbnails for previews (if required) 
Godot Engine
+2
Godot Engine Documentation
+2

Recommended / Optional Best Practices
These won’t necessarily block acceptance, but improve quality and avoid issues:

Place files under addons/your_asset_name/ when possible (for plugins) to avoid conflicts. 
Godot Engine Documentation

Fix or suppress script warnings so users don’t see errors/warnings. 
Godot Engine Documentation

Follow Godot script/style conventions (GDScript / C# style guides).

If you have screenshots, put them in a separate folder and add an (empty) .gdignore next to it so Godot does not import them as assets. 
Godot Engine Documentation

Use .gitattributes to mark files as export-ignore so unnecessary files are excluded in ZIP.

Copy your LICENSE and README into the plugin folder itself (not just root).

Provide example scenes / demos so users can see how to use your asset.

Include a changelog if possible.

Make sure your assets are lightweight and not including huge unnecessary files.

Suggested Validation Steps (before submission)
Do this as a sanity check:

Run in a clean Godot project

Import or enable your asset, test all features.

Look for missing dependencies, missing resources, broken scenes, runtime errors.

Check file structure

Ensure plugin folder paths are correct.

No stray backup files, temp files, or hidden junk.

.gitignore, .gitattributes, .gdignore are correctly set.

License & metadata consistency

Open your LICENSE file and ensure the license text corresponds to the one you pick in the submission.

Check that the “copyright holder / year” is correct.

Make sure the README / description matches the features you are uploading.

Icon image

Confirm the icon URL works (raw link).

Check dimensions, format, square aspect.

Previews

Verify image links or YouTube links are correct and working.

Thumbnail links (if needed) exist.

Versioning / commit / tag

If using Git, pick a stable commit or tag.

Ensure that the tag corresponds to the version you mention.

Verify that the commit/zip includes all necessary files (test downloading the ZIP and unzipping).

Submission form

Fill the form with accuracy (categories, version, URLs).

Preview the submission, check no field is left blank incorrectly.

Double-check for submodules

If you used submodules, ensure they are optional or included in the ZIP.

Clean up warnings / lint

Remove debug/test code or leave them disabled.

Confirm no console warnings or errors in Godot when using the asset.

Documentation

README / user guide / usage instructions are clear.

Include how to install, how to use, API (if applicable), examples.

Test download / installation

Simulate a user downloading the asset from the ZIP (or commit) and installing it in a fresh project.

Confirm it works without missing files.

Submit

Log into your Godot account.

Go to “Submit Asset” page.

Fill fields, upload previews, submit.

Wait for review (may take a few days) 
Godot Engine Documentation
+2
Godot Engine
+2

If you like, you can now send me your directory tree (list of files/folders) or specific files (README, plugin folder, .gitignore, etc.) and I can go through and point out any missing issues. Do you want me to check your files now?

You said:
how i am suppose to use and what should I add in
.gitignore, .gitattributes, .gdignore
ChatGPT said:
Great question — those three files (.gitignore, .gitattributes, .gdignore) help you keep your Godot AssetLib package clean so users only download what they need. Here’s a breakdown of what to use them for and some ready-to-use templates:

✅ .gitignore
This file tells Git what not to include in your repo (stuff that doesn’t belong in source control).
Typical entries for Godot projects:

# OS-specific
.DS_Store
Thumbs.db

# Godot-specific generated files
.import/
export.cfg
export_presets.cfg

# User/editor-specific
*.translation
*.tscn-folding
*.tres-folding

# Build outputs (if applicable)
bin/
dist/
*.exe
*.apk
*.pck
*.zip
*.log
👉 Keep source files (scenes, scripts, resources, icons, demo scenes) — ignore build artifacts and editor cache.

✅ .gitattributes
This file helps when users download a GitHub ZIP (AssetLib uses ZIP from repo).
You can exclude extra files like docs, screenshots, tests, etc. so they don’t appear in the ZIP.

Example:

# Exclude these from ZIP exports
/docs export-ignore
/screenshots export-ignore
/tests export-ignore
/.github export-ignore
.gitignore export-ignore
.gitattributes export-ignore
👉 This way, the ZIP users get is lightweight (no dev-only stuff).

✅ .gdignore
This is a Godot-specific file.
If you place an empty .gdignore inside a folder, Godot will ignore all files in that folder (they won’t be imported as resources).

Use it for:

Screenshots or icons used for AssetLib previews

Docs (markdown, text, pdf)

Assets not needed at runtime

Example project structure:

addons/my_plugin/
    plugin.cfg
    plugin.gd
    my_script.gd
    icon.png
docs/
    readme.md
    .gdignore   <- prevents Godot from importing docs
screenshots/
    preview1.png
    preview2.png
    .gdignore   <- prevents Godot from trying to import images
🔑 Rule of Thumb
.gitignore → Don’t commit unnecessary files.

.gitattributes → Don’t include unnecessary files in GitHub ZIP downloads.

.gdignore → Don’t let Godot import docs/screenshots as engine resources.

⚡ Question for you: do you want me to draft a ready-to-use set of these three files tailored for a Godot addon/plugin structure (addons/your_plugin_name/...) so you can drop them directly into your repo?

You said:
is there a reason why the docs ans screen shot are outside of the addons folder ?
ChatGPT said:
Yes 👍 — there’s a very good reason why docs and screenshots are usually kept outside the addons/ folder:

📂 Why keep them separate from addons/your_plugin_name/
addons/ is installed directly into the user’s project.

When someone downloads your asset and enables the plugin, the entire addons/your_plugin_name/ folder is copied into their project.

If you put docs and screenshots in there, they will be copied too, even though they’re useless at runtime.

Avoid clutter in user projects.

Users don’t want a bunch of markdown files, license copies, or screenshots showing up in their FileSystem dock.

They just want the plugin files (scripts, scenes, plugin.cfg, etc.).

Prevent import issues.

If you put screenshots in the plugin folder, Godot may try to import them as textures unless you .gdignore them.

Keeping them outside makes it cleaner and avoids accidental imports.

Godot AssetLib previews don’t come from the repo.

You upload screenshots separately to the AssetLib submission form.

They don’t need to ship with the addon at all — they’re only for the store page.

If you keep them in the repo, it’s usually just for versioning / documentation, not for users.

📂 Typical Good Layout
my_plugin_repo/
│
├─ addons/
│   └─ my_plugin/
│       ├─ plugin.cfg
│       ├─ plugin.gd
│       ├─ icon.png
│       ├─ scripts/...
│       └─ scenes/...
│
├─ docs/
│   ├─ README.md
│   ├─ USAGE.md
│   └─ .gdignore
│
├─ screenshots/
│   ├─ preview1.png
│   ├─ preview2.png
│   └─ .gdignore
│
├─ LICENSE
├─ README.md
├─ .gitignore
├─ .gitattributes
addons/my_plugin/ → only what’s required for the plugin to run.

docs/ → extra documentation (ignored by Godot, but useful in repo).

screenshots/ → preview images for AssetLib (not shipped to user projects).

Root README.md + LICENSE → for repo + GitHub page.

👉 So the rule is:
Keep addons/ clean = runtime only.
Everything else (docs, screenshots, tests, dev stuff) lives outside.

Do you want me to also show you how to make .gitattributes auto-exclude docs/ and screenshots/ from the ZIP that AssetLib pulls, so users never even download them?

You said:
Yes.
But also should I know ignore the root zone of the projet with a .gdignore ?
ChatGPT said:
Great question 👌 Let’s break this down carefully:

1. .gdignore at the root of your project
⚠️ Do NOT put a .gdignore in the root of your repo.

Reason:

A .gdignore tells Godot “ignore everything inside this folder”.

If you put it in the root, Godot won’t import anything, including your addon/plugin itself — effectively making your asset invisible to Godot.

That would defeat the whole purpose 😅.

👉 .gdignore should only live in folders that contain non-runtime resources you don’t want Godot to import (like docs/ or screenshots/).

2. Best use of .gdignore
Inside docs/ → to stop .md, .txt, .pdf from showing in Godot.

Inside screenshots/ → to stop .png previews from being imported as textures.

Inside tests/ (if you ship unit tests) → to keep test scenes/scripts from being imported into user projects.

Example:

docs/
    README.md
    .gdignore
screenshots/
    preview1.png
    preview2.png
    .gdignore
Each .gdignore is just an empty file.

3. .gitattributes for clean AssetLib ZIP
You want to make sure that when users download from the Godot AssetLib, the ZIP contains only addons/my_plugin and the root LICENSE/README.

Here’s a good .gitattributes:

# Ignore dev-only stuff in exported ZIPs
/docs export-ignore
/screenshots export-ignore
/tests export-ignore
/.github export-ignore
.gitignore export-ignore
.gitattributes export-ignore
This way:

AssetLib ZIP won’t include your docs or screenshots at all.

Users only get what they need.

✅ Recommended structure for your repo
my_plugin_repo/
│
├─ addons/
│   └─ my_plugin/
│       ├─ plugin.cfg
│       ├─ plugin.gd
│       ├─ icon.png
│       ├─ scripts/...
│       └─ scenes/...
│
├─ docs/
│   ├─ README.md
│   └─ .gdignore
│
├─ screenshots/
│   ├─ preview1.png
│   ├─ preview2.png
│   └─ .gdignore
│
├─ LICENSE
├─ README.md
├─ .gitignore
├─ .gitattributes
addons/ → shipped to the user.

docs/ & screenshots/ → useful for GitHub & submission, ignored by Godot & ZIP.

Root LICENSE & README → visible in repo & GitHub page.

✨ So the short answer:

❌ Don’t use .gdignore at the repo root.

✅ Only use .gdignore inside non-runtime folders (docs/, screenshots/).

✅ Use .gitattributes to keep the AssetLib ZIP clean.

Do you want me to draft a ready-to-drop set of .gitignore, .gitattributes, and .gdignore files for this exact layout so you can just copy them into your repo?

You said:
Should I add to gitatrribute
project.godot
ChatGPT said:
Excellent catch — this one trips up a lot of people 👀

Let’s go step by step:

🔎 What is project.godot?
It’s the Godot project configuration file at the root of your project.

It defines things like project settings, display options, and registered plugins.

Without it, Godot doesn’t recognize the folder as a project.

🤔 Should you export-ignore it in .gitattributes?
No — do NOT exclude it.

Here’s why:

Plugins (addons) need a host project to develop and test.

When you publish to the AssetLib, people don’t download your whole project, they download the ZIP at a specific path you define.

Example: if you set the download path to addons/my_plugin/, users won’t even see your project.godot.

If you set the root as the download path (repo root), then yes, project.godot would be included.

If you remove/ignore it, your repo stops being a valid Godot project on GitHub (harder for contributors to open and test).

🛠️ Best practice for AssetLib submissions
Keep project.godot in the repo (don’t ignore it).

In .gitattributes, only mark non-essential stuff (docs, screenshots, tests, CI config) as export-ignore.

When you submit to AssetLib, you can point the download folder directly to addons/my_plugin/ — then users only get the addon, not your whole test project.

That way:

Your repo = full project with test/demo scenes.

AssetLib users = only get the clean addon folder.

✅ Example .gitattributes for this setup:

# Ignore dev-only stuff in AssetLib ZIPs
/docs export-ignore
/screenshots export-ignore
/tests export-ignore
/.github export-ignore
.gitignore export-ignore
.gitattributes export-ignore
Notice: no project.godot here — you keep it in GitHub, but users don’t see it because they only download the addons/my_plugin/ path.

⚡ So the rule:

Keep project.godot in repo for dev/testing.

Don’t export-ignore it — instead, control what path AssetLib ZIP uses.

👉 Do you want me to show you how to set the AssetLib submission download path so users get only addons/my_plugin/ and not the full repo (with project.godot)?




No file chosenNo file chosen
ChatGPT can make mistakes. Check important info. See Cookie Preferences.
