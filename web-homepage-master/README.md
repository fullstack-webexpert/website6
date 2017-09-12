# web-homepage
Responsive and Touch-enabled accordion for WordPress and jQuery. ... Accordion Slider is fully responsive and even allows you to change the layout of the accordion for different screen sizes. ... The accordion slider can be navigated by keyboard or mouse wheel.
```javascript
$(window).scroll(function() {
    if ($(this).scrollTop() >= 50) {        // If page is scrolled more than 50px
        $('#return-to-top').fadeIn(200);    // Fade in the arrow
    } else {
        $('#return-to-top').fadeOut(200);   // Else fade out the arrow
    }
        
    //menu dynamic
    if($(this).scrollTop() >= 188){
      $('.top_header').addClass('small');
      $('.slider-icon').addClass('move');
    }
    else
      {
        $('.top_header').removeClass('small');
        $('.slider-icon').removeClass('move');
      
  }

});
$('#return-to-top').click(function() {      // When arrow is clicked
    $('body,html').animate({
        scrollTop : 0                       // Scroll to top of body
    }, 800);
});

$('a').click(function(){
    $('html, body').animate({
        scrollTop: $( $(this).attr('href') ).offset().top
    }, 800);
    return false;
});

```

## TODOS
- [x] Fix responsive issue
- [ ] Modify interface

## Change Log
1. Fix responsive issue
2. Modify README