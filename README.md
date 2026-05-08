# 𝕏 Clone (Twitter UI Replica)

![Project Status](https://img.shields.io/badge/Status-Completed-success)
![Tech Stack](https://img.shields.io/badge/Stack-HTML5%20%7C%20Tailwind%20CSS-blue)

A pixel-perfect, fully responsive front-end clone of X (formerly Twitter) built entirely with pure HTML and Tailwind CSS. 

This project was a deep dive into modern CSS layouts, focusing on recreating the complex, multi-column dashboard experience of one of the world's most visited websites while ensuring it gracefully degrades into a seamless mobile experience.

## ✨ Features

- **True-to-Life Dark Mode**: Replicated X's deep black (`#000000`) and dark gray (`bg-gray-800`) color palette.
- **Fluid Responsiveness**:
  - **Desktop (`xl`+)**: Classic 3-column layout (Left Nav, Feed, Right Sidebar).
  - **Tablet (`sm` to `xl`)**: Collapsed icon-only left navigation to save horizontal space.
  - **Mobile (`< sm`)**: Dynamic bottom navigation bar replacing the sidebar, just like the native app.
- **Modern Flexbox Layouts**: Utilized extensive flexbox techniques to handle complex tweet card headers, action bars, and flexible content sizing.
- **Zero JavaScript**: The entire visual structure, including scrollable feeds and sticky sidebars, is handled purely with CSS.

## 🛠️ Tech Stack

- **HTML5**: Semantic markup for accessibility and structure.
- **Tailwind CSS v4**: Utility-first CSS framework used for all styling. Compiled using the new `@tailwindcss/cli`.
- **Custom SVGs**: Integrated raw SVG code for pixel-perfect, scalable iconography matching the real app.

## 💡 What I Learned

Building this wasn't just about copying a design; it was about understanding *why* X is built the way it is. Some of my biggest takeaways:

1. **The Flexbox Wrap Trap**: I initially struggled with text overlapping in tweet headers on small screens. Learning to properly use `min-w-0`, `shrink-0`, and `flex-wrap` was a game-changer for responsive components.
2. **Horizontal Overflow Headaches**: Mobile screens are unforgiving. I learned how rigid fixed paddings (`px-26`) can break a layout, and how to swap them out for fluid constraints (`max-w-full`, `overflow-x-hidden`) to keep the viewport clean.
3. **Mobile-First Thinking**: It's much easier to build the mobile layout first and scale up to the 3-column desktop view than the other way around.

## 🚀 How to Run Locally

If you want to view the project or tinker with the code:

1. Clone this repository.
2. Ensure you have Node.js installed to run the Tailwind compiler.
3. Start the Tailwind CLI watcher:
   ```bash
   npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
   ```
4. Open `basic.html` in your browser (or use a local server like Live Server in VS Code).

## 🔮 Future Improvements

- [ ] Add smooth `transition` classes for hover states to make interactions feel more premium.
- [ ] Refactor the repeated Tweet card HTML into reusable components (maybe migrate to React or Vue).
- [ ] Implement a system font stack for typography that identically matches the native OS feel.

---
*Disclaimer: This is a personal learning project and is not affiliated with X Corp.*
