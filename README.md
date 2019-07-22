# Local-Weather

*Displays local weather instantly*

This is an app that allows you to display the current temperature at your location.


...

**Home Page**

<img src="/Weather.PNG" title="home page" alt="home page" width="500px">



---


## Table of Contents 

> Sections
- [Sample Code](#Sample_Code)
- [Installation](#installation)
- [Features](#features)
- [Contributing](#contributing)
- [Team](#team)
- [FAQ](#faq)
- [Support](#support)
- [License](#license)


---

## Sample Code

```javascript
// code
if(navigator.geolocation){
  navigator.geolocation.getCurrentPosition(function(position){ 
    var url= "https://fcc-weather-api.glitch.me/api/current?lat=" + position.coords.latitude + "&lon=" + position.coords.longitude;
      
    $.getJSON(url, function(data) {
      $("#temp").html(data.name+", "+data.sys.country+" <mu>"+ data.weather[0].description+"</mu>");
      $("#minutely").html(data.main.temp+"°C ");
      $("#minutely").html(data.main.temp*9/5+32+"°F")
      $("#two").addClass("mus");
      $("#one").removeClass("mus");        
          
      if(data.weather[0].description=="clouds"){
        $("#outside").css("background","red");   
      }
      else if(data.weather[0].description=="clear sky"){
        $("#outside").css("background","yellow");
      }
      else if(data.weather[0].description.indexOf("rain")!== -1){
        $("#outside").css("background","navy");   
      }
    });   
      
    document.getElementById('answer').innerHTML="latitude: "+ position.coords.latitude+"<br>longitude: "+position.coords.longitude;
  })
}

```

---

## Installation
## Features
## Usage (Optional)
## Documentation (Optional)
## Tests (Optional)
## Contributing
## Team

> Contributors/People

| [**seansangh**](https://github.com/seansangh) |
| :---: |
| [![seansangh](https://avatars0.githubusercontent.com/u/45724640?v=3&s=200)](https://github.com/seansangh)    |
| [`github.com/seansangh`](https://github.com/seansangh) | 

-  GitHub user profile

---

## FAQ

- **Have any *specific* questions?**
    - Use the information provided under *Support* for answers

---

## Support

Reach out to me at one of the following places!

- Twitter at [`@wwinvestingllc`](https://twitter.com/wwinvestingllc?lang=en)
- Github at [`seansangh`](https://github.com/seansangh)

---

## Donations (Optional)

- If you appreciate the code provided herein, feel free to donate to the author via [Paypal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=4VED5H2K8Z4TU&source=url).

[<img src="https://www.paypalobjects.com/webstatic/en_US/i/buttons/cc-badges-ppppcmcvdam.png" alt="Pay with PayPal, PayPal Credit or any major credit card" />](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=4VED5H2K8Z4TU&source=url)

---

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
- Copyright 2019 © <a>S.S.</a>
