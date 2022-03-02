# History

This project originates from a builspace.so project.

Network: Ethereum Ropsten
App: https://github.com/sharonlandis/wave-app
Run locally: npm start

Code for the original project, just in case I need it later on, is here:  
contracts/WavePortalCourse.sol
scriptsCourse/deployCourse.js
scriptsCourse/runCourse.js

Changes to the course project are desribed below

# Wave

Users connect their wallet, add their favorite comfort food to The Comfort Food Chain, and click wave button to submit their fav comfort food to the chain.

Your waves show up on in the app as soon as the txn goes through. But you can't see waves submitted via simultaneous sessions unless you refresh your page. The need to refresh was removed by adding a wave listener. The course version created duplicate waves b/c the app added new waves for all users. This was changed to only report other user's waves, as our own waves are already reported.

Users randomly win .0001 ETH for submitting a wave. The prize was removed, as the contract requires continuous funding to pay prizes. A contract can't be funded by sending it ETH, it has to be re-deployed. This is more trouble than it's worth.

Spam is reduced by forcing users to wait 1 minute to send another way. Mind you, the gas fee acts as a deterent as well. You can only get so much test ETH at a time.
