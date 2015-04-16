# UK Moment
### Manipulate and display GMT dates with Moment.js

under development

## Install
#### Node.js
```javascript
npm install uk-moment
```
```javascript
var moment = require('uk-moment');
```
#### Browser
```html
<script type="text/javascript" src="uk-moment.min.js"></script>
```
## API
#### Format Dates
```javascript
moment().tz("Europe/London").format('MMMM Do YYYY, h:mm:ss a'); // April 16th 2015, 8:58:59 pm
moment().tz("Europe/London").format('dddd');                    // Thursday
moment().tz("Europe/London").format("MMM Do YY");               // Apr 16th 15
moment().tz("Europe/London").format('YYYY [escaped] YYYY');     // 2015 escaped 2015
moment().tz("Europe/London").format();                          // 2015-04-16T21:03:19+01:00
```
#### Relative Time
```javascript
moment("20111031", "YYYYMMDD").tz("Europe/London").fromNow(); // 3 years ago
moment().tz("Europe/London").startOf('day').fromNow();        // 21 hours ago
moment().tz("Europe/London").endOf('day').fromNow();          // in 3 hours
moment().tz("Europe/London").startOf('hour').fromNow();       // a minute ago
```
#### Calendar Time
```javascript
moment().tz("Europe/London").subtract(10, 'days').calendar(); // 04/06/2015
moment().tz("Europe/London").subtract(6, 'days').calendar();  // Last Friday at 9:02 PM
moment().tz("Europe/London").subtract(3, 'days').calendar();  // Last Monday at 9:02 PM
moment().tz("Europe/London").subtract(1, 'days').calendar();  // Yesterday at 9:02 PM
moment().tz("Europe/London").calendar();                      // Today at 9:02 PM
moment().tz("Europe/London").add(1, 'days').calendar();       // Tomorrow at 9:02 PM
moment().tz("Europe/London").add(3, 'days').calendar();       // Sunday at 9:02 PM
moment().tz("Europe/London").add(10, 'days').calendar();      // 04/26/2015
```
#### UNIX timestamp formatting
```javascript
moment.tz(theTime, "Europe/London").format("HH:mm");
```
