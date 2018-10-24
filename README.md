# Liquid-amount
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
  package="com.taradov.alarmme"
  android:versionCode="15"
  android:versionName="0.1.15"
  android:installLocation="internalOnly">

  <uses-sdk
    android:minSdkVersion="11"
    android:targetSdkVersion="28"
    android:maxSdkVersion="28" />

  <uses-permission
    android:name="android.permission.VIBRATE" />

  <uses-permission
    android:name="android.permission.RECEIVE_BOOT_COMPLETED" /> 

  <application
    android:label="@string/app_name"
    android:icon="@drawable/ic_launcher">

    <activity
      android:name=".AlarmMe"
      android:label="@string/app_name">

      <intent-filter>
        <action android:name="android.intent.action.MAIN" />
        <category android:name="android.intent.category.LAUNCHER" />
      </intent-filter>
    </activity>

    <activity
      android:name=".EditAlarm"
      android:label="Edit alarm" />

    <activity
      android:name=".AlarmNotification"
      android:label="Alarm notification" />

    <activity
      android:name=".Preferences"
      android:label="Preferences" />

    <activity
      android:name=".About"
      android:label="About" />

    <receiver
      android:name=".AlarmReceiver"
      android:process=":remote" />

    <receiver android:name=".BootCompletedReceiver">
      <intent-filter>
        <action android:name="android.intent.action.BOOT_COMPLETED" />
        <category android:name="android.intent.category.DEFAULT" />
      </intent-filter>
    </receiver>

  </application>
</manifest>
