
# Rapport

****
In the MainActivity XML code, three widgets have been added: TextView, EditText and Button.
The TextView displays a greeting phrase "Hello", the EditText allows the user to enter a name(Which I didn't have before),
and the button sends data to another activity, "ShowActivity".


In the ShowActivity XML code, a widget, a TextView, has been added to display the data received from the intent.
Inten was used to send data to other activities, and Bundle was used to send key-value, like "String".
The key passed was "String" with a data type. Intent facilitates the transfer of data between activities in the application.


Finally, an arrow-like feature has been added to ShowActivity to make it easier to return to MainActivity.



****
## Följande grundsyn gäller dugga-svar:

- Ett kortfattat svar är att föredra. Svar som är längre än en sida text (skärmdumpar och programkod exkluderat) är onödigt långt.
- Svaret skall ha minst en snutt programkod.
- Svaret skall inkludera en kort övergripande förklarande text som redogör för vad respektive snutt programkod gör eller som svarar på annan teorifråga.
- Svaret skall ha minst en skärmdump. Skärmdumpar skall illustrera exekvering av relevant programkod. Eventuell text i skärmdumpar måste vara läsbar.
- I de fall detta efterfrågas, dela upp delar av ditt svar i för- och nackdelar. Dina för- respektive nackdelar skall vara i form av punktlistor med kortare stycken (3-4 meningar).

Programkod ska se ut som exemplet nedan. Koden måste vara korrekt indenterad då den blir lättare att läsa vilket gör det lättare att hitta syntaktiska fel.

```
 public void onClick(View view) {
                Intent intent = new Intent(MainActivity.this, ShowActivity.class);

                EditText nameEdit = findViewById(R.id.editTextName);
                String name = nameEdit.getText().toString();

                intent.putExtra("name", name); // Optional
                startActivity(intent);
            }
        });
    }
}
```

```
<TextView
        android:id="@+id/textViewName"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintBottom_toTopOf="@id/textViewName"/>

    <EditText
        android:id="@+id/editTextName"
        android:layout_width="200dp"
        android:layout_height="wrap_content"
        android:minHeight="48dp"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Name"
        tools:layout_editor_absoluteX="88dp"
        tools:layout_editor_absoluteY="232dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.5"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.5" />

    <Button
        android:id="@+id/sendButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Button"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.571" />

```

```
protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_show);

        Bundle extras = getIntent().getExtras();
        if (extras != null) {
            String name = extras.getString("name");

            // Do something with the name and number


            TextView nameView = findViewById(R.id.textViewNameShow);
            nameView.setText(name);
        }
    }
}
```

```
    <TextView
        android:id="@+id/textViewNameShow"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text=""
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintBottom_toTopOf="@id/textViewNameShow"/>
```
Bilder läggs i samma mapp som markdown-filen.

![](Screenshot_20230502_115909_.png)
![](Screenshot_20230502_115936_.png)

Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.
