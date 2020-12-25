# Animated Splash Screen

**Material Animated Android Splash Screen**

<img src="animated splash screen.gif" align="left"
width="100"
    hspace="10" vspace="10">

Android Splash Screen is the first screen visible to the user when the application’s launched. Splash screen is one of the most vital screens in the application since it’s the user’s first experience with the application.

Splash screens are used to display some animations (typically of the application logo) and illustrations while some data for the next screens are fetched.

## Preview
<img src="/screenshots/sabith_pkc_mnr_github_repo_splash_screen_intro.webp">

## Implementation
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
