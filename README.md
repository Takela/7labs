# Гончаров 803в1
Создадим приложение и добавляем две кнопки и два "текста"
```
<TextView
        android:id="@+id/textView"
        android:layout_width="88dp"
        android:layout_height="28dp"
        android:layout_marginStart="161dp"
        android:layout_marginTop="132dp"
        android:text="Текстовичок"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/b_save"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="38dp"
        android:layout_marginTop="385dp"
        android:onClick="save_skill"
        android:text="save"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/b_load"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="134dp"
        android:layout_marginTop="387dp"
        android:onClick="loader_skill"
        android:text="loadeu"
        app:layout_constraintStart_toEndOf="@+id/b_save"
        app:layout_constraintTop_toTopOf="parent" />

    <EditText
        android:id="@+id/editTextTextPersonName"
        android:layout_width="204dp"
        android:layout_height="50dp"
        android:layout_marginStart="100dp"
        android:layout_marginTop="120dp"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Кто я?"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView" />
        

# Гослинг

![Альтернативный текст](/image/1222.jpg)
