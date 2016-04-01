 var firebase = new Firebase("https://steams.firebaseio.com/");

 // monitor state changes and react to updates
 var authClient = new FirebaseSimpleLogin(chatRef, function(error, user) {
     if (error) {
         // an error occurred while attempting login
         console.log(error);
     } else if (user) {
         // user authenticated with Firebase
         console.log('User ID: ' + user.id + ', Provider: ' + user.provider);
     } else {
         // user is logged out
     }
 });

 // perform the login (to Facebook in this case)
 authClient.login('facebook');
 {
      rules: {
      //everyone can read everything
        ".read": true,
        //nobody can write to everything
        ".write": false
      }
    }
     {
     //The people key contains the list of registered users

          people: {

          //The variable $userid refers to the key under people for which the rule is evaluated

            $userid: {

            //clients can only write if the user id matches the token

              ".write": $userid == auth.id
            }
          }
        }
         {
              users: {

                $userid: {

                  ".write": $userid == auth.id,
                  a list of users they follow
                  following: {},
                   a list of users who follow them
                  followers: {},
                  //a list of sparks posted by them
                  feed: {}
                }
              }
            }
            {
                  feed: {
                    "$sparkid": {
                      ".write":
                        root.child('users/' + $userid + '/following').hasChild(auth.id) &&
                        root.child('sparks/' + $sparkid + '/author').val() == auth.id
                    }
                  }
                }
                {
                // making sure that every user in the following list is a valid user, and that anyone is able to add themselves to the follower list
                      following: {
                        $userid: {
                          ".validate": root.child('people').hasChild($userid)
                        }
                      },
                      followers: {
                        $userid: {
                          ".write": $userid == auth.id
                        }
                      }
                    }
                     {
                          sparks: {
                            $sparkid: {
                            //data refers to the object currently present at that location, and newData refers to the data that will be written if the rule succeeds
                              ".write": !data.exists(),
                              ".validate": newData.hasChildren(['author', 'content']),
                              author: {
                                ".validate": newData.val() == auth.id
                              },
                              content: {
                                ".validate": newData.isString()
                              }
                            }
                          }
                        }
                        var userid = info.id; // info is from the login() call earlier.
                          var sparkRef = firebase.child("sparks").push();
                          var sparkRefId = sparkRef.name();

                          // Add spark to global list.
                          sparkRef.set(spark);

                          // Add spark ID to user's list of posted sparks.
                          var currentUser = firebase.child("users").child(userid);
                          currentUser.child("sparks").child(sparkRefId).set(true);

                          // Add spark ID to the feed of everyone following this user.
                          currentUser.child("followers").once("value", function(list) {
                            list.forEach(function(follower) {
                              var childRef = firebase.child("users").child(follower.name());
                              childRef.child("feed").child(sparkRefId).set(true);
                            });
                          });
                           var feed = firebase.child("users").child(userid).child("feed");
                            feed.on("child_added", function(snapshot) {
                              var sparkID = snapshot.name();
                              var sparkRef = firebase.child("sparks").child(sparkID);
                              sparkRef.on("value", function(spark) {
                                // Render the spark into the user's feed.
                              });
                            });
