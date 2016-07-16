package br.com.fatecpg.mylistapp;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.EditText;
import android.widget.ListView;

import java.util.ArrayList;

public class MainActivity extends AppCompatActivity {

    ArrayList<String> times = new ArrayList<>();

    public void inserir(View view){
        EditText edit = (EditText)findViewById(R.id.editText);
        String texto = edit.getText().toString();
        times.add(texto);
    }

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        ListView list = (ListView)findViewById(R.id.listView);
        list.setAdapter(new ArrayAdapter<String>(this, android.R.layout.simple_list_item_1, times));
        list.setOnItemClickListener(new AdapterView.OnItemClickListener() {
            @Override
            public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
                times.remove(position);
            }
        });
    }
}
