# Ex_8_CheckBox
Develop a program to create a option menu using checkboxes and display the toast selected checkboxes with Android Studio
## AIM:
To Develop a program for creating a option menu using checkboxes and display the toast selected checkboxes with Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Once the Selected check box displayed to the user processed in MainActivity.java

Step 7: Save and run the application.


## Program:
 ```
Program to create an Option Menu
Developed by: Vishal Gowthaman K R
RegisterNumber: 212221230123
```

## MainActivity.java:
```
package com.example.ex_8;

import androidx.appcompat.app.AppCompatActivity;
import android.view.View;
import android.widget.CheckBox;
import android.widget.Toast;
import android.os.Bundle;

public class MainActivity extends AppCompatActivity {
    private CheckBox chkAndroid, chkJava, chkPhp, chkCpp, chkC;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        chkAndroid = findViewById(R.id.chkAndroid);
        chkJava = findViewById(R.id.chkJava);
        chkPhp = findViewById(R.id.chkPhp);
        chkCpp = findViewById(R.id.chkCpp);
        chkC = findViewById(R.id.chkC);
    }
    public void showSelected(View view) {

        String selected = "You selected: \n";

        if(chkAndroid.isChecked())
            selected += "Android";

        if(chkJava.isChecked())
            selected += "\nJava";

        if(chkPhp.isChecked())
            selected += "\nPHP";

        if(chkCpp.isChecked())
            selected += "\nCPP";

        if(chkC.isChecked())
            selected += "\nC";

        Toast.makeText(MainActivity.this, selected, Toast.LENGTH_SHORT).show();
    }
}
```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:gravity="center"
        android:text="Select Your favourite Programming language"
        style="@style/TextAppearance.AppCompat.Large"
        android:layout_margin="10dp"
        android:textStyle="bold"/>

    <CheckBox
        android:id="@+id/chkAndroid"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Android"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkJava"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Java"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkPhp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="PHP"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkCpp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="CPP"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkC"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="C"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <Button android:id="@+id/btnDisplay"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Display"
        android:layout_marginTop="20dp"
        android:onClick="showSelected"/>

</LinearLayout>
```
## Output
![81](https://github.com/Yuvadarshini-Sathiyamoorthy/Ex_8_CheckBox/assets/93482485/9757d407-2f63-4831-bf3c-fdf17642e25d)
![82](https://github.com/Yuvadarshini-Sathiyamoorthy/Ex_8_CheckBox/assets/93482485/438683da-6281-49f2-8def-59298231c1bd)

## Result:
Thus a Simple Android Application to create an check box and display the selected check box using Android Studio was developed and executed successfully.
