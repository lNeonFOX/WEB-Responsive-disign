# Assignment #3. Responsive Web Design (Media Queries + Bootstrap Grid)

**Name:** Torekhan Taimas
**Group:** IT-2503

## Project Structure

```
WEB assignment 3/
├── part1/
│   ├── part1.html
│   └── style.css
├── part2.html
│
├── part3/
│   ├── portfolio.html
│   └── style.css
├─ index.html
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

<img width="1917" height="355" alt="изображение" src="https://github.com/user-attachments/assets/4eb76bab-c47f-4032-bd38-fe2c69af973a" />


Tablet:

<img width="1051" height="382" alt="изображение" src="https://github.com/user-attachments/assets/85f98fe2-b3cd-4b17-9181-a70c6a8b92e8" />


Mobile:

<img width="1035" height="416" alt="изображение" src="https://github.com/user-attachments/assets/441fcde5-b7ac-439c-91ff-1af006bbe684" />


### Task 1. Responsive Layout with Media Queries

**Task:** Create a webpage with three boxes in a row. On desktop, display all three side by side. On tablet, display two boxes in a row. On mobile, display boxes stacked vertically. Use only CSS media queries (no Bootstrap).

**Result:** The boxes are in a flex container with `flex-wrap: wrap`. Their width changes with the screen size: one third of the row on desktop, one half on tablet, and the full width on mobile.

Desktop (three in a row):

<img width="1917" height="403" alt="изображение" src="https://github.com/user-attachments/assets/2f52b198-5086-479c-af20-0848d2cafa81" />


Tablet (two in a row):

<img width="1063" height="600" alt="изображение" src="https://github.com/user-attachments/assets/e5332ad6-272f-4988-9f05-505730d3e574" />


Mobile (stacked):

<img width="986" height="647" alt="изображение" src="https://github.com/user-attachments/assets/b37dd6b1-993a-4cb2-8940-784bf170e3df" />


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

<img width="1917" height="412" alt="изображение" src="https://github.com/user-attachments/assets/7da3378a-7f10-4ff4-9c94-fcbeebd60869" />


Tablet:

<img width="1087" height="602" alt="изображение" src="https://github.com/user-attachments/assets/a83d0056-2503-4778-b5fa-f28b8c80aa5d" />


Mobile:

<img width="1193" height="806" alt="изображение" src="https://github.com/user-attachments/assets/8effc3d0-0de3-4f18-a92a-309c6e3c3aa9" />


### Task 3. Bootstrap Navigation Bar

**Task:** Create a responsive navigation bar using Bootstrap components. It should include a logo on the left, links on the right, and collapse into a hamburger menu on smaller screens.

**Result:** The navbar uses `navbar-expand-lg`. The logo is `navbar-brand`, the links are in `navbar-nav ms-auto` so they are pushed to the right, and the hamburger button uses `data-bs-toggle="collapse"` to open the menu below 992px.

Desktop (full menu):

<img width="1917" height="142" alt="изображение" src="https://github.com/user-attachments/assets/a74b3682-9849-4f6c-b19c-876c1ffc0b3e" />


Mobile (collapsed, hamburger button):

<img width="515" height="95" alt="изображение" src="https://github.com/user-attachments/assets/f827011a-2a81-4d5b-8887-a5fea8a2936b" />


Mobile (menu opened):

<img width="512" height="286" alt="изображение" src="https://github.com/user-attachments/assets/72612bcc-c176-4a49-a84b-eecf8fc8a28d" />


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

<img width="1917" height="1032" alt="изображение" src="https://github.com/user-attachments/assets/7332505b-1e1e-40cf-8ddd-c4d6b133b760" />


Tablet:

<img width="1041" height="986" alt="изображение" src="https://github.com/user-attachments/assets/afe219b8-b8d9-402d-9648-bb4b23b84e14" />


Mobile:

<img width="513" height="990" alt="изображение" src="https://github.com/user-attachments/assets/c778f862-531c-42e4-a458-2a4812d5ea77" />


Mobile (navbar opened):

<img width="530" height="266" alt="изображение" src="https://github.com/user-attachments/assets/1cc43bdd-d019-4072-bf05-2bedfddf8270" />


---

## Summary of Work Process

I completed the assignment in three parts. In Part 1 I wrote the layout and typography with plain CSS and media queries only. I wrote the default styles for desktop and used `max-width` queries to override them for tablet and mobile. The main thing I learned there is that the order of the queries matters: the mobile query has to come after the tablet query, otherwise the tablet values win on small screens. Calculating the box widths with `calc()` and the gap size also took some attempts.

Bootstrap was the hardest part of this assignment for me. At first I did not understand how a few class names could replace so much CSS. It was difficult to understand how the 12-column grid works, how `col-12 col-md-6 col-lg-4` combine at different screen sizes, and why the grid is mobile-first while my own CSS was desktop-first. The navbar was also confusing because the hamburger menu only works when the Bootstrap JavaScript file is connected and the `data-bs-target` matches the `id` of the menu. I understood it better after opening DevTools and looking at the media queries inside Bootstrap's own CSS, and after realizing that the grid is just flexbox plus media queries, which I had already written myself in Part 1. Rows, columns and containers must also be nested correctly, otherwise the layout breaks.

In Part 3 I combined both approaches. Bootstrap handles the structure (navbar, grid, cards) and my own media queries handle the fine details (font sizes, spacing, hidden elements). I tested every page in Chrome DevTools at about 375px, 768px and 1200px and took the screenshots from there.
