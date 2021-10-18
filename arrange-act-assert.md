<pre>
import { VoteComponent } from './VoteComponent';

describe( 'VoteComponent', () => {

  // arrange Part: initialize the system of test. We creating the instance of the voteComponent.
  let component = new VoteComponent();
  
  // act Part: calling a method or function to execute the logic.
  component.upVote();
  
  // assert Part: to observe the test output.
  expect( component.totalVotes ).toBe(1);
} );
</pre>
