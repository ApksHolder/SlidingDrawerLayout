# SlidingDrawerLayout [![](https://jitpack.io/v/freeze-frame/SlidingDrawerLayout.svg)](https://jitpack.io/#freeze-frame/SlidingDrawerLayout)

A layout derived from ViewGroup, not any other indirect container, such as FrameLayout, SlidingPaneLayout or DrawerLayout.

<div align="center">
    <img src="https://github.com/ApksHolder/SlidingDrawerLayout/blob/master/SlidingDrawerLayout.gif" width="300">
</div>


## Layout File Sample:
```xml
<com.liuzhenlin.sliding_drawer_layout.SlidingDrawerLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/sliding_drawer_layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <!--
      ~ Use a ViewStub to lazily inflate the drawer View for the purpose of avoiding unnecessary
      ~ performance overhead before that View shown to the user.
      -->
    <ViewStub
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout="@layout/image_start_drawer"
        android:layout_gravity="start" />
    <!-- layout_gravity must be explicitly set, which will determine the drawer's placement -->

    <ViewStub
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout="@layout/image_end_drawer"
        android:layout_gravity="end" />

    <!-- below is your content view -->
    <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <android.support.v7.widget.Toolbar
            android:id="@+id/toolbar"
            android:layout_width="match_parent"
            android:layout_height="?android:attr/actionBarSize"
            app:contentInsetStartWithNavigation="0dp"
            android:background="@color/colorPrimary"
            app:title="@string/app_name"
            app:titleTextAppearance="@style/ActionBarTitleAppearance" />

        <ListView
            android:id="@+id/listview"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:layout_below="@id/toolbar"
            android:scrollbars="vertical" />

        <View
            android:layout_width="match_parent"
            android:layout_height="4dp"
            android:layout_below="@id/toolbar"
            android:background="@drawable/shadow_actionbar" />
    </RelativeLayout>
</com.liuzhenlin.sliding_drawer_layout.SlidingDrawerLayout>
```


## Usages:
### Public Methods:
#### Getters & Setters:
<img src="https://github.com/ApksHolder/SlidingDrawerLayout/blob/master/getters%20%26%20setters.png" width="300">

#### Open/Close a Drawer:
<img src="https://github.com/ApksHolder/SlidingDrawerLayout/blob/master/open:close%20drawer.png" width="300">

#### Listener Related:
<img src="https://github.com/ApksHolder/SlidingDrawerLayout/blob/master/listener%20releated.png" width="300">

### Attributes:
```xml
app:widthPercent_leftDrawer="unspecified"
app:widthPercent_rightDrawer="unspecified"
app:widthPercent_startDrawer="0.8"
app:widthPercent_endDrawer="0.9"
app:enabled_leftDrawer="true"
app:enabled_rightDrawer="true"
app:enabled_startDrawer="true"
app:enabled_endDrawer="true"
app:duration="256"
app:contentSensitiveEdgeSize="50dp"
app:contentFadeColor="@color/colorAccent"
```


## Pull Requests
I will gladly accept pull requests for bug fixes and feature enhancements but please do them
in the developers branch.


## License
Copyright 2018 刘振林

Licensed under the Apache License, Version 2.0 (the "License"); <br>
you may not use this file except in compliance with the License. You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License
is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express
or implied. See the License for the specific language governing permissions and limitations
under the License.
