# Sunshine App
This is the sunshine application for Udacity [Developing Android Apps: Android Fundamentals Course](https://www.udacity.com/course/developing-android-apps--ud853)

## Lesson 2: Connecting Sunshine to the cloud
Replacing the dummy data with real weather data by fetching data over OWM (Open Weather MAP) API.

##### Screenshot of app's current state:
![Screenshot of what I have done so far](http://s10.postimg.org/a2jq7894p/Lesson_2_Screenshot.png "Screenshot of what I have done so far")

Some issues you'll may face in this lesson:
* We can't perform network I/O on the main(UI) thread, you'll get error _android.os.NetworkOnMainThreadException_ . However it is possible to do epecially in earlier versions of Android, but it's a really danger idea so you'll have to override the default behavior, also prepare to the consequences e.g. the app'll come more unresponsive and extremly slow. 
[For more](http://stackoverflow.com/questions/6343166/android-os-networkonmainthreadexception)
* AsyncTask seems the right solution to get the job done (Not optimal though). AsyncTask in brief has 3 generic types (Params, Progress, Result) and 4 steps (onPreExecute, doInBackground, onProgressUpdate, onPostExecute)
[For more](http://developer.android.com/reference/android/os/AsyncTask.html)
* HTTP requests using _HttpURLConnection_ class and building URLs using Uri Class
* Parsing JSON format respons
