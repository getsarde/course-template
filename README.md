# course-template

A [Sarde](https://github.com/getsarde/sarde) site template for publishing course material: lessons, assignments, hands-on labs, and announcements. Clone it, replace the sample courses with your own, and build a static site you can host anywhere.

**Live demo:** [getsarde.github.io/course-template](https://getsarde.github.io/course-template/)

## What's included

- **Two sample courses** in `content/courses/`, Web Fundamentals and Python Essentials. Each course is a tab in the sidebar's course switcher, with lessons and an `assignments/` group.
- **Labs** in `content/labs/`, grouped by course. Multi-step labs show a progress bar and prev/next links that stay inside the lab, and `hello-world` shows a lab that fits on one page.
- **An announcements page** with a course schedule.
- **A homepage** with a hero and links to each course.

The sample pages use Sarde's Markdown extensions (tabs, steps, asides, collapsible panels, terminal blocks, file trees, a timeline) so you can see them in context. The [extensions guide](https://getsarde.github.io/sarde/docs/extensions/using-extensions/) lists every extension and its syntax.

The code samples show what Sarde's code blocks can do: file titles, a terminal frame, line numbers, labelled line highlights, inserted and deleted lines, highlighted words, focused lines, a collapsed block, and tabbed code groups. Each block also has a toolbar button that switches it between light and dark on its own. The [code blocks guide](https://getsarde.github.io/sarde/docs/guides/code-blocks/) covers each option.

## Run the site

You need the `sarde` command. The [Getting Started guide](https://getsarde.github.io/sarde/docs/start-here/getting-started/) covers installing it with Homebrew, the install script, or `go install`.

1. Clone the template:

   ```bash
   git clone https://github.com/getsarde/course-template.git my-course
   cd my-course
   ```

2. Start the dev server:

   ```bash
   sarde dev
   ```

   Open `http://localhost:4727`. The site rebuilds and the browser reloads each time you save a file.

3. Build the site for production:

   ```bash
   sarde build
   ```

   The finished site is in `dist/`. See [Deploying](https://getsarde.github.io/sarde/docs/start-here/deploying/) to publish it.

## Make it yours

1. In `sarde.yaml`, set `site.title`, `site.description`, and `site.url`, and change the homepage hero text and buttons under `homepage.hero`.
2. Replace the sample courses. Each directory in `content/courses/` is one course:
   - `_index.md` is the course overview. Its `title`, `description`, and `icon` appear in the course switcher.
   - Each other `.md` file is a lesson. Set `sidebar.order` to control the lesson order.
   - `sidebar.badge` adds a label such as "Beginner" or "Assignment" next to an entry in the sidebar.
3. Replace the sample labs. `content/labs/<course>/<lab>/` holds one lab: its `_index.md` is the lab introduction (with optional `learning_objectives`), and each step is a separate page ordered with `sidebar.order`.
4. Update `content/announcements.md` and the course links in `content/_index.md`.

Lessons, assignments, and lab pages include a "Replace this with..." note in their opening paragraph. Search for that phrase to find sample text you haven't replaced yet.

## Publish on GitHub Pages

The template includes a GitHub Actions workflow, `.github/workflows/deploy.yml`, that builds the site and publishes it to GitHub Pages on every push to `main`.

1. Push your copy of the template to a GitHub repository.
2. In the repository, open **Settings > Pages** and set **Source** to **GitHub Actions**.
3. Push to `main`, or run the workflow from the **Actions** tab.

The site is published at `https://<owner>.github.io/<repository>/`. The workflow reads that address from GitHub Pages and passes it to Sarde, so `sarde.yaml` needs no deployment settings, and a custom domain set under **Settings > Pages** works the same way. Until Pages is enabled, the workflow fails. Delete the workflow file if you host the site elsewhere; [Deploying](https://getsarde.github.io/sarde/docs/start-here/deploying/) covers other hosts.

## Learn more

- [Labs](https://getsarde.github.io/sarde/docs/teaching/labs/): lab structure, numbering, and progress
- [Tabbed navigation](https://getsarde.github.io/sarde/docs/guides/tabbed-navigation/): how the course switcher and course sidebars work
- [Frontmatter reference](https://getsarde.github.io/sarde/docs/reference/frontmatter/): every page field, including `sidebar.order` and `sidebar.badge`

## License

[MIT No Attribution (MIT-0)](LICENSE). You can use, change, and publish the template, including the sample content, without keeping the copyright notice or crediting this repository.
