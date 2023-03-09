# 3D Header Animation

Attractive title for your site

## Foundation

- **Setting up animations for movements**

```javascript
document.addEventListener("DOMContentLoaded", () => {
  const body = document.querySelector("body");
  cx = window.innerWidth / 2;
  cy = window.innerHeight / 2;

  body.addEventListener("mousemove", (e) => {
    clientX = e.pageX;
    clientY = e.pageY;

    request = requestAnimationFrame(updateMe);
  });

  function updateMe() {
    dx = clientX - cx;
    dy = clientY - cy;
    tiltx = dy / cy;
    tilty = dx / cx;
    radius = Math.sqrt(Math.pow(tiltx, 2) + Math.pow(tilty, 2));
    degree = radius * 12;
    gsap.to(".content", 1, {
      transform: `rotate3d(${tiltx},${tilty}, 0, ${degree}deg)`,
    });
  }
```





# Features
- Сustom design 
- Adaptation for all screens
- 3D animations
- Custom cursor

# References
- [Gsap](https://greensock.com/gsap/)
- [Sass](https://sass-lang.com)
- [Gulp](https://gulpjs.com)
- [Bootstrap](https://getbootstrap.com)
- [Cubic-bezier](https://cubic-bezier.com/#.17,.67,.83,.67)


## Screenshot

![ezgif com-video-to-gif](https://user-images.githubusercontent.com/113831614/224136162-69dc8604-99f6-4e5e-bf6e-7bf148a5606e.gif)


---
**How to make it work?**

Install the dependencies:
```shell
npm install
```
Running a web server:
```shell
gulp 
```
Build:
```shell
gulp buid
```
