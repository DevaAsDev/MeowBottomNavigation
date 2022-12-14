# MeowBottomNavigation

A simple & curved & material bottom navigation for Android. 

## Download  
build.gradle (project path)  
```groovy 
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}

```
build.gradle (module path)  
```groovy  
dependencies {  
 implementation 'com.github.DevaAsDev:MeowBottomNavigation:v1.0.1'
}  
```
## Usage  
Add Meow Bottom Navigation in xml  
```xml  
<com.darkappstore.meow.MeowBottomNavigation 
	 android:layout_width="match_parent"
	 android:layout_height="wrap_content" />
 ``` 
  
Add menu items in code.  
```java
bottomNavigation.add(new MeowBottomNavigation.Model(1, R.drawable.ic_home));  
bottomNavigation.add(new MeowBottomNavigation.Model(2, R.drawable.ic_explore));  
bottomNavigation.add(new MeowBottomNavigation.Model(3, R.drawable.ic_message));
```
Remember that icons must be vector drawable.   
Add vectorDrawables.useSupportLibrary = true to your build.gradle inside defaultConfig{ ... } 
## Customization  
```xml  
<com.darkappstore.meow.MeowBottomNavigation 
	android:layout_width="match_parent"
	android:layout_height="wrap_content"
	app:mbn_circleColor="#ffffff"
	app:mbn_backgroundBottomColor="#ffffff"
	app:mbn_countBackgroundColor="#ff6f00"
	app:mbn_countTextColor="#ffffff"
	app:mbn_countTypeface="fonts/SourceSansPro-Regular.ttf"
	app:mbn_defaultIconColor="#90a4ae"
	app:mbn_rippleColor="#2f424242"
	app:mbn_selectedIconColor="#3c415e"
	app:mbn_shadowColor="#1f212121"/>
```  
- You can change this properties in **Java** Realtime ⌚.   
  
## Listeners  
```java  
bottomNavigation.setOnClickMenuListener(new MeowBottomNavigation.ClickListener() {  
    @Override  
  public void onClickItem(MeowBottomNavigation.Model item) {  
        // your codes
  }  
});  
  
bottomNavigation.setOnShowListener(new MeowBottomNavigation.ShowListener() {  
    @Override  
  public void onShowItem(MeowBottomNavigation.Model item) {  
        // your codes
  }  
});  
  
bottomNavigation.setOnReselectListener(new MeowBottomNavigation.ReselectListener() {  
    @Override  
  public void onReselectItem(MeowBottomNavigation.Model item) {  
        // your codes
  }  
});
```
  
## Counter Badge  
Setting One Tab  
```java  
bottomNavigation.setCount(TAB_ID, STRING)  
```  
  
Clearing One Tab  
```java
bottomNavigation.clearCount(TAB_ID)  
```  
  
Clearing All Tabs  
```java
bottomNavigation.clearAllCounts(TAB_ID)  
```  
  
## Set Default Tab  
Use this function  
```java
bottomNavigation.show(TAB_ID)  
```
