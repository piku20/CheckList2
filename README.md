I need help in debugging my app
- needs to fix some deprecated functions.
- gradle needs to be fixed
- Could not find androidx.hilt:hilt-lifecycle-viewmodel:1.0.0.
Required by:
    project :app
Search in build.gradle files

Logcat:

FATAL EXCEPTION: main
  Process: com.example.checklist2, PID: 29570
  java.lang.RuntimeException: Unable to start activity ComponentInfo{com.example.checklist2/com.example.checklist2.ui.MainActivity}: java.lang.IllegalStateException: Hilt Activity must be attached to an @HiltAndroidApp Application. Did you forget to specify your Application's class name in your manifest's <application />'s android:name attribute?
    at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:2473)
    at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:2535)
    at android.app.ActivityThread.access$1100(ActivityThread.java:154)
    at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1396)
    at android.os.Handler.dispatchMessage(Handler.java:102)
    at android.os.Looper.loop(Looper.java:148)
    at android.app.ActivityThread.main(ActivityThread.java:5582)
    at java.lang.reflect.Method.invoke(Native Method)
    at com.android.internal.os.ZygoteInit$MethodAndArgsCaller.run(ZygoteInit.java:726)
    at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:616)
  Caused by: java.lang.IllegalStateException: Hilt Activity must be attached to an @HiltAndroidApp Application. Did you forget to specify your Application's class name in your manifest's <application />'s android:name attribute?
    at dagger.hilt.android.internal.managers.ActivityComponentManager.createComponent(ActivityComponentManager.java:76)
    at dagger.hilt.android.internal.managers.ActivityComponentManager.generatedComponent(ActivityComponentManager.java:66)
    at com.example.checklist2.ui.Hilt_MainActivity.generatedComponent(Hilt_MainActivity.java:47)
    at com.example.checklist2.ui.Hilt_MainActivity.inject(Hilt_MainActivity.java:69)
    at com.example.checklist2.ui.Hilt_MainActivity$1.onContextAvailable(Hilt_MainActivity.java:40)
    at androidx.activity.contextaware.ContextAwareHelper.dispatchOnContextAvailable(ContextAwareHelper.java:99)
    at androidx.activity.ComponentActivity.onCreate(ComponentActivity.java:362)
    at androidx.fragment.app.FragmentActivity.onCreate(FragmentActivity.java:216)
    at com.example.checklist2.ui.MainActivity.onCreate(MainActivity.kt:20)
    at android.app.Activity.performCreate(Activity.java:6321)
    at android.app.Instrumentation.callActivityOnCreate(Instrumentation.java:1108)
    at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:2426)
    at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:2535) 
    at android.app.ActivityThread.access$1100(ActivityThread.java:154) 
    at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1396) 
    at android.os.Handler.dispatchMessage(Handler.java:102) 
    at android.os.Looper.loop(Looper.java:148) 
    at android.app.ActivityThread.main(ActivityThread.java:5582) 
    at java.lang.reflect.Method.invoke(Native Method) 
    at com.android.internal.os.ZygoteInit$MethodAndArgsCaller.run(ZygoteInit.java:726) 
    at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:616) 
--------- beginning of main
