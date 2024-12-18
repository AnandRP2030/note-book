To publish your Honkit plugin project using GitHub Pages and remove the "Published by Honkit" watermark, follow these steps:

### 1. Publish Your Project Using GitHub Pages

GitHub Pages allows you to host your project directly from a GitHub repository. Here’s how you can do it:

#### Step 1: Set up the Honkit Build

1.  Build Your Honkit Project:  
    If you haven't already, you need to build your Honkit project first. In your project folder, run:

    honkit build

    This will generate a \_book folder with the compiled version of your book or documentation.

2.  Push the Build to a GitHub Repository:  
    If your repository is already set up on GitHub and you’ve pushed the source code, you need to push the built \_book folder (which contains the compiled HTML files) to a branch that GitHub Pages can serve.

    A typical approach is to push it to a gh-pages branch.

    - Switch to the gh-pages branch:

           git checkout -b gh-pages

    - Copy the contents of the \_book folder into the root directory of this branch.

           cp -r _book/* ./

    - Commit and push:

           git add .

      git commit -m "Publish Honkit book to GitHub Pages"
      git push origin gh-pages

#### Step 2: Enable GitHub Pages

1. Go to Your GitHub Repository:  
   Open your repository on GitHub.

2. Access Repository Settings:  
   Click on the "Settings" tab.

3. GitHub Pages Section:  
   Scroll down to the GitHub Pages section.

4. Select the `gh-pages` Branch:  
   From the "Source" dropdown, choose the gh-pages branch. This will make GitHub Pages serve the content from that branch.

5. Save and View:  
   After selecting the gh-pages branch, GitHub will automatically provide you with a link to your published site.

   It may take a few minutes for the site to be live.

---

### 2. Remove the "Published by Honkit" Watermark

The "Published by Honkit" watermark is part of the default theme for Honkit, and it appears at the bottom of each page in the generated documentation. If you want to remove it, you will need to customize the template.

#### Step 1: Customize the Theme

To remove or change the watermark, you will need to customize the theme used by Honkit.

1. Create a Custom Theme Directory:  
   In your project, create a directory called theme.

   mkdir theme

2. Copy the Default Theme Files:  
   You can copy the default theme’s footer HTML to customize it. Inside the theme directory, create a footer.html file and customize it.

   - Navigate to your node_modules/honkit/lib/theme folder and find the default footer.html.
   - Copy the contents of the footer and place it inside your theme/footer.html file.

3. Edit the Watermark:  
   In the footer.html, you should see a section where the watermark text is inserted. Remove or modify this section as needed.

#### Step 2: Tell Honkit to Use Your Custom Theme

1. Edit `book.json`:  
   Add the theme configuration to your book.json file to let Honkit know to use your custom theme.

   {
   "theme": "theme"
   }

2. Rebuild the Book:  
   After making the changes, rebuild your book using:

   honkit build

3. Publish Again:  
   After the build is complete, follow the same steps to push the new content to the gh-pages branch.

---

### 3. Final Steps

- After pushing your updates, your site should be live without the watermark.
- Visit the GitHub Pages URL provided in your repository settings to view the live version of your documentation without the watermark.

By following these steps, you’ll have successfully removed the Honkit watermark and published your project to GitHub Pages!

#note #book #gh-pages #publish
