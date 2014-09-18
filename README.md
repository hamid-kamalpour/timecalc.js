timecalc.js
===========

### Try it now!
If you're just here to calculate some times, go for it!  
Try it here: http://makhani.de/timecalc

### Currently supported time formats
* `hh:mm:ss`
    * ` 1:40:15` - 1 Hour, 40 Minutes, 15 Seconds
    * `03:2:7`  - 3 Hours, 2 Minutes, 7 Seconds
    * `02:180:75` - 4 Hours, 1 Minute, 15 Seconds
    * `1:40` - 1 Hour, 40 Minutes, 0 Seconds
    * `:1:40` - 0 Hours, 1 Minute, 40 Seconds
* hh as decimal value
    * `4` - 4 Hours
    * `2.5` - 2 Hours, 30 Minutes
    * `2,5` - 2 Hours, 30 Minutes (European Format)
* hh Hours mm Minutes ss Seconds

### Basic API-Usage:  
1. Include jQuery and timecalc.js:
    ```html
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/2.0.0/jquery.min.js"></script>
    <script src="js/timecalc.js"></script>
    ```

2. Let timecalc do all the work:
    ```javascript
    $('#time-input').timecalc( $('#time-output') );
    ```
    
    The total time is now bind to `$('#time-output')`. It will be refreshed in as soon as the input changes.
	
### Advanced API-Usage

You can also handle the update event yourself and do with whatever you want to do with the data.  
Here are some examples: 

```javascript
$('#time-input').timecalc();
$('#time-input').on('timecalcupdate', function ( event ) {
   $('#time-output').text('My Time: ' event.formattedTime);
}
```

```javascript
$('#time-input').timecalc();
$('#time-input').on('timecalcupdate', function ( event ) {
   $('#time-output-hr').text(event.hours + ' Hours');
   $('#time-output-min').text(event.minutes + ' Minutes');
   $('#time-output-sec').text(event.seconds + ' Seconds');
});
```

(will be updated in the future).

### Download:  
http://plugins.jquery.com/timecalc/


© 2014 Eric Lambrecht (http://makhani.de)

Licensed under MIT

