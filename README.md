## Directives

#### Prerequisite
* Create a project and import FormsModule 

#### Types of Directives
There are three kinds of directives in Angular:

 * Components—directives with a template.
 * Structural directives—change the DOM layout by adding and removing DOM elements.
 * Attribute directives—change the appearance or behavior of an element, component, or another directive.

#### Structural Directives
* e.g: *ngIf, *ngFor
```
<div *ngIf="products.length > 0">  
  <ul *ngFor="let p of products">
    <li>{{p}}</li>
  </ul>
</div>
```

#### Attribute Directives
* The ngModel directive, which implements two-way data binding, is an example of an attribute directive. 
* ngModel modifies the behavior of an existing element (typically <input>) by setting its display value property and responding to change events.
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
