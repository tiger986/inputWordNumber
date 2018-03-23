## How many characters can also be entered
#### HTML code
```html
<div class="uploadWorks_con_e">
	    <div class="uploadWorks_con_title">留言说明</div>
	    <div class="uploadWorks_con_e_text">
		      <textarea class="uploadWorks_con_e_text_con" placeholder="说出你的困惑，或是希望老师特别点评的地方"></textarea>
			<p>80</p>
		</div>
</div>
```
#### JS code
```javascript

$(function(){		
    var value = "";
		var length = 0;
		$(".uploadWorks_con_e_text_con").keyup(function(){
		    if(length <= 0){
				    value = $(".uploadWorks_con_e_text_con").val().substring(0, 80);
				    $(".uploadWorks_con_e_text_con").val(value);
			  }
			  length = 80 - $(".uploadWorks_con_e_text_con").val().length;
			  $(".uploadWorks_con_e_text").find("p").html(length);			
		});
})
