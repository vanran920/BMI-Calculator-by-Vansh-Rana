# Project Related to DOM

## Project Link 
[click here]()

# Solution Code

## Project 2

```javascript 
   
   // Here we have to take select whole form , 
// becuse it has submit button.

// Form when get submit , it done by post type and get type
// When i get submit , it value goes in url . 

const form = document.querySelector('form')
// const height =  parseInt(document.querySelector('#height').value) // value come in the form of string convert into int. // It will store empty value.
form.addEventListener('submit' , function(e) {
    e.preventDefault() // It will stop value to goes in url

    // How to select values. 
    const height =  parseInt(document.querySelector('#height').value) // value come in the form of string convert into int.
    const weight =  parseInt(document.querySelector('#weight').value) // value come in the form of string convert into int.
    const result =  document.querySelector('#bmi-category')

    if( ( height === '' ) || (height < 0) || (isNaN(height)) )
    {
        result.innerHTML = `Please Give a valid Height :- ${height}`
    }
    else if( ( weight === '' ) || (weight < 0) || (isNaN(weight)) )
    {
        result.innerHTML = `Please Give a valid weight :- ${weight}`
    }
    else
    {
        const bmi = (weight/ ((height*height)/10000)).toFixed(2)
        result.innerHTML = `<span>${bmi}</span>`
    }
})

``` 