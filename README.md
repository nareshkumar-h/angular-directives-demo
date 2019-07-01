## Directives

#### Prerequisite
* Create a project and import FormsModule 

#### Types of Directives
There are three kinds of directives in Angular:

 * Components—directives with a template.
 * Structural directives—change the DOM layout by adding and removing DOM elements.
 * Attribute directives—change the appearance or behavior of an element, component, or another directive.

#### Structural Directives
* Structural directives are responsible for HTML layout. 
* They shape or reshape the DOM's structure, typically by adding, removing, or manipulating elements.
* e.g: *ngIf, *ngFor

#### Attribute Directives
```
<input type="text" [(ngModel)]="productName" />
```

#### Create a Custom Directive
```
ng generate directive highlight
```
```
@Directive({
  selector: '[appHighlight]'
})
export class HighlightDirective {

  constructor(el: ElementRef) {
    el.nativeElement.style.backgroundColor = 'yellow';
 }

}
```

#### Use Custom Directive
```
<p appHighlight>Highlight me!</p>
```
