
<script src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script>
<script src="js/masonry-docs.min.js"></script>
<script>

$(window).bind("load", function() {


		$('div.cart-philosophies-normal').masonry({
			columnWidth: 'div.cart-philosophies-normal',
			itemSelector: 'cart-philosophies-normal'
		});
		$('div.cart-philosophies-definition').masonry({
			columnWidth: 'div.cart-philosophies-definition',
			itemSelector: 'cart-philosophies-definition'
		});
		$('div.cart-philosophies-guides').masonry({
			columnWidth: 'div.cart-philosophies-guides',
			itemSelector: 'cart-philosophies-guides'
		});

	});


</script>
