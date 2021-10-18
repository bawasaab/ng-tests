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
