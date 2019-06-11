

[原地址](https://github.com/koral--/android-gif-drawable)

### 配置

#### Gradle (Android Studio)

在APP-build.gradle文件中配置如下

dependencies {
    implementation 'pl.droidsonroids.gif:android-gif-drawable:1.2.17'
}


在project-build.gradle文件中配置如下

buildscript {
    repositories {
        mavenCentral()
    }
}
allprojects {
    repositories {
        mavenCentral()
    }
}




XML模式


<pl.droidsonroids.gif.GifImageView 
       android:layout_width="match_parent" 
       android:layout_height="match_parent" 
       android:src="@drawable/src_anim" 
       android:background="@drawable/bg_anim" 
/>  


代码模式


<pl.droidsonroids.gif.GifImageButton    
android:id="@+id/gifImageButton"    
android:layout_width="match_parent"    
android:layout_height="match_parent"   
 />
	
gifImageButton =(GifImageButton) findViewById(R.id.gifImageButton);
  gifImageButton.setImageResource(R.drawable.gif1);
  final MediaController mc = new MediaController(this);
  mc.setMediaPlayer( ( GifDrawable ) gifImageButton.getDrawable() );
  mc.setAnchorView( gifImageButton );
  gifImageButton.setOnClickListener( new View.OnClickListener(){    
        @Override    
        public void onClick ( View v )    {        
              mc.show();    
        }  
  }
 );



