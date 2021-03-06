# Multiplatform Preferences

**Work In Progress**

Use a single object : `Preferences` in your kotlin shared projects

Compatible with kotlin android and kotlin native for iphone

```kotlin
class MyPresenter {
    val preferences = Preferences()

    fun start(){
        preferences.getString("userName")?.let {
            view.displayUser(it)
        }
        
        val age = preferences.getInt("age", 18)
        view.displayUserAge(age)
    }
}
```


# Download

## common
```
implementation "com.gitub.florent37:multiplatform-preferences-common:0.0.3"
```

## ios

Uses inside the NSUserDefaults

```
implementation "com.gitub.florent37:multiplatform-preferences-ios:0.0.3"
```

## android

Uses inside the SharedPreferences

```
implementation "com.gitub.florent37:multiplatform-preferences-android:0.0.3"
```

## Methods

```kotlin
class Preferences(name: String? = null) {

    fun setInt(key: String, value: Int)
    fun getInt(key: String, defaultValue: Int): Int
    fun getInt(key: String): Int?

    fun setFloat(key: String, value: Float)
    fun getFloat(key: String, defaultValue: Float): Float
    fun getFloat(key: String): Float?

    fun setLong(key: String, value: Long)
    fun getLong(key: String, defaultValue: Long): Long
    fun getLong(key: String): Long?

    fun setString(key: String, value: String)
    fun getString(key: String, defaultValue: String): String
    fun getString(key: String): String?

    fun setBoolean(key: String, value: Boolean)
    fun getBoolean(key: String, defaultValue: Boolean): Boolean
    fun getBoolean(key: String): Boolean?

    fun remove(key: String)
    fun clear()

    fun hasKey(key: String): Boolean
}
```

## TODO

Add a sample
 
## License
        
    Copyright 2017 Russell Wolf
    
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
    
       http://www.apache.org/licenses/LICENSE-2.0
    
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
