# Assignment #3. Responsive Web Design (Media Queries + Bootstrap Grid)

**Name:** Torekhan Taimas
**Group:** IT-2503

## Project Structure

```
WEB assignment 3/
├── part1/
│   ├── index.html
│   └── style.css
├── part2/
│   └── index.html
├── part3/
│   ├── index.html
│   └── style.css
└── README.md
```

---

## Part 1. Media Queries

Tasks 0 and 1 are on the same page: `part1/index.html`.
Custom CSS is written desktop-first: desktop styles are the default, and `max-width` media queries override them for tablet and mobile.

Breakpoints:

| Device  | Width           |
|---------|-----------------|
| Desktop | 1024px and up   |
| Tablet  | 768px - 1023px  |
| Mobile  | up to 767px     |

### Task 0. Responsive Typography

**Task:** Create a simple webpage with headings and paragraphs. Use media queries to change font sizes for mobile, tablet, and desktop.

**Result:** The page contains an `h1`, an `h2` and two paragraphs. Font sizes are largest on desktop, medium on tablet, and smallest on mobile.

Desktop:

![Task 0 desktop](screenshots/task0-desktop.png)

Tablet:

![Task 0 tablet](screenshots/task0-tablet.png)

Mobile:

![Task 0 mobile](screenshots/task0-mobile.png)

### Task 1. Responsive Layout with Media Queries

**Task:** Create a webpage with three boxes in a row. On desktop, display all three side by side. On tablet, display two boxes in a row. On mobile, display boxes stacked vertically. Use only CSS media queries (no Bootstrap).

**Result:** The boxes are in a flex container with `flex-wrap: wrap`. Their width changes with the screen size: one third of the row on desktop, one half on tablet, and the full width on mobile.

Desktop (three in a row):

![Task 1 desktop](screenshots/task1-desktop.png)

Tablet (two in a row):

![Task 1 tablet](screenshots/task1-tablet.png)

Mobile (stacked):

![Task 1 mobile](screenshots/task1-mobile.png)

---

## Part 2. Bootstrap Grid System

Tasks 2 and 3 are on the same page: `part2/index.html`.

### Task 2. Bootstrap Responsive Columns

**Task:** Build a responsive layout using Bootstrap's 12-column grid with three columns. On desktop, each column takes 4 columns (3 equal parts). On tablet, two columns on the first row and one on the second row. On mobile, all columns stacked.

**Result:** Each column uses the classes `col-12 col-md-6 col-lg-4`.

- Mobile: `col-12`, each column takes the full width.
- Tablet (768px and up): `col-md-6`, two columns per row, the third wraps to the second row.
- Desktop (992px and up): `col-lg-4`, three equal columns.

Desktop:

![Task 2 desktop](screenshots/task2-desktop.png)

Tablet:

![Task 2 tablet](screenshots/task2-tablet.png)

Mobile:

![Task 2 mobile](screenshots/task2-mobile.png)

### Task 3. Bootstrap Navigation Bar

**Task:** Create a responsive navigation bar using Bootstrap components. It should include a logo on the left, links on the right, and collapse into a hamburger menu on smaller screens.

**Result:** The navbar uses `navbar-expand-lg`. The logo is `navbar-brand`, the links are in `navbar-nav ms-auto` so they are pushed to the right, and the hamburger button uses `data-bs-toggle="collapse"` to open the menu below 992px.

Desktop (full menu):

![Task 3 desktop](screenshots/task3-desktop.png)

Mobile (collapsed, hamburger button):

![Task 3 mobile collapsed](screenshots/task3-mobile-collapsed.png)

Mobile (menu opened):

![Task 3 mobile opened](screenshots/task3-mobile-opened.png)

---

## Part 3. Combined Project

### Task 4. Responsive Portfolio Page

**Task:** Create a portfolio page using both Media Queries and Bootstrap Grid. Requirements: a header with a Bootstrap navbar; a main section divided into two parts (left: portfolio projects arranged with the Bootstrap grid as cards, right: sidebar with personal info and contact details); a footer across the bottom. Apply custom media queries to adjust font sizes, spacing, and element visibility for mobile, tablet, and desktop.

**Result:**

- Header: Bootstrap navbar with a collapsing menu.
- Projects: `col-12 col-lg-8`, with cards inside a nested `row row-cols-1 row-cols-md-2`.
- Sidebar: `col-12 col-lg-4`, with personal info and contact details. On screens below 992px it moves under the projects.
- Footer: full width at the bottom of the page.
- Custom media queries (desktop-first) change font sizes, section padding, card image height, and visibility. The tagline and the skills line are hidden on mobile. The sidebar is sticky on desktop only.

Desktop:

![Task 4 desktop](screenshots/task4-desktop.png)

Tablet:

![Task 4 tablet](screenshots/task4-tablet.png)

Mobile:

![Task 4 mobile](screenshots/task4-mobile.png)

Mobile (navbar opened):

![Task 4 mobile menu](screenshots/task4-mobile-menu.png)

---

## Summary of Work Process

I completed the assignment in three parts. In Part 1 I wrote the layout and typography with plain CSS and media queries only. I wrote the default styles for desktop and used `max-width` queries to override them for tablet and mobile. The main thing I learned there is that the order of the queries matters: the mobile query has to come after the tablet query, otherwise the tablet values win on small screens. Calculating the box widths with `calc()` and the gap size also took some attempts.

Bootstrap was the hardest part of this assignment for me. At first I did not understand how a few class names could replace so much CSS. It was difficult to understand how the 12-column grid works, how `col-12 col-md-6 col-lg-4` combine at different screen sizes, and why the grid is mobile-first while my own CSS was desktop-first. The navbar was also confusing because the hamburger menu only works when the Bootstrap JavaScript file is connected and the `data-bs-target` matches the `id` of the menu. I understood it better after opening DevTools and looking at the media queries inside Bootstrap's own CSS, and after realizing that the grid is just flexbox plus media queries, which I had already written myself in Part 1. Rows, columns and containers must also be nested correctly, otherwise the layout breaks.

In Part 3 I combined both approaches. Bootstrap handles the structure (navbar, grid, cards) and my own media queries handle the fine details (font sizes, spacing, hidden elements). I also had a problem with the CSS file not loading because of a wrong path in the `link` tag, which I fixed by using the correct relative path. I tested every page in Chrome DevTools at about 375px, 768px and 1200px and took the screenshots from there.
