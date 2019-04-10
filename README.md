实验截图：
https://github.com/7419adf/ExtendActivity/blob/master/images/1.png
https://github.com/7419adf/ExtendActivity/blob/master/images/2.png
https://github.com/7419adf/ExtendActivity/blob/master/images/3.png
https://github.com/7419adf/ExtendActivity/blob/master/images/4.png
https://github.com/7419adf/ExtendActivity/blob/master/images/5.png
https://github.com/7419adf/ExtendActivity/blob/master/images/6.png
https://github.com/7419adf/ExtendActivity/blob/master/images/7.png
https://github.com/7419adf/ExtendActivity/blob/master/images/8.png
https://github.com/7419adf/ExtendActivity/blob/master/images/9.png
https://github.com/7419adf/ExtendActivity/blob/master/images/10.png
https://github.com/7419adf/ExtendActivity/blob/master/images/11.png

主要代码：
preferences.xml

<?xml version="1.0" encoding="utf-8"?>
<PreferenceScreen xmlns:android="http://schemas.android.com/apk/res/android" >

    <!--In-line preferences -->
    <com.example.ex4.MyPreferenceCategory
        android:title="In-line preferences">
        <CheckBoxPreference android:key="checkbox_0"
            android:title="Checkbox preference"
            android:summary="This is a checkbox" >
        </CheckBoxPreference>
    </com.example.ex4.MyPreferenceCategory>

    <!--Dialog-based preferences -->
    <com.example.ex4.MyPreferenceCategory
        android:title="Dialog-based preferences">
        <EditTextPreference
            android:key="package_name_preference"
            android:title="Edit text preference"
            android:summary="An example that uses an edit text dialog"
            android:dialogTitle="Enter your favorite animal" />
        <ListPreference
            android:title="List preference" android:key="gender"
            android:summary="An example that uses a list dialog"
            android:dialogTitle="Choose one"
            android:entryValues="@array/gender_value_list"
            android:entries="@array/gender_name_list"/>
    </com.example.ex4.MyPreferenceCategory>

    <!--Launch preferences -->
    <com.example.ex4.MyPreferenceCategory
        android:title="Launch preferences">
        <PreferenceScreen
            android:key="screen_preference"
          android:title="Screen preference"
          android:summary="Shows another screen of preferences">
            <CheckBoxPreference android:key="checkbox_0"
                android:title="Toggle preference"
                android:summary="Preference that is on the next screen but same hierarchy" >
            </CheckBoxPreference>
        </PreferenceScreen>

        <PreferenceScreen
            android:title="Intent preference"
            android:summary="Launches an Activity from an intent" >
        <intent
        android:action="android.intent.action.VIEW"
        android:data="http://www.qq.com"></intent>
        </PreferenceScreen>

    </com.example.ex4.MyPreferenceCategory>

    <!--Preference attributes -->
    <com.example.ex4.MyPreferenceCategory
        android:title="Preference attributes">
        <CheckBoxPreference
            android:key="parent_checkbox_preference"
            android:summary="This is visually parent"
            android:title="Parent checkbox preference" />
        <CheckBoxPreference
            android:dependency="parent_checkbox_preference"
            android:key="child_checkbox_preference"
            android:summary="This is visually a child"
            android:title="Child checkbox preference" />
    </com.example.ex4.MyPreferenceCategory>
</PreferenceScreen>
