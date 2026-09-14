# Mogshade Games website

This folder contains the complete private-preview website for Mogshade Games.

It is a plain static website. There is no build process, no software to install, and no external artwork, JavaScript, tracking or mailing-list service.

## What is included

- `index.html`: the homepage and five-game showcase
- `about.html`: the full Mogshade Games story
- `styles.css`: all colours, typography and responsive layout rules
- `404.html`: a friendly page for incorrect addresses
- `robots.txt`: asks search engines not to index this private preview

Every game is marked **In Development**:

1. The Tell-Tale Club
2. KHAOS
3. Regency: The Season
4. Grannie’s Hoose
5. The Slaughter Slog

## Look at the site on your computer

1. Extract the ZIP file.
2. Open the extracted `mogshade-site` folder.
3. Double-click `index.html`.
4. Your normal web browser should open the homepage.
5. Test the Games, About and Mailing list links.

The website may also be previewed from a simple local web server, but this is optional. Double-clicking `index.html` is enough for an initial review.

## Recommended route: private GitHub repository and Vercel

GitHub will hold the files. Vercel will turn them into the website whenever the GitHub files change.

### Part 1: put the files on GitHub

1. Sign in to [GitHub](https://github.com/).
2. Use the plus menu in the upper-right corner and choose **New repository**.
3. Name it `mogshade-games-site`.
4. Choose **Private**.
5. Do not add another README, because this package already contains one.
6. Create the repository.
7. In the empty repository, choose **Add file**, then **Upload files**.
8. Drag the five extracted website files into the upload area. Upload the files themselves, not the outer folder or the ZIP.
9. Check that `index.html` appears at the top level of the repository.
10. Enter a short message such as `Add first Mogshade website` and commit the files.

Official GitHub help: [Creating a new repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)

### Part 2: connect the repository to Vercel

1. Sign in to [Vercel](https://vercel.com/) using your GitHub account.
2. Create a new project and import `mogshade-games-site` from GitHub.
3. Leave the project root as the repository root.
4. This site has no framework, build command or output folder. Vercel can serve the HTML and CSS files directly.
5. Deploy the project.
6. Open the generated address and check the homepage and About page.

Once connected, future changes committed to GitHub will create new Vercel deployments automatically.

Official Vercel help: [Deploying GitHub projects with Vercel](https://vercel.com/docs/git/vercel-for-github)

## Keep the preview private

The `noindex` settings in these files discourage search engines, but they do not stop somebody opening a URL they already know.

For a protected Vercel preview:

1. Open the project in Vercel.
2. Open **Settings**.
3. Select **Deployment Protection**.
4. Enable Vercel Authentication for the preview and deployment URLs.
5. Share only an access-controlled preview link with reviewers.

Vercel currently makes Standard Protection available across its plans, but its free protection does not make a production domain private. Use protected preview or deployment URLs during review and check the current plan details before relying on a production address.

Official Vercel help: [Deployment Protection](https://vercel.com/docs/deployment-protection)

GitHub Pages is designed to publish a website publicly. Even when a plan permits the source repository to be private, the published Pages website is public. For that reason, GitHub Pages is not the recommended private-preview route.

Official GitHub help: [Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

## Before a public launch

Complete these jobs only when the website is ready for everyone:

1. Remove `<meta name="robots" content="noindex, nofollow">` from `index.html`, `about.html` and `404.html`.
2. Delete `robots.txt`, or replace `Disallow: /` with the crawler rules you want.
3. Connect the mailing-list area to a real mailing provider before adding an email form.
4. Add final, approved artwork only when it is ready.
5. Add working game pages when there is enough public information for each project.
6. Add a custom domain and verify every page on a phone and computer.

## Safe editing rules

- Keep `index.html`, `about.html`, `404.html` and `styles.css` together.
- Keep status wording as real text rather than placing it inside artwork.
- Avoid changing filenames unless every link to that file is changed too.
- Do not place private, personal or confidential information in the website files.
- Keep the older prototypes in a separate archive so they are not uploaded by mistake.

## Current status

This package is ready for private review. It has not been published and its mailing-list area does not collect personal information.
