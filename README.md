# cinema-app
This project is imitation of cinema web-site. All info about movie, movie-session, users, shopping carts and orders are stored in data base. Supports role based authorization (admin and user) with password encryption. Made using general REST principles. Created with usage of Tomcat, SQL and Spring Framework.
## Features
<ul>
  <li> Authentication and registration service</li>
  <li> Create and find movies</li>
  <li> Create, find and update movie sessions</li>
  <li> Create and find cinema halls</li>
  <li> Ability to create shopping cart that attached to specific user</li>
  <li> Ability to display list of all movies, movie sessions and cinema halls</li>
  <li> Ability to add tickets to shopping cart</li>
  <li> Support roles with different access to resources (USER and ADMIN)</li>
  <ul>
    <li>Admins can get customer info, add movies, add cinema halls, manage movie sessions</li>
    <li>Users can register, create shopping cart, add tickets to movie session, complete order</li>
  </ul>
</ul>

## Getting Started
<ol>
  <li> Clone this reprositority</li>
  <li> Create schema in your MySql Workbanch</li>
  <li> In <code>resources/db.properties</code> add correspondive data, instead of templates(<code>YOUR_DRIVER</code>, <code>YOUR_DATABASE_URL</code>, <code>YOUR_USERNAME_IN_DATABASE</code>, <code>YOUR_PASSWORD_FOR_DATABASE</code>), for correct SQL connection</li>
  <li> Establish connection to your SQL database (for example using <code>Database</code> option in <code>Intelij Ultimate</code>)</li>
  <li> Configure <code>Apache Tomcat</code></li>
  <li> Launch application</li>
  <li> Copmlete authentication for admin with data: login <code>admin@i.ua</code> and password <code>admin123</code> or for user: login <code>user@i.ua</code> and password <code>user123</code>. These users are already injected into our app.</li>
  <li> Send various requests via <code>Postman</code> service</li>
</ol>

## Structure
<ul>
  <li><code>config</code> - contains configuration for Spring (including application context and configuration to beans)</li>
  <li><code>controller</code> - contains endpoints that can resive and handle various HTTP requests</li>
  <ul>
    <li><code>AuthenticationController</code> - for authentication proccess</li>
    <li><code>CinemaHallController</code> - for adding cinema hall and get list of all cinema halls.</li>
    <li><code>CustomGlobalExceptionHandler</code> - for handle various exception with HTTP requests.</li>
    <li><code>MovieController</code> - for adding movie and get list of all movies.</li>
    <li><code>MovieSessionController</code> - for adding, deleting, updating and to find aviable movie sessions.</li>
    <li><code>OrderController</code> - for compleating user orders and get orders history.</li>
    <li><code>ShoppingCartController</code> - for creating shopping cart with movie session and geting shopping cart via users login.</li>
    <li><code>UserController</code> - for finding user via login.</li>
  </ul>
  <li><code>dao</code> - contains Data Access Object interfaces and their implementations for interaction with data base.</li>
  <li><code>dto</code> - contains Data Transfer Objects that helps to unify requests and responses in the controllers.</li>
  <li><code>exception</code> - contains custom DataProcessingException for handling exceptions in dao layer.</li>
  <li><code>lib</code> - contains classes and interfaces for email and password validations.</li>
  <li><code>model</code> - contains a models of the objects that the application works with.</li>
  <li><code>service</code> - contains services interface and implementations that are responsible for performing business logic and coordinating the interactions between the controllers and the DAO.</li>
</ul>

## Used technologies
<ul>
  <li>Java <code>v.17.0.5</code></li>
  <li>Maven <code>v.3.8.6</code></li>
  <li>MySql <code>v.8.0.24</code></li>
  <li>Tomcat <code>v.9.0.73</code></li>
  <li>Hibernate ORM <code>v.5.6.14</code></li>
  <li>Spring Framework <code>v.5.3.20</code></li>
  <li>Spring Security<code>v.5.6.10</code></li>
</ul>

## Authors
<a href="https://github.com/RandomEastEcho">Gleb Iaroshevych</a>
