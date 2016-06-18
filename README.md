# AndSes3Ass2
Android Session 3 Assignment 2
Main Activiy.java
package me.rk.andses3ass1;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.RelativeLayout;
import android.widget.TextClock;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity implements View.OnClickListener{

    private TextView mtext;
    private RelativeLayout mred;
    private RelativeLayout morange;
    private RelativeLayout myellow;
    private RelativeLayout mgreen;
    private RelativeLayout mblue;
    private RelativeLayout mindigo;
    private RelativeLayout mvoilet;


    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        mred=(RelativeLayout) findViewById(R.id.red);
        mred.setOnClickListener(this);

        morange=(RelativeLayout) findViewById(R.id.orange);
        morange.setOnClickListener(this);

        myellow=(RelativeLayout) findViewById(R.id.yellow);
        myellow.setOnClickListener(this);

        mgreen=(RelativeLayout) findViewById(R.id.green);
        mgreen.setOnClickListener(this);

        mblue=(RelativeLayout) findViewById(R.id.blue);
        mblue.setOnClickListener(this);

        mindigo=(RelativeLayout) findViewById(R.id.indigo);
        mindigo.setOnClickListener(this);

        mvoilet=(RelativeLayout) findViewById(R.id.voilet);
        mvoilet.setOnClickListener(this);

        mtext=(TextView) findViewById(R.id.text);
        Toast.makeText(this, "Main Activity onCreate", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onStart() {
        super.onStart();
        Toast.makeText(this,"Main Activity onStart", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onResume() {
        super.onResume();
        Toast.makeText(this, "MainActivity onResume", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onPause() {
        super.onPause();
        Toast.makeText(this, "Main Activity onPause", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onStop() {
        super.onStop();
        Toast.makeText(this, "Main Activity onStop", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onDestroy() {
        super.onDestroy();
        Toast.makeText(this,"Main Activity onDestroy", Toast.LENGTH_SHORT).show();
    }

    @Override
    public void onClick(View v) {
        int id=v.getId();
        switch(id){
            case R.id.red:
                mtext.setText("Red clicked");
                Toast.makeText(this, "Red is clicked", Toast.LENGTH_SHORT).show();
                break;

            case R.id.orange:
                mtext.setText("Orange clicked");
                Toast.makeText(this, "Orange is clicked", Toast.LENGTH_SHORT).show();
                break;

            case R.id.yellow:
                mtext.setText("Yellow clicked");
                Toast.makeText(this, "Yellow is clicked", Toast.LENGTH_SHORT).show();
                break;

            case R.id.green:
                mtext.setText("Green clicked");
                Toast.makeText(this, "Green is clicked", Toast.LENGTH_SHORT).show();
                break;

            case R.id.blue:
                mtext.setText("Blue clicked");
                Toast.makeText(this, "Blue is clicked", Toast.LENGTH_SHORT).show();
                break;

            case R.id.indigo:
                mtext.setText("Indigo clicked");
                Toast.makeText(this, "Indigo is clicked", Toast.LENGTH_SHORT).show();
                break;

            case R.id.voilet:
                mtext.setText("Voilet clicked");
                Toast.makeText(this, "Voilet is clicked", Toast.LENGTH_SHORT).show();
                break;

        }

    }
}

Activity Main.xml
<?xml version="1.0" encoding="utf-8"?>
<GridLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"

    tools:context="me.rk.andses3ass1.MainActivity">

    <TextView
        android:id="@+id/text"
        android:layout_width="wrap_content"
        android:layout_centerHorizontal="true"
        android:layout_height="wrap_content"
        android:text="Selected Colour"
        android:textSize="32dp"
        android:background="@color/colorPrimary"
        android:textColor="#FFFFFF"/>

    <RelativeLayout
        android:id="@+id/red"
        android:layout_width="match_parent"
        android:layout_height="69dp"
        android:layout_row="1"
        android:layout_column="0"
        android:layout_below="@+id/text"
        android:background="#ff0000"></RelativeLayout>

    <RelativeLayout
        android:id="@+id/orange"
        android:layout_width="match_parent"
        android:layout_height="69dp"
        android:background="#ff7300"
        android:layout_row="2"
        android:layout_column="0"></RelativeLayout>

    <RelativeLayout
        android:id="@+id/yellow"
        android:layout_width="match_parent"
        android:layout_height="69dp"
         android:background="#fff701"
        android:layout_row="3"
        android:layout_column="0"></RelativeLayout>

    <RelativeLayout
        android:id="@+id/green"
        android:layout_width="match_parent"
        android:layout_height="69dp"
        android:background="#62ff01"
        android:layout_row="4"
        android:layout_column="0" />

    <RelativeLayout
        android:id="@+id/blue"
        android:layout_width="match_parent"
        android:layout_height="69dp"
        android:background="#0112ff"
        android:layout_row="5"
        android:layout_column="0" />

    <RelativeLayout
        android:id="@+id/indigo"
        android:layout_width="match_parent"
        android:layout_height="69dp"
        android:background="#8801ff"
        android:layout_row="6"
        android:layout_column="0" />

    <RelativeLayout
        android:id="@+id/voilet"
        android:layout_width="match_parent"
        android:layout_height="69dp"
        android:background="#ee01ff"
        android:layout_row="7"
        android:layout_column="0" />

</GridLayout>
