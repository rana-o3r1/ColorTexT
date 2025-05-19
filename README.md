
# Colorful Animated TextView

একটি কাস্টম Android TextView লাইব্রেরি যা টেক্সটে রঙিন গ্র্যাডিয়েন্ট এবং অ্যানিমেশন যুক্ত করে UI-কে করে তোলে আরও আকর্ষণীয় ও প্রাণবন্ত।

---

## Features

- কাস্টম গ্র্যাডিয়েন্ট রঙ যুক্ত করা যায়
- অ্যানিমেশন চালু/বন্ধ করা যায়
- নির্দিষ্ট শব্দ বা অক্ষর থেকে রঙ শুরু করা যায়
- XML ও Java উভয় দিক থেকেই সহজ ব্যবহারের সুবিধা

---

## Installation

### ✅ Step 1: Add `.aar` file to your project

`com.odri.txtview.v1.aar` ফাইলটি `app/libs` ফোল্ডারে কপি করুন।

### ✅ Step 2: Enable flatDir repository

`settings.gradle` বা `build.gradle (Project Level)` ফাইলে নিচের কোড যুক্ত করুন:

```gradle
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        google()
        mavenCentral()
        flatDir {
            dirs 'app/libs'
        }
    }
}
```

অথবা
```
flatDir {
            dirs 'app/libs'
        }

```


### ✅ Step 3: Add dependency in app-level build.gradle

```gradle
implementation(name: 'com.odri.txtview.v1', ext: 'aar')
```

---

## Usage

### XML Layout

```
<com.odri.txtview
    android:id="@+id/tv"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Hi I Am O3R1"
    android:textSize="24sp"
    android:textColor="#000000" />
```

### Java Integration

java

TxtView tv = findViewById(R.id.tv);

// গ্র্যাডিয়েন্ট রঙ সেট করুন
```
tv.kiColorDiba(new int[]{
    0xFFE91E63, 0xFF2196F3, 0xFF4CAF50
});
```

// অ্যানিমেশন চালু করুন
```
tv.danceDekhabo(true);
```

// নির্দিষ্ট শব্দ থেকে রঙ শুরু করুন (যেমন: দ্বিতীয় শব্দ থেকে)
```
tv.kotoWordPorDekhabo(2);
```

// নির্দিষ্ট অক্ষর থেকে রঙ শুরু করুন (যেমন: ৫ম অক্ষর থেকে)
```
tv.kotoCharPorDekhabo(5);
```

---

## Example Output

**টেক্সট:**
Hi I'am O3R1
**উপরে দেওয়া সেটিংস অনুযায়ী:**
- দ্বিতীয় শব্দ "আমাদের" থেকে রঙ শুরু হবে
- পঞ্চম অক্ষর থেকে রঙ পরিবর্তন শুরু হবে
- স্মুথ অ্যানিমেশন সহ রঙ পরিবর্তিত হবে

---

## License

এই লাইব্রেরিটি শুধুমাত্র শেখার উদ্দেশ্যে বানিয়েছি। তাই আপনার মতামত সসম্মানে...

---

## Contact

**Author:** [Rana-O3R1]  
**Email:** fakeodri@gmail.com  
**GitHub:** [https://github.com/rana-o3r1](https://github.com/rana-o3r1)
