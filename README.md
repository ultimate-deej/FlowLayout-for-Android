FlowLayout for Android
======================
This is a FlowLayout implementation for Android.

Important notice!
-----------------

I once needed it. Now its job done long ago.

It works. But it lacks some features, it's not on jcenter or maven central, and design of the library can be better overall.

It is not maintained.

Features
--------

Four **flow directions** (similar to WinForms). They are:
- leftToRight
- rightToLeft
- topDown
- bottomUp

You can also optionally specify **gravity** for layout. *Center* and *fill* are supported.

Layout child can force starting a new line if **layout_breakLine** attribute set to *true*.

To limit max number of lines use **maxLines** attribute. Default is 0.

Usage example
-------------
```xml
<?xml version="1.0" encoding="utf-8"?>
<org.deejdev.android.FlowLayout xmlns:android="http://schemas.android.com/apk/res/android"
                                xmlns:app="http://schemas.android.com/apk/res-auto"
                                app:flowDirection="leftToRight"
                                app:elementSpacing="4dp"
                                app:lineSpacing="16dp"
                                android:maxLines="50"
                                android:gravity="center"
                                android:layout_width="fill_parent"
                                android:layout_height="fill_parent">

    <Button
        android:text="button1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

    <Button
        android:text="button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

    <Button
        android:text="button3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

    <Button
        android:text="button4"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

    <Button
        android:text="button5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

    <Button
        app:layout_breakLine="true"
        android:text="button6"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
</org.deejdev.android.FlowLayout>
```
This results in the following:

![Centered FlowLayout](https://raw.github.com/ultimate-deej/FlowLayout-for-Android/master/screenshots/center.png)

Same with gravity set fo *fill* and without gravity respectively:

![Fill](https://raw.github.com/ultimate-deej/FlowLayout-for-Android/master/screenshots/fill.png)
![No gravity](https://raw.github.com/ultimate-deej/FlowLayout-for-Android/master/screenshots/no-gravity.png)

TODO
----
- Implement margins for child views
