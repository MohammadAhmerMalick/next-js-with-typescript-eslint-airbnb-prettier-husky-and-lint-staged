This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) and on top of that it includes [configurations](https://gist.github.com/MohammadAhmerMalick/8475a869766d038e6923dabb8ba86847) for ESLint, Airbnb, Prettier, Husky and Lint Staged.

## Note

If we want the Eslint to fix the staged files then modify `buildEslintCommand` function in `.lintstagedrc.js` file to:

```js
const buildEslintCommand = (filenames) =>
  `next lint --fix --file ${filenames
    .map((f) => path.relative(process.cwd(), f))
    .join(' --file ')}`
```

## Source

If you prefer to do all the configurations manually then follow [This Tutorial](https://gist.github.com/MohammadAhmerMalick/8475a869766d038e6923dabb8ba86847) where we will create Next.js project with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) and do all the configurations manually on top of that.

## Getting Started

Install the dependencies:

```
npm i
```

then, run the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
