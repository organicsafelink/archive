This is just a basic version i will continue updating it gradually.

# Documentation

1. Just add this javascript in your site above </body>

<script>
// Array of your random post URLs
let postsArray = ['post1.html', 'post2.html', 'post3.html'];
function googleurl(){
    window.location.href = 'https://www.google.com/search?q=site:YourWebsite.com';
}
</script>

<script src=''/>

2. In the html page/post in which you will add the link add it like this :-

<!-- These are the links on your original website. Add as many as you like. -->
<a href="#" data-url="your_destination_url_1" onclick="redirectToRandomPost(this)">Go to destination 1</a>
<a href="#" data-url="your_destination_url_2" onclick="redirectToRandomPost(this)">Go to destination 2</a>

3. In the post which you will redirect after clicking on one of the safe-link add the following code

<!-- This is the countdown timer -->
<p id="countdown">30 seconds remaining</p>

<!-- This is the button that will appear after the countdown. It's hidden by default. -->
<button id="continueButton" style="display: none;" onclick="redirectToGoogle()">Continue</button>

4. Lastly add the following code on the homepage of your site where you will send the user from the search page

<!-- This is the countdown timer -->
<p id="countdown2">30 seconds remaining</p>

<!-- This is the button that will appear after the countdown. It's hidden by default. -->
<button id="continueButton2" style="display: none;" onclick="redirectToDestination()">Continue</button>

## Please note that this is just an alpha build it doesn't conatins any css, i will improve it in the future builds
