# jquery.equaliseHeights
Equalise heights of elements


## Example use

```html
<!DOCTYPE html>
<html>
<head>
<script src="http://code.jquery.com/jquery-1.11.1.min.js"></script>
<script src="jquery.equaliseHeights.js"></script>
</head>
<body>
  <div class="toEqualise" style="float: left; background:#aaa;">
    <p>Test</p>
    <p>Test</p>
    <p>Test</p>
  </div>
  <div class="toEqualise" style="float: left; background:#ddd;">
    <p>Test</p>
    <p>Test</p>
  </div>
<script>
  jQuery('.toEqualise').equaliseHeights();
</script>
</body>
</html>
```

## Options

```javascript
$('.toEqualise').equaliseHeights({
    useMinHeight: false,
    delay: 200,
    runEqualise: function () {
        return true;
    }
});
```

Attribute		        | Type	  	  | Default		      | Description
---			            | ---		      | ---				      | ---
`useMinHeight`      | *bool*  	  | `false`		      | Equalise heights to the shortest element rather than the default tallest
`delay`	            | *int*	      | `200`	          | debounce delay
`runEqualise`	      | *function*  | function () {return true;}    | function that decides whether to run the equalise script or reset the heights, allows script to run at different breakpoints
