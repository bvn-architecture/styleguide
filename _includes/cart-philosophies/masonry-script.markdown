
<script src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script>
<script src="js/masonry-docs.min.js"></script>
<script>


$('.cart-philosophies-wrapper').masonry({
	columnWidth: '.cart-philosophies-block',
	itemSelector: '.cart-philosophies-block',
	gutter: 8
});

var delay=50; //1000 = 1 seconds





        $('h1.cart-collapsible-div').click(function(){
        	//alert("It's loaded!") 
            setTimeout(function(){
			$('.cart-philosophies-wrapper').masonry();
			}, delay); 
        })

//$('.cart-philosophies-wrapper').masonry('reloadItems');

//window.onload = function () { alert("It's loaded!") }

</script>
