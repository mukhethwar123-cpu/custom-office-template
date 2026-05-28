# Urban Threads Boutique (Custom Office Templates)

## Project overview
Urban Threads Boutique is a static, multi-page web presence built with **HTML/CSS**. It includes navigation across core pages (Home, About, Services, Contact, Products) and a **Products → Enquiry** flow where visitors can select a design and jump directly to an enquiry section.

Static website (HTML/CSS) for Urban Threads Boutique with multi-page navigation and a Products -> Enquiry interaction.


---

## File structure

```text
Custom Office Templates/
├─ index.html
├─ pages/
│  ├─ About.html
│  ├─ Contact.html
│  ├─ Services.html
│  ├─ product.html
│  └─ mobilisation.html
├─ CSS/
│  └─ style.css
├─ assests/
│  ├─ background.jpg
│  ├─ backgroung pic 3.jpg
│  ├─ backgroung pic.avif
│  ├─ design 1.jpg
│  ├─ design 2.jpg
│  ├─ design 3.jpg
│  ├─ design 4.jpg
│  ├─ design 5.jpg
│  ├─ design 6.jpg
│  ├─ Manager.jpg
│  ├─ Sale Assistence.jpg
│  ├─ Stylist.jpg
│  ├─ urban threads logo.jpeg
│  ├─ Laptop 1440px screenshoot.png
│  ├─ Tablet 768px Screenshot.png
│  └─ Mobile 375px screenshot.png
└─ README.md
```

## Pages included


### `index.html` (Home)
- Top navigation (Home, About, Services, Contact, Products, Mobilisation)

- Hero/intro content and featured collection section
- Footer with social links

### `pages/About.html` (About)
- Navigation + About content
- Mission/Vision/Values/History style sections
- Team section with images
- Footer with social links

### `pages/Services.html` (Services)
- Navigation + list of services
- Service image highlights
- Footer with address/contact info and social links

### `pages/Contact.html` (Contact)
- Navigation + contact info (cell/address/email)
- Embedded Google Map (iframe)
- Contact form + success modal placeholder
- Footer with social links

### `pages/product.html` (Products)
- Navigation + a products/design catalog (Design 1..Design 6)
- Each design has a **Choose Design X** button
- A **Product of Interest** dropdown
- **Product Enquiry** form section
- Smooth “jump to enquiry” experience when selecting products



- **Product Enquiry** form section
- Smooth “jump to enquiry” experience when selecting products

---

## Assets
- Images are stored in `assests/` (logo, backgrounds, and design images).
- Global background image is configured in `CSS/style.css`.

---

## Styling

### Global stylesheet: `CSS/style.css`
Defines:
- Theme variables (`--primary`, `--primary2`, etc.)
- Background gradients and the fixed hero background (`.page-bg`)
- Shared navigation styling (pill buttons)
- Product grid styling (`ul.products-list`)
- Form/button styling
- Social links styling

---

## Product navigation update (implemented)

### Goal
Allow visitors to navigate through products and instantly move to the enquiry form, while keeping product details hidden until a product is selected.

### Changes in `pages/product.html`
1. **Clickable product selection**
   - Each **Choose Design X** button has `class="choose-btn"` and `data-design="Design X"`.

2. **Dropdown + reveal logic**
   - When a user clicks **Choose Design X**:
     - The enquiry dropdown (`#enquiry-product`) is set to the chosen design.
     - All design info blocks (`.design-info`) are hidden.
     - Only the selected design’s info block is shown.
     - The page scrolls smoothly to `#enquiry-section`.

3. **Hide product information on initial load**
   - Added an extra `hideAllInfos()` call to force all `.design-info` blocks to remain hidden until the user clicks a **Choose Design** button.

4. **Jump link**
   - Added a **Jump to enquiry** link that anchors to `#enquiry-section`.

### Dropdown mapping
- Dropdown options were adjusted so their `value` matches `Design 1..Design 6`.
- Example: choosing `data-design="Design 2"` sets `#enquiry-product` to the option with `value="Design 2"`.

---

## CSS updates for the product page

### Changes in `CSS/style.css`
- Smooth scrolling enabled:
  - `html { scroll-behavior: smooth; }`
- Added styling for the jump link:
  - `.jump-to-enquiry` and hover effect.

---

## Files modified (this update)
- `pages/product.html`
- `CSS/style.css`
- `README.md` (documenting the website + the update)

---

## Change log

- **2026-05-27**: Added mobilisation screenshots (Laptop/Tablet/Mobile) from `assests/`.
  - Screenshots used:
    - `assests/Laptop 1440px screenshoot.png`
    - `assests/Tablet 768px Screenshot.png`
    - `assests/Mobile 375px screenshot.png`
  - Updated navigation (where applicable).
  - Updated this `README.md` with file structure + documentation.


## How to test (quick checklist)
1. Open `pages/product.html` in a browser.

2. Verify that **all design information is hidden** initially.
3. Click **Choose Design 1** (then try other designs).
4. Confirm:
   - dropdown selection updates
   - only the selected design info becomes visible
   - the page smooth-scrolls to **Product Enquiry**
5. Use **Jump to enquiry** link to verify anchor scrolling.
## Screenshots
Here are sample screen displays of the website across different devices:


- **Laptop (1024px)**:  
  ![Laptop View](assests/Laptop%201440px%20screenshoot.png)

- **Tablet (768px)**:  
  ![Tablet View](assests/Tablet%20768px%20Screenshot.png)

- **Mobile (320px)**:  
  ![Mobile View](assests/Mobile%20375px%20screenshot.png)

