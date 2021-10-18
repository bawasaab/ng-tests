# expected component

<pre>
import { FormBuilder, Validators, FormGroup } from '@angular/forms';

export class TodoFormComponent {
  form: FormGroup;
  
  constructor( fb: FormBuilder ) {
    this.form = fb.group({
      name: ['', validators.required],
      email: ['']
    });
  }
}
</pre>

# start testing

<pre>
import { FormBuilder } from '@angular/forms';
import { TodoFormComponent } from './TodoFormComponent';

describe( 'TodoFormComponent', () => {

var component: TodoFormComponent;

beforeEach( () => {
  component = new TodoFormComponent( new FormBuilder() );
} );

it( 'should create a form with two controls', () => {

    // without Arrange and Act, we dont need them in this case because we are not acting on it. Go straigth ti the 
    
    // Assert part
    expect(component.form.contains('name')).toBeTruthy();
    expect(component.form.contains('email')).toBeTruthy();
    
} );

it( 'should make name controls required', () => {
    
    // Arrange part
    let control = component.form.get('name');    
    
    // Act part
    control.setValue(''); // value to empty
    
    // Assert part
    expect(control.valid).toBeFalsy();
} );

} );
</pre>
