JUST TESTING CONTENT_FOR
=====

This is a sample app to try out content_for in Rails.

The idea is that in your layout you call `yield`, and from the views you will yield the corresponding view. To get a second yield you use `:content_for`. In the layout you will do something like this:

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
<%= yield :sidebar %>

<% yield %>
	
</body>
</html>

```

then in `app/views/home/index.html` for example you call `content_for`

```
<%= content_for :sidebar do %>
	<div id="sidebar">
		<ul>
			<li>hey</li>
			<li>hey</li>
			<li>hey</li>
			<li>hey</li>
			<li>hey</li>
		</ul>
	</div>
<% end %>

<h1>Home#index</h1>
<p>Find me in app/views/home/index.html.erb</p>
```

;) seya


