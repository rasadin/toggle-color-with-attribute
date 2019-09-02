# toggle-color-with-attribute
https://codepen.io/Paulie-D/pen/952eac5ab270d5b25452248f0c91c2ed/
 ..................... html.....................
 <link href="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3999/reset_1.css" rel="stylesheet">

<div class="wrapper">
  <nav id="sections">
    <ul>
      <li class="section" data-color="red"><a href="#">Red</a></li>
      <li class="section" data-color="green"><a href="#">Green</a></li>
      <li class="section" data-color="orange"><a href="#">Orange</a></li>
    </ul>
  </nav>
  <div class="wrap">
    <div id="red" class="text">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quam sit voluptatibus autem neque dicta adipisci quas perferendis quis dolor excepturi aperiam eius maxime sunt corrupti aliquam perspiciatis nemo reprehenderit recusandae iusto tempore. Aspernatur perferendis consequatur hic commodi. Earum consequuntur voluptas ut molestias deserunt animi ex harum ratione libero eaque praesentium.</p>
    </div>
    <div id="green" class="text">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quam sit voluptatibus autem neque dicta adipisci quas perferendis quis dolor excepturi aperiam eius maxime sunt corrupti aliquam perspiciatis nemo reprehenderit recusandae iusto tempore. Aspernatur perferendis consequatur hic commodi. Earum consequuntur voluptas ut molestias deserunt animi ex harum ratione libero eaque praesentium.</p>
    </div>
    <div id="orange" class="text">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quam sit voluptatibus autem neque dicta adipisci quas perferendis quis dolor excepturi aperiam eius maxime sunt corrupti aliquam perspiciatis nemo reprehenderit recusandae iusto tempore. Aspernatur perferendis consequatur hic commodi. Earum consequuntur voluptas ut molestias deserunt animi ex harum ratione libero eaque praesentium.</p>
    </div>
  </div>
</div>

.......................html........................



..................css..............................

body {
}

nav ul {
  text-align: center;
}

.section {
  display: inline-block;
}

.section a {
  display: block;
  text-decoration: none;
  padding:15px;
  border:1px solid green;
  border-bottom:none;
  border-radius:8px 8px 0 0;
  background-color: lightgreen;
  color:white;
  font-weight: bold;
  text-shadow:1px 1px 2px black;
}

.text{
  height:100px;
  background-color: #fff;
  padding:0.5em;
  background-color: #bbc;
}

.wrap {
  border:1px solid green;
}

#red.highlight p {
  color:red;
}

#green.highlight p {
  color: green;
}

#orange.highlight p {
  color:orange;
}

................css................................




........................js..........................


$(document).ready(function() {
  $('.section').click(function() {
    $('.wrap > div').removeClass('highlight');
    //var color = $(this).data('color');
    $('#' + $(this).data('color')).addClass("highlight");
  });
});



.......................js.....................
