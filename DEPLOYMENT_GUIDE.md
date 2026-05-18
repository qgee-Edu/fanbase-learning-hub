# Deployment guide: GitHub web upload

Step by step for getting this package into your existing `fanbase-learning-hub` repo using only the GitHub web interface.

**Total time: about 10 minutes.**

The single most important rule: **never upload the zip file itself**. Always unzip first, then upload the *contents* folder by folder. The web uploader will sometimes flatten zip contents, which is what broke the last deploy.

---

## Step 1: Unzip the package on your computer

1. Download `fanbase-learning-hub.zip` (the file Claude gave you).
2. Double-click it to unzip.
3. You'll see a folder called `fanbase-learning-hub`. Open it.
4. Inside, you should see this structure:

```
fanbase-learning-hub/
├── docs.json
├── index.mdx
├── README.md
├── DEPLOYMENT_GUIDE.md  (this file)
├── business-center/
├── creator-academy/
├── images/
└── knowledge-center/
```

Keep this folder open in Finder/File Explorer. You'll be uploading from here.

---

## Step 2: Wipe the existing repo on GitHub

1. Go to `https://github.com/qgee-Edu/fanbase-learning-hub`
2. **Important:** Make sure you're on the `main` branch (the dropdown near the top left).
3. Click into each file and folder in the repo and delete it. Here's the fast way:

For files at the root (docs.json, index.mdx, README.md, etc):
- Click the filename
- Click the trash can icon at the top right of the file view
- Scroll down, type a commit message like "Wipe for fresh build"
- Click "Commit changes"
- Repeat for each file at root

For folders (business-center, creator-academy, knowledge-center, images, mnt):
- Click into the folder
- Click into each file inside
- Delete each file using the trash icon
- The folder disappears once it's empty (GitHub doesn't track empty folders)

When you're done, your repo should be completely empty. The page will show "This repository is empty."

---

## Step 3: Upload the root files first

1. On the empty repo page, click the **"Add file"** dropdown near the top right.
2. Click **"Upload files"**.
3. From your unzipped `fanbase-learning-hub` folder on your computer, drag these 4 files onto the upload area:
   - `docs.json`
   - `index.mdx`
   - `README.md`
   - `DEPLOYMENT_GUIDE.md` (optional, can skip if you want)
4. Scroll down. Commit message: "Add root files"
5. Click **"Commit changes"**.

Wait for GitHub to finish. You'll see the 4 files at the repo root.

---

## Step 4: Upload the business-center folder

Here's the critical trick: **GitHub's uploader lets you "type a folder path" into the filename area before committing.** This is how you place files into a folder without dragging the folder itself.

1. On your repo page, click **"Add file" > "Upload files"** again.
2. From your computer, open the `fanbase-learning-hub/business-center/` folder.
3. Select all 4 `.mdx` files inside (overview.mdx, getting-paid.mdx, payment-account-setup.mdx, subscriptions-and-pricing.mdx).
4. Drag them onto the GitHub upload area.
5. **Important:** At the top of the upload page, you'll see a breadcrumb that says `fanbase-learning-hub /`. Click in that area where the breadcrumb is and **type** `business-center/` then press Tab or click outside the field. The path should now show `fanbase-learning-hub / business-center /`.
6. Scroll down, commit message: "Add business-center module pages"
7. Click **"Commit changes"**.

After this commit, the `business-center` folder will exist in your repo with all 4 files inside it.

---

## Step 5: Upload the knowledge-center folder

Same drill, different folder:

1. Click **"Add file" > "Upload files"**.
2. Open the `fanbase-learning-hub/knowledge-center/` folder on your computer.
3. Select all 3 `.mdx` files inside (overview.mdx, getting-started.mdx, fanbase-features.mdx).
4. Drag them to the GitHub upload area.
5. In the breadcrumb at top, type `knowledge-center/`.
6. Commit message: "Add knowledge-center module pages"
7. Commit.

---

## Step 6: Upload the creator-academy folder

1. Click **"Add file" > "Upload files"**.
2. Open the `fanbase-learning-hub/creator-academy/` folder on your computer.
3. Select all 4 `.mdx` files inside.
4. Drag them to the GitHub upload area.
5. Type `creator-academy/` in the breadcrumb.
6. Commit message: "Add creator-academy module pages"
7. Commit.

---

## Step 7: Upload the images folders

Three sub-folders to do here. The home hero image goes at the root.

### 7a. Root image (home-hero.svg)

1. Click **"Add file" > "Upload files"**.
2. Drag just `images/home-hero.svg` from your computer.
3. Type `images/` in the breadcrumb.
4. Commit message: "Add home hero image"
5. Commit.

### 7b. business-center images

1. Click **"Add file" > "Upload files"**.
2. Open `fanbase-learning-hub/images/business-center/` on your computer.
3. Select all 5 image files inside (4 SVG + 1 PNG).
4. Drag them up.
5. Type `images/business-center/` in the breadcrumb.
6. Commit. Commit message: "Add business-center images"

### 7c. knowledge-center images

1. Click **"Add file" > "Upload files"**.
2. Open `fanbase-learning-hub/images/knowledge-center/` on your computer.
3. Select all 7 image files inside.
4. Drag them up.
5. Type `images/knowledge-center/` in the breadcrumb.
6. Commit. Commit message: "Add knowledge-center images"

### 7d. creator-academy images

1. Click **"Add file" > "Upload files"**.
2. Open `fanbase-learning-hub/images/creator-academy/` on your computer.
3. Select all 9 image files inside.
4. Drag them up.
5. Type `images/creator-academy/` in the breadcrumb.
6. Commit. Commit message: "Add creator-academy images"

---

## Step 8: Verify the repo structure

When you're done, your repo's root view should look like this:

```
business-center/        (folder, 4 files inside)
creator-academy/        (folder, 4 files inside)
images/                 (folder, 22 files across subfolders)
knowledge-center/       (folder, 3 files inside)
DEPLOYMENT_GUIDE.md
README.md
docs.json
index.mdx
```

Click into each folder to verify the files landed in the right place. **There should be NO loose `.mdx` files at the root except `index.mdx`.** If you see files like `getting-paid.mdx` floating at the root, that file got dropped in the wrong place and needs to be moved (see Troubleshooting below).

---

## Step 9: Wait for Mintlify to deploy

Mintlify auto-deploys on every push. Each commit you made in steps 3 through 7 triggered a build. The final build (after all your commits) is what matters.

1. Go to `https://dashboard.mintlify.com` and click into your Fanbase project.
2. Click **Deployments** in the left sidebar.
3. Look at the most recent deployment. It should say "Successful" with a green check.
4. If you see a failed build (red X), click into it to see the error. Send Claude the error message.

---

## Step 10: Check the live site

Go to `https://fanbase.mintlify.app/`

You should see:
- A dark purple landing page
- The Fanbase lightning bolt hero
- Three tabs at the top: Business Center, Knowledge Center, Creator Academy
- All three tabs lead to pages with content (no 404s)

If everything renders, you're done.

---

## Troubleshooting

### "404 Page Not Found" on a specific page

That page didn't upload to the right folder. Click into the folder it should be in and check if it's there. If not, re-upload it using Step 4/5/6's instructions, making sure the breadcrumb shows the right folder path.

### Some `.mdx` files ended up at the repo root

You skipped typing the folder path in the breadcrumb during upload. Fix:

1. Click the misplaced file
2. Click the pencil icon to edit
3. In the filename field at the top, change `getting-paid.mdx` to `business-center/getting-paid.mdx`
4. Click "Commit changes"
5. The file moves into the right folder

### Build fails on Mintlify

Go to Mintlify dashboard > Deployments > click the failed build > read the error message. Send the exact text to Claude.

### Images don't load

The image file path in MDX doesn't match the file's actual location in the repo. Check that `images/knowledge-center/2-1-cover.png` actually exists at that path in the repo.
