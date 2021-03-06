# Ngx-Angular-Autocomplete
[NPM Package](https://www.npmjs.com/package/ngx-angular-autocomplete)
Simple Angular Autocomplete Component 
## Getting Started

### Installation
Step 1 : `npm  install ngx-angular-autocomplete`
### API
Step 2 :  `Import the NgxAutocompleteModule:`

```sh
import { NgxAutocompleteModule } from 'ngx-autocomplete' 
  @NgModule({
    declarations: [AppComponent],
    imports: [NgxAutocompleteModule],
    bootstrap: [AppComponent]
 })
export class AppModule {} 
```
Selector: ` ngx-autocomplete `

Step 3 :
    In `app.component.html`
        
```sh
<ngx-autocomplete [searchKeyword]="'name'" 
    [inputId]="'searchEmployee'" 
    [placeholderValue]="'Enter the Employee Name'" 
    [entries]="employees" 
    (selectedValue)="selectEvent($event)">
</ngx-autocomplete>
```
   
In `app.component.ts`
```sh
import { Component } from '@angular/core';
    @Component({
        selector: 'app-root',
        templateUrl: './app.component.html',
        styleUrls: ['./app.component.css']
    })
    export class AppComponent {
        title = 'ngx-autocomplete-test';
        public employees = [
        {
          "id": 1,
          "name": "Parsifal",
          "gender": "Male"
        }, {
          "id": 2,
          "name": "Mirabel",
          "gender": "Female"
        }, {
          "id": 3,
          "name": "Verne",
          "gender": "Male"
        }, {
          "id": 4,
          "name": "Julissa",
          "gender": "Female"
        }, {
          "id": 5,
          "name": "Chaddy",
          "gender": "Male"
        }, {
          "id": 6,
          "name": "Cosme",
          "gender": "Male"
        }]
      selectEvent(event) {
        console.log(event)
     }}
```
            
# API

### @Input()

| Input                    | Type           |     Required     |  Description |
| -------------------------|:--------------:| ----------------:|:-------------|
| [searchKeyword]            | string         | true             | Variable name on which the search is to be performed |
| [inputId]                  | string         | true             | set the id of input box |
| [placeholderValue]         | string         | false            | input box placeholder |
| [entries ]                 | array of objects| true            | Array of Objects on which the search is to be performed |

### @Output()

| Output                   | Return         |   Description    |
| -------------------------|:--------------:| ----------------:|
| ( selectedValue )            | string         | true             |

# Author
+ **[Shilpa syal](https://twitter.com/shilpasyal55)** 

