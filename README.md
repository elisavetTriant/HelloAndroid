# HelloAndroid
This is a small Android App that shows Udacity's contact information. It also has a button that opens a spesific url to the devices' default browser. This was made for the  Google Developer Challenge 2017-2018 as an assignment to practice with Layouts, TextViews and ImageViews.

This is what the UI looks like on my device (Lenovo tablet Lollipop API22), portrait and landscape:

![Udacity HelloAndroid App Portrait](https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/screenshots/Screenshot_HelloAndroid_portrait_revised.png  "Udacity HelloAndroid App Portrait")

![Udacity HelloAndroid App Landscape](https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/screenshots/Screenshot_HelloAndroid_landscape_revised.png  "Udacity HelloAndroid App Landscape")

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
            android:layout_margin="@dimen/elements_margin_small"/>

    <ScrollView
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:fillViewport = "true">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            style="@style/ContactInfoViewGroupStyleSmall">

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
                        android:text="@string/company"
                        style="@style/ContactInfoTextViewsStyleSmall"/>
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
                        android:text="@string/address"
                        style="@style/ContactInfoTextViewsStyleSmall" />
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
                        android:text="@string/phone"
                        style="@style/ContactInfoTextViewsStyleSmall"/>
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
                        android:text="@string/email"
                        style="@style/ContactInfoTextViewsStyleSmall" />
                </LinearLayout>

                <Button
                    android:id="@+id/contact_button"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/contact"
                    style="@style/ContactInfoButtonSmall"
                    />
            </LinearLayout>
    </ScrollView>
</LinearLayout>
```
The design caters for different layout for landscape orientation, file: https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/app/src/main/res/layout-land/activity_main.xml

It also caters for larger screen-sizes both portrait and landscape ( files https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/app/src/main/res/layout-large/activity_main.xml and https://github.com/elisavetTriant/HelloAndroid/blob/Mentor-Suggestions/app/src/main/res/layout-large-land/activity_main.xml )

Don't forget to take a look at the resources folder ( /app/res/values ) and take a look at the code there also. For instance the styles.xml code looks like this now: 
```xml
<resources>

    <!-- Base application theme. -->
    <style name="AppTheme"  parent="Theme.AppCompat.Light.DarkActionBar">
        <!-- Customize your theme here. -->
        <item name="android:colorPrimary">@color/primary</item>
        <item name="android:colorPrimaryDark">@color/primary_dark</item>
        <item name="android:colorAccent">@color/accent</item>
    </style>

    <style name="ContactInfoViewGroupStyleSmall">
        <item name="android:layout_marginLeft">@dimen/elements_margin_small</item>
        <item name="android:layout_marginRight">@dimen/elements_margin_small</item>
        <item name="android:layout_marginBottom">@dimen/elements_margin_small</item>
        <item name="android:background">@color/primary_dark</item>
    </style>

    <style name="ContactInfoViewGroupStyleSmallLandscape">
        <item name="android:layout_marginRight">@dimen/elements_margin_small</item>
        <item name="android:layout_marginTop">@dimen/elements_margin_small</item>
        <item name="android:layout_marginBottom">@dimen/elements_margin_small</item>
        <item name="android:background">@color/primary_dark</item>
    </style>

    <style name="ContactInfoViewGroupStyleLarge">
        <item name="android:layout_marginLeft">@dimen/elements_margin_large</item>
        <item name="android:layout_marginRight">@dimen/elements_margin_large</item>
        <item name="android:layout_marginBottom">@dimen/elements_margin_large</item>
        <item name="android:background">@color/primary_dark</item>
    </style>

    <style name="ContactInfoViewGroupStyleLargeLandscape">
        <item name="android:layout_marginRight">@dimen/elements_margin_large</item>
        <item name="android:layout_marginTop">@dimen/elements_margin_large</item>
        <item name="android:layout_marginBottom">@dimen/elements_margin_large</item>
        <item name="android:background">@color/primary_dark</item>
    </style>

    <style name="ContactInfoTextViewsStyleSmall">
        <item name="android:textColor">@color/icons</item>
        <item name="android:textSize">@dimen/contact_info_elements_font_size_small</item>
        <item name="android:padding">@dimen/contact_info_elements_padding_small</item>
    </style>

    <style name="ContactInfoTextViewsStyleLarge">
        <item name="android:textColor">@color/icons</item>
        <item name="android:textSize">@dimen/contact_info_elements_font_size_large</item>
        <item name="android:padding">@dimen/contact_info_elements_padding_large</item>
    </style>

    <style name="ContactInfoButtonSmall">
        <item name="android:layout_margin">@dimen/elements_margin_small</item>
        <item name="android:background">@color/accent</item>
        <item name="android:gravity">center</item>
        <item name="android:textColor">@color/primary_text</item>
        <item name="android:textSize">@dimen/contact_info_elements_font_size_small</item>
    </style>

    <style name="ContactInfoButtonLarge">
        <item name="android:layout_margin">@dimen/elements_margin_large</item>
        <item name="android:background">@color/accent</item>
        <item name="android:gravity">center</item>
        <item name="android:textColor">@color/primary_text</item>
        <item name="android:textSize">@dimen/contact_info_elements_font_size_large</item>
    </style>

</resources>

```

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
* https://developer.android.com/guide/topics/ui/look-and-feel/themes.html (Styles and Themes)
