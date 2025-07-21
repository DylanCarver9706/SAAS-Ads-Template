# Subscription-Based SAAS Application Template

A modern web application built with Next.js that provides PDF utilities with an Ads access model.

## Tech Stack

- **Frontend**: Next.js
- **Analytics**: PostHog

## Getting Started

To use this template for your own project, follow these steps:

1. Click "Use this template" > "Create a new repository" button at the top of this repository to make a new repo with this template
1. Clone the repository to your local machine
1. Create a `.env.local` file in the root directory and add the following environment variables:

   ```
   ## PostHog Analytics
   NEXT_PUBLIC_POSTHOG_KEY=your_posthog_project_api_key
   POSTHOG_HOST=https://us.i.posthog.com

   ## Google Adsense
   NEXT_PUBLIC_GOOGLE_ADSENSE_ID=your_google_adsense_id
   ```

   To get this key:

   - **PostHog**: Visit https://us.posthog.com, go to Settings > Project Details to get the project API key
   - **Google AdSense**: We will get this later once we deploy

1. Install dependencies:

   ```bash
   npm install
   ```

1. Run the development server:

   ```bash
   npm run dev
   ```

1. Clean up and customize the template:

   - Remove PDF components and pages
   - Run `npx depcheck` to check for unused dependencies and remove them from package.json (except @types/node, autoprefixer, and postcss)
   - Delete the `.next` and `node_modules` directories as well as the `package-lock.json`
   - Run `npm install` to fully remove the unused dependencies
   - Update app name in:
     - package.json
     - layout.tsx
     - not-found.tsx
   - Update navbar links
   - Add terms of use/service, privacy policy, and contact page
   - Set up a new directory named `public` at the root of the project
   - Create and add your logo:
     - Design or obtain your logo in PNG format
     - Add the PNG file to the `public` directory
     - Convert the PNG to ICO format:
       - Visit [cloudconvert.com/png-to-ico](https://cloudconvert.com/png-to-ico) to convert a PNG file to an ico file
     - Replace the existing `favicon.ico` in the `app` directory with your new one
   - Update the icons app metadata in `app/layout.tsx` with the paths to point to your new `.PNG` files in the public directory
     - This is so the icon appears in the dev environment

1. Add features to the app

1. When done adding features, check for build issues:

   ```bash
   npm run build
   ```
1. Add additional private environment variables (not prefixed with NEXT_PUBLIC_) in the build commands section of the amplify.yml file

1. Add, commit, and push the code:

1. Deploy and configure your application for Ads:
   - Purchase a custom domain from a service like GoDaddy
   - Follow steps 1-3 in this [article](https://medium.com/@dylancarver14/how-to-verify-site-ownership-for-google-adsense-in-a-next-js-15-app-c7d9a80e0964) to add a new site on [Google AdSense](https://www.google.com/adsense)
   - Deploy app on [AWS Amplify](https://us-east-2.console.aws.amazon.com/amplify/apps) and set Environment Variables to everything from the `.env.local` file
   - Use purchased custom domain in deployed Amplify app using this [tutorial](https://www.youtube.com/watch?v=uaG2mMYLI68)
   - Follow step 5 and on in this [article](https://medium.com/@dylancarver14/how-to-verify-site-ownership-for-google-adsense-in-a-next-js-15-app-c7d9a80e0964) to verify the app domain's site in Google AdSense

## Features

- PDF utilities
- Analytics tracking
- Google AdSense
- Modern, responsive UI

## License

This project is available as a template for building your own SAAS applications.
