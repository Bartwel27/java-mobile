# java-mobile
A repostory to help you get started with a java android studio mobile application, for android version 7 andoid nughet, this will work approximatly on 98% android devices

You can edit the ```activity_main.xml``` file to this or keep it as it is.
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</LinearLayout>
```


## Design XML
Here are some of the attributes you can use on an XML widget to design a mobile interface

**LinearLayout View**
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    android:orientation="vertical"
    android:padding="24dp" >
```
The android:```layout_width``` and ```layout_height``` with value *match_parent* attributes will be used to fix the width and height of the widget to match its parent layout width and height, this will actually help the width and height to stay in constant the same with its parent size.

**EditText View**
```
<EditText
        android:id="@+id/emailEditText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginBottom="16dp"
        android:hint="Email"
        android:inputType="textEmailAddress" />
```

# Making a Second Screen
