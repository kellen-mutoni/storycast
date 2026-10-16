# StoryCast

StoryCast is an accessible 3-page microsite that shares short audio and video stories about how local films and music get made. It is built with semantic HTML5 and Sass, with no frameworks.

## Pages

- **Home** (`index.html`): introduces StoryCast and features stories.
- **Story** (`story/story-1.html`): a behind-the-scenes video with captions, an audio-only version, a transcript, and related stories.
- **About** (`about.html`): the mission, the accessibility features, and how to engage.

## Project structure

```
storycast/
  index.html
  about.html
  README.md
  StoryCast_Research.pdf
  story/
    story-1.html
  sass/
    _colors.scss
    _typography.scss
    _spacing.scss
    _layout.scss
    _components.scss
    _pages.scss
    main.scss
  css/
    main.css
  assets/
    story-1.mp4
    story-1.rw.vtt
    story-1.en.vtt
```

## Accessibility checklist

- [x] Semantic HTML5: `header`, `nav`, `main`, `article`, `section`, `figure`, `footer`.
- [x] One `h1` per page, with headings in order (h1, h2, h3).
- [x] Video has captions in Kinyarwanda and English (`<track>`), and a description (`<figcaption>`).
- [x] Audio-only version of the story using `<audio>`.
- [x] Full text transcript on the Story page.
- [x] Colors meet WCAG AA: black on cream 20.3:1, olive on cream 10.7:1.
- [x] Visible focus outline on every link, button, and player control.
- [x] Full keyboard navigation, tested with the Tab key only.
- [x] "Skip to main content" link on every page.
- [x] `aria-current="page"` marks the current page in the menu.
- [x] `aria-label` and `aria-labelledby` name the menus and sections.
- [x] `lang` attributes: pages are English, Kinyarwanda words are marked `lang="rw"`.
- [x] Sizes use `rem`, so text scales with the user's browser settings.

## Design and code approach

- **Sass:** partials and tokens for colors, typography, and spacing.
- **Naming:** BEM (block, element, modifier), for example `card__title` and `card--soon`.
- **Cascade layers:** `base`, `layout`, and `components`.
- **Layouts:** CSS Grid for the card lists and Flexbox for the header, menu, and footer.
- **Container query:** the `card` component changes layout based on its own width.

## Run locally

1. Download or clone this repository.
2. Open the `storycast` folder in VS Code.
3. Right-click `index.html` and choose **Open with Live Server**.

## Research

The sitemap, wireframes link, and high-fidelity mockups link are in `StoryCast_Research.pdf`.