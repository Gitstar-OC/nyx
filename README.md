# NYX

Writing MDX inside a Nextjs app is easy. Learn how to do that! 

"NYX - Next.js MDX Template
Welcome to NYX, a Next.js template repository designed to make it easy to build websites or applications with MDX (Markdown + JSX). This template provides a pre-configured Next.js setup with MDX support, allowing you to create content-rich pages with the power of Markdown and React components. Whether you're building a blog, documentation site, or a personal portfolio, NYX has you covered!
Features

Next.js 14 with App Router
MDX integration for writing Markdown with JSX
Tailwind CSS for styling
Pre-configured ESLint and Prettier for code quality
File-based routing with MDX files
Ready-to-use template for blogs, portfolios, or documentation sites

Prerequisites
Before you begin, ensure you have the following installed:

Node.js (v18 or later)
npm or Yarn
Git

Getting Started
Follow these steps to set up and run the NYX template locally.
1. Clone the Repository
Clone this repository to your local machine:
git clone https://github.com/your-username/nyx.git
cd nyx

2. Install Dependencies
Install the required dependencies using npm or Yarn:
npm install

or
yarn install

3. Run the Development Server
Start the Next.js development server:
npm run dev

or
yarn dev

Open http://localhost:3000 in your browser to see the application.
4. Project Structure
Here's an overview of the project structure:
nyx/
├── pages/
│   ├── _app.js        # Custom App component
│   ├── index.mdx      # Homepage (MDX)
│   └── [...slug].js  # Dynamic route for MDX pages
├── public/           # Static assets
├── styles/           # CSS files (e.g., Tailwind CSS)
├── mdx-components/   # Custom MDX components
├── next.config.js    # Next.js configuration
├── package.json      # Project dependencies
└── README.md         # This file

Writing MDX
MDX allows you to write Markdown with embedded JSX, making it perfect for creating dynamic content. Here's how to write MDX in this template:
1. Create an MDX File
Add a new .mdx file in the pages/ directory or a subdirectory (e.g., pages/blog/my-post.mdx). The file name determines the route. For example:

pages/index.mdx → /
pages/blog/my-post.mdx → /blog/my-post

2. Write MDX Content
Here's an example of an MDX file (pages/index.mdx):
---
title: Welcome to NYX
description: A Next.js MDX template
---

# Welcome to NYX

This is an MDX-powered page! You can write **Markdown** and include React components.

import { Button } from '../mdx-components/Button';

<Button>Click Me!</Button>


Frontmatter: Use YAML frontmatter (e.g., title, description) to add metadata.
Markdown: Write standard Markdown for text content.
JSX: Import and use React components within your MDX.

3. Create Custom Components
Store custom React components in the mdx-components/ directory. For example, create mdx-components/Button.js:
export function Button({ children }) {
  return (
    <button className="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600">
      {children}
    </button>
  );
}

Import and use these components in your MDX files.
4. Styling with Tailwind CSS
This template uses Tailwind CSS for styling. Apply Tailwind classes directly in your MDX or React components. For example:
<div className="text-center p-8 bg-gray-100">
  <h1 className="text-4xl font-bold">Hello, NYX!</h1>
</div>

Configuration
Next.js MDX Setup
The template uses @next/mdx for MDX support. The configuration is already set up in next.config.js:
const withMDX = require('@next/mdx')();

module.exports = withMDX({
  pageExtensions: ['js', 'jsx', 'mdx'],
});

This allows Next.js to recognize .mdx files as pages.
Dynamic Routes
The pages/[...slug].js file handles dynamic routes for MDX files. It uses getStaticPaths and getStaticProps to pre-render MDX pages at build time.
Customizing Layouts
Modify pages/_app.js to add global layouts or providers:
import '../styles/globals.css';

function MyApp({ Component, pageProps }) {
  return <Component {...pageProps} />;
}

export default MyApp;

Building for Production
To build the application for production:
npm run build

Start the production server:
npm run start

Deploying
You can deploy this Next.js application to platforms like Vercel, Netlify, or any Node.js hosting service. For Vercel:

Push your repository to GitHub, GitLab, or Bitbucket.
Import the repository into Vercel.
Deploy with default settings.

Contributing
Contributions are welcome! To contribute:

Fork the repository.
Create a new branch (git checkout -b feature-name).
Make your changes.
Commit and push (git push origin feature-name).
Open a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Learn More

Next.js Documentation
MDX Documentation
Tailwind CSS Documentation

Happy coding with NYX! 🚀
" 
