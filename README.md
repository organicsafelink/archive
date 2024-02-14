# Important Notice ‼️ [![](https://data.jsdelivr.com/v1/package/gh/theamanstark/organic-safelink/badge)](https://www.jsdelivr.com/package/gh/theamanstark/organic-safelink)

### This repository is just now a read-only archive; all future versions of organic-safelink and its different variants will be launched under [github.com/organicsafelink](https://github.com/organicsafelink) at [organicsafelink.com](https://organicsafelink.com). We're still working on the future version of this tool, and it's going to be a major update, so please bear with us. 

<br>

# Key Information

### # Demo 👉 [click here](https://go.amanstark.com/safelink-demo). 
### # Video tutorial for wordpress is here 👉 [video link](https://www.youtube.com/watch?v=zBnZnqaUQJQ).
### # Video tutorial for blogger is here 👉 [video link](https://www.youtube.com/watch?v=ZMICx047g_g).
### # You can know the status of the safelink by sending http request at `amanstark.com/safelink`
### # Use this Telegram bot to raise issues, offer suggestions, and report bugs, as well as to check the status of the safelink 👉 [bot link](https://t.me/therandombot).
### # When a new version is launched, a toast will appear on your site prompting you to upgrade to the most recent version, as shown below 👇
<br>

![Safelink Toast](https://github.com/theamanstark/organic-safelink/raw/1.2.1/assets/toast.gif)
<br>
<br>

# Documentation

1. Just add these two JavaScript's in your site above `</body>`

    (i) For Wordpress 👇

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

    (ii) For Blogger 👇

    ```javascript
    <script>/*<![CDATA[*/
    const config = {
    postsArray: ['post1.html', 'post2.html', 'post3.html'], // Array of your random post URLs
    googleRedirectURL: 'https://www.google.com/search?q=site:YourWebsite.com', // Google search URL
    countdownSeconds: 30, // Countdown timer variable
    };
    /*]]>*/</script>
    ```
    
    ```html
    <script src='https://cdn.jsdelivr.net/gh/theamanstark/organic-safelink@1.2.1/script.min.js'></script>
    ```      
    
3. In the HTML page/post in which you will add the link, add it like this:

    ```html
    <!-- These are the links on your original website. Add as many as you like. -->
    <a href="#" data-url="https://www.your_destination_url_1.com" class="redirectLink">Go to destination 1</a>
    <a href="#" data-url="https://www.your_destination_url_2.com" class="redirectLink">Go to destination 2</a>
    <a href="#" data-url="https://www.your_destination_url_3.com" class="redirectLink">Go to destination 3</a>
    <!-- You can create an infinite number of safe links; just keep adding them according to your needs. -->
    ```

4. In the post which you will redirect after clicking on one of the safe links, add the following code:

    (i) Add this to the top of your post, so users can easily see the countdown timer when the safelink redirects to any of the random post URLs you've specified in the config.

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

    (ii) Put this at the bottom of your post so that when the countdown finishes, the "Continue" button shows at the bottom.

    ```html
    <!-- This is the button that will appear after the countdown. It's hidden by default. -->
    <div id="continueButtonMessage" style="display: none;flex-direction: column;align-items: center;" class="sky-note">
    <p class='pcustom' style="font-size: 1.3em;margin-bottom: -10px !important;" align='center'>Clicking on the <span class='pscustom'>Continue</span> button will redirect you to the Google search page. Click our site, <span class='pscustom'>Site_Name_Here</span>, from the first search result to get your link.</p> 
    <button class="bubbly-button" id="continueButton" style="display: none;">Continue</button>
    </div>
    ```

5. Lastly, add the following code on the homepage of your site where you will send the user from the search page:

    (i) Add this to the top of your site's homepage so users can easily see the countdown timer after coming from the Google search page.

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

    (ii) Add this button at the bottom of your site's homepage so that when the countdown finishes, the "Go to Link" button shows at the bottom.

    ```html
    <!-- This is the button that will appear after the countdown. It's hidden by default. -->
    <div align='center'>
    <button class="bubbly-button" id="continueButton2" style="display: none;">Go to Link</button>
    </div>
    ```

<br>

**Credits**: Organic Safelink v1.2 created by [Aman Singh](https://www.amanstark.com).
