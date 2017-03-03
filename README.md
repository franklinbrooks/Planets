# A New Yorker's Guide to Scale in the Solar System

While I was researching my first project ('Save Our Satellites' game) at GA, I first thought of the incredible displays at The Rose Center for Earth and Space at the American Museum of Natural History. Also, I came across a number of really cool JavaScript/CSS models of our solar system and other stellar imagery.  All of these are informative and fun, giving a good sense of the names and order of the planets, and their orbital paths and relative speeds.

BUT, there was one thing with which they all struggle: it's hard to convey a sense of the scale of the solar system.

I wondered how I could relate the relative sizes and distances of the planets in our solar system to something I could better understand: the geography of my home, New York City.

This web project is a thought experiment that seeks to let the user appreciate the how small the Big Apple is on a cosmic scale. 

### Screenshot:
![Screenshot](http://franklinchristopherbrooks.com/images/PlanetsScreenShot.png)

#### [Link to Live Site](https://desolate-everglades-65827.herokuapp.com/)  
#### [Link to Repo](https://github.com/franklinbrooks/Planets)  
#### [Link to ZenHub](https://github.com/franklinbrooks/Planets#boards?repos=82419944)  

## Getting Started

This project includes a package.JSON file which provides details for the above dependencies and others. These files are imported into the node_modules folder by Node Package Manager. Font-Awesome and Materialize-CSS are linked via CDN.

Download or clone repo.
Run npm install in terminal.
Run npm start from terminal.

## Code Example: Rendering an A-Frame
When the user explores relative size and position of planets versus the New York City street grid, a Google Maps Street View is rendered in an i-frame via API call.  Over this, I z-indez an A-Frame of a sphere scaled to the size of its orbit over Manhattan. 

```javascript

    <div style="position:relative;height:400px;width:80%;margin:0 auto">

      <iframe width="100%" height="400"
        src="https://www.google.com/maps/embed/v1/streetview?key=<%= process.env.GOOGLE_KEY %>&location=40.722472,-73.999280&heading=45&pitch=5&fov=100">
      </iframe>

      <div style="width:900px;height:400px;z-index:2;position:absolute;top:0px">
        <a-scene embedded style="left:250;height:300;width:400">
          <a-sphere position="0 1.8 -1" radius=".03" color="#e58c5d"></a-sphere>
        </a-scene>
      </div>

    </div>

    <div class="container section no-pad-bot">
      <p style="text-align:center">Jupiter is the large planet, 46cm in size, above Broadway in SoHo. (Use arrow keys / mouse to pan / zoom)</p>
    </div>


````

## Built With

* [Node](https://nodejs.org/) - The backend web framework used
* [NPM](https://www.npmjs.com/) - Dependency Management
* [Express](expressjs.com) - The frontend web framework used

## Minimum Viable Product
- Use PostgreSQL & Express to build full stack web app
- Layout and style your front-end, so that is Responsive and uses a CSS Framework
- Deploy your application online so it's publicly accessible

### Possible Future Improvements
In no particular order, I would like to add:
  1. Microinteractions to improve UX
  1. Quiz at the end of the tour
  1. API call to NASA or other observatory db reporting current location of planets overhead
  

## Author

* **Franklin Brooks** - *Initial work* - [Franklin Christopher Brooks](https://github.com/franklinbrooks)

## Acknowledgments

* This project was developed as part of the Web Development Immersive program at General Assembly in NYC, February 2017. My mentors for this build were Ariana and Vince. My thanks to them!

* Inspiration
