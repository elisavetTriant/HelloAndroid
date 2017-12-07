# HelloAndroid
This is a small Android App that shows Udacity's contact information. It also has a button that opens a spesific url to the devices' default browser. This was made for the  Google Developer Challenge 2017-2018 as an assignment to practice with Layouts, TextViews and ImageViews.

This is how the App looks like on Android Studio 3:

![The Project on Android Studio](https://github.com/elisavetTriant/HelloAndroid/blob/master/screenshots/Screenshot_HelloAndroid_AndroidStudio.png "The Project on Android Studio")

And this is what the UI looks like on my device (Lenovo tablet Lollipop API22), portrait and landscape:

![Udacity HelloAndroid App Portrait](https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/screenshots/Screenshot_HelloAndroid_portrait.jpg  "Udacity HelloAndroid App Portrait")

![Udacity HelloAndroid App Landscape](https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/screenshots/Screenshot_HelloAndroid_landscape.jpg  "Udacity HelloAndroid App Landscape")

And here is what the layout xml code looks like (file app/src/main/res/layout/activity_main.xml, or https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/app/src/main/res/layout/activity_main.xml):

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical"
        android:background="@color/primary_light"
        tools:context="co.elisavet.helloandroid.MainActivity">

    <ImageView
            android:id="@+id/udacity_contact_photo_image_view"
            android:layout_width="match_parent"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:scaleType="centerCrop"
            android:src="@drawable/udacity_contact_photo"
            android:layout_margin="@dimen/udacity_ImageView_margin_small"/>

    <ScrollView
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:fillViewport = "true">
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="@dimen/elements_margin_small"
            android:background="@color/primary_dark"
            android:orientation="vertical">

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal">

                    <ImageView
                        android:id="@+id/ic_business_image_view"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:padding="@dimen/contact_info_elements_padding_small"
                        android:scaleType="centerCrop"
                        android:src="@drawable/ic_business_white_18dp" />

                    <TextView
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:padding="@dimen/contact_info_elements_padding_small"
                        android:text="@string/company"
                        android:textColor="@color/icons"
                        android:textSize="@dimen/contact_info_elements_font_size_small" />
                </LinearLayout>

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal">

                    <ImageView
                        android:id="@+id/ic_location_image_view"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:padding="@dimen/contact_info_elements_padding_small"
                        android:scaleType="centerCrop"
                        android:src="@drawable/ic_location_on_white_18dp" />

                    <TextView
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:padding="@dimen/contact_info_elements_padding_small"
                        android:text="@string/address"
                        android:textColor="@color/icons"
                        android:textSize="@dimen/contact_info_elements_font_size_small" />
                </LinearLayout>

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal">

                    <ImageView
                        android:id="@+id/ic_phone_image_view"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:padding="@dimen/contact_info_elements_padding_small"
                        android:scaleType="centerCrop"
                        android:src="@drawable/ic_phone_white_18dp" />

                    <TextView
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:padding="@dimen/contact_info_elements_padding_small"
                        android:text="@string/phone"
                        android:textColor="@color/icons"
                        android:textSize="@dimen/contact_info_elements_font_size_small" />
                </LinearLayout>

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal">

                    <ImageView
                        android:id="@+id/ic_mail_image_view"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:padding="@dimen/contact_info_elements_padding_small"
                        android:scaleType="centerCrop"
                        android:src="@drawable/ic_mail_outline_white_18dp" />

                    <TextView
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:padding="@dimen/contact_info_elements_padding_small"
                        android:text="@string/email"
                        android:textColor="@color/icons"
                        android:textSize="@dimen/contact_info_elements_font_size_small" />
                </LinearLayout>

                <Button
                    android:id="@+id/contact_button"
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:layout_margin="@dimen/elements_margin_small"
                    android:background="@color/accent"
                    android:text="@string/contact"
                    android:textAlignment="center"
                    android:textColor="@color/primary_text"
                    android:textSize="@dimen/contact_info_elements_font_size_small" />
            </LinearLayout>
    </ScrollView>
</LinearLayout>
```
The design caters for different layout for landscape orientation, file: https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/app/src/main/res/layout-land/activity_main.xml

It also caters for larger screen-sizes both portrait and landscape ( files https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/app/src/main/res/layout-large/activity_main.xml and https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/app/src/main/res/layout-large-land/activity_main.xml )

Don't forget to take a look at the resources folder ( /app/res/values ) and take a look at the code there also. 

The java code looks like this ( app/src/main/java/co/elisavet/helloandroid )
```java
package co.elisavet.helloandroid;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.content.Intent;
import android.net.Uri;
import android.view.View;
import android.widget.Button;


public class MainActivity extends AppCompatActivity {

    Button UrlOpen;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        UrlOpen = (Button)findViewById(R.id.contact_button);

        UrlOpen.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View v) {

                Intent Getintent = new Intent(Intent.ACTION_VIEW,Uri.parse("https://in.udacity.com/contact/"));
                startActivity(Getintent);

            }
        });

    }
}

```
More resources
* https://developer.android.com/training/basics/supporting-devices/index.html, (Supporting Different Devices)
* https://developer.android.com/training/multiscreen/screendensities.html, (Supporting Different Densities)
* https://developer.android.com/training/multiscreen/screensizes.html, (Supporting Different Screen Sizes)
* https://developer.android.com/training/basics/supporting-devices/screens.html, (Supporting Different Screens)
* https://www.android-examples.com/open-website-url-in-androids-web-browser-from-application/, (Open Website Url in Android’s Web browser from application)
* https://developer.android.com/training/basics/firstapp/starting-activity.html, (Start Another Activity)
* https://developer.android.com/guide/topics/resources, (App Resources)
* https://guides.codepath.com/android/Understanding-App-Resources, (Understanding App Resources)
* https://developer.android.com/reference/android/widget/ScrollView.html (ScrollView)
