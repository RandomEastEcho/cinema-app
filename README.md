# cinema-app
This project is imitation of cinema web-site. All info about movie, movie-session, users, shopping carts and orders are stored in data base. Supports role based authorization (admin and user) with password encryption. Created with usage of Tomcat, SQL and Spring Framework.
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
  <li> In resources/db.properties add correct data for your SQL connection</li>
  <li> Establish connection to your SQL database</li>
  <li> Configure Apache Tomcat</li>
  <li> Launch application</li>
  <li> Copmlete authentication for admin with data: login <code>admin@i.ua</code> and password <code>admin123</code> or for user: login <code>user@i.ua</code> and password <code>user123</code>. These users are already injected into our app.</li>
  <li> Send various requests via Postman service</li>
</ol>

## Structure
<ul>
  <li>config - contains configuration for Spring (including application context and configuration to beans)</li>
  <li>controller - contains endpoints that can resive and handle various HTTP requests</li>
  <ul>
    <li>AuthenticationController - for authentication proccess</li>
    <li>CinemaHallController - for adding cinema hall and get list of all cinema halls.</li>
    <li>CustomGlobalExceptionHandler - for handle various exception with HTTP requests.</li>
    <li>MovieController - for adding movie and get list of all movies.</li>
    <li>MovieSessionController - for adding, deleting, updating and to find aviable movie sessions.</li>
    <li>OrderController - for compleating user orders and get orders history.</li>
    <li>ShoppingCartController - for creating shopping cart with movie session and geting shopping cart via users login.</li>
    <li>UserController - for finding user via login.</li>
  </ul>
  <li>dao - contains Data Access Object interfaces and their implementations for interaction with data base.</li>
  <li>dto - contains Data Transfer Objects that helps to unify requests and responses in the controllers.</li>
  <li>exception - contains custom DataProcessingException for handling exceptions in dao layer.</li>
  <li>lib - contains classes and interfaces for email and password validations.</li>
  <li>model - contains a models of the objects that the application works with.</li>
  <li>service - contains services interface and implementations that are responsible for performing business logic and coordinating the interactions between the controllers and the DAO.</li>
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
