DevOps - This app is using w3Code.
```java
// w3Code.
public static class w3Code {
        public static List<AlertDialog.Builder> a0001, b0001, c0001;
}
```
```java
// Java using w3Code.
public AlertDialog.Builder getBuilder() {
        w3Code.a0001 = Collections.singletonList(new AlertDialog.Builder(AppCode.this));
        w3Code.a0001.get(0).setCancelable(true);
        w3Code.a0001.get(0).setIcon(R.drawable.ic_online_24);
        w3Code.a0001.get(0).setTitle("Close Application");
        w3Code.a0001.get(0).setMessage("Confirm that you want to close this application. Are you sure?");
        w3Code.a0001.get(0).setPositiveButton("Yes", (dialog, id) -> new Handler(Looper.getMainLooper()).postDelayed(() -> {
            w3Code.a0011 = Collections.singletonList(new Intent(AppCode.this, MainClose.class));
            startActivity(w3Code.a0011.get(0));
            overridePendingTransition(R.anim.slide_in_right, R.anim.slide_out_left);
            finish();
        }, 1000));
        w3Code.a0001.get(0).setNegativeButton("No", (dialog, id) -> dialog.dismiss());
        return w3Code.a0001.get(0);
}
