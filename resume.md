---
# This page uses Hydejack's `about` layout, which shows the primary author's picture and about text at the top.
# You can change it to the regular `page` layout if you want.
layout: page

# The title of the page.
title: Resume

# Write a short (~150 characters) description of each blog post.
# This description is used to preview the page on search engines, social media, etc.
description: >
  Resume for Timothy Truty
  

# You can show the description on the page by deleting this line:
hide_description: true

# Setting `menu` will generate an entry in the sidebar.
menu: true
order: 4
---

<style>
body {
	background: #fff;
	font: 15px Arial, Helvetica, sans-serif;
	line-height: 1.4;
	margin: 50px 0;
	margin-bottom: 100px;
}
em {
	color: #999;
}
p {
	line-height: 1.4;
}
ul {
	margin-bottom: 0;
}
section {
	margin-bottom: 2em;
}
blockquote {
	margin: 0;
	margin-bottom: 1em;
}
.item {
	margin-bottom: 1em;
}
#resume {
	margin: 0 auto;
	max-width: 480px;
	padding: 0 20px;
}
#basics {
	margin-bottom: -10px;
}
#basics h3 {
	margin-top: 1.5em;
}
#basics .contact strong,
#location strong {
	clear: both;
	float: left;
	line-height: 1.3;
	width: 120px;
}
#profiles,
#skills {
	overflow: hidden;
}
#profiles .item,
#skills .item {
	float: left;
	width: 50%;
}</style>


<!DOCTYPE HTML>
<head>
  <meta http-equiv="Content-type" content="text/html; charset=utf-8"/>
  <title>jQuery AutoBars Example</title>

  <link rel="stylesheet" href="boilerplate.css">
  
  <script src="https://code.jquery.com/jquery-2.1.1.min.js" type="text/javascript"></script>
  <script src="//cdnjs.cloudflare.com/ajax/libs/handlebars.js/2.0.0/handlebars.min.js" type="text/javascript" charset="utf-8"></script>
  <script src="//maxcdn.bootstrapcdn.com/bootstrap/3.2.0/js/bootstrap.min.js"></script>
  <script src="jquery-autobars.js" type="text/javascript"></script>
  <script src="boilerplate.hbs" type="text/x-handlebars-template"></script>
  <script type="text/javascript">
    $(document).ready(function() {
      $(document).autoBars(function() {
        $.getJSON("resume.json", function(json) {

          var data = { "resume" : json};
          
          var $html = $.handlebarTemplates['boilerplate'](data);
          $('body').append($html);
        })
        .fail(function(jqxhr, textStatus, error) { 
           var err = textStatus + ", " + error;
           console.log( "Request Failed: " + err );
         });
      });
    })
  </script>
</head>
<body>
</body>
{:.lead}

[blog]: https://ttruty.github.io/blog/
[portfolio]: https://ttruty.github.io/portfolio/
[resume]: https://ttruty.github.io/resume/
[welcome]: https://ttruty.github.io/
