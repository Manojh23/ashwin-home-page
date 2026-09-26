# Ashwin's Personal Home Page

A front-end only personal website built with plain HTML, CSS and ES6 modules.
The visual language is built from trapezoids and a muted palette.

- **Author:** Ashwin Satish Bhat
- **Course:** [CS5610 Web Development](https://johnguerra.co/classes/webDevelopment_online_fall_2026/index.html),
  Northeastern University

## Objective

Build a personal home page that runs entirely in the browser without using any additional libraries or frameworks. It has to hold real information about me
and my work, be organised well enough that someone else can find their way
around the source, and include an original component of my own rather than a
stock template.

The site is three pages:

- **Home** — who I am, what I'm learning, and the projects I care about.
- **Work** — the full project write-ups, plus my ink sketches and pixel art.
- **Lab** — a deliberately AI-generated page, kept next to the hand-written
  ones so the two can be compared.

## Original component

The original component is a set of vim motions that work across the whole
site: `h` and `l` move between pages, `gg` returns to the top, and `?` opens
the shortcut list. The idea comes from [learn.nvim](https://github.com/bash-win/learn.nvim), a Neovim plugin I wrote for practising motions.

## Screenshots

### Home

![Home page, showing the intro heading, a short bio and interest tags on a dark background](images/screenshots/Home.png)

### Work

![The art section of the Work page, showing a pixel art knight in a framed gallery panel](images/screenshots/Art.png)

### Lab

![The AI-generated Lab page, showing the trapezoid lattice background and the telemetry panel](images/screenshots/AI.png)

## Running it locally

```sh
npm install
npm start
```

`npm start` serves the folder at <http://localhost:3000>. A server is needed
rather than opening `index.html` directly: you can use reload to host the server locally.

## Scripts

| Script                 | What it does                     |
| ---------------------- | -------------------------------- |
| `npm start`            | Serve the site on a local port   |
| `npm run lint`         | ESLint over the JavaScript       |
| `npm run format`       | Format everything with Prettier  |
| `npm run format:check` | Check formatting without writing |

## Structure

- `css/` — stylesheets, one per page plus the shared base, layout and
  components
- `js/` — ES6 modules; the Lab page's modules live in `js/ai/`
- `images/` — the favicon, my artwork in `images/art/`, and screenshots

## Links

- [`Demonstration`](https://www.youtube.com/watch?v=kpwYC8rTG5I)
- [`Presentation`](https://www.youtube.com/watch?v=f3o7HpAzjEY)

## Generative AI

Generative AI was used to create some parts of this codebase. The entirety of the `Lab` page was entirely AI generated.

- **Models:** Claude Opus 5.5 and Claude Opus 5
- **Tool:** Claude Code

The (`ai.html`) page was entirely AI generated, including the markup, `css/ai.css`, and the modules under
`js/ai/`. It sits beside Home and Work so the two styles can be compared. The
favicon and the layout of the project presentation were generated as well.

Development was iterative, with review and correction between
them. One example, from the start of the Lab page:

> Based on the design document and the code already existing in the repo for
> the home and work pages, create a page called Lab that sits beside the work
> page. You are only allowed to use plain HTML, CSS and JavaScript. The motif
> and the color scheme should follow the ones already existing. Do not make
> changes until we decide on what should be put on the page. Give me exactly
> what you will change.

## License

MIT
