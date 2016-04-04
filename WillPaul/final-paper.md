# Content vs. meta-data ownership in the cloud-computing age
*Will Paul*

<!--
Articulate the value of archiving meta-data

Introduce the problem space
  | Fundamental shift in the web from distributed to centralized
  | Fundamental shift in media culture from physical to digital to streamed
  | What does this new ownership mean for us as a society?

Centralization and the churn of modern day business culture.
  | Silicon Valley churn, Grooveshark example, data loss
  |

Value of digital data preservation
  |

Outcomes:
* Identical libraries
* User removed from the discovery process
* User locked into a single vendor
  * User loses data from shutdown (see Grooveshark)
-->

Over the last several decades the Internet has undergone a fundamental shift, from a distributed 'web' of personal sites in the early days to the centralized, indexed, narrowcasted Internet of today. At the same time Silicon Valley has rapidly focused on converting physical commodities into information commodities, primarily using this new Internet as the distribution medium. At first glance this does not seem that troubling, as it has in general made the average consumers life easier. We like having our free (as in price) cloud services, and will no doubt enjoy the ['fog'](http://www.webopedia.com/TERM/F/fog-computing.html) services to come, but at what social cost?

A concrete example of this is the music industry, which has gone through a number of technological cycles, from physical ownership (vinyl, tape, cd) to digital ownership (iTunes) to subscription-based renting (Napster, Spotify, etc.). The root product has not changed, but rather the medium of transfer and storage. For the consumer of a streaming service this would only be the bandwidth and perhaps some volatile, encrypted cache hidden somewhere on their file-system. But even this is almost ethereal for mobile consumer's as cellular companies scramble to make deals with streaming services, ['setting music free'](http://www.t-mobile.com/offer/free-music-streaming.html) so that even the cost of bandwidth is abstracted away.

In this new environment everyone's media libraries are basically identical. The act of physically raking through sleeves of new music at the record store or the hand-picked mix tape have been replaced with automated discovery systems that take in meta-data and output our future listening histories. In this way the authorship over a music library has been flipped, now orchestrated by a proprietary system that monitors and curates in a sort of black-box feedback loop.

That is of course not to say that discovery systems or data science projects in general are wholly negative–or positive for that matter. The issue arises when they are placed within a closed system that cannot be picked apart and analyzed. Machine learning in general inherently relies on two components: data and tuning. And while tuning on the surface seems quite technical and obfuscated, even for researchers there is a great deal of subjectivity. This act of getting into the system, turning its knobs and seeing how that affects the output is itself a sort of creative process. Which of course is something never exposed to the end user, instead a new playlist appears every week and it is passively consumed.

However, perhaps the most tangible issue with streaming services (and the one the corporations are probably themselves most aware) is the vendor lock-in. Previously if a music listener switched from buying CDs down the street to buying albums on iTunes, what they had previously bought stuck with them and they didn't lose anything in the switch. Now if someone makes the switch from Google Play to Spotify their whole personal music history is lost. Listening history, playlists, 'saved' songs artists, rating schemes, really all the aspects that make music listening personal get left behind.

Worse, with the current Silicon Valley business model of churn and burn, who is to say that a user's current streaming provider is going to be around in the next year, much less the next ten? A somber, recent example of this was Grooveshark, which while it had been in legal trouble for a while, was shutdown basically without warning. What happens to all that user meta-data? Because of the vendor lock-in instant, massive data loss.

So what can we do about it? In the case of listening history Last.fm has done a great job making pluggable tools ('scrobblers') for tracking listening data on any platform in an open, easily accessible way. Whether they maintain this openness in the face of being acquired by CBS is yet to be seen, but so far it has done that job well.

On the data science-front there is an exciting white paper out from the New Media Lab at MIT (['Enigma'](http://enigma.media.mit.edu/enigma_full.pdf)) that describes a: 'decentralized computation platform with guaranteed privacy.' Basically, a clever rethinking of the blockchain that allows for distributed client side storage in such a way that each client's data never leaves their own device unencrypted, yet still allows computation to take advantage of the entire data set. While no machine learning has been built on top of it yet, it is the basic building block necessary to perform client-side machine learning.

On the playlist side of things I am currently working on an open source platform ([upm](http://upbeet.github.io/upm/)) for syncing playlist data from local and cloud platforms. The server was designed such that it can be run as a cloud platform (deployable to Heroku or OpenShift) by anyone or run in the background of user's own computer. The client is a web application that is run as a native app through GitHub's Electron so that it has access to the local file system and is not restricted to just streaming services. These three design choices (open, server or background, cloud or local) were consciously made to avoid creating just another proprietary service to be acquired and shifted away from its original goals.
