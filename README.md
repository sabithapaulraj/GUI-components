# Ex.No: 1 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
1.Start a new project in Android Studio.

2.Design a simple layout(.xml File).

3.Inside MainActivity.java , create the button function

4.Create button for colors and fonts while clicking color or font button should change the color and font.

5.Display corresponding changes in application.

## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by: Sabitha P
Registeration Number : 212222040137
*/
```
### In activitymain.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        android:textSize="48sp"
        android:textStyle="bold|italic"
        app:layout_constraintBottom_toTopOf="@+id/button1"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.544" />

    <Button
        android:id="@+id/button1"
        android:layout_width="273dp"
        android:layout_height="89dp"
        android:text="Change Font Size"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button2"
        android:layout_width="264dp"
        android:layout_height="77dp"
        android:text="Change Text Colour"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button1" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
### In MainActivity.java
```
package com.example.guicomponents;


import android.graphics.Color;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

import com.example.guicomponents.R;

public class MainActivity extends AppCompatActivity
{
    int ch=1;
    float font=30;
    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t= (TextView) findViewById(R.id.textView);
        Button b1= (Button) findViewById(R.id.button1);
        b1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                t.setTextSize(font);
                font = font + 5;
                if (font == 50)
                    font = 30;
            }
        });
        Button b2= (Button) findViewById(R.id.button2);
        b2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                switch (ch) {
                    case 1:
                        t.setTextColor(Color.RED);
                        break;
                    case 2:
                        t.setTextColor(Color.GREEN);
                        break;
                    case 3:
                        t.setTextColor(Color.BLUE);
                        break;
                    case 4:
                        t.setTextColor(Color.CYAN);
                        break;
                    case 5:
                        t.setTextColor(Color.YELLOW);
                        break;
                    case 6:
                        t.setTextColor(Color.MAGENTA);
                        break;
                }
                ch++;
                if (ch == 7)
                    ch = 1;
            }
        });
    }
}
```

## OUTPUT
![WhatsApp Image 2024-03-11 at 09 22 21_a0ac74ae](https://github.com/sabithapaulraj/GUI-components/assets/118343379/2679f97c-cc94-4620-821a-daa500e515b5)
![WhatsApp Image 2024-03-11 at 09 22 21_49d0f160](https://github.com/sabithapaulraj/GUI-components/assets/118343379/d97351d0-0fac-4675-9e21-290fecd65c2d)
![WhatsApp Image 2024-03-11 at 09 22 21_01dfca32](https://github.com/sabithapaulraj/GUI-components/assets/118343379/ad5b5a95-7c2e-49a2-9d2b-db97014af23f)
![WhatsApp Image 2024-03-11 at 09 22 22_b91525d5](https://github.com/sabithapaulraj/GUI-components/assets/118343379/7b6f7dbf-3bee-4ffc-a063-fe97981a0e7b)
![WhatsApp Image 2024-03-11 at 09 23 15_0f3ca20a](https://github.com/sabithapaulraj/GUI-components/assets/118343379/d43658d2-fa1d-4d96-a18e-7b6f53269b7f)

## Working in Android Studio
![Screenshot 2024-04-20 184948](https://github.com/sabithapaulraj/GUI-components/assets/118343379/76013e01-ea8f-4d4b-9f8a-ccae715ef720)



## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.


