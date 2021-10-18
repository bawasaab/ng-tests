#UNIT TEST
----------

here include file to be tested.

describe( 'test suit name', () => {


    it( 'should return a message hi', () => {

        saveResultInVariable = call_function_from_included_file();

        expect( saveResultInVariable ).toBe('hi');
    } );
} );
