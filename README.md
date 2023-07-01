# Documentation

### # Video tutorial for wordpress is here 👉 [video link](https://www.youtube.com/watch?v=zBnZnqaUQJQ).
### # Video tutorial for blogger is here 👉 [video link](https://www.youtube.com/watch?v=ZMICx047g_g).
### # You can know the status of the safelink by sending https request at `xqc.amanstark.com`
### # You may also use this Telegram bot to raise issues, offer suggestions, and report bugs, as well as to check the status of the safelink 👉 [bot link](https://t.me/therandombot).
<br>



1. Just add this JavaScript in your site above `</body>`

    ```javascript
    <script>
    const config = {
    postsArray: ['post1.html', 'post2.html', 'post3.html'], // Array of your random post URLs
    googleRedirectURL: 'https://www.google.com/search?q=site:YourWebsite.com', // Google search URL
    countdownSeconds: 30, // Countdown timer variable
    };
    </script>
    ```
    
    ```html
    <script src='https://cdn.jsdelivr.net/gh/theamanstark/organic-safelink@1.2.1/script.min.js'></script>
    ```
    
2. In the HTML page/post in which you will add the link, add it like this:

    ```html
    <!-- These are the links on your original website. Add as many as you like. -->
    <a href="#" data-url="https://www.your_destination_url_1.com" class="redirectLink">Go to destination 1</a>
    <a href="#" data-url="https://www.your_destination_url_2.com" class="redirectLink">Go to destination 2</a>
    <a href="#" data-url="https://www.your_destination_url_3.com" class="redirectLink">Go to destination 3</a>
    ```

3. In the post which you will redirect after clicking on one of the safe links, add the following code:

    ```html
    <!-- This is the countdown timer -->
    <div id="countdown" style="display: none;">
    <div class='safelink-countdown'></div>
    <div class="sky-note">
    <div class='safelink-header'> 
    <p class='pcustom' align='center'>Scroll Down and click on <span class='pscustom'>Continue</span> button for destination</p> 
    </div> 
    <div align='center' class='safelink-footer'> 
    <div class="aScrD">
    <svg class="counterline" viewBox="0 0 24 24"><path d="M22 11.07V12a10 10 0 1 1-5.93-9.14"></path><polyline points="23 3 12 14 9 11"></polyline>
    </svg>Congrats! Link is Generated</div>
    </div>
    </div>
    </div>
    ```

    ```html
    <!-- This is the button that will appear after the countdown. It's hidden by default. -->
    <div id="continueButtonMessage" style="display: none;flex-direction: column;align-items: center;" class="sky-note">
    <p class='pcustom' style="font-size: 1.3em;margin-bottom: -10px !important;" align='center'>Clicking on the <span class='pscustom'>Continue</span> button will redirect you to the Google search page. Click our site, <span class='pscustom'>Site_Name_Here</span>, from the first search result to get your link.</p> 
    <button class="bubbly-button" id="continueButton" style="display: none;">Continue</button>
    </div>
    ```

4. Lastly, add the following code on the homepage of your site where you will send the user from the search page:

    ```html
   <!-- This is the countdown timer -->
    <div id="countdown2" style="display: none;">
    <div class='safelink-countdown'></div>
    <div class="sky-note">
    <div class='safelink-header'> 
    <p class='pcustom' align='center'>Scroll Down and click on <span class='pscustom'>Go to Link</span> button for destination</p> 
    </div> 
    <div align='center' class='safelink-footer'> 
    <div class="aScrD">
    <svg class="counterline" viewBox="0 0 24 24"><path d="M22 11.07V12a10 10 0 1 1-5.93-9.14"></path><polyline points="23 3 12 14 9 11"></polyline>
    </svg>Congrats! Link is Generated</div>
    </div>
    </div>
    </div>
    ```

    ```html
    <!-- This is the button that will appear after the countdown. It's hidden by default. -->
    <button class="bubbly-button" id="continueButton2" style="display: none;">Go to Link</button>
    ```

**Note**: Complete documentation coming soon.
