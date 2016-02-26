
<script src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script>
<script src="js/masonry-docs.min.js"></script>
<script>

$('.cart-philosophies-wrapper').masonry({
	columnWidth: '.cart-philosophies-block',
	itemSelector: '.cart-philosophies-block',
	gutter: 8
	
});

function refreshClick() { 
	
}

document.getElementById("cart-collapsible-div").onclick = function() {myFunction()};
function myFunction() {
   // alert("It's loaded!") 
    $('.cart-philosophies-wrapper').delay(800).masonry();
}

//$('.cart-philosophies-wrapper').masonry('reloadItems');

//window.onload = function () { alert("It's loaded!") }

</script>
