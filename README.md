# WS_Android-DownloadImagefromURL_Function
Android download image from URL.

> Example

```java
public static Bitmap getBitmapFromURL(String src) 
{
        try {
            Log.e("src",src);
            URL url = new URL(src);
            HttpURLConnection connection = (HttpURLConnection) url.openConnection();
            connection.setDoInput(true);
            connection.connect();
            InputStream input = connection.getInputStream();
            Bitmap myBitmap = BitmapFactory.decodeStream(input);
            Log.e("Bitmap","returned");
            return myBitmap;
        } 
        catch (IOException e) 
        {
            e.printStackTrace();
            Log.e("Exception",e.getMessage());
            return null;
        }
}
```
