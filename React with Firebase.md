## Good reference 
### Authentication Example by rwieruch
* Turoial: https://www.robinwieruch.de/complete-firebase-authentication-react-tutorial/#react-firebase-setup
* Context Example : https://medium.com/workshop-me/render-props-react-createcontext-but-how-9c8e457a90e3
* Repo: https://github.com/rwieruch/react-firebase-authentication

### Other examples (database ETC.)
* Repo: https://github.com/jeescu/react-firebase

## How to setup user specific database
* https://firebase.google.com/docs/database/security/quickstart?authuser=0
```
{
  "rules": {
    "users": {
      "$uid": {
        ".read": "$uid === auth.uid",
        ".write": "$uid === auth.uid"
      }
    }
  }
}
```

* 좋은 rule example : https://github.com/firebase/friendlypix-web/blob/master/database-rules.json

## Reference 
* React context API : https://reactjs.org/docs/context.html
Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. 

* Firebase check list: https://firebase.google.com/support/guides/launch-checklist
* Firebase database rules: https://firebase.google.com/docs/database/security/
