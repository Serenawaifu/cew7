DGrealtor Portfolio Website

A high-performance, single-page real estate portfolio website built with Next.js, Tailwind CSS, and a Google Form backend.

🚀 Features

Responsive Design: Optimized for all devices from Mobile (240p) to 4K Desktop.

Hero Slideshow: 15-second auto-transitioning background images of premium commercial properties.

Custom Contact Form: Integrated with Google Forms for backend data collection, featuring strict validation (Gmail/Yahoo/Indian Phone) and a custom glass-morphism UI.

Infinite Scroll: Smooth marquee animations for client logos and awards.

Fluid Typography: Uses clamp() functions to ensure text scales perfectly across all screen sizes.

📂 Project Structure

/
├── app/
│   ├── layout.js       # Main layout and font configuration
│   └── page.js         # Core logic: Slideshow, Contact Form, All Sections
├── components/
│   └── ContactModal.js # (Logic merged into page.js for optimization)
├── public/
│   └── logos/          # Place your images here
│       ├── header-footer/
│       └── companies/
├── styles/
│   └── globals.css     # Global styles, animations, and Tailwind imports
└── README.md


🛠️ Setup Guide

1. Install Dependencies

Ensure you have Node.js installed, then run:

npm install
# or
yarn install


2. Configure Google Form

To make the contact form work, you need to connect it to your Google Form.

Create a Google Form with fields: Full Name, Contact Info, Subject, Message.

Click the three dots (top right) -> Get pre-filled link.

Fill in dummy data and click Get Link.

Copy the link and inspect the entry IDs (e.g., entry.123456789).

Open app/page.js and replace the placeholders:

action="...": Replace with your form's response URL (ending in /formResponse).

name="entry.XXXX": Replace with your specific entry IDs.

3. Add Custom Images

Logos: Place your logo files in public/logos/.

Hero Images: Update the backgroundImages array in app/page.js with paths to your local images or external URLs.

4. Run Development Server

npm run dev


Open http://localhost:3000 to view it in the browser.

🎨 Customization

Colors: Modify tailwind.config.js or app/layout.js variables.

Fonts: The project uses Montserrat and Playfair Display. You can change these in app/layout.js.
