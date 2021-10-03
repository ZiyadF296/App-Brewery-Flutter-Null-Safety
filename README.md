# AppBrewery Flutter : Null Safety Guide

## Read Before Starting

- **DISCLAIMER : This repository is not an official outcome of [London AppBrewery Team](https://github.com/londonappbrewery)**

- This repository is made to help new students get through [**AppBrewery Flutter Course**](https://www.udemy.com/course/flutter-bootcamp-with-dart/)

- This repository contains notes for **only coding (project) sections** and explains what has changed and what's the difference.

- If something is not covered here, **start a dicussion**, not an issue! I will try to add it then.

- Use latest verions of required **`packages`** and **`plugins`**, find them on [**pub.dev**](https://pub.dev/)

## Index

#### 1. [Terminology](#terminology)

#### 2. [Common issues and fixes](#common-issues-and-fixes)

  1. #### [Using old Flutter SDK?](#1-using-old-flutter-sdk)
  
  2. #### [Android license status unknown](#2-android-license-status-unknown)
  
  3. #### [Option to create a new package is missing](#3-option-to-create-a-new-package-is-missing)

#### 3. [Resources](#resources)

#### 4. [Code to Update](#code-to-update)

  1. #### [Section 3 : I Am Rich App](#section-3--i-am-rich-app-lesson-28)
  
  2. #### [Section 7 : Dicee App](#section-7--dicee-app-lesson-53)
  
  3. #### [Section 9 : Xylophone App](#section-9--xylophone-app-lessons-76-77)
  
  4. #### [Section 10 : Quizzler App](#section-10--quizzler-app-lesson-94)
  
  5. #### [Section 12 : BMI Calculator App](#section-12--bmi-calculator-app-lessons-125-126-128-129)
  
  6. #### [Section 13 : Clima App](#section-13--clima-app-lesson-140)

## Terminology

##### [Go back to Index](#index)

### 1. Deprecated

- You will often come across **`deprecated`** stuff, where it says **This is `deprecated`**. This means two things, first, Flutter team will no longer maintain this code, secondly, it's **not recommended** to use it anymore since it's not maintained any more. You should use alternatives that usually you will find in the deprecation message.

### 2. Null Safety

- **Null safety is not your enemy!** It's there you help you so you to avoid common bugs and mistakes. This can help make your app crash less and act upon your intended behavior.

- Dart has **`sound null safety`**. Basically, if you're writing any code that dart thinks might end up being **`null`**, it will warn you.

- Read more : [**Sound Null Safety**](https://dart.dev/null-safety), [**Understanding Null Safety**](https://dart.dev/null-safety/understanding-null-safety), [**Null Safety in Flutter**](https://flutter.dev/docs/null-safety)

## Common Issues and Fixes

##### [Go back to Index](#index)

#### 1. Using old Flutter SDK?

- Use latest **`Flutter SDK`**, currently I am using **`2.2`** in **`stable channel`**

  - To upgrade your Flutter version to latest, run **`flutter upgrade`** in your **`Terminal / Command Prompt`**.

#### 2. **`Android license status unknown`**

- There are couple of things that can cause this issue to popup, these are the common solutions:

  ##### Solution 1. Accept the new ones!

  - Just run **`flutter doctor --android-licenses`**

  - Normally, this fixes your Android licenses issue.

  ##### Solution 2. Install / Update SDK Command Line Tools

  - Open settings panel by,
  
    - **`File > Settings`** (**Windows and Linux**)

    - **`Android Studio > Preferences`** (**Mac**)

  - Then navigate to,
  
    **`Appearance & Behavior > System Settings > Android SDK`**

  - Select the **`SDK Tools` Tab**

  - Select **`Android SDK Command Line Tools`** and click **`Apply`**

  - A dialog will pop up and ask you if you want to install these.
  
    Click Yes/OK and let these tools to install, after that, close **`Android Studio`** and **`restart`** it.
  
    <img src="https://github.com/DetainedDeveloper/App-Brewery-Flutter-Null-Safety/blob/master/images/guide/android_studio_sdk_tools.png?raw=true" width=506 height=378>

#### 3. Option to create a new **`package`** is missing

  - Sometimes with newer versions of Android Studio or any Android related tools, the Android license tends to be **`unknown`**. This is because the new tool is not yet supported by Flutter. For that reason, it's recommended not to upgrade Android tools until Flutter officially supports it.

  - Note that **`New > Package`** and **`New > Directory (Folder)`** options have now been merged.

  - So, to create a new **`package`** or just a **`folder`**, simply use **`New > Directory`** option.

## Resources

##### [Go back to Index](#index)

#### 1. Try out Null Safety on [DartPad](https://dartpad.dev/?null_safety=true)

#### 2. Read Updated [Flutter Docs](https://flutter.dev/docs)

#### 3. Watch and Follow [Flutter's Official YouTube Channel](https://www.youtube.com/channel/UCwXdFgeE9KYzlDdR7TG9cMw)
- To learn more about Null Safety and staying updated in general.

# Code to Update

## Section 3 : I Am Rich App (Lesson 28)

##### [Go back to Index](#index)

- You right clicked on **`res`** folder but didn't find **`Image Asset`**? Don't worry Follow these steps,

  - Right click on **`android`** folder and a pop-up menu wiil open up.
  
    From that, select **`Flutter > Open Android Module in Android Studio`**

    **If this doesn't work for you then follow these steps**,
  
  **1.** Close current project by pressing **`File > Close Project`**
  
  **2.** Now you will have the first screen of Android Studio.
  
  **3.** Press **`Open an Existing Project`**, then **`Open File or Project`** dialog will open.
  
  **4.** Here, navigate to your **Flutter project** in which, you want to add **`Image Asset`**
  
  **5.** Expand that and you will find **`android`** folder. Select that and press **`OK`**
  
- **Both ways** should open **Android Part** of your **Flutter Project** in **`Android Studio`**.
  
- Now, at bottom right, if it's running any **`gradle`** processes, let it run. Don't interrupt! However, if you close it, it'll rebuild everything when you reopen it. So, no need to worry!
  
- After that long build process completes, you can find  **`Image Asset`** option when you click on **`res`** folder, **Yay**!
  
- Add assets and again, **`File > Close Project`**, **`Open an Existing Project`** and this time, select your **Flutter Project** and continue!

## Section 7 : Dicee App (Lesson 53)

##### [Go back to Index](#index)

- **`FlatButton`** is **`deprecated`**, so use **`TextButton`** instead.

## Section 9 : Xylophone App (Lessons 76, 77)

##### [Go back to Index](#index)

- Getting a very descriptive error when trying to use **`audioplayers` plugin**?
  
  - All you need to do is open **`android > build.gradle` (Project Level `gradle` file)**
  
  - Inside **`buildscript {}`**, you'll find **`ext.kotlin_version` (Line 2 in file unless modified)**
  
  - Replace whatever version it is with [**Latest Stable Kotlin Version**](https://kotlinlang.org/docs/releases.html#release-details)
  
  - As of **July 23, 2021** it is, **`ext.kotlin_version = '1.5.21'`**
  
  - Now, **re-install** the app. If it's already running, press **Stop**, run **`flutter clean`** in the terminal then press **Run (Play)** once again. This simply erases your app and rebuilds it to avoid any old build caches of the previous version.

- **`FlatButton`** is **`deprecated`**, so use **`TextButton`** instead.

  - **HOWEVER**, for this module, you won't be adding any **`child`** to **`FlatButton`**, this will throw an error because **`child`** is a **`required`** property.
  
  - So, for **Xylopone Keys**, use **`MaterialButton`** instead of **`FlatButton`**

## Section 10 : Quizzler App (Lesson 94)

##### [Go back to Index](#index)

- Due to **`null safety`**, all variables in a class must have a value assigned, when created. If not, they must be declared **`Nullable`** intentionally. This rule also applies to **`Stateless`** and **`Stateful`** widgets. On top of that, in classes extending **`StatelessWidget`**, all variables must be declared **`final`**

- So, make your **`Question`** class like this,
  ```dart
  class Question {
    String questionText;
    bool questionAnswer;

    Question(this.questionText, this.questionAnswer);

    // If you want to make your class required named parameters instead of positioned arguments, use this syntax:
    Question({
        required this.questionText, 
        required this.questionAnswer,
    });
  }
  ```

    - **`@required`** is replaced by just **`required` (Without @ sign)**
    
    - Here, the **Keyword `this`** points to **current context**, which happens to be **`Question`** class.

- **`FlatButton`** is **`deprecated`**, so use **`TextButton`** instead.

## Section 12 : BMI Calculator App (Lessons 125, 126, 128, 129)

##### [Go back to Index](#index)

- **`@required`** is replaced by just **`required` (Without @ sign)**

- So, while making **`ReusableCard`**, lesson shows you can skip using **`cardChild`** property, but that isn't possible, due to **`null safety`**
  
  - This part is tricky, because now you can't have null arguments anymore.
  
  - So, you must have to intentionally make it **`Nullable`**, by adding **`?`** to it, like this,
    ```dart
    class ReusableCard extends StatelessWidget {
      final Color colour;
      final Widget? cardChild;

      const ReusableCard({Key? key, required this.colour, this.cardChild}): super(key: key);

      @override
      Widget build(BuildContext context) {
        return Container(
          decoration: BoxDecoration(
            color: colour, 
          ),
          child: child,
        );
      }
    }
    ```
    
  - Use it like **`ReusableCard(color: Colors.amber)`** and your app won't crash.

- But, it's not same for **`IconContent`**, **`Icon`** can have **`null`** value, but **`Text`** can't!
    ```dart
    class IconContent extends StatelessWidget {
      final IconData? icon;
      final String? label;

      const IconContent({Key? key, this.icon, this.label}): super(key: key);

      @override
      Widget build(BuildContext context) {
        return Column(
          children: [
            Icon(icon),
            Text(label ?? ''),
          ],
        );
      }
    }
    ```
  
  - So using **`??`** operator, you need to check if label is **`null`** or not, if it is, then you must provide a **`String`** value to it. Here, I provided an empty String.
    
    - To clarify, **`??`** basically tells Dart that if the **`label`** value is **`null`** then use the value on the right side value after the **`??`** operator.

  - Even if you don't pass any arguments like **`IconContent()`**, your app won't crash.

- According to **Lesson 129**, **`ReusableCard`** now has a parameter named **`onPress`**, to get it working, use this,
  ```dart
  class ReusableCard extends StatelessWidget {
    final Color colour;
    final Widget? cardChild;
    final void Function()? onPress;

    const ReusableCard({Key? key, required this.colour, this.cardChild, this.onPress}): super(key: key);

    @override
    Widget build(BuildContext context) {
      return GestureDetector(
        onTap: onPress,
        child: Container(
          decoration: BoxDecoration(
            color: colour, 
          ),
          child: child,
        ),
      );
    }
  }
  ```
  - Because **`GestureDetector`**'s **`onTap`** propery wants **`void Function()?`** as argument.

- In **Lesson 128**, **`_InputPageState`** has a new variable which haven't been initialized. As I already told you, you must initialize them or make them **`Nullable`**.
  ```dart
  class _InputPageState extends State<InputPage> {
    Gender? selectedGender;
  }
  ```

  - Here, making it **`Nullable`** will do the job. Rest of the code will work perfectly fine.

## Section 13 : Clima App (Lesson 140)

##### [Go back to Index](#index)

- When running this app on a **Physical Device**, you will need **Internet Permission** because the app is sending an external network request. For example, you are requesting data from an [API](https://en.wikipedia.org/wiki/API) like [OpenWeatherMap](https://openweathermap.org/api). This is an external source outside your app. Any external source requested will fail unless you follow the steps below:

  - **`Android` :** For this, open **`AndroidManifest.xml`** by navigating to,
    
    **`android > app > src > main > AndroidManifest.xml`**
    
    and add the following line,

    ```xml
    <uses-permission android:name="android.permission.INTERNET"/>
    ```

    **Keep the existing location permissions** and add this above/below them.
    Add it under **`manifest`** tag, like this,

    ```xml
    <manifest xmlns:android="http://schemas.android.com/apk/res/android"
      package="detaineddeveloper.example.clima">

      <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
      <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>

      <!--Keep the existing location permisions above (whichever you have added previously)-->
      <uses-permission android:name="android.permission.INTERNET"/>
    
      <application
        android:label="clima"
        android:icon="@mipmap/ic_launcher">
        .
        .
        .
      </application>
    </manifest>
    ```

  - **`iOS` :** I don't know, I don't have an **`iOS`** device!
