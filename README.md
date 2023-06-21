# Documentation

1. Just add this JavaScript in your site above `</body>`

    ```javascript
    // Array of your random post URLs
    let postsArray = ['post1.html', 'post2.html', 'post3.html'];

    // Google search URL
    let googleSearchUrl = 'https://www.google.com/search?q=site:YourWebsite.com';

    // Countdown timer variable
    let timeleft = 30;
    ```
    
    ```html
    <script src='https://cdn.jsdelivr.net/gh/theamanstark/organic-safelink@1.1/safelink-code/main.min.js'></script>
    ```
    
2. In the HTML page/post in which you will add the link, add it like this:

    ```html
    <!-- These are the links on your original website. Add as many as you like. -->
    <a href="#" data-url="your_destination_url_1" onclick="redirectToRandomPost(this)">Go to destination 1</a>
    <a href="#" data-url="your_destination_url_2" onclick="redirectToRandomPost(this)">Go to destination 2</a>
    ```

3. In the post which you will redirect after clicking on one of the safe links, add the following code:

    ```html
    <!-- This is the countdown timer -->
    <p id="countdown1" style="display: none;">30 seconds remaining</p>

    <!-- This is the button that will appear after the countdown. It's hidden by default. -->
    <button id="continueButton1" style="display: none;" onclick="redirectToGoogle()">Continue</button>
   
    <!-- This is the javascript initiator -->
    <script>startCountdown('countdown1', 'continueButton1');</script>
    ```

4. Lastly, add the following code on the homepage of your site where you will send the user from the search page:

    ```html
    <!-- This is the countdown timer -->
    <p id="countdown2" style="display: none;">30 seconds remaining</p>

    <!-- This is the button that will appear after the countdown. It's hidden by default. -->
    <button id="continueButton2" style="display: none;" onclick="redirectToDestination()">Continue</button>

    <!-- This is the javascript initiator -->
    <script>startCountdown('countdown2', 'continueButton2');</script>
    ```

**Note**: Please note that this is just an alpha build; it doesn't contain any CSS. I will improve it in future builds.
