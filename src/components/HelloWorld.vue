
<template>
<body style="background-color:Tomato;">
<h1>My <span style="color:red">VUEJS</span>Assignment</h1>
  



<div>  
  <ul>
      <li><a href="https://www.w3schools.com">C</a></li>
    <li>  <a href="https://www.w3schools.com/php/">PHP</a></li>
     <li> <a href="https://www.javatpoint.com/java-tutorial">JAVA</a></li>
	 <li> <a href="https://www.javatpoint.com/java-oops-concepts">OOP</a></li>
	  </ul>
 
</div>	  
<div>
  <table  border="3" bordercolor = black align = center>
  
  <thead>
      <tr>
        <th><b>Name</b></th>
        <th><strong>Description</strong></th>
        <th>Price</th>
		<th>Image</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="product in products" track-by="id">
        <td>{{product.name}}</td>
        <td>{{product.description}}</td>
        <td>{{product.price}}</td>
		<td><a href="https://www.amazon.in/Programming-Languages-Books/b?ie=UTF8&node=4149459031"><img :src="product.image" width="500"></a></td>
		
      </tr>
    </tbody>
  </table>
  </div>
  <div class="pagination">
  <a href="#">&laquo;</a>
  <a href="https://books.google.co.in/books?id=WM7aTX2hr7EC&source=gbs_similarbooks">1</a>
  <a href="https://books.google.co.in/books/about/Programming_PHP.html?id=h-E1lVko-skC&redir_esc=y">2</a>
  <a href="https://books.google.co.in/books/about/The_Java_Language_Specification.html?id=Ww1B9O_yVGsC">3</a>
  <a href="https://books.google.co.in/books?id=WM7aTX2hr7EC&source=gbs_similarbooks">4</a>
  <a href="#">&raquo;</a>
</div>

  </div>
  
   
  </div>
 
	
  </body>
  </template>

<script>


import bell from "../assets/logo2.png"
import php from "../assets/logo6.png"
import java from "../assets/logo4.png"
import oop from "../assets/logo5.png"


export default {
  data () {
    return {
      products: [
        {
          id: '1',
          name: ' C Language',
          description: 'C is a procedural programming language Author:Dennis Ritchie ',
          price: 399,
		  image : bell
		 

        },
        {
          id: '2',
          name: 'PHP',
          description: 'PHP is scripting language Author:Rasmus Lerdorf',
          price: 995,
		  image: php
        },
        {
          id: '3',
          name: 'JAVA ',
          description:'Java is a high-level programming language Author:James Gosling.',
          price: 595,
		  image: java
        },
		{
          id: '4',
          name: 'OOP',
          description: 'OOP is Object Orirented Programmning LanugageAuthor:Dennis Ritchie',
          price: 195,
		  image: oop
        },
		
      ]
    }
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div{
    text-align: center;
}
body {
    font-family: cambria;
}
[title~=logos] {
    border: 5px solid yellow;
}
table, th, td {
    border: 2px solid black;
    border-collapse: collapse;
	 border-spacing: 15px;
}

th, td {
     padding: 10px;
}
th {
    text-align: left;
}
td {
    text-align: left;
}

h1, h2  {
    background-color: blue;
	font-weight: normal;
}
img {
    
    border: 1px solid #ddd;
    border-radius: 4px;
    padding: 5px;
    width: 200px;
}
img:hover {
    box-shadow: 0 0 2px 1px rgba(0, 140, 186, 0.5);
}
ul {
  list-style-type:"width:100%;";
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
    color: yellow;
}
.pagination {
    display: inline-block;
}

.pagination a {
    color: black;
    float: left;
    padding: 8px 16px;
    text-decoration: none;
}

.pagination a.active {
    background-color: #4CAF50;
    color: white;
    border-radius: 5px;
}

.pagination a:hover:not(.active) {
    background-color: #ddd;
    border-radius: 5px;
}

</style>
