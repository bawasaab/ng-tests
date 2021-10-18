# VoteComponent
<pre>

import { EventEmitter } from '@angular/core';

export class VoteComponent {
  
  totalVotes = 0;
  voteChanged = new EventEmitter();
  
  upVote() {
    this.totalVotes++;
    this.voteChanged.emit( this.totalVotes );
  }
  
  downVote() {
    this.totalVotes--;
    this.voteChanged.emit( this.totalVotes );
  }
}
</pre>


# VoteComponent test event emitter

<pre>
import { VoteComponent } from './VoteComponent';

describe( 'VoteComponent', () => {

var component = new VoteComponent();

beforeEach( () => {
  component = new VoteComponent();
} );

it( 'should raise vote changed event when up voted', () => {

    let totalVotes = null;
    
    // arrange part
    component.voteChanged.subscribe( (totVot) => { totalVotes = totVot } );
    
    // act part
    component.upVote();
    
    // assert part
    expect(totalVotes).not.toBeNull();
} );

} );

</pre>
