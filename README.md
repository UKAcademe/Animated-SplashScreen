# Lottie Animated Splash Screen

**Lottie Animated Android Splash Screen**

<img src="animated splash screen.gif" align="left"
width="100"
    hspace="10" vspace="10">

Android Splash Screen is the first screen visible to the user when the application’s launched. Splash screen is one of the most vital screens in the application since it’s the user’s first experience with the application.

Splash screens are used to display some animations (typically of the application logo) and illustrations while some data for the next screens are fetched.

## What is Lottie and Why Lottie

A Lottie is a JSON-based animation file format that enables designers to ship animations on any platform as easily as shipping static assets. They are small files that work on any device and can scale up or down without pixelation.

Lottie is a mobile library for Android and iOS that parses Adobe After Effects animations exported as json with Bodymovin and renders them natively on mobile!
For the first time, designers can create and ship beautiful animations without an engineer painstakingly recreating it by hand. They say a picture is worth 1,000 words so here are 13,000:

- It is multi-platform. You can use Lottie files on iOS, Android, web and React Native without modification.
- It is resolution independent and scalable at run-time.
- Its file size is super small
- Allows for high quality animations on multiple platforms and resolutions by mixing vector and raster elements and applying transformations at run-time.
- Exposes animation elements and parameters to use as targeting elements to add interactivity and manipulate at run-time.


## Preview
<img src="/screenshots/sabith_pkc_mnr_github_repo_splash_screen_intro.webp">

## Implementation

Add lottie as a gradle dependency to our android project in android studio
For this, just go into your app level build.gradle file located at app/build.gradle and add the following lines in dependencies code block.

```groovy
implementation 'com.airbnb.android:lottie:3.5.0'
```
first open the layout file where you wish to add the animation, and add the below code under the root layout or wherever you want to add the animation.

```groovy
 <com.airbnb.lottie.LottieAnimationView
        android:id="@+id/animation_view"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:lottie_autoPlay="true"
        app:lottie_loop="true"
        app:lottie_rawRes="@raw/splashscreen" />
```
</br>
Now the timer is based on `postDelayed()` public method. This method will help us to queue a process to a certain period of time that we set for the method and app will perform that task after that time period.

First we set the time for the timer using a very simple `int SPLASH_TIME` variable
```groovy
int SPLASH_TIME = 3000; //This is 3 seconds
```

```groovy
new Handler().postDelayed(new Runnable() {
            @Override
            public void run() {
                //Do any action here. Now we are moving to next page
                Intent intent = new Intent(SplashScreenActivity.this, MainActivity.class);
                startActivity(intent);
                //This 'finish()' is for exiting the app when back button pressed from Home page which is MainActivity
                finish();
            }
        }, SPLASH_TIME);
```



<br><br>
<h4>Hey, while you're here why don't you think of following Us for awesome projects like this, ah? <a href="https://github.com/UKAcademe">Follow Us on Our Profile!</a></h4>

<br>


This app make it easy for you to implement Splash screen very easily into your Android App. 
