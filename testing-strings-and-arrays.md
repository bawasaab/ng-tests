# testing strings

import greet from greet.ts; // simple greeting message with provided name

describe( 'greet', () => {

it( 'should contain a name deepak', () => {

    result = greet('deepak');

    # specific test
    expect( result ).toBe('hi deepak'); // as we see if the message in future modified to "hi deepak!" our test fails
    
    
    # general test
    expect( result ).toContain('deepak'); // as we see if the message in future modified to "hi deepak!" our test still pass
} );

} );


# testing arrays
import status from status.ts; // returns array of status i.e ['OPEN', 'CLOSE', 'DELETED']

describe( 'status', () => {

it( 'should contain OPEN', () => {

    result = status();
    
    expect( result ).toBe('OPEN');
    expect( result ).toBe('CLOSE');
    expect( result ).toBe('DELETED');
} );

} );
