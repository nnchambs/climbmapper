# climbmapper

An experiment built on Node.js using Mountain Project climbing route data and my climbing area data. 

You can see the app live at www.climbmapper.com

<h3>About</h3>
The goal of this app is to provide a better toolset for visualizing where someone wants to climb based on their MountainProject.com ToDos and Ticks.  While the initial interest was to leverage Mountain Project there is a general interest to break away from that connection to allow for other integrations and possibly the ability to add routes solely to ClimbMapper.  However, none of that is in the works right now. 

<h4>Current Features</h4>
* MountainProject.com user integration
* Tick and ToDo downloads from user profiles
* Mapping ToDo/Tick density by location (climbing area and partial crag level support)
* Charting grade breakdown, route type (trad, sport, boulder, alpine), and height (in # of pitches) on hover of locations
* Displaying a list of routes with preview images and supplemental info on click of a location with links to the respective route in MountainProject.com
* User profile management
* Data issue reports
* Ability to filter maps and charts by route types (trad, sport, boulder, alpine)
* Ability to search for climbing areas
* Ability to add new climbing areas or crags
* Ability to edit existing areas or crags
* Ability to use a time slider for visualizing user ticks across time
* Charting of user ticks by route type and type across time

<h3>The future</h3>

<b>NOTE:</b> After some interest from the community it was decided that this project is being ported from a Proof of Concept implementation to something we all can be more proud of.  The target stack will include:

** See the <a href="https://github.com/justinlewis/climbmapper/tree/reactify" >reactify</a> branch for the work in progress

Basic Front-end
* React
* WebPack/Babel
* Redux
* Bootstrap

Visualization Specific
* Leaflet.js
* D3.js

Backend
* Node 9.9.1
* PostgreSQL 9.6.1 (PostGIS 2 >)
* Python 2.7 (for some data processing)


<h3>Want to help out?</h3>
Awesome! 

<h4>1.  Dev Database Setup</h4>

<ol>
<li> Install PostgreSQL if you don't have it installed already.
<li> Create 'climbmapper' database with PostGIS installed.
<li> Create a new login user called 'app_user' who is a read only user.
<li> **There is another user used in the production environment which you probably don't need but conatact me if you do end up needing it.
<li> Populate the database by restoring climbmapper/project_setup/climbmapper.backup.
</ol>

<h4>2.  Dev Server Env Setup</h4>

<ol>
<li> Install Node.js if you don't have it installed already.
<li> Pull the repo to your local webserver root (typically /var/www on Linux using Apache HTTPD).
<li> CD into the climbmapper root directory.
<li> Type 'npm install' in your terminal when cd'd into the cimbmapper root directory.
<li> Type 'webpack' in your terminal when cd'd into the cimbmapper root directory.
<li> Type 'npm start' in your terminal when cd'd into the cimbmapper root directory.
<li> Access the site at http://localhost:8080/climbmapper
</ol>

<h4>3.  Making Changes</h4>
<ol>
<li> Make a branch
<li> When you make changes run webpack in your terminal to compile your changes (simply type webpack)
<li> Refresh your browser
<li> Use the 'issues' tab in GitHub for reporting or accepting tickets.
</ol>

<h4>General Needs</h4>
See the issues tab for more details.

<ol>
<li> Migration from a Proof of Concept to a real app (IN PROGRESS - see reactify branch)
<li> Better security authentication
<li> UI/UX makeover (especially with editing locations)
<li> Stronger domain models that help minimize the bridge to Mountain Project
<li> Connectors to other climbing websites (8a.nu, thecrag.com, etc...)
<li> Ability to add routes directly to ClimbMapper
</ol>

## Project Status
(WIP) - adds filter by route type functionality, webpack config, displays area name in left sidebar, adds Redux structure, and more! 

#### Example:

This project is currently in development. Users can filter tweets by username and keyword and see visual data representation. Functionality to sort by additional parameters is in progress.

## Project Screen Shot(s)

#### Example:   

[ PRETEND SCREEN SHOT IS HERE ]

[ PRETEND OTHER SCREEN SHOT IS HERE ]

## Installation and Setup Instructions

#### Example:  

Clone down this repository. You will need `node` and `npm` installed globally on your machine.  

To Visit App:

`localhost:8080/climbmapper`  

## Reflection

  - What was the context for this project? (ie: was this a side project? was this for Turing? was this for an experiment?)
   ⋅⋅⋅I met Justin at the ReactJS meetup here in Denver where he was looking for contributors to this little side project of his. As a user of Mountain Project and rock climber I thought this might be the perfect project to take on for my side project. Upon further inspection, it offered many, many challenges and both forced me to learn and dabble in unfamiliar technologies.
  - What did you set out to build?
   ⋅⋅⋅I originally had the goal of porting the entire front-end of Climbmapper from JS/Jquery to React/Redux. My favorite instructor, Taylor, took one look at the pre-existing code and gasped. He suggested that it was going to be a real challenge, but that I would (hopefully) learn a lot.
  - Why was this project challenging and therefore a really good learning experience?
    ⋅⋅⋅I inherited a metric sh!t ton of someone's half-finished code, which was a potent mix of React, jQuery, and VanillaJS. Some of it worked, some of it didn't, and some of it worked every once in a while.  Additionally, the development environment was loosely configured with a not-very-well-documented back-end Posgres/PosGis setup. This was an entirely different experience than starting an app from scratch and revealed itself to be a much different programming and problem solving process than what I'd previously experienced at Turing. I felt like I had stepped up into the
  - What were some unexpected obstacles?
    ⋅⋅⋅Setting up the develop environment
  
  - What tools did you use to implement this project?
      - This might seem obvious because you are IN this codebase, but to all other humans now is the time to talk about why you chose webpack instead of create react app, or D3, or vanilla JS instead of a framework etc. Brag about your choices and justify them here.  
    ⋅⋅⋅React/Redux, Node, PostgreSQL, pgAdmin (application), postGIS, Webpack, Jest, Babel, Enzyme, and React-Leaflet (this is what I worked with - the rest of the app uses many other technologies)

#### Additional Notes:  

I adopted the reactifying duties for this project and will one day become the king of Climbmapper's front-end development and approver of all PRs. This is a long-term open source project that I'm extremely excited to be contributing to, and I hope potential employers will see value in it. We're hoping to launch the fully reactify'd version this spring, just in time for climbing season to really get going. It feels awesome to be involved with both the open source software and climbing communities with this project, and I am PSYCHED to continue working on it. 
