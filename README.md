# slide-menu
Contemporary website design affords only so much space to your website navigation. Many navigational areas, while capable of supporting child dropdowns, can only fit so many items before a space becomes crowded. For large or enterprise websites, the challenge can become how to fit all of the necessary top-level links to support a clear navigation experience. In this article, [Solodev](https://www.solodev.com/blog/) will teach you how to create a slide down menu for your website using HTML, CSS, and JavaScript. 

## Tutorial

For detailed instructions, view Solodev's [How to Add a Slide Down Menu to your Nav](https://www.solodev.com/blog/web-design/how-to-add-a-slide-down-menu-to-your-nav.stml) article.

## Demo

Try out a working example on [JSFiddle](https://jsfiddle.net/solodev/ju2uLroh/).

## HTML

The slidedown menu contains the following basic HTML markup.
```
<div class="header">
  <div class="container">
	<!-- Navigation Menu Start -->
	<div class="navigation">
	  <div class="row">
        <!-- Navigation Menu Link Lists -->
        <div class="col-sm-4 col-xs-12">
          <div class="menu">
            <span class="br-lblue"><i class="fa fa-desktop"></i> &nbsp; Menu Column</span>
            <div class="menu-list">
              <ul>
                <li>
                  <a href="#"><i class="fa fa-gear red"></i> Service</a>
                </li>
                <li>
                  <a href="#"><i class="fa fa-check-square-o lblue"></i> Features</a>
                </li>
                <li>
                  <a href="#"><i class="fa fa-user pink"></i> About Us</a>
                </li>
                <li>
                  <a href="#"><i class="fa fa-picture-o orange"></i> Gallery</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col-sm-4 col-xs-6">
          <div class="menu">
            <span class="br-green"><i class="fa fa-desktop"></i> &nbsp; Menu Column</span>
            <div class="menu-list">
              <ul>
                <li>
                  <a href="#"><i class="fa fa-camera green"></i> Portfolio</a>
                </li>
                <li>
                  <a href="#"><i class="fa fa-comments-o blue"></i> Blog Page</a>
                </li>
                <li>
                  <a href="#"><i class="fa fa-table red"></i> Pricing Table</a>
                </li>
                <li>
                  <a href="#"><i class="fa fa-times lblue"></i> Coming Soon</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col-sm-4 col-xs-6">
          <div class="menu">
            <span class="br-red"><i class="fa fa-desktop"></i> &nbsp; Menu Column</span>
            <div class="menu-list">
              <ul>
                <li>
                  <a href="#"><i class="fa fa-puzzle-piece pink"></i> Products</a>
                </li>
                <li>
                  <a href="#"><i class="fa fa-phone orange"></i> Contact Us</a>
                </li>
                <li>
                  <a href="#"><i class="fa fa-sign-in green"></i> Login / Register</a>
                </li>
                <li>
                  <a href="#"><i class="fa fa-question blue"></i> 404 Error Page</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
<!-- Navigation menu end -->
        
<div class="menu-btn">
  <a onclick="documentTrack('#');" href="#">Menu <i class="fa fa-chevron-down"></i></a>
</div> 
        
<div class="head">
  <div class="container">
    <div class="row">
	  <div class="col-md-3 col-sm-4">
		<!-- Logo and Head Text -->
		<div class="logo">
			<!-- Logo Icon and Heading --><img alt="" class="img-responsive" src="https://www.solodev.com/assets/logo.png"><span><a onclick="documentTrack('index.html');" href="index.html">Rocket</a></span>
		</div>
	  </div>
	  <div class="col-md-3 hidden-sm">
		&nbsp;
	  </div>
	</div>
  </div>
</div>        
```

## CSS

All required CSS is in slide-menu.css

## JavaScript

The slide down menu requires the following JavaScript:
```
$(document).ready(function(){
  $(".menu-btn").on('click',function(e){
	  e.preventDefault();
		
		//Check this block is open or not..
	  if(!$(this).prev().hasClass("open")) {
		  $(".header").slideDown(400);
		  $(".header").addClass("open");
		  $(this).find("i").removeClass().addClass("fa fa-chevron-up");
	  }
	  
	  else if($(this).prev().hasClass("open")) {
		  $(".header").removeClass("open");
		  $(".header").slideUp(400);
		  $(this).find("i").removeClass().addClass("fa fa-chevron-down");
	  }
  });
}); 
```

## External Includes

This tutorial includes the following third party resources.
```
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet" >
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
```
