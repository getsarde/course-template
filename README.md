# course-template

A [Sarde](https://github.com/getsarde/sarde) site template for publishing course material: lessons, assignments, hands-on labs, and announcements. Clone it, replace the sample courses with your own, and build a static site you can host anywhere.

**Live demo:** [getsarde.github.io/course-template](https://getsarde.github.io/course-template/)

## What's included

- **Two sample courses** in `content/courses/`, Web Fundamentals and Python Essentials. Each course is a tab in the sidebar's course switcher, with lessons, an `assignments/` group, and its own announcements and schedule pages.
- **Labs** in `content/labs/`, grouped by course. Multi-step labs show a progress bar and prev/next links that stay inside the lab, and `hello-world` shows a lab that fits on one page.
- **A site-wide announcements page** for news that affects every course, plus a sample banner (in `sarde.yaml`) that appears only on one course's lessons and labs.
- **A homepage** with a hero and links to each course.
- **Quick navigation:** press <kbd>Ctrl</kbd>+<kbd>/</kbd> (<kbd>Cmd</kbd>+<kbd>/</kbd> on Mac) to jump to a page by name, through the Telescope plugin enabled in `sarde.yaml`.

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

The [Course Template guide](https://getsarde.github.io/sarde/docs/teaching/course-template/) in the Sarde docs walks through the site and how to change it:

- [What's in the template](https://getsarde.github.io/sarde/docs/teaching/course-template/#what-s-in-the-template): every file and what it is for
- [Courses](https://getsarde.github.io/sarde/docs/teaching/course-template/#courses): course overviews, the order of pages in a course, assignments, and the course catalog
- [Schedules](https://getsarde.github.io/sarde/docs/teaching/course-template/#schedules): the weekly timeline, and collapsible weeks for a full semester
- [Announcements](https://getsarde.github.io/sarde/docs/teaching/course-template/#announcements): course news, site-wide news, and a banner for one course
- [Replace the sample content](https://getsarde.github.io/sarde/docs/teaching/course-template/#replace-the-sample-content): a checklist for making the site your own

## Publish on GitHub Pages

`.github/workflows/deploy.yml` publishes the site to GitHub Pages on every push to `main`. In the repository, open **Settings > Pages** and set **Source** to **GitHub Actions**; until then the workflow fails. [Publish on GitHub Pages](https://getsarde.github.io/sarde/docs/teaching/course-template/#publish-on-github-pages) covers the details and other hosts.

## License

[MIT No Attribution (MIT-0)](LICENSE). You can use, change, and publish the template, including the sample content, without keeping the copyright notice or crediting this repository.
