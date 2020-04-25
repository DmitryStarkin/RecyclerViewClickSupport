**Recycler view click Library**

Adds the ability to click on recycle view

Source: http://www.littlerobots.nl/blog/Handle-Android-RecyclerView-Clicks/

Usage:

1 in project level build.gradle add:
```
repositories {
........
        maven { url "https://jitpack.io" }
   }
```

2 in module level build.gradle add:
```
dependencies {
...........
         implementation 'com.github.DmitryStarkin:RecyclerViewClickSupport:1.1.0'
   }
```

3 in code -


```Java
ItemClickSupport.addTo(mRecyclerView).setOnItemClickListener(new ItemClickSupport.OnItemClickListener() {
    @Override
    public void onItemClicked(RecyclerView recyclerView, int position, View v) {
        // do it
    }
});

ItemClickSupport.addTo(mRecyclerView).setOnItemClickListener(new ItemClickSupport.OnItemClickListener() {
    @Override
    public void onItemLongClicked(RecyclerView recyclerView, int position, View v) {
        // do it
    }
});
```