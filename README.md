# weatherApp
Weather application built with JS/CSS/HTML with the use of OpenWeatherMap API. 
http://seyransweatherapp.online/ is my version of the applcaiton 

For the code to be fully functional, downlaod my code and get your own API key from OpenWeatherMap 

In WeatherApp.js, 

let weather = {

    apiKey: "YOUR API KEY GOES HERE",  <-------------------
    fetchWeather: function (city)
    {
        
            fetch
            (
                "https://api.openweathermap.org/data/2.5/weather?q="
                +city
                + "&units=metric&appid=" 
                + this.apiKey
            )
            .then((response) => response.json())
            .then((data) => this.dispplayWeather(data));
        
    },

Side Note, the background pictures are generated by the description of the weather. If it is cloudy, the background picture would display something related to clouds. 
If that is not of your liking, it can be changed here:
In WeatherApp.js
 document.body.style.backgroundImage = "url('https://source.unsplash.com/1920x1080/?"+ description +"')"
 The "+ description +" can be changed to anything. Plus the size of the displayed image can be conrolled as well. 
 
 Also the default location on app load is Toronto, but than can also be chanegd in WeatherApp.js
 weather.fetchWeather("Toronto"); 


fetch
            (
                "https://api.openweathermap.org/data/2.5/weather?q="
                +city
                + "&units=metric&appid=" 
                + this.apiKey
            )
            The URL can be changed as well based on the data you would like to display. All the options will be displayed on https://openweathermap.org/
Data can also be fetched from a downlaoded JSON or XML file. more info on that would be on the website as well. 
