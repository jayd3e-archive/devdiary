TODO:
* add tipsy tips to a lot of interface elements
* make 'mark read' icon change the background of the condensed post
* link the solutions number to the solutions
* infinite scroll
* change -1 scores to red
* start keeping track of a user's score
* make group text not look like shit, by including ProximaNova-Bold

* add buttons to all comments/solutions
* get taken directly to your comment after you make it
* add spinners where necessary for search
* also make a new user, and streamline new user experience
* make bio work
* up the limit on files just a bit
* exit change avatar modal upon save or exit
* add error pages
* move clusterstrap into main project.  It's beginning to lose its meaning
* extend timeout time, and "remember me" check box
* notifications to self
* "mark viewed" needs to alternate between viewed/unviewed
* subnav constraints

User Testing With Dan:
* Maybe have it say "save" instead of "Edit" in the window for editing thread questions
* Was unable to cancel out of the uploading screen for the profile picture
* Once I uploaded a profile pic the upload screen does not go away after clicking "Save"
* When I try to comment on a post that I made it tells me to "reply" to myself. It then leaves a notification that I myself posted something and "dantheman replied to you". Personally I dont think it should have a notification for somethine I posted myself.
* The bar at the top of the screen that allows you to arrow through all of the groups that you are involved with goes on forever if you keep clicking it, it does not loop back around when you make it to the end of all your groups. Which for me is only one so far.
* Nothing told me that I was in the intro to pharmacy practice group page when I went from a users post to another group that they had posted onto. Only after I followed the group did it show me what group page I was on

User Testing With Dan(Whiteboard):
* refreshing is annoying, live updates
* link to specific group needs an immediate follow button
* leaderboard
* week by week
* user whitelist/blacklist
* hide posts
* sharing resources and files
* in piazza students talk to teachers most of the time, as opposed to other students
* biggest advantage is a social network feel.  Students helping students

NOTE:
*  The problem I was having with scrollTop was due to the fact that I was hiding the reply textarea,
AFTER I had already called scrollTop to find out where I needed to scroll.

Architecture TODO:
* Comment/solution need an add/close add_reply_reply_section_el function.  Not just one toggle function. STATELESS.