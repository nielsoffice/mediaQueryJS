# mediaQueryJS

```JS

<script>

function myFunction(x) {
  if (x.matches) { // If media query matches
    document.body.style.backgroundColor = "yellow";
  } else {
   document.body.style.backgroundColor = "pink";
  }
}

var x = window.matchMedia("(max-width: 700px)")
myFunction(x) // Call listener function at run time
x.addListener(myFunction) // Attach listener function on state changes

</script>

// display only in mobile 

  // detect scroll top for fixed menu class cource at footer 
 jQuery(function() {
	 

  var getElement    = jQuery('#section-3935-13637').addClass('ftrFixedHide');
  var heightFromTop = 600;    
	 
  function onlyMobile(x) {
 
   if (x.matches) { // If media query matches
    
	$(document).scroll(function() {     
		
	let topval = $(document).scrollTop();  
      
	if(topval >= heightFromTop ){ 
	  getElement.removeClass('ftrFixedHide');  	
          getElement.addClass('ftrFixed'); 
        } else {  
          getElement.removeClass('ftrFixed');  
	  getElement.addClass('ftrFixedHide'); 
        }  

   });
   
  }  
  
 }

  var x = window.matchMedia("(max-width: 480px)");
   
  onlyMobile(x);
	 
  x.addListener(onlyMobile); 

  });

```

Demo 2

```JS
<script>

 jQuery(() => {

  let doResize = window.screen.availWidth; 
	 
  const wSize = ( doResize >= 541 )	? doResize : false;
	 
  const wSizeTablet = ( doResize  = 992 ) ? doResize : false;
	
  const wSizeMobile = ( doResize  = 768 ) ? doResize : false;
	 
  const giftPosition = function(rS) {
	  
    if (window.matchMedia("(max-width: "+wSize+"px)").matches) {
	
      let elemContainer = (jQuery('#div_block-203-322').width() / 2) + 5; 
      let eC = Math.trunc(elemContainer);
      let _img = jQuery('#image-207-322');	  
	  
	  _img.css( { "margin-right" : eC+"px"} );
	 
     } 
	  
  }
  
  // >= 540px
  giftPosition(wSize);
	 
  // giftPosition(wSize);
	
 });
 
</script>
```
