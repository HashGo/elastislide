elastislide
===========

This is an extension of the Elastislide responsive jQuery carousel plugin http://tympanus.net/codrops/2011/09/12/elastislide-responsive-carousel/

Options
=======

speed       : 450,  
// animation speed
 
easing      : '',   
// animation easing effect
 
imageW      : 190,  
// the images width
 
margin      : 3,    
// image margin right
 
border      : 2,    
// image border
 
minItems    : 1,    
// the minimum number of items to show. 
// when we resize the window, this will 
// make sure minItems are always shown 
// (unless of course minItems is higher 
// than the total number of elements)
 
current     : 0,    
// index of the current item
// when we resize the window, 
// the plugin will make sure that 
// this item is visible 
 
onClick     : function() { return false; } 
// click item callback
// Example of how to get the index
// of the clicked element:
/*
$('#carousel').elastislide({
    onClick  :  function( $item ) {
        alert( 'The clicked item´s index is ' + $item.index() )
    }
});
*/


It is also possible to dynamically add new items to the carousel. The following is an example on how to achieve that:

var $items  = $('<li><a href="#"><img src="images/large/1.jpg" alt="image01" /></a></li><li><a href="#"><img src="images/large/2.jpg" alt="image01"/></a></li>');
$('#carousel').append($items).elastislide( 'add', $items );
