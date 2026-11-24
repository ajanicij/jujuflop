## What is jujuflop?

**jujuflop** is an open-source, Git-based publishing platform designed to make managing and publishing a personal website or blog simple, portable, and independent of any particular hosting platform.

The central idea is that **your content lives in a Git repository**. Articles, pages, images, and other assets are maintained as ordinary files, using Markdown and YAML front matter. The repository can be hosted anywhere Git is supported, such as GitHub, GitLab, or a self-hosted Git server.

jujuflop takes care of turning that content into a published website.

### How it works

The project is built around three main responsibilities:

- **Content repository** — The source of truth for the website. It contains Markdown articles and pages, metadata, images, and other static assets. The content format aims to follow conventions established by popular static site generators such as Hugo and Zola, rather than introducing an entirely new format.

- **Publishing engine** — Synchronizes with the content repository, processes and validates content, generates HTML and other published artifacts, builds a search index, and generates feeds such as RSS and Atom. It can also serve as the integration point for publishing content to social and federated platforms.

- **Web server** — Serves the generated website and provides interactive functionality such as search and comments. It handles visitor-facing requests independently of the publishing process.

These responsibilities are logically separated so that the publishing engine and web server can be implemented, deployed, and replaced independently.

### Design principles

jujuflop follows a few straightforward principles:

- **Git as the source of truth.** Content is stored in a regular Git repository, making it easy to version, back up, migrate, and manage.
- **Portable content.** Markdown and YAML front matter keep content readable and usable outside jujuflop. Compatibility with Hugo and Zola conventions is a priority.
- **Separation of concerns.** Content management, publishing, and serving the website are distinct responsibilities.
- **No platform lock-in.** The content repository should not depend on a particular hosting provider, cloud platform, or web server.
- **Open standards and interoperability.** Where possible, use established formats and protocols, including RSS, Atom, ActivityPub, and AT Protocol.
- **Keep it simple.** Start with a small, useful system and introduce additional capabilities only when there is a real need for them.

### The goal

The goal is not to build another large, all-in-one content management system. It is to build a small, understandable, and extensible publishing platform that gives authors control over their content and the freedom to publish it wherever they choose.

jujuflop should be useful first as a personal publishing tool, while leaving room to grow into something more capable over time.
