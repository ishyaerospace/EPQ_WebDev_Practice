# DOM animations

HTML
* basic webpage
* animation div
* animation container
* style elements
    - container element should be created with `style = "position: relative"`
    - animation element should be created with `style = position: absolute"`

JS
javascript animation is done by programming gradual changes in an element's style
The changes are called by a timer. when the timer interval is small, the animation looks contiuous.

basic template code:

`id = setInterval(frame, 5);`
`function frame() {`
`  if (/* test for finished */) {`
`    clearInterval(id);`
`  } else {`
`    /* code to change the element style */ `
`  }`
`}`

fo full code see DOM_Animation.html
