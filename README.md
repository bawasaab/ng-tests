# Tesing in angular


#UNIT TEST
----------

<pre>
here include file to be tested.

describe( 'enter test suit name', () => {


    it( 'test description i.e. should return a message hi', () => {

        saveResultInVariable = call_function_from_included_file();

        expect( saveResultInVariable ).toBe('hi');
    } );
} );

</pre>
