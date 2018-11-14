## 다른앱 auth 정보를 firebase auth로 마이그레이션 하기
### Firebase CLI 
* Firebase CLI의 auth:import를 쓰면 됨  (auth:import)
* https://github.com/firebase/firebase-tools

### 코드로도 가능 
* https://firebase.google.com/docs/auth/admin/import-users
* 내 경우에는 (BCRYPT)를 사용하여 해싱하여 아래 코드를 사용

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
