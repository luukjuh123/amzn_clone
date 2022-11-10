

## Getting Started

This is my clone of the amazon website. The login works through NextAuth with a connection through a Google account.  
To make the basket work you need to deploy a backend on firebase and add the multiple files to this project:

1. First: 
    Add this to an .env.local file:
    ```
        # Authentication
        GOOGLE_ID=
        GOOGLE_SECRET=
        NEXTAUTH_URL=http://localhost:3000

        # Stripe
        STRIPE_PUBLIC_KEY=
        STRIPE_SECRET_KEY=

        # Stripe Terminal/CLI
        STRIPE_SIGNING_SECRET=

        HOST=http://localhost:3000

        # Need to add this to... google cloud
        # http://localhost:3000/api/auth/callback/google
    ```
2. Second:
    