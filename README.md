# Next.js Portfolio Website

A modern, responsive portfolio website built with Next.js, React, and MDX. Showcase your projects, work experience, and skills with a clean, customizable interface.

## Technologies Used

- [Next.js 15](https://nextjs.org/) - React framework with App Router
- [React 19](https://react.dev/) - UI library
- [MDX](https://mdxjs.com/) - Markdown for content with JSX components
- [TailwindCSS](https://tailwindcss.com/) - Utility-first CSS framework
- [Framer Motion](https://www.framer.com/motion/) - Animation library
- [Tech Stack Icons](https://www.npmjs.com/package/tech-stack-icons) - Technology icons
- [Rehype Highlight](https://github.com/rehypejs/rehype-highlight) - Syntax highlighting

## Features

- **Projects Showcase** - Display your projects with detailed MDX content
- **Work History** - Share your professional experience
- **Responsive Design** - Looks great on all devices
- **Dark/Light Mode** - Automatic theme switching
- **MDX Support** - Write content in Markdown with React components
- **SEO Optimized** - Built-in SEO best practices

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/nextjs-portfolio-website.git
   cd nextjs-portfolio-website
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the development server:
   ```bash
   npm run dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Usage

### Adding Projects

1. Create a new MDX file in `src/data/projects/` with the following format:
   ```mdx
   ---
   title: "Project Name"
   teamSize: 4
   role: "Your Role"
   description: "Brief description of the project"
   duration: "MM/YYYY–MM/YYYY"
   techStack:
     - Technology1
     - Technology2
   githubUrl: "https://github.com/your-project"
   ---

   # Introduction

   Project content in Markdown format...
   ```

2. Add the project to `src/data/projects.ts`:
   ```typescript
   {
     slug: 'project-slug',
     title: 'Project Name',
     image: '/projects/image.jpg',
     description: 'Brief description',
     startDate: 'YYYY-MM',
     endDate: 'YYYY-MM',
     techStack: ['Tech1', 'Tech2'],
   }
   ```

### Adding Work Experience

Create a new MDX file in `src/data/work/` with your work experience details.

## Project Structure

```
nextjs-portfolio-website/
├── public/              # Static assets
├── src/
│   ├── app/             # Next.js App Router
│   │   ├── projects/    # Projects pages
│   │   ├── work/        # Work experience pages
│   │   └── page.tsx     # Home page
│   ├── components/      # React components
│   ├── data/            # Content data
│   │   ├── projects/    # Project MDX files
│   │   └── work/        # Work experience MDX files
│   └── lib/             # Utility functions
├── next.config.ts       # Next.js configuration
└── package.json         # Project dependencies
```

## Deployment

This project can be deployed to any platform that supports Next.js applications:

### Vercel (Recommended)

```bash
npm install -g vercel
vercel
```

### Static Export

```bash
npm run build
```

The static site will be generated in the `dist` directory as configured in `next.config.mjs`.

## License

MIT License
