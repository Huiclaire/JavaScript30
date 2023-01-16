![App Screenshot](https://github.com/Huiclaire/JavaScript30/blob/master/10-Hold_Shift_and_Check_Checkboxes/images/js30-day9.png)

# 10 - Hold Shift to Check Multiple Checkboxes
When a user clicks a checkbox and holds Shift button, then clicks another checkbox a few rows down, all the checkboxes in between those two checkboxes should be checked.


## Demo
view demo [here]

## Lesson learned
Pseudo code:
- get access to checkboxes
```javascript
const checkboxes = document.querySelectorAll('.inbox input[type="checkbox"]');

function handleCheck(e) {
    console.log("clicked");

}
```
- listen for one of them to get clicked or change (with function handleCheck)
```javascript
checkboxes.forEach(checkbox => checkbox.addEventListener('click', handleCheck));
```

- make a function handleCheck
```javascript
    // check if they had the shift key down
    // AND check that they are checking it,
    let inBetween = false;
    if(e.shiftKey && this.checked) {
      // go ahead and do what we please
      // loop over every single checkbox
      checkboxes.forEach(checkbox => {
        console.log(checkbox);
        if(checkbox === this || checkbox === lastChecked) {
          inBetween = !inBetween; // define the range of inBetween with if statement
          console.log('Starting to check them in between!')
        }

        if(inBetween) {
          checkbox.checked = true;
        }
      });
    }

    console.log(e);

    lastChecked = this;
  }

```
