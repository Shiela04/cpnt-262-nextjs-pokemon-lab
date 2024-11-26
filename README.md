# This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.js`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

## Bugs identified and fixed

### Debugging the Navigation in layout.js

- Issue:
  Navigation links are missing the href attribute.
- Solution:
  href attribute was added to Home and About Links with the proper paths

### Fixing Data Fetching in page.js

1. Incorrect API URL

- Solution:
  changed the API URL to the correct URL

2. Incorrect dependecy in useEffect that causes an infinite loop

- Solution:
  removed pokemonList from the dependency array

3. No error handling

- Solution:
  added error handling with a try-catch block

### Debugging Dynamic Routes in page.js

- Issue:
  Clicking a Pokemon link routes incorrectly.
- Solution:
  changed the href to {`/pokemon/${index + 1}`} to use Next.js dynamic routing syntax

### Improving about/page.js

- Issue:
  The About page lacks a way to navigate back to the Home page.
- Solution:
  Added a link using the Next.js Link component

### Fixing Pokemon Details Page in [id]/page.js

1. Pokemon link was broken

- Solution:
  Used Template Literals to update the broken pokemon link and connect the id to the state value of id

2. Missing error handling for invalid Pokemon IDs

- Solution:
  added error handling with a try-catch block

3. Incorrect property for Pokemon images

- Solution:
  changed the property to the correct one in the image source

## What I Learned

I learned how to properly add navigation links and add correct href attribute. I'm more confident now with error handling with a try-catch block.
