## How to  
### through Firebase CLI 
* It's possible through Firebase CLI auth:import by using batch importing (auth:import)
* https://github.com/firebase/firebase-tools

### throguth code 
* https://firebase.google.com/docs/auth/admin/import-users

### Im my case, from BCRYPT with Java
```
try {
  List<ImportUserRecord> users = Collections.singletonList(ImportUserRecord.builder()
      .setUid("some-uid")
      .setEmail("user@example.com")
      .setPasswordHash("password-hash".getBytes())
      .setPasswordSalt("salt".getBytes())
      .build());
  UserImportOptions options = UserImportOptions.withHash(Bcrypt.getInstance());
  UserImportResult result = FirebaseAuth.getInstance().importUsers(users, options);
  for (ErrorInfo indexedError : result.getErrors()) {
    System.out.println("Failed to import user: " + indexedError.getReason());
  }
} catch (FirebaseAuthException e) {
  System.out.println("Error importing users: " + e.getMessage());
}
```


## References
* firebase tool :  https://firebase.google.com/docs/cli/auth
* stackoverflow 1 : https://stackoverflow.com/questions/16053273/firebase-import-users-from-existing-app
* stackoverflow 2 : https://stackoverflow.com/questions/40427243/migrate-user-authentication-to-firebase-auth
* import through code : https://firebase.google.com/docs/auth/admin/import-users
