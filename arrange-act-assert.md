<pre>
import { VoteComponent } from './VoteComponent';

describe( 'VoteComponent', () => {

  it( 'should increment the total votes if upvoted', () => {
    // arrange Part: initialize the system of test. We creating the instance of the voteComponent.
    let component = new VoteComponent();
  
    // act Part: calling a method or function to execute the logic.
    component.upVote();
  
    // assert Part: to observe the test output.
    expect( component.totalVotes ).toBe(1);
  } );
  
  it( 'should decrement the total votes if downvoted', () => {
    // arrange Part: initialize the system of test. We creating the instance of the voteComponent.
    let component = new VoteComponent();
  
    // act Part: calling a method or function to execute the logic.
    component.downVote();
  
    // assert Part: to observe the test output.
    expect( component.totalVotes ).toBe(-1);
  } );
} );
</pre>


# Refactor the above test using beforeEach

# beforeEach( () => {} );

<pre>
import { VoteComponent } from './VoteComponent';

describe( 'VoteComponent', () => {

  // arrange Part: initialize the system of test. We creating the instance of the voteComponent.
  let component: VoteComponent;
  
  // here we are creating the new instance every time before the next test run.
  beforeEach( () => {
    component = new VoteComponent();
  } );
    
  it( 'should increment the total votes if upvoted', () => {
  
    // act Part: calling a method or function to execute the logic.
    component.upVote();
  
    // assert Part: to observe the test output.
    expect( component.totalVotes ).toBe(1);
  } );
  
  it( 'should decrement the total votes if downvoted', () => {
    // arrange Part: initialize the system of test. We creating the instance of the voteComponent.
  
    // act Part: calling a method or function to execute the logic.
    component.downVote();
  
    // assert Part: to observe the test output.
    expect( component.totalVotes ).toBe(-1);
  } );
} );
</pre>
