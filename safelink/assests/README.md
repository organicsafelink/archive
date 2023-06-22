# Documentation

**Note**: This directory contains the css of the timer. It contains two versions: a minified version for direct use and an unminified version if you want to customise it further.
</br>

1. If you wish to modify the timer to your liking and needs, here is the unminified CSS version.
 
```css
svg.counterline {
  fill: none !important;
  stroke: #08102b;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke-width: 1;
  height: 16px;
  width: 16px;
}

.pscustom {
  color: #d81b60;
}

.aScrD {
  position: relative;
  z-index: 1;
  font-family: Google Sans Text, Arial, Helvetica, sans-serif;
  font-size: 13px;
  opacity: 0.8;
  display: inline-flex;
  align-items: center;
  gap: 5px;
  color: black;
}

.pcustom {
  font-size: 1.2rem;
  font-weight: 700;
  margin-bottom: 15px !important;
  margin-top: 10px !important;
  color: black;
}

.sky-note {
  display: none;
  position: relative;
  padding: 20px 20px 20px 50px;
  background: rgb(216, 27, 96, 0.09);
  color: #d81b60;
  font-size: 0.85rem;
  font-family: var(--fontB);
  line-height: 1.6em;
  border-radius: 15px;
  overflow: hidden;
}
.sky-note.countdown-done {
  display: block;
}
.sky-note:before {
  content: "";
  width: 60px;
  height: 60px;
  background: #d81b60;
  display: block;
  border-radius: 50%;
  position: absolute;
  top: -8px;
  left: -12px;
  opacity: 0.05;
}
.sky-note:after {
  content: "\002A";
  position: absolute;
  left: 18px;
  top: 20px;
  font-size: 22px;
  min-width: 15px;
  text-align: center;
}

/* extra dark mode css can be deleted */
.dark .sky-note {
}

.safelink-countdown {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 10px;
  border-radius: 10px;
  background: rgb(216, 27, 96, 0.09);
  overflow: hidden;
}
.safelink-countdown::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background: #d81b60;
  opacity: 1;
  animation: decrease-safelink-width var(--total-duration) linear;
}
.safelink-countdown::after {
  content: "Please wait " attr(data-current-countdown) " seconds...";
  position: relative;
  z-index: 2;
  color: black;
  animation: color-change var(--total-duration) linear;
}

@keyframes color-change {
  0% {
    color: black;
    opacity: 1;
  }
  80% {
    color: white;
    opacity: 1;
  }
  100% {
    color: white;
    opacity: 1;
  }
}

.safelink-countdown[data-current-countdown="0"]::after {
  content: "Almost Ready...";
  color: white;
}
@keyframes decrease-safelink-width {
  0% {
    width: 0;
    opacity: 0;
  }
  20% {
    opacity: 0.8;
  }
  100% {
    width: 100%;
  }
}
.safelink-header:not(.countdown-done) > *:not(.safelink-countdown),
.safelink-header.countdown-done .safelink-countdown,
.safelink-footer:not(.countdown-done) {
  display: none;
}
```
</br>

2. If you don't want to modify anything and prefer the standard design, utilising the minified version of the CSS will be the best option because it has been entirely optimised. This version can be used by adding it using one of the ways listed below.

   (i) You can load the CSS externally using the below code; just add it above </head> in your site.

       ```html
       <link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/theamanstark/organic-safelink@1.2/safelink/assests/timer-minified.min.css">
       ```
