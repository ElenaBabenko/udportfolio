## Website Performance Optimization portfolio project

Here a the optimizations I performed.

### For index.html

PageSpeed Mobile score - 94/100, desktop score - 100/100.

- Cleaned up (removed unused styles) and minified CSS
- JS and CSS are served asynchronosly
- Made a small optimized version or pizza image to reduce file size
- Optimized font delivery

Didn't have time to figure out what to do with analytics JS and minification tools. But the score is above 90.

### For pizza.html

- Optimized pizzaria.jpeg from over 2 MB to 200 KB

#### For the moving pizzas:

- Reduced number of background pizzas from 200 to smaller size based on screen size
- replaced document.querySelectorAll with document.getElementsByClassName
- in updatePositions() replaced basicLeft with translate3D, moved scrollTop out of the loop
- in mark-up made movingPizzas1 div span the whole width of the container so that the moving pizzas always appear in the same place horizontally. Initially their position would jump between screen sizes.

#### For the pizza size switcher:

- reduced number of ingredient and name options, as well as the number of generated pizzas
- replaced a repeated selector with a variable (pizzaElems)
- moved layout calculations outside of the loop
- added translateZ to .randomPizzaContainer img to force in on a separate layer
- switched how pizza images sizes are updated. Instead of changing column width I used transform scale. Not sure why I'm not seeing improvement in performance? and why the class is not being added to the first two pizza?
- tried adding transform: translateZ(0) and will-change to .randomPizzaContainer img but it seemed to make performance even worse, generated a lot of goast bars...


