# weatherApp
Weather application built with JS/CSS/HTML with the use of OpenWeatherMap API
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

