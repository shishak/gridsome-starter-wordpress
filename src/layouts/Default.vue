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
  <footer>
  <div class="footer-container">
    <section class="footer-main">
      <article>
       <h3>Learn</h3>
        <ul>
          <li><a href="#!">Guides</a></li>
          <li><a href="#!">Reference</a></li>
          <li><a href="#!">Samples</a></li>
          <li><a href="#!">Libraries</a></li>
          <li><a href="#!">Github</a></li>
        </ul>
      </article>
      <article>
        <h3>Learn</h3>
        <ul>
          <li><a href="#!">Guides</a></li>
          <li><a href="#!">Reference</a></li>
          <li><a href="#!">Samples</a></li>
          <li><a href="#!">Libraries</a></li>
          <li><a href="#!">Github</a></li>
        </ul>
      </article>
      <article>
        <h3>Stay connected</h3>
        <ul>
          <li><a href="#!">Blog</a></li>
          <li><a href="#!">Firebase Summit</a></li>
          <li><a href="#!">Facebook</a></li>
          <li><a href="#!">Twitter</a></li>
          <li><a href="#!">YouTube</a></li>
        </ul>
      </article>
      <article>
        <h3>Support</h3>
        <ul>
          <li><a href="#!">Contact support</a></li>
          <li><a href="#!">Stack Overflow</a></li>
          <li><a href="#!">Google Group</a></li>
          <li><a href="#!">Release notes</a></li>
          <li><a href="#!">FAQs</a></li>
          <li><a href="#!">Legacy documentation</a></li>
        </ul>
      </article>
    </section>
    <hr>
    <section class="footer-bottom">
      <small>© 2019 Google. All rights reserved.
      </small>
      <ul>
        <li><a href="#!">Facebook</a></li>
        <li><a href="#!">Twitter</a></li>
      </ul>
    </section>
  </div>
</footer>
  
</template>

<style>


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


*,:after,:before{box-sizing:inherit}

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
      padding-top: 20px;
    padding-left: 30px;
    padding-right: 30px;
    padding-bottom: 20px;
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

.box table {
  display: none;
 }

  
.box:nth-of-type(4), .box:nth-of-type(5), .box:nth-of-type(9), .box:nth-of-type(10), .box:nth-of-type(14), .box:nth-of-type(15), .box:nth-of-type(19), .box:nth-of-type(20), .box:nth-of-type(24), .box:nth-of-type(25), .box:nth-of-type(29), .box:nth-of-type(30) {
   width: 50%; 
}

 .box:nth-of-type(4) h2, .box:nth-of-type(5) h2 {
        color: #fff;
    font-size: 34px;
    line-height: 34px;
    margin-top: -170px;
    margin-left: 20px;
    width: 500px;
}

.box:nth-of-type(1) img, .box:nth-of-type(2) img, .box:nth-of-type(3) img {
   display: none;
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

 .box:nth-of-type(4) h2, .box:nth-of-type(5) h2 {
    margin-top: 10px;
    margin-left: 10px;
    width: auto;
}

.box:nth-of-type(1) img, .box:nth-of-type(2) img, .box:nth-of-type(3) img {
   display: block;
}


}
  
  
  

.box:nth-of-type(2) h2, .box:nth-of-type(4) h2, .box:nth-of-type(8) h2, .box:nth-of-type(9) h2, .box:nth-of-type(13) h2, .box:nth-of-type(14) h2, .box:nth-of-type(17) h2, .box:nth-of-type(22) h2 {
   font-family: Roboto,Helvetica,Arial,sans-serif;
    font-weight: 600;
}

 .grid-item:nth-of-type(4), .grid-item:nth-of-type(5) {
    background-image: linear-gradient(180deg,transparent,rgba(0, 0, 0, 0.24));
    
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




footer{background:#f1f1f1;float:left;width:100%}

.footer-main{display:grid;grid-gap:1rem;

grid-template-columns:repeat(auto-fit,minmax(250px,1fr));margin-bottom:5em}

.footer-container{margin:0 auto;max-width:1140px;padding:4em 0 2em}

.footer-bottom{align-items:center;display:flex;justify-content:space-between}

section{margin:1em 0}ul{list-style-type:none}

.footer-bottom ul{align-items:center;display:flex;flex-direction:row;font-size:90%}

.footer-bottom ul li{color:rgba(0,0,0,.7);margin:0 .5em}

article{font-size:90%}

article h3{color:rgba(0,0,0,.7);font-weight:400}

article ul{color:rgba(0,0,0,.6);display:flex;flex-direction:column;margin-top:1em}

article ul li{margin:.4em 0}

article ul li a:hover{text-decoration:underline}

</style>
