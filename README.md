# IntendGetUrl
输入URL网址，点击按钮，将发起浏览网页的行为
~~~
package com.example.intendgeturl;

import android.content.Intent;
import android.net.Uri;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {
    private static String MY_ACTION = "view.ACTION_VIEW";
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final EditText text1 = (EditText) findViewById(R.id.editText);
        Button rdcy=(Button)findViewById(R.id.button2);
        rdcy.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Uri uri = Uri.parse("http://"+text1.getText().toString());
                Intent intent = new Intent(Intent.ACTION_VIEW);
                startActivity(intent);
            }
        });
    }
}
~~~
## AndroidManifest.xml
~~~
<activity android:name=".Main2Activity">
            <intent-filter>
                <action android:name="android.intent.action.VIEW"/>
            </intent-filter>
        </activity>
        
~~~
![image](https://github.com/1158509577/IntendGetUrl/blob/master/app/src/main/res/resultimage/1.png)

![image](https://github.com/1158509577/IntendGetUrl/blob/master/app/src/main/res/resultimage/2.png)

![image](https://github.com/1158509577/IntendGetUrl/blob/master/app/src/main/res/resultimage/3.png)
