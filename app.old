var express = require("express");
var app = express();

app.get("/", function(req, res){
	//res.send("<h1>Welcome to the homepage!</h1><h2> blah blah</h2>") //too painful to type an HTML page this way, so use "render" method and templates istead:
	res.render("home.ejs") //this template file shd be placed in the "views" subdir and the "ejs" npm package shd be installed with --save parameter
});

app.get("/fallinlovewith/:thing", function(req, res){
	var thing = req.params.thing;
//	res.send("You fell in love with " + thing);
	res.render("love.ejs", {thingVar: thing});
});

app.get("/posts", function(req, res){
	var posts=[
		{title: "Post 1", author: "Suzy"},
		{title: "My adorable pet bunny", author: "Charlie"},
		{title: "Can you believe this pomsky?", author: "Colt"}
	];
	
	res.render("posts.ejs", {posts: posts});
	
});

app.listen(process.env.PORT, process.env.IP, function(){
	console.log("Server is listening!!!")
});