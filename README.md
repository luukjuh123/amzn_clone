

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
   Create a firebase.js file and at the configuration from firebase
        ```
        // Your web app's Firebase configuration
        import firebase from "firebase";
        const firebaseConfig = {
            apiKey: "",
            authDomain: "",
            projectId: "",
            storageBucket: "",
            messagingSenderId: "",
            appId: ""
        };

        const app = !firebase.app.length ? firebase.initializeApp(firebaseConfig) : firebase.app();

        const db = app.firestore();

        export default db;
        ```
3. Third:
    Add a permissions.json file and at the following details (Can copy these details from Firebase):
     ```
        {
        "type": "",
        "project_id": ",
        "private_key_id": "",
        "private_key": "",
        "client_email": "",
        "client_id": "",
        "auth_uri": "https://accounts.google.com/o/oauth2/auth",
        "token_uri": "https://oauth2.googleapis.com/token",
        "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
        "client_x509_cert_url": ""
        }
 ```
