# Documentation

**Note**: This directory contains the css of the timer. It contains two versions: a minified version for direct use and an unminified version if you want to customise it further.
</br>

1. If you wish to modify the timer to your liking and needs, here are the ways to get the unminified CSS version.

   (i) The unminified version may be found in the same location. Simply check above for a file called timer-unminified.min.css. I've provided links to both the github source and the jsdeliverr CDN for your convenience.

      ```markdown
      <a href="https://go.amanstark.com/f78umnbqdxu">Unminified Css Github Link</a>
      ```

      ```markdown
      <link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/theamanstark/organic-safelink@1.2/safelink/assests/timer-unminified.min.css">
      ```

   (i) Alternatively, you may acquire the unminified CSS by executing this Python code, which will automatically beautify the minified CSS and output the timer's unminified CSS.

       <pre>
      ```python
        import requests
        import cssbeautifier

        # URL of the CSS file
        url = "https://cdn.jsdelivr.net/gh/theamanstark/organic-safelink@1.2/safelink/assests/timer-minified.min.css"

        # Fetch the CSS file content
        response = requests.get(url)
        css_code = response.text

        # Beautify the CSS code
        beautified_css = cssbeautifier.beautify(css_code)

        # Print the beautified CSS
        print(beautified_css)

      ```
      </pre>

3. If you don't want to modify anything and prefer the standard design, utilising the minified version of the CSS will be the best option because it has been entirely optimised. This version can be used by adding it using one of the ways listed below.

   (i) You can load the CSS externally using the below code; just add it above </head> in your site.

      ```markdown
      <link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/theamanstark/organic-safelink@1.2/safelink/assests/timer-minified.min.css">
      ```

   (ii) You may also add the minified CSS straight to your site, like I mentioned in the first step with the unminified version.

      ```css
      .safelink-countdown,.sky-note{position:relative;background:rgb(216,27,96,.09);overflow:hidden}svg.counterline{fill:none!important;stroke:#08102b;stroke- 
      linecap:round;stroke-linejoin:round;stroke-width:1;height:16px;width:16px}.pscustom{color:#d81b60}.aScrD{position:relative;z-index:1;font-family:Google 
      Sans Text,Arial,Helvetica,sans-serif;font-size:13px;opacity:.8;display:inline-flex;align-items:center;gap:5px;color:#000}.pcustom{font-size:1.2rem;font- 
      weight:700;margin-bottom:15px!important;margin-top:10px!important;color:#000}.sky-note{display:none;padding:20px 20px 20px 50px;color:#d81b60;font- 
      size:.85rem;font-family:var(--fontB);line-height:1.6em;border-radius:15px}.sky-note.countdown-done{display:block}.sky-            
      note:before{content:"";width:60px;height:60px;background:#d81b60;display:block;border-radius:50%;position:absolute;top:-8px;left:-12px;opacity:.05}.sky- 
      note:after{content:"\002A";position:absolute;left:18px;top:20px;font-size:22px;min-width:15px;text-align:center}.safelink-countdown{display:flex;align- 
      items:center;justify-content:center;padding:10px;border-radius:10px}.safelink- 
      countdown::before{content:"";position:absolute;top:0;left:0;height:100%;width:100%;background:#d81b60;opacity:1;animation:decrease-safelink-width var(-- 
      total-duration) linear}.safelink-countdown::after{content:"Please wait " attr(data-current-countdown) " seconds...";position:relative;z- 
      index:2;color:#000;animation:color-change var(--total-duration) linear}@keyframes color-change{0%{color:#000;opacity:1}100%,80% 
      {color:#fff;opacity:1}}.safelink-countdown[data-current-countdown="0"]::after{content:"Almost Ready...";color:#fff}@keyframes decrease-safelink-width{0% 
      {width:0;opacity:0}20%{opacity:.8}100%{width:100%}}.safelink-footer:not(.countdown-done),.safelink-header.countdown-done .safelink-countdown,.safelink- 
      header:not(.countdown-done)>:not(.safelink-countdown){display:none}
      ```
