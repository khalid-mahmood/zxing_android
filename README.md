Zxing Libarary for Android Studio Usage

Just Import to Your project.

Intent intent = new Intent("com.google.zxing.client.android.SCAN");

intent.putExtra("SCAN_MODE", "SCAN_MODE");

startActivityForResult(intent, QRCODE_REQUEST);

Result:     

@Override

    public void onActivityResult(int requestCode, int resultCode, Intent intent) {
        super.onActivityResult(requestCode, resultCode, intent);
        if (requestCode == QRCODE_REQUEST) {
            if (resultCode == RESULT_OK) {
                String contents = intent.getStringExtra("SCAN_RESULT");
                Log.e("contents", contents);
            } else if (resultCode == RESULT_CANCELED) {
            }

        }
    }
