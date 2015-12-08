Offline Setup Instructions
==========================

If you are attempting to run the score server in an offline enviorment you 
will need to alter the following lines in `app/views/layouts/application.html.erb`

  **From**
```html
    <link rel="stylesheet" type="text/css" href="//cdnjs.cloudflare.com/ajax/libs/c3/0.4.0/c3.min.css">
    <script src="//cdnjs.cloudflare.com/ajax/libs/d3/3.4.13/d3.min.js"></script>
    <script src="//cdnjs.cloudflare.com/ajax/libs/c3/0.4.0/c3.min.js"></script>
    <script src="//cdnjs.cloudflare.com/ajax/libs/moment.js/2.5.1/moment.min.js"></script>
```

  **To**
```html
    <link rel="stylesheet" type="text/css" href="/assets/c3.min.css">
    <script src="/assets/d3.min.js"></script>
    <script src="/assets/c3.min.js"></script>
    <script src="/assets/moment.min.js"></script>
```
  
Next
  move `c3.min.css`, `d3.min.js`, `c3.min.js`, `moment.min.js` from the offline setup folder to the `public/assets` folder
 
 
After that has been accomplished delete the following line from `app/views/layouts/application.html.erb`
```ruby
  <%= debug(params) if Rails.env.development? %>
```