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
android:layout_height="wrap_content
android:text="Hello World!"/>

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

# Second Screen
Lemme walk you through on how to make a second screen

```
    <TextView
        android:id="@+id/goNextpage"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="16dp"
        android:clickable="true"
        android:focusable="true"
        android:gravity="left"
        android:text="Sign up?"
        android:textColor="#0A5DAE"/>
```
Our main forcus is defining an XML element it can be any, and giving it a android:id attribute ```android:id="@+id/goNextpage"``` and assign it with your desired  id name, you can use any, but you have to remember it, so that we can call it when we want to click it...will be continued

# View with a border radius

making a border radius on a View or a Widget in android takes only 2 steps
1. Create a drawable file
2. set it as your background

```
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android" >                                   
    <solid android:color="@color/silver_98" />
    <corners android:radius="16dp" />
</shape>
```

# Making an Activity
This code is used for creating an activity in android,

```
view myview = findViewById(R.id.myviewid);
myview.setOnClickListener(new View.OnClickListener(){
   @Override
   public void onClick(View v) {
     Intent myintent = new Intent(MainActivity.this, SecondActivity.class);
      startActivity(myintent);
   }
});
```

# Making Light and Dark screen
Navigate to the directory ``` res/values/theme.xml ``` and copy paste this code in your theme.xml file
```
<resources xmlns:tools="http://schemas.android.com/tools">
    <!-- Base application theme. -->
    <style name="Base.Theme.YOUR-APPLICATION-NAME"
        parent="Theme.Material3.DayNight.NoActionBar">

        <item name="colorPrimary">#FFFFFF</item>
        <item name="android:statusBarColor">#FFFFFF</item>
        <item name="android:windowLightStatusBar">true</item>

    </style>

    <style name="Theme.BeeCalculator" parent="Base.Theme.BeeCalculator" />
</resources>
```
so this will basically JUST make your screens top action bar change to light screen when you change your devices theme color to color ``` #FFFFFF ``` which is white or light theme.
you also have to make it change when you change your phones theme to dark or black which is ``` #121212 ```, so to prevent android giving you the default purple color, navigate to the below directory.
``` res/values-night/theme.xml ``` and copy paste this code.
```
<resources xmlns:tools="http://schemas.android.com/tools">

    <style name="Base.Theme.YOUR-APPLICATION-NAME"
        parent="Theme.Material3.DayNight.NoActionBar">

        <item name="colorPrimary">#121212</item>
        <item name="android:statusBarColor">#121212</item>
        <item name="android:windowLightStatusBar">false</item>

    </style>

</resources>
```
