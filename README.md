# Animation Auth Screen Design ✨

This project demonstrates a beautifully animated **Authentication Screen** built with **MotionLayout** in Android using Kotlin.

## 🚀 Features

- Login/Signup UI with smooth transitions
- Modern MotionLayout-based animations
- Clean and reusable component structure
- Fully responsive design
- Built using Jetpack libraries

## 🔗 App Link
[![Download](https://img.shields.io/badge/Download-APK-blue)](https://drive.google.com/file/d/1Fz71jNEgTyi1m1aMc5oiT7g9SKELFMZW/view?usp=drive_link)

## 📸 Screenshots

| Login | Animated Transition | Signup |
|-------|---------------------|--------|
| ![login](Screenshot/Screenshot_20250621_220838.jpg) | ![transition](Screenshot/video.gif) | ![signup](Screenshot/Screenshot_20250621_220847.jpg) |

> 💡 Add your screenshots in a `screenshots/` folder and link them here

## 🛠️ Tech Stack

- **Kotlin**
- **MotionLayout**
- **ConstraintLayout**
- **XML**
- 
## 📁 Project Structure 

<pre><code>app/</code> 
  ├── <code>res/</code>
  │ ├── <code>layout/</code> 
  │ │ └── <code>activity_main.xml</code> # Contains MotionLayout 
  │ ├── <code>drawable/</code> # Background shapes, icons 
  │ ├── <code>xml/</code> # MotionScene XML 
  │ └── <code>values/</code> # Strings, themes 
  ├── <code>java/com/example/authscreen/</code> 
  │ └── <code>MainActivity.kt</code> # Main screen logic </pre>

## 🎬 MotionScene XML Code
```xml
<?xml version="1.0" encoding="utf-8"?>
<MotionScene xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto">

    <ConstraintSet android:id="@+id/start">
        <Constraint
            android:id="@+id/view"
            android:layout_width="180dp"
            android:layout_height="180dp"
            android:scaleX="1.8"
            android:scaleY="1.8"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

        <Constraint
            android:id="@+id/view1"
            android:layout_width="150dp"
            android:layout_height="150dp"
            android:scaleX="1.8"
            android:scaleY="1.8"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

        <Constraint
            android:id="@+id/register_box"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:scaleX="0"
            android:scaleY="0"
            android:visibility="gone" />

        <Constraint
            android:id="@+id/register_btn"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            app:layout_constraintBottom_toBottomOf="parent" />

        <Constraint
            android:id="@+id/linearLayout1"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="12dp"
            android:alpha="1"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent" />
        <Constraint
            android:id="@+id/linearLayout2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginBottom="12dp"
            android:alpha="0"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent" />
    </ConstraintSet>

    <ConstraintSet android:id="@+id/end">
        <Constraint
            android:id="@+id/view"
            android:layout_width="140dp"
            android:layout_height="140dp"
            android:elevation="2dp"
            android:scaleX="1.8"
            android:scaleY="1.8"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

        <Constraint
            android:id="@+id/view1"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:scaleX="2"
            android:scaleY="2"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

        <Constraint
            android:id="@+id/textView"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:alpha="0" />

        <Constraint
            android:id="@+id/textView1"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:alpha="1" />

        <Constraint
            android:id="@+id/login_box"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:scaleX="0"
            android:scaleY="0"
            android:visibility="gone" />

        <Constraint
            android:id="@+id/linearLayout1"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="12dp"
            android:alpha="0"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent" />
        <Constraint
            android:id="@+id/linearLayout2"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="12dp"
            android:alpha="1"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent" />
    </ConstraintSet>

    <Transition
        app:constraintSetEnd="@+id/end"
        app:constraintSetStart="@+id/start"
        app:duration="500"
        app:motionInterpolator="linear">

        <OnClick
            app:clickAction="toggle"
            app:targetId="@+id/register_btn" />

    </Transition>

    <Transition
        app:constraintSetEnd="@+id/start"
        app:constraintSetStart="@+id/end"
        app:duration="500"
        app:motionInterpolator="linear">
        <OnClick
            app:clickAction="toggle"
            app:targetId="@+id/login_btn" />
    </Transition>
</MotionScene>
```

## 🎨 Colors Used

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
    <color name="primary">#F77B30</color>
    <color name="secondary">#1B635E</color>
</resources>
```

## 👨‍💻 About Me

I'm Ataussamad Ansari, a passionate Android Developer with experience in building apps using Kotlin, Jetpack Compose, Firebase, and MotionLayout. I love crafting clean UI and exploring animation frameworks in Android. Always learning and building!

## 📫 Contact Me

- 📧 Email: ataussamadansari@gmail.com
- 🔗 LinkedIn: [linkedin.com/in/ataussamadansari](https://www.linkedin.com/in/ataussamadansari)
- 🧑‍💻 GitHub: [@ataussamadansari](https://github.com/ataussamadansari)
- 📄 Resume: [Ataussamad Ansari Resume](https://drive.google.com/file/d/1Ob5hChthWgXRn82XSfEbys-_ZunM4k48/view?usp=drive_link)


