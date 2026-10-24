# Firebase setup

The site uses the existing Firebase project `shadin-portfolio`.

## 1. Enable admin login

1. Open Firebase Console for `shadin-portfolio`.
2. Open **Authentication -> Sign-in method**.
3. Enable **Email/Password**.
4. Open **Authentication -> Users** and create the admin email/password you will use at `/admin.html`.

## 2. Apply Firestore rules

From the folder containing `firestore.rules`, run:

```powershell
firebase login
firebase use shadin-portfolio
firebase deploy --only firestore:rules
```

The rules allow public contact submissions but only authenticated users can read or delete messages.

## 3. Admin inbox

Open `/admin.html`, sign in with the Firebase admin account, and manage messages from the `contactMessages` collection.
