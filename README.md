# Гончаров 803в1
Создадим приложение и добавляем две кнопки и два "текста"

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
        
Сохранение в файл:

public void save_skill(View view)
    {
        try
        {

            EditText textBox = (EditText) findViewById(R.id.editTextTextPersonName);
            String text = textBox.getText().toString();
            try {
                file.createNewFile();
            }
            catch (IOException ex)
            {
                Toast.makeText(this, ex.getMessage(), Toast.LENGTH_SHORT).show();
            }
            FileOutputStream fos = new FileOutputStream(file);
            fos.write(text.getBytes());
            fos.close();
            Toast.makeText(this, "Текстовый файл успешно сохранён!", Toast.LENGTH_SHORT).show();
        } catch (IOException e)
        {
            e.printStackTrace();
            Toast.makeText(this, e.getMessage(), Toast.LENGTH_SHORT).show();
        }
    }
    
Загрузка из файла

 public void loader_skill(View view)
    {
        try
        {
            FileInputStream fin = new FileInputStream(file);
            byte[] bytes = new byte[fin.available()];
            fin.read(bytes);
            String text = new String(bytes);
            TextView textView = (TextView) findViewById(R.id.textView);
            textView.setText(text);
            fin.close();
        } catch (IOException ex)
        {
            Toast.makeText(this, ex.getMessage(), Toast.LENGTH_SHORT).show();
        }
    }
    
Проверить работоспособность

![Alt text](/image/1.png)
![Alt text](/image/2.png)

# Гослинг

![Альтернативный текст](/image/1222.jpg)
