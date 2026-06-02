A futuristic, high-fidelity Student Dashboard built with Next.js, Supabase, Tailwind CSS, and Framer Motion.
This project demonstrates new-edge design principles: hardware-accelerated animations, zero layout shifts, and buttery-smooth user experiences powered by server-rendered data.

✨ Features
Dark Mode Only: Deep backgrounds (near-black, dark gray) with glowing gradient accents.

Bento Grid Layout:

Sidebar (Left): Slim, collapsible navigation.

Main Content (Right): Dynamic grid with:

Hero Tile: Greeting (Welcome back, [Name]) + daily learning streak.

Course Tiles: Fetched dynamically from Supabase.

Activity Tile: Contribution graph / activity chart.

Animations & Interactions (Framer Motion):

Staggered page load (tiles fade in sequentially, translate upward).

Card hover states (scale up ~1–2%, border glow/gradient shift).

Sidebar micro-interactions (background highlight snaps via layoutId).

Course Card Specs:

Icon (from icon_name in Supabase).

Title (course name).

Animated progress bar (0% → progress value on load).

Subtle gradient mesh / grain texture background.

Responsive Design:

Desktop (>1024px): Full Bento grid + sidebar visible.

Tablet (768px–1024px): Sidebar collapses to icons, grid → 2 columns.

Mobile (<768px): Sidebar becomes bottom nav/hamburger, grid stacks vertically.

🛠 Tech Stack
Framework: Next.js (App Router required)

Database/BaaS: Supabase (PostgreSQL)

Styling: Tailwind CSS

Animations: Framer Motion

Icons: Lucide React / Radix Icons

Strict Constraints:

No “div soup” → use semantic HTML (<nav>, <main>, <article>, <section>).

Zero layout shifts → use transform + opacity only for animations.

Modular components → reusable, maintainable architecture.

📦 Data Integration
Supabase table schema:

id (uuid, primary key)  
title (text)  
progress (integer)  
icon_name (text)  
created_at (timestamp)


Fetch data via Next.js Server Components (RSC) using @supabase/ssr or @supabase/supabase-js.

Loading states → loading.tsx or <Suspense> with pulsing skeleton loaders.

Graceful error handling for DB connection failures.

⚙️ Environment Variables
Create a .env.example file in the root of the project:

bash
NEXT_PUBLIC_SUPABASE_URL=your-supabase-url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-supabase-anon-key
⚠️ Important:

Do NOT commit your actual .env file.

Only commit .env.example to document required variables.

🚀 Getting Started
Clone the repo:

bash
git clone https://github.com/yash30150-pra/TASK.git

Install dependencies:

bash
npm install
Set up environment variables:

Copy .env.example → .env

Add your Supabase project credentials.

Run the dev server:

bash
npm run dev
Open http://localhost:3000 (localhost in Bing) in your browser.

📱 Responsive Breakpoints
Desktop: Full grid + sidebar.

Tablet: Sidebar → icons only, grid → 2 columns.

Mobile: Sidebar → bottom nav/hamburger, grid → vertical stack.

🎨 Design Philosophy
This dashboard is not just about visuals — it’s about feel:

Hardware-accelerated animations.

Zero layout shifts.

Smooth, physics-based micro-interactions.

A futuristic, immersive learning experience.
