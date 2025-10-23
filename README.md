# `TaGroup`



The TagGroup is a special layout with a set of tags. You can use it to tag people, books or anything you want.

Also you can contribute new idea to me.



# Usage

## Step 1

#### Gradle
```groovy
dependencies {
   compile 'me.gujun.android.taggroup:library:1.4@aar'
}
```

#### Maven
```xml
<dependency>
    <groupId>me.gujun.android.taggroup</groupId>
    <artifactId>library</artifactId>
    <version>1.4</version>
    <type>apklib</type>
</dependency>
```

## Step 2

Use it in your own code:
```xml
<me.gujun.android.taggroup.TagGroup
    android:id="@+id/tag_group"
    style="@style/TagGroup" />
```

```java
TagGroup mTagGroup = (TagGroup) findViewById(R.id.tag_group);
mTagGroup.setTags(new String[]{"Tag1", "Tag2", "Tag3"});
```
Use `setTags(...)` to set the initial tags in the group.

#### How to submit a new tag?

To "submit" a new tag as user press "Enter" or tap the blank area of the tag group, also you can "submit" a new tag via `submitTag()`.

**Note**: Google keyboard (a few soft keyboard not honour the key event) currently not supported "Enter" key to "submit" a new tag.

#### How to delete a tag?

To delete a tag as user press "Backspace" key or double-tap the tag which you want to delete.

#### How to detect tag click event?

Implement a callback interface: `TagGroup.OnTagClickListener`, and set the listener via `setOnTagClickListener()`.


# Build

run `./gradlew assembleDebug` (Mac/Linux)

or

run `gradlew.bat assembleDebug` (Windows)


