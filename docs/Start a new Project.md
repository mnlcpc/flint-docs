## Setup

1. [Download Flint](https://github.com/mnlcpc/flint/archive/refs/heads/main.zip) or clone the repository with `git clone https://github.com/mnlcpc/flint.git`
2. Unzip the repository and open the folder in your code editor
3. Run `npm install` to install the dependencies
4. Rename the file `.example.env.local` to `.env.local`
5. Open the `.env.local` file and fill in your project details. In the file you'll find inline comments to help you with that. To get some of the values you'll need to perform the next steps.
6. Launch Docker Desktop then run `supabase start` . This starts the local database on docker and applies migrations.
   1. Take notes of your local ANON_KEY and SERVICE_ROLE_KEY. Add them to the `.env.local` file as TEST values.
7. Populate the `.env.local` file with the correct development ("TEST") and production ("LIVE") values.
   1. **Stripe** : get the API keys from the [Stripe dashboard](https://dashboard.stripe.com/apikeys)
   2. Run script `npm run stripe:listen` and copy the webhook signing secret for local development
   3. **Supabase** : Take the values for production from the [supabase project settings](https://app.supabase.com/), and the values for local development are the ones you got when you launched supabase start
   4. **Posthog** : get the API keys from the [Postohog dashboard](https://us.posthog.com/)
   5. **Resend** : get the API keys from the [Resend dashboard](https://resend.com/)
   6. Configure the integration Resend / Supabase so that you can send emails with no limits and from your domain.
8. Run `npm run supabase:link` to link your local environment to your Supabase project
9. Push your project on Github
10. Go on Vercel and link your Github Project, so that Vercel will take care of deployment.
11. Copy local env values to your your project settings on Vercel

Now everthing is setup, you can run `npm run dev` to start your local development server.
