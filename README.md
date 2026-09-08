# Duo Pixel Seller AI — Live MVP

This version uses a real server-side OpenAI API instead of the local demo generator.

## Important security rule
Never put `OPENAI_API_KEY` inside `index.html`. The browser calls `/api/generate`, and the serverless function calls OpenAI with the secret key.

## Deploy on Vercel
1. Put this folder in a GitHub repository.
2. Import the repository into Vercel.
3. In Vercel Project Settings → Environment Variables, add `OPENAI_API_KEY`.
4. Optionally add `OPENAI_MODEL=gpt-5.6-luna`.
5. Deploy.

## Payment setup
The frontend is prepared for hosted checkout URLs. Do not put secret payment credentials in the frontend.

For Nepal-based payments, Khalti and eSewa both provide web payment gateways, but merchant onboarding/KYC is required before live collection. Configure their official merchant integration on the server before switching to production payments.

For a global checkout provider, first verify that it can legally onboard and pay out to your actual country/entity. Do not use a fake country, borrowed account, or someone else's identity.
