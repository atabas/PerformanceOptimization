## Website Performance Optimization portfolio project

- Time to resize pizzas [DONE]: 0.9ms (less than 5ms )
- Critical rendering path for index.html [DONE]:PageSpeed score (mobile: 95, desktop: 96) >= 90
- Framerate for pizza.html [DONE]: should be 60fps
- Comments in main.js [DONE]

### Optimizations for pagespeed (index.html):
- Compressed images
- Inline CSS instead of style.css
- Used async for analytics and perfmatters.js; moved google analytics code to perfmatters.js
- Used media query for print.css so that it doesn't have to load except when printing

### Optimizations for FPS :
- Moved some variables outside loop so that they don't have to be calculated everytime (eg dx, newWidth, etc)
- stored scroll position and value to prevent being calculated everytime
- stored document.querySelectorAll calculations in one query/variable where possible to prevent expensive calculations everytime
- Made changes for updatePositions and scroll to prevent document selector being called everytime

### Resources used:
- http://compressjpeg.com/
- http://jscompress.com/
- Pagespeed Insights
- https://www.udacity.com/course/ud884
- Piazza (Udacity nanodegree discussion forum)

### How to Run
Some useful tips to help you get started:

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
2. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok 8080
  ```

3. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional
4. Tested FPS by using the counter in Chrome for pizza.html

