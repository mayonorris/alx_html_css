# Headphones — Pixel-Perfect Landing Page (HTML & CSS)

Implement a responsive, accessible landing page **from a Figma design**, using **only HTML & CSS** (no frameworks, no JS—until Task 8). The goal is to reproduce the designer’s intent with clean, reusable styles and solid responsive behavior.

---

## 🎯 Objectives

- Rebuild the provided Figma layout faithfully (desktop & ≤480px mobile).
- Apply semantic HTML, modern CSS, and accessibility best practices.
- Use a small, reusable design system (variables, utilities, components).
- Keep code validator-friendly and easy to iterate on.

---

## 🧭 Design Source

- Duplicate the Figma file to your Drafts to inspect sizes, spacing, colors, fonts.
- If missing locally, install the fonts:
  - **Source Sans Pro**
  - **Spin-Cycle-OT**
- Some values in Figma are fractional—round sensibly.

> **Interaction notes (must-haves):**
> - Mobile layout at **≤480px** viewport width  
> - **Links** `:hover/:active` color: `#FF6565`  
> - **Buttons** `:hover/:active` change **opacity: 0.9**  
> - Content **max-width: 1000px**, centered

---

## 📁 Project Structure

```text
alx_html_css/
└─ headphones/
├─ README.md
├─ 0-index.html 0-styles.css # Header/Hero
├─ 1-index.html 1-styles.css # + “What we do…”
├─ 2-index.html 2-styles.css # + “Our results”
├─ 3-index.html 3-styles.css # + Contact us
├─ 4-index.html 4-styles.css # + Footer (static final)
├─ 6-index.html 6-styles.css # CSS-only pentagons
├─ 7-index.html 7-styles.css # Animations
├─ 8-index.html 8-styles.css 8-script.js # Hamburger (≤480px)
├─ assets/ # images_, icons (holberton_school-icon), svgs
└─ fonts/ # (optional) local font files
```


---

## 🧩 Sections to Implement

1. **Header / Hero** (Task 0)  
   - Logo + navigation (desktop), hero copy, CTA button, background image with overlay.

2. **“What we do…”** (Task 2)  
   - Four feature cards (icon + heading + text). Use the provided **icon font**.

3. **“Our results”** (Task 3)  
   - Dark panel with four stat pentagons (initially image-based).

4. **Contact us** (Task 4)  
   - Accessible form: name, email, message, submit button.

5. **Footer** (Task 5)  
   - Logo, small navigation/socials, legal line.

6. **CSS-only pentagons** (Task 6)  
   - Replace stat images with **pure CSS** (e.g., `clip-path: polygon(...)`).

7. **Animations** (Task 7)  
   - Tasteful hover/entrance effects; respect `prefers-reduced-motion`.

8. **Hamburger menu** (Task 8)  
   - At ≤480px, swap nav for a hamburger that toggles the menu (JS allowed here).

---

## 🧱 CSS Foundations

- **Reset / Base**
  ```css
  * , *::before, *::after { box-sizing: border-box; }
  html, body { margin: 0; }
:root {
  --maxw: 1000px;
  --brand: #FF6565;
  --text: #161616;
  --muted: #8f8f8f;
  --bg-dark: #0c1b2a; /* adjust per Figma */
  --radius-pill: 28px;
  --space: 16px;
}
.container { max-width: var(--maxw); margin-inline: auto; padding-inline: var(--space); }
.section { padding-block: 64px; }
@media (max-width: 480px) { .section { padding-block: 40px; } }

a:hover, a:active { color: var(--brand); }
.btn:hover, .btn:active { opacity: .9; }

## Attribution

Design by Nicolas Philippot (UI/UX).
Built for the ALX Front-End curriculum.