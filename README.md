# Personal Profile Website (Nuxt.js + Tailwind CSS)

A modern, responsive two-page personal profile website developed for **Jobert Jan** built with **Nuxt 4**, **Vue 3 Composition API**, and **Tailwind CSS**.

---

## 🌟 Overview & Key Features

- **Nuxt 4 Directory Architecture**: Explores and implements standard Nuxt conventions using `app/pages`, `app/components`, `app/layouts`, and `public`.
- **Two Complete Pages**:
  - **Homepage (`app/pages/index.vue`)**: Welcoming hero section, profile picture avatar (`/berto1.jpg`), professional role, short introduction, statistics cards, call-to-actions, and core competencies.
  - **Profile Page (`app/pages/profile.vue`)**: Comprehensive personal details (contact, location, stack), educational background with timeline & course tags, technical skills and interests, and personal hobbies.
- **Seamless Navigation**: Responsive navbar with `<NuxtLink>` route-matching active state indicators, contact quick-link, and smooth mobile menu drawer.
- **Modern Styling**: Utility-first styling with **Tailwind CSS**, gradient highlights, custom badge tags, and clean typography.
- **SEO & Meta**: Customized page titles and metadata via `useHead`.

---

## 📁 Project Folder Structure

```text
nuxt-profile-task/
├── app/
│   ├── assets/
│   │   └── css/
│   │       └── main.css           # Tailwind CSS import & global styles
│   ├── components/
│   │   ├── Navbar.vue             # Header with navigation menu & active indicator
│   │   └── Footer.vue             # Footer with copyright & quick links
│   ├── layouts/
│   │   └── default.vue            # Default layout wrapping Navbar, <slot />, Footer
│   ├── pages/
│   │   ├── index.vue              # Homepage (Intro, avatar, welcome, quick stats)
│   │   └── profile.vue            # Personal Profile (Info, education, skills, hobbies)
│   └── app.vue                    # Root application component mounting layouts & pages
├── public/
│   ├── berto1.jpg                 # Personal profile picture / avatar
│   ├── favicon.ico                # Site favicon
│   └── robots.txt                 # Search engine directives
├── screenshots/
│   ├── homepage.png               # High-res screenshot of Homepage
│   ├── profile.png                # High-res screenshot of Profile Page
│   └── folder_structure.png       # Screenshot of project folder tree
├── nuxt.config.ts                 # Nuxt & Tailwind Vite configuration
├── package.json                   # Project scripts and dependencies
├── tsconfig.json                  # TypeScript compiler settings
└── README.md                      # Documentation
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18.x or later recommended)
- npm or pnpm

### Installation
```bash
# Clone the repository or extract the ZIP file
cd nuxt-profile-task

# Install dependencies
npm install
```

### Development Server
Start the development server with Hot-Module-Replacement (HMR) at `http://localhost:3000`:
```bash
npm run dev
```

### Production Build & Preview
Build the static application:
```bash
# Generate static build
npm run build

# Preview locally
npx serve .output/public
```

---

## 📸 Deliverables

- **Homepage Screenshot**: [`screenshots/homepage.png`](./screenshots/homepage.png)
- **Profile Page Screenshot**: [`screenshots/profile.png`](./screenshots/profile.png)
- **Folder Structure Screenshot**: [`screenshots/folder_structure.png`](./screenshots/folder_structure.png)
- **Source Code Archive**: Included as `nuxt-profile-source-code.zip`

---

## 👤 Author

**Jobert Jan**  
Senior Web Developer  
- Email: [timerinserver@gmail.com](mailto:timerinserver@gmail.com)
