# Veyra — Weekend Experience Discovery & Booking

![Veyra](https://img.shields.io/badge/Veyra-Weekend%20Experiences-8B5CF6?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML5-Static-E34F26?logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-Responsive-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?logo=javascript&logoColor=111)

**Veyra** is a modern, premium website concept for discovering and booking memorable weekend experiences around Pune, Maharashtra. It is designed for students and young professionals who want to spend less time planning and more time exploring.

The website combines a cinematic travel aesthetic with a fully responsive interface, interactive experience discovery, a simulated multi-step booking flow, authentication forms, an image gallery, testimonials, FAQs, and light/dark themes.

> **Tagline:** Your next story starts here.

## Live Demo

After GitHub Pages is enabled, the site will be available at:

**https://suyashpandey8088-cell.github.io/veyra-website/**

## Preview

The home page opens with the headline **“Make Your Weekend Unforgettable.”** and introduces visitors to curated trekking, camping, creative, cycling, and photography experiences.

The visual direction uses:

- Deep navy backgrounds
- Electric-purple accents
- Subtle gradients and atmospheric glows
- Large editorial typography
- Cinematic travel and lifestyle photography
- Smooth hover, entrance, and parallax effects

## Features

### Experience discovery

- Six sample experiences across multiple categories
- Search by title, description, or location
- Filter by experience type or “vibe”
- Date selection from the main search panel
- Responsive animated experience cards
- Ratings, pricing, location, difficulty, and category information
- Favourite/save buttons with visual feedback

Included sample experiences:

- Sunrise Trek to Kalsubai
- Clay & Chai: Pottery Social
- Midnight City Cycling
- Lakeside Camping Escape
- Street Photography Walk
- Secret Sahyadri Trail

### Four-step booking flow

The booking interface simulates the complete customer journey:

1. Select an experience
2. Choose a date and number of guests
3. Enter contact details
4. Review and confirm the booking

The flow includes basic client-side validation, dynamic totals, step indicators, and confirmation feedback.

> The current booking flow is a front-end demonstration. It does not process real payments, reserve inventory, or send confirmation emails.

### User interface and interactions

- Sticky, translucent navigation bar
- Responsive mobile navigation menu
- Parallax hero background
- Scroll-triggered entrance animations
- Smooth anchor scrolling
- Experience-card hover effects
- Testimonials carousel with navigation and indicators
- Expandable FAQ accordion
- Full-screen image gallery lightbox
- Newsletter signup confirmation
- Login and signup modal
- Dark and light appearance modes
- Toast notifications for user actions

### Responsive design

The layout adapts to desktop, tablet, and mobile screen sizes. Major grids, navigation controls, search filters, forms, galleries, and typography are reorganized for smaller devices.

## Technology

The project intentionally uses a lightweight, dependency-free front-end stack:

- **HTML5** for semantic page structure
- **CSS3** for layout, responsive design, themes, gradients, and animation
- **Vanilla JavaScript** for filtering, modals, booking state, gallery behavior, testimonials, validation, and theme switching
- **Google Fonts** for DM Sans and Manrope when network access is available

There is no framework, package manager, build process, or server-side dependency. The website can be hosted on any static hosting provider.

## Project Structure

```text
veyra-website/
├── assets/
│   ├── cinematic-western-ghats-trekking-young-p-1.jpg
│   ├── cinematic-western-ghats-trekking-young-p-2.jpg
│   ├── cinematic-western-ghats-trekking-young-p-3.jpg
│   ├── night-cycling-city-young-people-india-ci-1.jpg
│   ├── night-cycling-city-young-people-india-ci-2.jpg
│   ├── pune-pottery-workshop-young-adults-moder-1.jpg
│   └── pune-pottery-workshop-young-adults-moder-2.jpg
├── .gitignore
├── index.html
├── styles.css
├── script.js
└── README.md
```

### Main files

- **`index.html`** — Contains the complete page structure, navigation, sections, forms, modals, gallery, footer, and metadata.
- **`styles.css`** — Defines the visual system, themes, responsive layouts, animations, cards, booking interface, and component styles.
- **`script.js`** — Contains sample experience data and all client-side interactions.
- **`assets/`** — Stores local images used throughout the website.

## Run Locally

No installation or build step is required.

### Option 1: Open the file directly

Clone the repository and open `index.html` in a browser:

```bash
git clone git@github.com:suyashpandey8088-cell/veyra-website.git
cd veyra-website
```

Then open `index.html`.

### Option 2: Start a local web server

Using Python:

```bash
python3 -m http.server 4173
```

Open:

```text
http://localhost:4173
```

Using Node.js:

```bash
npx serve .
```

## Deploy to GitHub Pages

1. Open the GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select the `main` branch.
5. Select `/ (root)` as the publishing folder.
6. Click **Save**.

GitHub will build and publish the static website. Initial deployment may take a few minutes.

## Customization

### Edit experiences

Experience data is stored in the `experiences` array near the top of `script.js`:

```javascript
{
  id: 1,
  title: "Sunrise Trek to Kalsubai",
  cat: "Adventure",
  tag: "BESTSELLER",
  place: "Kalsubai · 2h 45m away",
  desc: "Chase dawn above the clouds at Maharashtra’s highest peak.",
  price: 1499,
  rating: "4.9",
  img: "assets/cinematic-western-ghats-trekking-young-p-2.jpg",
  level: "Moderate"
}
```

Add, remove, or modify objects in this array to update the available experiences. Category names should correspond to the filter buttons in `index.html`.

### Change colors

The main design tokens are CSS custom properties at the beginning of `styles.css`:

```css
:root {
  --bg: #070815;
  --card: #101326;
  --text: #f7f5ff;
  --muted: #a8a8bb;
  --purple: #8b5cf6;
  --accent: #d0ff6a;
}
```

Light-theme values are defined under:

```css
html[data-theme="light"]
```

### Replace images

Place new image files inside `assets/` and update their paths in:

- The hero background declaration in `styles.css`
- The experience data in `script.js`
- The gallery markup in `index.html`

For best results, use compressed WebP or optimized JPEG images with consistent aspect ratios.

### Update business details

Contact information, location, social links, and footer content can be edited in `index.html`. Current demonstration details are:

- **Email:** hello@veyra.example
- **Phone:** +91 98765 43210
- **Location:** Pune, Maharashtra

The `.example` email domain is intentionally non-operational and should be replaced before launch.

## Production Integration

This repository is currently a static front-end prototype. A production booking platform would typically require:

- A backend application and database
- User account creation and secure authentication
- Real-time experience inventory and availability
- Booking persistence and management
- Payment processing through a provider such as Razorpay or Stripe
- Transactional email or SMS notifications
- Secure server-side form validation
- Contact and newsletter integrations
- Admin tools for managing experiences and bookings
- Privacy policy, terms, cancellation policy, and consent management
- Monitoring, analytics, backups, and error reporting

Never place payment secrets, API keys, database credentials, or private tokens in front-end JavaScript or commit them to the repository.

## Accessibility

The site includes semantic sections, labelled controls, alternative image text, keyboard-accessible native elements, visible interactive states, and Escape-key support for modal/lightbox dismissal.

Before a production release, consider completing a formal accessibility review covering:

- Focus trapping and focus restoration in modal dialogs
- Full keyboard testing
- Screen-reader announcements for dynamic content
- Color contrast verification in both themes
- Reduced-motion support
- Form error associations and instructions
- Automated and manual WCAG 2.2 testing

## Performance Recommendations

For production deployment:

- Convert large images to AVIF or WebP
- Provide responsive `srcset` image variants
- Add explicit image width and height attributes
- Lazy-load below-the-fold gallery images
- Minify CSS and JavaScript
- Self-host or optimize font delivery
- Add caching and security headers through the hosting platform
- Test with Lighthouse and real mobile devices

## Browser Support

The website is intended for current versions of:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Apple Safari
- Modern mobile browsers

Some visual effects rely on modern CSS capabilities such as `backdrop-filter`, `color-mix()`, CSS custom properties, and Intersection Observer. Older browsers may display simplified effects.

## Image and Content Notice

This project is a demonstration concept. Included images and sample content should be reviewed for appropriate commercial usage rights before any public or commercial launch. Replace demonstration imagery with original photography or properly licensed assets where required.

All prices, ratings, availability, testimonials, contact details, and booking confirmations are sample data and do not represent real services.

## Future Enhancements

Potential next steps include:

- Persistent user accounts and saved favourites
- Real booking and payment integration
- Location-based recommendations
- Interactive maps
- Host profiles and verified reviews
- Coupon and referral support
- Group booking tools
- Admin dashboard
- Progressive Web App support
- Multilingual content
- Automated email and WhatsApp notifications

## License

No open-source license has been added yet. Unless a license is provided, the repository’s contents remain under the copyright of the repository owner, and standard copyright rules apply.

---

Built as a premium front-end concept for **Veyra** — *Your next story starts here.*
