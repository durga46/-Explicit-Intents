# <p align="center"> Ex.No:2b Explicit Intents</p>


Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents and to create two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.

## AIM:
To display factorial number using Explicit Intents in Android Studio.

## EQUIPMENTS REQUIRED:
Android Studio(Min. required Artic Fox)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “ex.no.2″ and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: display factorial number using Explicit Intents in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```python
/*
Program to print the text “Implicit and Explicit Intents”.
Developed by: DurgaDevi P
Registeration Number : 212220230015
*/

## Explicit Intent
### MainActivity.java
```java
package com.example.firstapp;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {
    EditText etNumber;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        etNumber=findViewById(R.id.etNumber);
    }
    public void displayFactorial(View view){
        Intent i=new Intent(MainActivity.this,MainActivity2.class);
        i.putExtra("number",etNumber.getText().toString());
        startActivity(i);
    }
}
```
## activity_main.xml
```python
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText android:id="@+id/etNumber"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="@string/enter_the_number"
        android:inputType="number"
        android:layout_marginTop="50dp"
        android:importantForAutofill="no" />

    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/factorial"
        android:onClick="displayFactorial"/>

</LinearLayout>
```
## MainActivity2.java
```python
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText android:id="@+id/etNumber"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="@string/enter_the_number"
        android:inputType="number"
        android:layout_marginTop="50dp"
        android:importantForAutofill="no" />

    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/factorial"
        android:onClick="displayFactorial"/>

</LinearLayout>
```
## activity_main2.xml
```python
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity2"
    android:padding="20dp">

    <TextView android:id="@+id/tv"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:text="@string/factorial_of_number_is"
        style="@style/TextAppearance.AppCompat.Large"/>

</RelativeLayout>
```
## OUTPUT
![v3](https://user-images.githubusercontent.com/75235704/168261249-8f43542d-ad9e-4741-a3db-f2c916a9a1df.png)


![v4](https://user-images.githubusercontent.com/75235704/168261271-df1370c5-5844-44a7-ad35-143f5d6d5bd7.png)


## RESULT
Thus a Simple Android Application to display factorial of the same number using Explicit Intents using Android Studio is developed and executed successfully.
