FindiT — Firebase website package

1. Open index.html in Acode.
2. Replace the firebaseConfig placeholder values with the config from Firebase > Project settings > Your apps > SDK setup and configuration > Config.
3. In Firebase Authentication, enable Anonymous sign-in.
4. In Firestore Database > Rules, publish the contents of firestore.rules.
5. Test using a local web server or deploy using a hosting provider that serves static files over HTTPS.

Important:
- This version does NOT use Firebase Storage. It compresses photos and stores them in Firestore documents as a temporary small-project workaround. Firestore has a 1 MiB document limit; this code rejects photos above a conservative encoded-size threshold. This is not suitable for large-scale use.
- The Firestore rules allow every authenticated anonymous visitor to read, create, edit and delete every item. Anyone can delete other people's posts. Only use with awareness of this risk.
- Do not publish personal contact details or sensitive information.
- Firebase web config is intended to be present in client code; security must come from Authentication and Firestore Rules, not from hiding the config.
