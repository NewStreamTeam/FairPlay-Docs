Here's the content from the `contributors.html` file, converted into Markdown format:

# FairPlay for Developers - Contribution Guide

## Introduction and Project Philosophy

Welcome\! We are delighted by your interest in contributing to our mission to redefine streaming. FairPlay is a 100% free, ad-free platform dedicated to relevant and entertaining content. Our philosophy is rooted in openness, transparency, and community collaboration. By joining our contributors, you're not just coding; you're participating in a movement for a fairer, richer web.

Whether you're an experienced developer, translator, designer, or simply passionate about our cause, your contribution is valuable. Together, we are building a space where quality and ethics come first.

## Development (Setup)

This section is for developers wishing to contribute directly to FairPlay's code. Follow these steps to set up your environment and understand our processes.

### Development Environment

To get started, make sure you have the following prerequisites installed:

  * Node.js (LTS version recommended)
  * npm or yarn
  * Git

Clone our main GitHub repository:

```bash
git clone https://github.com/NewStreamTeam/NewStream-Website.git
cd NewStream-Website
```

Install Next.js project dependencies:

```bash
npm install
# or
yarn install
```

Configure your environment variables by creating a `.env.local` file at the root of the project. You will need your Supabase keys (available on your Supabase dashboard):

```
NEXT_PUBLIC_SUPABASE_URL=YOUR_SUPABASE_URL
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_SUPABASE_ANON_KEY
```

To run the project locally, execute:

```bash
npm run dev
# or
yarn dev
```

The application will be accessible at `http://localhost:3000`.

### Code Structure

The FairPlay project is a **Next.js** application in **TypeScript**, using **Supabase** for the database and **Tailwind CSS** for styling. Here is the file and folder organization:

```
/   # Project Root
├── README.md
├── package.json            # Dependencies and NPM scripts
├── next.config.ts          # Next.js configuration
├── tailwind.config.js      # Tailwind CSS customization
├── tsconfig.json           # TypeScript options
├── public/                 # Static files (icons, images…)
├── lib/
│   └── supabase.ts         # Supabase client initialization (server-side)
└── src/
    ├── app/                # Next.js “app” folder
    │   ├── globals.css     # Global styles
    │   ├── layout.tsx      # Root layout
    │   └── page.tsx        # Homepage
    ├── components/         # Reusable React components
    │   ├── Layout.tsx
    │   ├── UploadModal.tsx
    │   ├── UserMenu.tsx
    │   └── icons.tsx
    ├── lib/                # Application-side utilities
    │   ├── supabase.ts     # Supabase client for the frontend
    │   ├── publicApi.ts    # API key verification and rate-limiting
    │   ├── recommend.ts    # Video recommendation logic
    │   └── utils.ts        # Helper functions
    ├── pages/              # File-based routes
    │   ├── api/            # Internal and public endpoints
    │   │   ├── index.ts
    │   │   ├── login.ts
    │   │   ├── register.ts
    │   │   ├── videos.ts
    │   │   ├── videos/[id].ts
    │   │   └── v1/         # Public API (/api/v1)
    │   │       ├── index.ts
    │   │       ├── login.ts
    │   │       ├── register.ts
    │   │       ├── videos.ts
    │   │       └── videos/[id].ts
    │   ├── login.tsx       # Authentication form
    │   ├── upload.tsx      # Video upload
    │   ├── videos.tsx      # Video list
    │   └── video/[id].tsx  # Video details
    └── types.ts            # Shared TypeScript types

```

### Contribution Process (Git Workflow)

We use a workflow based on feature branches and Pull Requests (PRs):

1.  **Fork** the FairPlay repository on GitHub.
2.  **Clone** your fork locally.
3.  Create a new **feature branch** from `main`: `git checkout -b feature/your-feature` or `bugfix/bug-fix`.
4.  **Commit** your changes atomically and with clear messages.
5.  **Push** your branch to your fork: `git push origin feature/your-feature`.
6.  Open a **Pull Request (PR)** on the main FairPlay repository. Describe the changes precisely, solved issues, and include screenshots if relevant.
7.  Respond to comments during the **code review** and make necessary modifications.

### Tests

Each new feature or bug fix must be accompanied by relevant tests. We use **Jest** and **React Testing Library** for unit and integration testing of components and functions. To run the tests:

```bash
npm test
# or
yarn test
```

Good code coverage is essential for FairPlay's stability. Make sure all tests pass before submitting a PR.

### API

You can use our API for free.

To access the API, you can use the following endpoints:

  * `/api/v1/videos` To access every single video in the database, including: Title, link, description, notation...
  * `/api/v1/videos/{id}` To access a specific video by its ID, including: Title, link, description, notation...
  * `/api/v1/login` To log in to your account, you need to provide your email and password.
  * `/api/v1/register` To register a new account, you need to provide your email, password, and pseudo.

More endpoints are going to be added and improved soon.

## Contributions (Non-Developers)

Not a coder? No problem\! There are many ways to contribute to FairPlay's success.

### Translation

Help us make FairPlay accessible worldwide. We manage text localization via JSON files. If you wish to translate FairPlay into a new language or improve an existing translation, please contact us on Discord for instructions and files to translate.

### Writing and Documentation

Good documentation is key to a successful Open Source project. Whether it's to improve our existing guides, create new tutorials, write blog posts, or enrich our technical wiki, your writing talent is welcome. All documentation files are in Markdown and are versioned in the `/docs` folder of our main repository.

### Design (UI/UX)

User experience is paramount. If you have UI/UX design skills, feel free to propose mockups (e.g., on Figma), provide feedback on ergonomics, or suggest visual improvements. We are open to new ideas to make FairPlay even more intuitive and pleasant, while respecting our design principles based on Tailwind CSS.

### Moderation

To maintain a healthy and respectful environment, we rely on volunteer moderators. Their role is to ensure that interactions remain constructive and that content respects our guidelines (no misinformation, politics, or religion). A detailed moderation guide is available for members of our moderation community.

### Testing and Bug Reports

Even before writing a line of code, testing the application is an invaluable contribution. If you find a bug, please report it via our [GitHub issue tracker](https://www.google.com/search?q=https://github.com/NewStreamTeam/NewStream-Website/issues) by following the provided template. Provide as many details as possible (reproduction steps, environment, screenshots) to help us reproduce and fix it.

### Promotion and Communication

Spread the word about FairPlay\! Share our project on social media, tell your friends, or write an article. Any form of promotion helps FairPlay reach a wider audience and find new contributors. Don't hesitate to contact us if you have ideas for partnerships or events.

## Code of Conduct

FairPlay is committed to providing a welcoming and inclusive environment for everyone, regardless of experience, gender, sexual orientation, disability, personal appearance, race, ethnicity, religion, or nationality.

We expect all contributors to show respect, courtesy, and open-mindedness. Harassing, discriminatory, or disrespectful behavior will not be tolerated. Discussions on political and religious topics, as well as the spread of misinformation, are strictly prohibited to maintain an environment focused on relevant and entertaining content.

If you observe inappropriate behavior, please report it immediately to [contact.newstreamteam@gmail.com](mailto:contact.newstreamteam@gmail.com).

## Useful Resources

Here are some essential links to help you on your contribution journey:

  * [Official GitHub Repositories](https://github.com/NewStreamTeam/NewStream-Website/)
  * API Documentation (Coming Soon)
  * [Join our Community Discord server](https://discord.gg/AZBwM6u9Kr)
  * FAQ for Contributors

## Project License

FairPlay is an Open Source project distributed under the [MIT License](https://opensource.org/licenses/MIT). This means that the code is free to be used, modified, and distributed, under certain conditions. By contributing to FairPlay, you agree that your contributions are also subject to this license.

Please refer to the `LICENSE.md` file in the main repository for full details.
