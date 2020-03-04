
# **Proposal:** [A website that recommends Spotify music based on current weather]

**Author(s):** Nguyễn Đức Anh, Hà Tuấn Dũng, Trần Minh Hiếu

**Group:** 12

**Last updated:** 4/1/2020

**Source at:** [Github's repository](https://github.com/sanebinary/mood-ify.net)

## **Project Description**
### **Problem diagnosis**
This is a proposal for the required project of the Software Engineering course. 

The popular audio streaming platform - *Spotify* - has a huge collections of tracks. However, a feature that is not currently implemented in this media service is to make playlist recommendations based on user current location's weather. In particular, such feature has been reported to exist through a website called *Climatune*. But currently, that web server is out of service.

Weather has a huge impact on which types of music people opt to listen to (https://www.accuweather.com/en/weather-news/accuweather-spotify-launch-climatune-to-produce-playlists-customized-to-weather/29477). For example, when it is rainy, most users will likely put on chillwave, downtempo with more acoustic song. In contrast, sunny days encourage users to listen to upbeat and high-energy songs. If provided with such a recommendation system, customer satisfaction when logging in to Spotify to listen to music will increase.

### **Proposed treatment**

To address this lack of functionality, the project aims to be a web application integrating with Spotify through the platform API. The user will be provided with a field to submit their current location when they first visit the website: [mood-ify.net](http://mood-ify.net). Through the usage of OpenWeatherMapAPI, when received location from user, weather data at that current location is returned. Taking the weather data as input, the algorithm will determine the most suitable music to play for that current location. 

> Benefit: Users will gain an even more personalized experience when using the web app and in turn creates more traffics for the Spotify platform. 

### **Targeted Customers**
- Millenials: Both working and stay at home adults are the main customers of Spotify, are likely to turn on music when they are at work.
- Teenagers and students: The majority of Spotify listeners are teenagers. While at home, they often put on music for background listening or when they study.

### **Application Features and Description**
- Requires users to sign in to their Spotify account via the web page to obtain their authorization code and then exchange it with the access token.
- Provided the user with a search bar to enter their location information.
- With the provided information, the application searches that location weather.
- Then, a playlist (or multiple playlists) compatible with the weather is returned to the user.

In order for the application to access end users' Spotify data and features along with fetching data from Spotify, follow the [Authorization Guide](https://developer.spotify.com/documentation/general/guides/authorization-guide/) of Spotify API. A form with the lable *cities* is then given to the users. After the users enter their location, a list of options that are closely related or similar to the location users enter (in case there are typos or there are multiple weather in a city due to it having many regions) will appear for them to choose. This is done with the help of OpenWeatherMapAPI. After that, the current weather of that place is displayed, together with a list of songs fitting to that weather. This list is curated through Spotify API's "audio features". Songs are given statistics such as *energy, instrumentalness, liveness, etc*... These statistics will be choosen and seeded based on the weather by our team. The location will be passed into the *locale* field. This will give playlists and songs that are related to the location.

### **Tools and resources**
HTML / CSS <br>
Javascript  <br>
Spotify API <br>
OpenWeatherMap API <br>
Spotify Account integration <br>
Codeigniter Framework <br>
Apache Server <br>
Hosting Web using Amazon Web Services <br>

### **Challenges**
The main product challenges will be to create an effective method for recommending playlists and making sure that the Spotify and OpenWeatherMap integration works properly. Some of the team members lack experiences in creating a software. 

### **Figma Prototype Link**
*https://www.figma.com/proto/hECCWsGyjfPBfcCyYVjfbq/Moodify.net?node-id=75%3A26&scaling=min-zoom*