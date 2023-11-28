[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/_e9whi2b)

[Documentation on - RUKDY FC Website]

# Initiation & Background

RUKDY FC is one of my website project that ive made this website focus on my football organization between my colleagues while im in college, you may asked why ? due to it's memories and excitement i would like to make a fully functional website that people can interact towards the organization.I made this website by using HTML, CSS & Javascript and several images and a JSON animation.

## HTML & CSS

On the HTML & CSS that i would like to point out is the semantics and design that i've made first thing first probably the HEADER and then we go on to HERO , SECTION and finish it off with CONTACT US as the footer. The color design is quite simple making it all white and some animation and buttons or border with navy blue. 

At some point i've made a color spectrum in text with html css as you can see this is the highlights of the code itself 

## HTML for Text w/ Color Spectrum
 
![Foto Dokum 1](/documentation%20/docum.png)

## CSS for Text w/ Color Spectrum
![Foto Dokum 2](documentation%20/docum2.png)


## LOTTIE


 I also add an animation of a soccer ball inside a soccer jumping on a goalpost to the other one.

![Lottie Animation](/documentation%20/lottie%20file.png)



this animation i picked up from [Lottie](https://lottiefiles.com/),it's a free website to download animation that has been contributed from animators around the globe.

to make it work all you need is CDNS file to connect within the html 
>HTML 
```html
    <!--CDN LOTTIE-->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bodymovin/5.12.2/lottie.min.js"></script>
```
from [CDNJS](https://cdnjs.com/libraries/bodymovin)

![CDNS](documentation%20/cdns.png)

to add this file so it can be animated in the website i use this code in HTML

>HTML & SCRIPT
```html
<script>
    var animation = bodymovin.loadAnimation({container: document.getElementById('animation container')
    ,path: 'lottie-hero.json'
    ,render: 'svg'
    ,loop: true
    ,autoplay: true
    ,name:'lapangan bola'
});
</script>
```

In this website there's a carousel that i've made using Javascript

>Javascript

```javascript

    const buttons = document.querySelectorAll("[data-carousel-button]")

buttons.forEach(button => {
    button.addEventListener("click", () => {
        const offset = button.dataset.carouselButton === "next" ? 1 : -1
        const slides = button
        .closest("[data-carousel]")
        .querySelector("[data-slides]")

    const activeSlide = slides.querySelector("[data-active]")
    let newIndex = [...slides.children].indexOf(activeSlide)+offset
    if (newIndex <0) newIndex = slides.children.length - 1 
    if (newIndex >= slides.children.length) newIndex = 0

    slides.children[newIndex].dataset.active = true
    delete activeSlide.dataset.active
    })
})
```
In summary, this JavaScript code is designed to create a basic carousel functionality. It selects buttons with a specific attribute (data-carousel-button), and when a button is clicked, it calculates the index of the next or previous slide based on the value of the button's data-carousel-button attribute ("next" or "prev"). It then updates the data-active attribute to highlight the new active slide and removes the data-active attribute from the previously active slide. The carousel is working if to be structured with a container within the carousel
having the attribute data-carousel and containing slides with the attribute data-slides.

# DEPLOYING

For the hosting and domain purchase i use [Niagahoster](https://hpanel.hostinger.com/) as my main server due to its cheap and reliable 

![Hosting](documentation%20/dns.png)

and the deployment i use [Vercel](https://vercel.com/leonaramudas-projects) i mean it's free and ease to use so why not ?

![Deployment](documentation%20/deployment.png)

Sincerely,Leon


