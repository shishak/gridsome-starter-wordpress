<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link to="/">Gridsome</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about">About</g-link>
      </nav>
    </header>
    <slot/>
  </div>
</template>

<style>

img {
  max-width: 100%;
}
nav[role="navigation"] {
  text-align: center;
}
nav[role="navigation"] a {
  display: inline-block;
  margin: 1.0em 0.75em 2.0em;
}
.layout {
  max-width: 1200px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}
.header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}
.nav__link {
  margin-left: 20px;
}
.post-list {
  list-style: none;
  padding-left: 0;
}
.post-list li {
  padding: 1em 0;
}



*,
*:before,
*:after {
  box-sizing: inherit;
}
html {
  box-sizing: border-box;
  color: #303030;
}
body {
  font-family: Georgia,Cambria,"Times New Roman",Times,serif;
  background: #fafafa;
  padding: 0;
  margin: 0;
}
a {
  text-decoration: none;
  color: #303030;
}




h1, h2 {
  margin-left: 0;
  margin-bottom: 0;
  margin-right: 0;
  margin-top: 8px;
  letter-spacing: -0.5px;
}

h1 {
  font-size: 48px;
    font-weight: 500;
    line-height: 48px;
    margin-top: 50px;
}

h2 {
  font-size: 1.5rem;
  font-weight: 400;
}






.grid-item {
  display: flex;
  flex-direction: column;
  width: 100%;
  margin-bottom: 1.5rem;
  background: #fff;
  border-radius: 6px;
  overflow: hidden;
  border: 1px solid #dcdcdc;
 }
.grid-item:hover {
  cursor: pointer;
}
.grid-item img {
  width: 100%;
  max-height: 220px;
  object-fit: cover;
}


.grid {
    display: flex;
    flex-wrap: wrap;
    margin: 0 -15px;
}
.box {
    width: 33.33%;
    display: flex;
    padding: 0 10px;
}
  
.box:nth-of-type(4), .box:nth-of-type(5), .box:nth-of-type(9), .box:nth-of-type(10), .box:nth-of-type(14), .box:nth-of-type(15), .box:nth-of-type(19), .box:nth-of-type(20), .box:nth-of-type(24), .box:nth-of-type(25), .box:nth-of-type(29), .box:nth-of-type(30) {
   width: 50%; 
}
@media all and (max-width: 800px) {
.box {
   width: 100%;
}
.box:nth-of-type(4), .box:nth-of-type(5), .box:nth-of-type(9), .box:nth-of-type(10), .box:nth-of-type(14), .box:nth-of-type(15), .box:nth-of-type(19), .box:nth-of-type(20), .box:nth-of-type(24), .box:nth-of-type(25), .box:nth-of-type(29), .box:nth-of-type(30) {
   width: 100%;
}
.grid-item {
    margin-bottom: 0.5rem;
}
}
  
  
  

.box:nth-of-type(2) h2, .box:nth-of-type(4) h2, .box:nth-of-type(8) h2, .box:nth-of-type(9) h2, .box:nth-of-type(13) h2, .box:nth-of-type(14) h2, .box:nth-of-type(17) h2, .box:nth-of-type(22) h2 {
   font-family: Roboto,Helvetica,Arial,sans-serif;
    line-height: 28px;
    font-weight: 500;
}
@media only screen and (min-width: 64em) {
.box:nth-of-type(4) img, .box:nth-of-type(5) img {
    
    max-height: 300px;
	
}
 .box:nth-of-type(4) .gradient, .box:nth-of-type(5) .gradient {
    background-image: linear-gradient(180deg,transparent,rgba(0, 0, 0, 0.24));
    height: 280px;
    margin-top: -250px;
}
	
 .box:nth-of-type(4) h2, .box:nth-of-type(5) h2 {
    color: #fff;
    font-size: 25px;
    position: absolute;
    margin-top: -130px;
    margin-left: 50px;
    margin-right: 50px;
    width: 33%;
}

}
.box:nth-of-type(1) img, .box:nth-of-type(2) img, .box:nth-of-type(3) img {
   display: none;
}
.grid-item div {
   font-size: 0;
}

.grid-item div p {
  display: none;
}

.grid-item div p:nth-of-type(1) {
   display: block;
}

</style>
